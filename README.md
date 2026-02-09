# Steam CLI Launcher (Linux)

Um script simples em Python para listar jogos instalados da Steam no Linux e iniciá-los diretamente pelo terminal.

Nada de abrir a Steam, caçar jogo com o mouse e perder tempo.

## Funcionalidades

- Lista jogos instalados da Steam
- Ordena os jogos em ordem alfabética
- Abre o jogo selecionado via `steam://rungameid`
- Ignora Steam Linux Runtimes automaticamente
- Funciona direto no terminal

> Observação: versões do Proton instaladas pela Steam **aparecem na lista**, pois também são registradas como apps. Os runtimes da Steam foram filtrados manualmente no script.

## Estrutura do projeto

```text
steam-cli-launcher/
├── steam-games        # script principal (executável, sem extensão)
├── steam-games.py     # versão de testes / desenvolvimento
├── README.md
```

- steam-games é o arquivo pensado para uso diário
- steam-games.py é apenas para testes e ajustes no código

## Requisitos

- Linux

- Steam instalada

- Python 3

- Biblioteca vdf

## Instalando a dependência

``` bash
pip install vdf
```

Ou, dependendo da distro:

``` bash
sudo pacman -S python-vdf
```

## Instalação

Dê permissão de execução:

``` bash
chmod +x steam-games
```

No meu caso, coloquei o arquivo em:

``` text
~/.local/bin/
```

Assim o script pode ser executado de qualquer lugar no terminal, desde que `~/.local/bin/` esteja no `PATH`.

## Uso

Basta rodar:

``` bash
steam-games
```

O script vai listar os jogos instalados.
Digite o número correspondente ao jogo e ele será iniciado automaticamente pela Steam.

## Observações

- Testado em Fedora KDE (Linux)

- Apenas jogos instalados localmente aparecem

- Protons instalados pela Steam aparecem na lista

- Steam Linux Runtimes são ignorados
