# 🐳 Docker - Fundamentos

## 📖 O que é Docker?

O Docker é uma plataforma de virtualização baseada em containers que permite empacotar aplicações e todas as suas dependências em ambientes isolados e portáveis.

Em vez de instalar manualmente linguagens, bibliotecas, bancos de dados e configurações em cada computador ou servidor, o Docker cria um ambiente padronizado que funciona da mesma forma em qualquer lugar.

Isso resolve um dos problemas mais comuns no desenvolvimento de software:

> "Na minha máquina funciona."

Com Docker, a aplicação é executada dentro de um container, garantindo que o comportamento seja o mesmo em ambientes de desenvolvimento, teste e produção.

---

## 🎯 Para que serve?

O Docker é amplamente utilizado para:

* Padronizar ambientes de desenvolvimento
* Facilitar o deploy de aplicações
* Executar múltiplos serviços isolados
* Simplificar a configuração de projetos
* Melhorar a portabilidade entre sistemas
* Suportar arquiteturas modernas baseadas em microsserviços
* Automatizar pipelines de CI/CD

Exemplos comuns:

* APIs Node.js
* Aplicações Python (Django/FastAPI)
* Bancos de dados (PostgreSQL, MongoDB, MySQL)
* Cache com Redis
* Frontend com React ou Next.js

---

# 🧠 Conceitos Fundamentais

## Container vs Máquina Virtual

### Máquina Virtual (VM)

Uma máquina virtual simula um computador completo, incluindo seu próprio sistema operacional.

Características:

* Possui sistema operacional próprio
* Consome mais memória e armazenamento
* Inicialização mais lenta
* Maior isolamento

### Container

Um container compartilha o kernel do sistema operacional hospedeiro e executa apenas o necessário para a aplicação funcionar.

Características:

* Leve e rápido
* Inicialização em segundos
* Menor consumo de recursos
* Fácil escalabilidade

### Comparação

| Característica              | Máquina Virtual | Container |
| --------------------------- | --------------- | --------- |
| Sistema Operacional Próprio | Sim             | Não       |
| Consumo de Recursos         | Alto            | Baixo     |
| Inicialização               | Lenta           | Rápida    |
| Portabilidade               | Média           | Alta      |

---

## 📦 O que é uma Imagem?

Uma imagem é um modelo imutável utilizado para criar containers.

Ela contém:

* Sistema base
* Dependências
* Bibliotecas
* Configurações
* Código da aplicação

### Analogia

Imagine uma receita de bolo.

A receita descreve exatamente como o bolo deve ser preparado, mas ainda não é o bolo.

Da mesma forma, a imagem descreve tudo que o container precisa para existir.

---

## 🚀 O que é um Container?

Um container é uma instância em execução de uma imagem.

Quando uma imagem é executada, o Docker cria um container.

### Analogia

Imagem → Receita de bolo

Container → Bolo pronto

Uma mesma imagem pode gerar diversos containers.

---

## ⚙️ Como o Docker Funciona Internamente?

Quando executamos um comando Docker, diversos componentes trabalham juntos.

Fluxo simplificado:

Docker CLI → Docker Engine → containerd → runc → Container

### Docker CLI

Interface de linha de comando utilizada pelo desenvolvedor.

Exemplos:

```bash
docker run
docker ps
docker logs
```

### Docker Engine

É o núcleo do Docker.

Responsável por:

* Gerenciar imagens
* Criar containers
* Controlar redes
* Gerenciar volumes

### containerd

Gerencia o ciclo de vida dos containers.

Responsável por:

* Criar
* Executar
* Pausar
* Remover containers

### runc

Ferramenta de baixo nível responsável por criar e executar os processos isolados dentro do Linux.

---

# 🔒 Isolamento de Containers

Cada container possui seu próprio ambiente.

Isso significa que:

* Processos são isolados
* Arquivos são isolados
* Configurações são isoladas
* Dependências são isoladas

Exemplo:

Container A:

```txt
Node.js
```

Container B:

```txt
Python
```

Os dois podem coexistir sem conflitos.

---

# 🏗️ Arquitetura Moderna com Containers

Em aplicações reais, normalmente utilizamos vários containers trabalhando juntos.

Exemplo:

```txt
┌─────────────┐
│    Nginx    │
└──────┬──────┘
       │
┌──────▼──────┐
│  API Node   │
└──────┬──────┘
       │
┌──────▼──────┐
│ PostgreSQL  │
└─────────────┘
```

Cada serviço executa em seu próprio container.

Benefícios:

* Escalabilidade
* Organização
* Segurança
* Facilidade de manutenção

---

# 📚 Resumo

Nesta aula aprendemos:

✅ O que é Docker

✅ Para que serve

✅ Diferença entre Container e Máquina Virtual

✅ O que é uma Imagem

✅ O que é um Container

✅ Como o Docker funciona internamente

✅ Conceitos de Docker Engine, containerd e runc

✅ Isolamento de aplicações

✅ Arquiteturas modernas baseadas em containers

---

# 🎯 Próximos Passos

Na próxima aula serão abordados:

* docker run
* docker ps
* docker stop
* docker start
* docker rm
* docker images
* docker logs

Além da criação dos primeiros containers na prática.
