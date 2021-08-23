---
description: Demonstra como criar um Lista de Atalhos personalizado para um aplicativo, incluindo a adição de uma categoria e tarefas personalizadas.
title: Exemplo de lista de atalhos personalizada
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 60DEDB01-8F8F-4c25-8FCC-8EAC461A99B7
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 3eb6f5db0b9576f360abcbaacb8a8a5a291d3dbe07754281954ea585d3ebe965
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968825"
---
# <a name="custom-jump-list-sample"></a>Exemplo de lista de atalhos personalizada

Demonstra como criar um Lista de Atalhos personalizado para um aplicativo, incluindo a adição de uma categoria e tarefas personalizadas.

Este tópico inclui as seções a seguir.

-   [Requirements](#requirements)
-   [Baixando o exemplo](#downloading-the-sample)
-   [Compilando o exemplo](#building-the-sample)
-   [Executando o exemplo](#running-the-sample)
-   [Tópicos relacionados](#related-topics)

## <a name="requirements"></a>Requisitos



| Produto                                | Versão mínima do produto |
|----------------------------------------|-------------------------|
| Windows                                | Windows 7               |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Baixando o exemplo

| Localização      | URL do caminho                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Exemplo de CustomJumpList](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/CustomJumpList) |

## <a name="building-the-sample"></a>Compilando o exemplo

Para criar o exemplo no prompt de comando:

1.  Abra a janela do prompt de comando e navegue até o diretório do projeto **CustomJumpList.**
2.  Digite `msbuild CustomJumpListSample.sln`.

Para criar o exemplo usando Microsoft Visual Studio (preferencial):

1.  Abra Windows Explorer e navegue até o diretório do projeto **CustomJumpList.**
2.  Clique duas vezes no ícone do arquivo CustomJumpListSample.sln para abrir o projeto Visual Studio.
3.  No menu **Compilar**, selecione **Compilar Solução**.

## <a name="running-the-sample"></a>Executando o exemplo

1.  Navegue até o diretório que contém o novo executável usando o prompt de comando ou Windows Explorer.
2.  Na linha de comando, insira `CustomJumpListSample.exe` . Como alternativa, no Windows Explorer, clique duas vezes no ícone para CustomJumpListSample.exe.
3.  Este exemplo deve ser executado como administrador na primeira vez que for executado para que possa instalar os registros de tipo de arquivo necessários. Depois que os tipos de arquivo foram registrados, o exemplo pode ser executado como um usuário padrão.
4.  Selecione as opções no menu no aplicativo de exemplo para ver como elas afetam o Lista de Atalhos aplicativo na barra de tarefas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[IDs de modelo de usuário do aplicativo (AppUserModelIDs)](appids.md)
</dt> </dl>

 

 



