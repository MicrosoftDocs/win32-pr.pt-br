---
description: Demonstra como usar as \_ APIs NotifyIcon e Shell NotifyIconGetRect do Shell \_ para exibir um ícone de notificação.
title: Exemplo NotificationIcon
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 9F31DB2D-4B12-4f65-AC91-25B4B5B1CB46
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 1569d162aef358130910081bee80354cb64f690d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104967971"
---
# <a name="notificationicon-sample"></a>Exemplo NotificationIcon

Demonstra como usar as APIs [**\_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) e [**shell \_ NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) do Shell para exibir um ícone de notificação.

Este tópico inclui as seções a seguir.

-   [Descrição](#description)
-   [Requisitos](#requirements)
-   [Baixando o exemplo](#downloading-the-sample)
-   [Compilando o exemplo](#building-the-sample)
-   [Executando o exemplo](#running-the-sample)

## <a name="description"></a>Description

Além do uso do [**shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) e do [**shell \_ NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) para exibir um ícone de notificação, este exemplo também demonstra como exibir uma janela submenu rica, um menu de contexto e uma notificação de balão.

> [!Note]  
> [**Shell \_ do O NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) só está disponível no Windows 7 e versões posteriores.

 

## <a name="requirements"></a>Requisitos



| Produto                                | Versão mínima do produto |
|----------------------------------------|-------------------------|
| Windows                                | Windows 7               |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Baixando o exemplo

| Localização      | URL do caminho                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Exemplo de NotificationIcon](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/NotificationIcon) |

## <a name="building-the-sample"></a>Compilando o exemplo

Para criar o exemplo do prompt de comando:

1.  Abra a janela do prompt de comando e navegue até o diretório do projeto **NotificationIcon** .
2.  Digite `msbuild NotificationIcon.sln`.

Para criar o exemplo usando Microsoft Visual Studio (preferencial):

1.  Abra o Windows Explorer e navegue até o diretório do projeto **NotificationIcon** .
2.  Clique duas vezes no ícone do arquivo NotificationIcon. sln para abrir o projeto no Visual Studio.
3.  No menu **Compilar** , selecione **Compilar solução**.

## <a name="running-the-sample"></a>Executando o exemplo

1.  Navegue até o diretório que contém o novo executável, usando o prompt de comando ou o Windows Explorer.
2.  Na linha de comando, digite `NotificationIcon.exe` . Como alternativa, no Windows Explorer, clique duas vezes no ícone para NotificationIcon.exe.

> [!Note]  
> Os ícones de notificação especificados com um GUID são protegidos contra falsificação, Validando que apenas um único aplicativo os registra. Esse registro é executado na primeira vez que você chama o Shell \_ NotifyIcon (Nim \_ Add,...) e o nome do caminho completo do aplicativo de chamada é armazenado. Se posteriormente você mover o arquivo binário para um local diferente, o sistema não permitirá que o ícone seja adicionado novamente. Consulte o [**shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) para obter mais informações.

 

 

 



