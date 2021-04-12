---
description: O ICE57 valida que componentes individuais não misturam dados por computador e por usuário. Essa ação personalizada de ICE verifica entradas de registro, arquivos, caminhos de chave de diretório e atalhos não anunciados.
ms.assetid: 3c82efa7-9cf3-4bcd-8ec4-b81d1d7aa0a6
title: ICE57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a59d609e5d7de0011666be0b5cc5e76417d8e67d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170839"
---
# <a name="ice57"></a>ICE57

O ICE57 valida que componentes individuais não misturam dados por computador e por usuário. Essa ação personalizada de ICE verifica entradas de registro, arquivos, caminhos de chave de diretório e atalhos não anunciados.

A combinação de dados por usuário e por computador no mesmo componente pode resultar na instalação parcial do componente para alguns usuários em um ambiente de vários usuários.

Consulte a propriedade [**AllUsers**](allusers.md) .

## <a name="result"></a>Resultado

O ICE57 posta um erro se encontrar algum componente que contenha entradas de registro por computador e por usuário, arquivos, caminhos de chave de diretório ou atalhos não anunciados.

## <a name="example"></a>Exemplo

ICE57reports os seguintes erros para o exemplo mostrado.

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
| Component1 | Directorya | 0          | FileA   |
| Component2 | Directorya | 4          | RegKeyB |
| Component3 | Directorya | 0          | FileC   |
| Component4 | Directorya | 4          | RegKeyD |



 

[Tabela do registro](registry-table.md) (parcial)



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
| Arquiva | Component4  |



 

[Tabela de diretórios](directory-table.md)



| Diretório  | Pai do diretório \_ | DefaultDir |
|------------|-------------------|------------|
| TARGETDIR  |                   | SourceDir  |
| Directorya | TARGETDIR         | Directorya |



 

Para corrigir os erros, reorganize o aplicativo de modo que cada componente contenha apenas recursos por usuário ou por máquina, e não ambos.

A primeira mensagem de erro é postada porque Component1 contém fileA (por máquina) e a chave do Registro HKCU RegKeyA (por usuário).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



