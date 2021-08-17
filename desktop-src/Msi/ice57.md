---
description: O ICE57 valida que os componentes individuais não combinam dados por computador e por usuário. Essa ação personalizada ICE verifica entradas, arquivos, caminhos de chave de diretório e atalhos não anunciados.
ms.assetid: 3c82efa7-9cf3-4bcd-8ec4-b81d1d7aa0a6
title: ICE57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d875264ed1fbc0f7dedac863c21801e5180ae879c9c255af7cf4b36e5d402970
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635157"
---
# <a name="ice57"></a>ICE57

O ICE57 valida que os componentes individuais não combinam dados por computador e por usuário. Essa ação personalizada ICE verifica entradas, arquivos, caminhos de chave de diretório e atalhos não anunciados.

A combinação de dados por usuário e por computador no mesmo componente pode resultar em apenas uma instalação parcial do componente para alguns usuários em um ambiente de vários usuários.

Consulte a [**propriedade ALLUSERS.**](allusers.md)

## <a name="result"></a>Resultado

O ICE57 postará um erro se encontrar qualquer componente que contenha entradas, arquivos, caminhos de chave de diretório ou atalhos não anunciados por computador e por usuário.

## <a name="example"></a>Exemplo

ICE57reporta os erros a seguir para o exemplo mostrado.

``` syntax
Component 'Component1' has both per-user and per-machine 
    data with a per-machine KeyPath. 
 
WARNING: Component 'Component2' has both per-user and 
    per-machine data with an HKCU Registry KeyPath. 
 
Component 'Component3' has a registry entry that 
    can be either per-user or per-machine and a per-machine KeyPath. 
 
Component 'Component4' has both per-user data and 
    a keypath that can be either per-user or per-machine.
```

[Tabela de componentes](component-table.md) (parcial)



| Componente  | Diretório  | Atributos | KeyPath |
|------------|------------|------------|---------|
| Component1 | DirectoryA | 0          | FileA   |
| Component2 | DirectoryA | 4          | RegKeyB |
| Component3 | DirectoryA | 0          | FileC   |
| Component4 | DirectoryA | 4          | RegKeyD |



 

[Tabela do Registro](registry-table.md) (parcial)



| Registro | Root | Componente\_ |
|----------|------|-------------|
| RegKeyA  | 1    | Component1  |
| RegKeyB  | 1    | Component2  |
| RegKeyC  | -1   | Component3  |
| RegKeyD  | -1   | Component4  |



 

[Tabela de arquivos](file-table.md) (parcial)



| Arquivo  | Componente\_ |
|-------|-------------|
| FileA | Component1  |
| FileB | Component2  |
| FileC | Component3  |
| Arquivado | Component4  |



 

[Tabela de diretórios](directory-table.md)



| Diretório  | Pai do \_ Diretório | Defaultdir |
|------------|-------------------|------------|
| Targetdir  |                   | SourceDir  |
| DirectoryA | Targetdir         | DirectoryA |



 

Para corrigir os erros, reorganize o aplicativo de forma que cada componente contenha apenas recursos por usuário ou por computador, e não ambos.

A primeira mensagem de erro é postada porque Component1 contém FileA (por computador) e a chave do Registro HKCU RegKeyA (por usuário).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



