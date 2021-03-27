---
description: Demonstra como implementar um verbo do shell usando os métodos ExplorerCommand e ExplorerCommandState.
title: Exemplo de verbo de comando do Explorer
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2310A6AA-EAF9-4d7a-A784-04931BDC2089
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: a35662c3df0e0fcddae049ccfaac2d9e3e265ee3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837032"
---
# <a name="explorer-command-verb-sample"></a>Exemplo de verbo de comando do Explorer

Demonstra como implementar um verbo do shell usando os métodos ExplorerCommand e ExplorerCommandState.

Este tópico inclui as seções a seguir.

-   [Requisitos](#requirements)
-   [Baixando o exemplo](#downloading-the-sample)
-   [Compilando o exemplo](#building-the-sample)
-   [Executando o exemplo](#running-the-sample)

## <a name="requirements"></a>Requisitos



| Produto                                | Versão mínima do produto |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Baixando o exemplo

| Localização      | URL do caminho                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Exemplo de ExplorerCommandVerb](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/ExplorerCommandVerb) |

## <a name="building-the-sample"></a>Compilando o exemplo

Para criar o exemplo do prompt de comando:

1.  Abra a janela do prompt de comando e navegue até o diretório do projeto **ExplorerCommandVerb** .
2.  Digite `msbuild ExplorerCommandVerb.sln`.

Para criar o exemplo usando Microsoft Visual Studio (preferencial):

1.  Abra o Windows Explorer e navegue até o diretório do projeto **ExplorerCommandVerb** .
2.  Clique duas vezes no ícone do arquivo ExplorerCommandVerb. sln para abrir o projeto no Visual Studio.
3.  No menu **Compilar** , selecione **Compilar solução**.

## <a name="running-the-sample"></a>Executando o exemplo

1.  Navegue até o diretório que contém o ExplorerCommandVerb.dll, usando o prompt de comando ou o Windows Explorer. Certifique-se de usar o arquivo DLL de 64 bits no Windows de 64 bits.
2.  Na linha de comando, digite `regsvr32.exe ExplorerCommandVerb.dll` .
3.  Dois novos verbos serão mostrados no menu de contexto quando você clicar com o botão direito do mouse em um arquivo. txt.

 

 



