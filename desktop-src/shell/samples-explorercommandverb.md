---
description: Demonstra como implementar um verbo shell usando os métodos ExplorerCommand e ExplorerCommandState.
title: Exemplo de verbo de comando do Explorer
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2310A6AA-EAF9-4d7a-A784-04931BDC2089
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 3ec8f4c88ea01aad410e982fc24fd248f3c1826d8c8657e904844b535e621fd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719178"
---
# <a name="explorer-command-verb-sample"></a>Exemplo de verbo de comando do Explorer

Demonstra como implementar um verbo shell usando os métodos ExplorerCommand e ExplorerCommandState.

Este tópico inclui as seções a seguir.

-   [Requirements](#requirements)
-   [Baixando o exemplo](#downloading-the-sample)
-   [Compilando o exemplo](#building-the-sample)
-   [Executando o exemplo](#running-the-sample)

## <a name="requirements"></a>Requisitos



| Produto                                | Versão mínima do produto |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Baixando o exemplo

| Location      | URL do caminho                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Exemplo de ExplorerCommandVerb](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/ExplorerCommandVerb) |

## <a name="building-the-sample"></a>Compilando o exemplo

Para criar o exemplo no prompt de comando:

1.  Abra a janela do prompt de comando e navegue até o **diretório do projeto ExplorerCommandVerb.**
2.  Insira `msbuild ExplorerCommandVerb.sln`.

Para criar o exemplo usando Microsoft Visual Studio (preferencial):

1.  Abra Windows Explorer e navegue até o diretório do projeto **ExplorerCommandVerb.**
2.  Clique duas vezes no ícone do arquivo ExplorerCommandVerb.sln para abrir o projeto Visual Studio.
3.  No menu **Compilar**, selecione **Compilar Solução**.

## <a name="running-the-sample"></a>Executando o exemplo

1.  Navegue até o diretório que contém o ExplorerCommandVerb.dll, usando o prompt de comando ou Windows Explorer. Use o arquivo DLL de 64 bits em um arquivo de 64 bits Windows.
2.  Na linha de comando, insira `regsvr32.exe ExplorerCommandVerb.dll` .
3.  Dois novos verbos serão mostrados no menu de contexto quando você clicar com o botão direito do mouse em um .txt arquivo.

 

 



