---
description: Demonstra sobreposições de ícone da barra de tarefas e barras de progresso.
title: Exemplo de status periférico da barra de tarefas
ms.topic: article
ms.date: 05/31/2018
ms.assetid: E4B693FB-EE7D-47d0-A5D8-91205AD4A3DC
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 793c09853e3174f426b7b41685f2593daaae9b6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104989074"
---
# <a name="taskbar-peripheral-status-sample"></a>Exemplo de status periférico da barra de tarefas

Demonstra sobreposições de ícone da barra de tarefas e barras de progresso.

Este tópico inclui as seções a seguir.

-   [Descrição](#description)
-   [Requisitos](#requirements)
-   [Baixando o exemplo](#downloading-the-sample)
-   [Compilando o exemplo](#building-the-sample)
-   [Executando o exemplo](#running-the-sample)
-   [Tópicos relacionados](#related-topics)

## <a name="description"></a>Description

Este exemplo cria um botão de barra de tarefas de exemplo no qual ele demonstra o uso de [**ITaskbarList3:: SetOverlayIcon**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setoverlayicon) permitindo que você aplique várias sobreposições escolhidas em um menu.

O exemplo também fornece a opção de simular um indicador de progresso no botão, demonstrando o uso de [**ITaskbarList3:: SetProgressState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressstate) e [**ITaskbarList3:: SetProgressValue**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressvalue) mostrando a primeira um indicador de progresso indeterminado (TBPF \_ indeterminado) e, em seguida, um indicador proporcional normal (TBPF \_ normal).

## <a name="requirements"></a>Requisitos



| Produto                                | Versão mínima do produto |
|----------------------------------------|-------------------------|
| Windows                                | Windows 7               |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Baixando o exemplo

| Localização      | URL do caminho                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Exemplo de TaskBarPeripheralStatus](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/TaskbarPeripheralStatus) |

## <a name="building-the-sample"></a>Compilando o exemplo

Para criar o exemplo do prompt de comando:

1.  Abra a janela do prompt de comando e navegue até o diretório do projeto **TaskbarPeripheralStatus** .
2.  Digite `msbuild PeripheralStatus.sln`.

Para criar o exemplo usando Microsoft Visual Studio (preferencial):

1.  Abra o Windows Explorer e navegue até o diretório do projeto **TaskbarPeripheralStatus** .
2.  Clique duas vezes no ícone do arquivo PeripheralStatus. sln para abrir o projeto no Visual Studio.
3.  No menu **Compilar** , selecione **Compilar solução**.

## <a name="running-the-sample"></a>Executando o exemplo

1.  Navegue até o diretório que contém o novo arquivo executável (por exemplo, `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\TaskbarPeripheralStatus\Win32\Debug` ), usando o prompt de comando ou o Windows Explorer.

    -   Se estiver usando a linha de comando, digite `PeripheralStatus.exe` .
    -   Se estiver usando o Windows Explorer, clique duas vezes no ícone para PeripheralStatus.exe.

    Uma nova janela será aberta, com um botão da barra de tarefas associado.

2.  Para demonstrar sobreposições, escolha **sobreposição 1** ou **sobreposição 2** no menu de **status periférico** da janela. A sobreposição escolhida aparece no botão da barra de tarefas. Para remover a sobreposição, escolha **limpar sobreposição**.
3.  Para demonstrar a barra de progresso, escolha **simular progresso** no menu de **status periférico** da janela. O botão da barra de tarefas mostrará um indicador de progresso indeterminado e alternará para um indicador normal.
4.  Escolha **sair** no menu **arquivo** da janela para encerrar o programa.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Extensões da barra de tarefas](taskbar-extensions.md)
</dt> </dl>

 

 



