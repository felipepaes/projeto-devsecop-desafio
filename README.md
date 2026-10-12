# Desafio DevSecOps — Gerenciador de Tarefas

## Sobre o Projeto
Este repositório faz parte do desafio prático do módulo de DevSecOps da ADA Tech.
Você receberá este projeto com vulnerabilidades propositais e uma pipeline incompleta.
Seu objetivo é **implementar a pipeline de segurança** e **corrigir as vulnerabilidades**.

## Estado atual
A pipeline está **incompleta**. Os steps de segurança precisam ser implementados por você.

## Sua missão
1. Implementar os steps de segurança no `pipeline.yml`
2. Fazer a pipeline **quebrar** ao detectar os problemas
3. Corrigir as vulnerabilidades encontradas
4. Fazer a pipeline **passar** com tudo verde ✅
5. Documentar o funcionamento da pipeline neste README

## O que implementar
- [x] Secrets Scanning com **Gitleaks**
    - [x] **Github** Secrets
- [ ] SAST com **Semgrep**
- [ ] SCA com **Grype**
- [ ] Assinatura do artefato com cosign
- [ ] Deploy com **GitHub Pages**

## Como a pipeline funciona
> **Substitua este bloco pela sua explicação após implementar a pipeline.**
> Descreva cada step, o que ele faz e por que ele é importante para a segurança.

## URL de Produção
> Adicione aqui o link do GitHub Pages após o deploy.

---


# ChangeLogs


obs. os commits tentam seguir a especificações do [Conventional Commits](https://www.conventionalcommits.org/pt-br/v1.0.0/) para facilitar a navegação pelo código e futuras consultas aos PRs e commits.

## Secrets Scanning com GitLeaks + Github Secrets

- Foi adicinada a action do Gitleaks. Também foi implementada a funcionalidade do github secrets para injetar variáveis de ambiente durante o pipeline.

- Outro ajuste foi o gatilho para que a pipeline rode nos Pull Requests, isso facilita a desenvolvimento, refinamento e teste da pipeline.

- Também foi adicionada uma checagem para executar o Deploy somente em pushs diretamente à branch main

PR - [Secret Scanning e Github Secrets](https://github.com/felipepaes/projeto-devsecop-desafio/pull/2)

---

## SAST - Semgrep

- adicionado o semgrep ao pipeline com pip

- o scan encontrou um ponto de bloqueio

- realizado ajuste no código para passar pelo pipeline com sucesso

PR - [ci: adiciona SAST (semgrep) ao pipeline](https://github.com/felipepaes/projeto-devsecop-desafio/pull/3)

---

## SCA - Grype

- grype detectou vulnerabilidades nas dependências npm

- versões das dependências npm atualizadas

- grype detectou vulnerabilidades na action download-artifact

- versão da action download-artifact atualizada

- grype passou sem vulnerabilidades detectadas

PR - [ci: adiciona SCA (Grype) ao pipeline](https://github.com/felipepaes/projeto-devsecop-desafio/pull/4)

---

