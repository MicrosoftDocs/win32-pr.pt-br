---
description: Demonstra uma barra de ferramentas de miniatura, um controle de barra de ferramentas ativo inserido na visualização em miniatura de uma janela, usado para fornecer acesso aos comandos de chave de uma janela sem fazer com que o usuário restaure ou ative a janela do aplicativo.
title: Exemplo da barra de ferramentas em miniatura da barra de tarefas
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 4936FF67-19EE-4963-BE4C-3D40350C64A9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e61208f15772a43138e6cd7a38fd6327445bdfa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968093"
---
# <a name="taskbar-thumbnail-toolbar-sample"></a>Exemplo da barra de ferramentas em miniatura da barra de tarefas

Demonstra uma barra de ferramentas de miniatura, um controle de barra de ferramentas ativo inserido na visualização em miniatura de uma janela, usado para fornecer acesso aos comandos de chave de uma janela sem fazer com que o usuário restaure ou ative a janela do aplicativo.

Este tópico inclui as seções a seguir.

-   [Descrição](#description)
-   [Requisitos](#requirements)
-   [Baixando o exemplo](#downloading-the-sample)
-   [Compilando o exemplo](#building-the-sample)
-   [Executando o exemplo](#running-the-sample)
-   [Tópicos relacionados](#related-topics)

## <a name="description"></a>Description

Este exemplo mostra como fornecer uma barra de ferramentas simples para uma visualização de miniaturas da barra de tarefas. A barra de ferramentas consiste em três botões. Clicar em um botão exibe uma janela para confirmar que o botão foi ativado. As seguintes APIs são demonstradas:

-   [**ITaskbarList3::ThumbBarAddButtons**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbaraddbuttons)
-   [**ITaskbarList3::ThumbBarSetImageList**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbarsetimagelist)
-   Estrutura [**ThumbButton**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-thumbbutton)

## <a name="requirements"></a>Requisitos



| Produto                                | Versão mínima do produto |
|----------------------------------------|-------------------------|
| Windows                                | Windows 7               |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Baixando o exemplo

| Localização      | URL do caminho                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Exemplo de TaskbarThumbnailToolbar](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/TaskbarThumbnailToolbar) |

## <a name="building-the-sample"></a>Compilando o exemplo

Para criar o exemplo do prompt de comando:

1.  Abra a janela do prompt de comando e navegue até o diretório do projeto **TaskbarThumbnailToolbar** .
2.  Digite `msbuild ThumbnailToolbar.sln`.

Para criar o exemplo usando Microsoft Visual Studio (preferencial):

1.  Abra o Windows Explorer e navegue até o diretório do projeto **TaskbarThumbnailToolbar** .
2.  Clique duas vezes no ícone do arquivo ThumbnailToolbar. sln para abrir o projeto no Visual Studio.
3.  No menu **Compilar** , selecione **Compilar solução**.

## <a name="running-the-sample"></a>Executando o exemplo

1.  Navegue até o diretório que contém o novo arquivo executável (por exemplo, `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\TaskbarThumbnailToolbar\Debug` ), usando o prompt de comando ou o Windows Explorer.

    -   Se estiver usando a linha de comando, digite `ThumbnailToolbar.exe` .
    -   Se estiver usando o Windows Explorer, clique duas vezes no ícone para ThumbnailToolbar.exe.

    Uma nova janela será aberta, com um botão da barra de tarefas associado.

2.  Focalize o cursor sobre o botão da barra de tarefas **ThumbnailToolbar** para que a visualização seja exibida. Clique em um dos três botões (verde, amarelo, vermelho) mostrado na barra de ferramentas da visualização.
3.  Escolha **sair** no menu **arquivo** da janela para encerrar o programa.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Extensões da barra de tarefas](taskbar-extensions.md)
</dt> </dl>

 

 



