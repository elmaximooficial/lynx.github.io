# Lynx
Um motor de jogos rápido, nos editores e nos controles.

# Sobre este Documento
Este documento, assim como toda a Wiki disponível no GitHub, tem como objetivo documentar as escolhas e implementação da engine, portanto tem um caráter muito mais técnico e de baixo nível. Todas as especificações contidas aqui podem mudar em uma velocidade bastante alta, porém é importante mantê-lo sempre atualizado, para evitar a falta de documentação presente em outros motores (como a Bevy por exemplo).
Esta documentação estará disponível a todos os usuários, porém separado por seções baseadas na especialidade de cada um (uma seção para Programadores, outra para artistas, outra para Game Designers, etc).

# Objetivo do Projeto
Buscamos desenvolver um motor de jogos rápido e eficiente, que abstraia somente quando necessário, porém que permita modularidade e modificações sempre que o usuário necessitar (permitimos alterações até mesmo no cerne do motor).
Para alcançar tais objetivos, devemos escolher primeiro uma base forte, que no mercado atual é o sistema de ECS, já que este permite um código eficiente (em tempo e memória) com uma base de código organizada e modular.
A implementação de ECS da Lynx é uma forma ligeiramente diferente de ECS arquetípico (mais detalhes na entrada específica), que tem um overhead de memória reduzido e uma eficiência maior para acessos parciais.
A segunda forma que pretendemos atingir nossos objetivos é utilizando de duas formas de scripting: para não programadores (Lua, Python e talvez JavaScript) e para programadores (Rust, C, C++ e talvez Go).
Em terceiro lugar, a engine poderá ser utilizada puramente por código, ou puramente pelo editor gráfico, ambas as abordagens devem incorrer em baixas penalidades de performance, e focar em manter uma base de código organizada e modular.
