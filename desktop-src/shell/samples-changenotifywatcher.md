---
description: Demonstra como escutar notificações de alteração do Shell em uma pasta ou item no namespace do Windows Explorer.
title: Exemplo de observador de notificação de alteração
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 02A7C5B4-94F2-4c35-9290-4C816E5CF63A
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 5d0ac6ccb2dd2328d81b77d03bffc68dfa9a70cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170696"
---
# <a name="change-notify-watcher-sample"></a>Exemplo de observador de notificação de alteração

Demonstra como escutar notificações de alteração do Shell em uma pasta ou item no namespace do Windows Explorer.

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
| GitHub  | [Exemplo de ChangeNotifyWatcher](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/ChangeNotifyWatcher) |

## <a name="building-the-sample"></a>Compilando o exemplo

Para criar o exemplo do prompt de comando:

1.  Abra a janela do prompt de comando e navegue até o diretório do projeto **ChangeNotifyWatcher** .
2.  Digite `msbuild ChangeNotifyWatcher.sln`.

Para criar o exemplo usando Microsoft Visual Studio (preferencial):

1.  Abra o Windows Explorer e navegue até o diretório do projeto **ChangeNotifyWatcher** .
2.  Clique duas vezes no ícone do arquivo ChangeNotifyWatcher. sln para abrir o projeto no Visual Studio.
3.  No menu **Compilar** , selecione **Compilar solução**.

## <a name="running-the-sample"></a>Executando o exemplo

1.  Navegue até o diretório que contém o novo executável, usando o prompt de comando ou o Windows Explorer.
2.  No prompt de comando, digite `ChangeNotifyWatcher.exe`. Como alternativa, no Windows Explorer, clique duas vezes no ícone para ChangeNotifyWatcher.exe.
3.  Para demonstrar o efeito, AppUserModelIDs (IDs de modelo de usuário do aplicativo) Selecione uma pasta para assistir clicando em **"escolher..."** ou usando arrastar e soltar em uma pasta de uma janela do Windows Explorer na exibição de lista do exemplo.

 

 



