<a id="readme-top"></a>

[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![LinkedIn][linkedin-shield]][linkedin-url]

<br />
<div align="center">
  <h3 align="center">🏓 PingPongOS</h3>

  <p align="center">
    Sistema Operacional didático feito em C - Trabalho da disciplina de Sistemas Operacionais (CI1215) na UFPR 
    <br />
  </p>
</div>

---

## 📖 Sobre o Projeto

**PingPongOS** (ou PPOS) é um Sistema Operacional que executa inteiramente dentro de um processo do Linux, o que permite usar ferramentas de depuração, como Valgrind e GDB

A versão atual do PingPongOS suporta múltiplas tarefas com preempção por tempo, escalonador baseado em prioridades, semáforos, filas de mensagens, alocador de memória heap, acesso a disco e sistema de arquivos. Devido à característica de executar em um processo Linux, o PPOS não suporta memória virtual, separação usuário/kernel e chamadas de sistema por traps.

O PPOS segue a estrutura típica de um RTOS (Real-Time Operating System), um sistema operacional com espaço de memória único, no qual o núcleo e as aplicações são compilados juntos, formando uma única imagem binária.

Além disso, o trabalho da disciplina foi feito em 13 entregas diferentes, cada uma focando em partes diferentes de um sistema operacional, então o projeto também contém arquivos para testes de cada uma dessas entregas.

<p align="right">(<a href="#readme-top">voltar ao topo</a>)</p>

---

## 📁 Estrutura do Projeto

```
ppos/
├── hardware/          emulação do hardware
|   ├── disk*          disco rígido
|   ├── cpu.*          operações da CPU/chipset
|   ├── serial.*       porta serial (console) 
|   └── makefile
├── kernel/            núcleo do PPOS
|   ├── ppos.*         núcleo (arquivo principal)
|   ├── macros.h       macros de uso geral
|   ├── ctx.*          trocas de contexto (assembly e C)
|   ├── tcb.h          task control block (descritor de tarefa)
|   ├── task.*         gestão básica de tarefas
|   ├── dispatcher.*   despachante de tarefas
|   ├── scheduler.*    escalonador de tarefas
|   ├── time.*         gestão do tempo
|   ├── semaphore.*    spinlocks e semáforos
|   ├── mqueue.*       filas de mensagens
|   ├── memory.*       gestão de memória heap
|   ├── block.*        acesso aos blocos do disco
|   ├── syscall.h      funções acessíveis às aplicações
|   └── makefile
├── lib/
|   ├── map.*          biblioteca de mapas genéricos
|   ├── queue.*        biblioteca de filas genéricas
|   ├── pplibc.*       mini-biblioteca C padrão
|   └── makefile
├── test/
|   ├── pingpong-*.c     programas de teste dos projetos
|   ├── pingpong-*.txt   saídas esperadas dos testes
|   └── makefile
└── makefile
```

<p align="right">(<a href="#readme-top">voltar ao topo</a>)</p>

---

## 📬 Contato

hassevini — [github.com/hassevini](https://github.com/hassevini)

E-mail - hassevini@gmail.com

OttoSchmidt - [github.com/OttoSchmidt](https://github.com/OttoSchmidt)

Link do projeto: [https://github.com/hassevini/PingPongOS](https://github.com/hassevini/PingPongOS)

<p align="right">(<a href="#readme-top">voltar ao topo</a>)</p>

---

## 🙏 Agradecimentos

* [Best-README-Template](https://github.com/othneildrew/Best-README-Template) — template base deste README

---

<!-- MARKDOWN LINKS & IMAGES -->
[stars-shield]: https://img.shields.io/github/stars/hassevini/PingPongOS.svg?style=for-the-badge
[stars-url]: https://github.com/hassevini/PingPongOS/stargazers
[issues-shield]: https://img.shields.io/github/issues/hassevini/PingPongOS.svg?style=for-the-badge
[issues-url]: https://github.com/hassevini/PingPongOS/issues
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://www.linkedin.com/in/hassevini
