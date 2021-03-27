---
description: Demonstra como estender o menu de atalho do tipo "arrastar e soltar" (às vezes chamado de menu de contexto).
title: Exemplo NonDefaultDropMenuVerb
ms.topic: article
ms.date: 05/31/2018
ms.assetid: F19B7561-D280-41df-A829-15960FEB12F8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 9d326e012fb78b04fd542f88d49c370e8aeab613
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297235"
---
# <a name="nondefaultdropmenuverb-sample"></a>Exemplo NonDefaultDropMenuVerb

Demonstra como estender o menu de atalho do tipo "arrastar e soltar" (às vezes chamado de menu de contexto).

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
| GitHub  | [Exemplo de NonDefaultDropMenuVerb](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/NonDefaultDropMenuVerb) |

## <a name="building-the-sample"></a>Compilando o exemplo

Para criar o exemplo do prompt de comando:

1.  Abra a janela do prompt de comando e navegue até o diretório do projeto **NonDefaultDropMenuVerb** .
2.  Digite `msbuild NonDefaultDropMenuVerb.sln`.

Para criar o exemplo usando Microsoft Visual Studio (preferencial):

1.  Abra o Windows Explorer e navegue até o diretório do projeto **NonDefaultDropMenuVerb** .
2.  Clique duas vezes no ícone do arquivo NonDefaultDropMenuVerb. sln para abrir o projeto no Visual Studio.
3.  No menu **Compilar** , selecione **Compilar solução**.

## <a name="running-the-sample"></a>Executando o exemplo

1.  Navegue até o diretório que contém o novo arquivo DLL, usando o prompt de comando ou o Windows Explorer.
2.  Copie NonDefaultDropMenuVerb.dll para o diretório do sistema (por exemplo, C: \\ Windows \\ System32).
3.  Em um prompt de comando, digite `regedit NonDefaultDropMenuVerb.reg` .
4.  Use o botão direito do mouse para arrastar um arquivo de uma pasta para outra. Você verá itens de menu adicionais para a operação de soltar.

 

 



