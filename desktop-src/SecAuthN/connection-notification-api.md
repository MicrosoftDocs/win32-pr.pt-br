---
description: O roteador de vários provedores (MPR) chama as funções de notificação de conexão ao se conectar ou desconectar um recurso de rede. Para receber essas notificações, você pode implementar essas funções em uma DLL.
ms.assetid: 62559eab-dd2f-43fa-9b09-5e4d82efc879
title: API de notificação de conexão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 352d5cb09923a666e3fe1474e9fd2ebe033f05be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091325"
---
# <a name="connection-notification-api"></a>API de notificação de conexão

O [*roteador de vários provedores*](/windows/desktop/SecGloss/m-gly) (MPR) chama as funções de notificação de conexão ao se conectar ou desconectar um recurso de rede. Para receber essas notificações, você pode implementar essas funções em uma DLL.

O MPR chama a função [**AddConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-addconnectnotify) antes e depois de tentar cada operação de adição de conexão ([**WNetAddConnection**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnectiona), [**WNetAddConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a)ou [**WNetAddConnection3**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection3a)). Essa função não é chamada quando o MPR está restaurando automaticamente as conexões de rede.

O MPR chama a função [**CancelConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-cancelconnectnotify) antes e depois de tentar cada operação Cancel-Connection ([**WNetCancelConnection**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnectiona) ou [**WNetCancelConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnection2a)).

Para obter mais informações sobre as funções do WNet, consulte [sistema de rede do Windows](/windows/desktop/WNet/windows-networking-wnet-).

Para obter mais informações sobre como criar e registrar um aplicativo que recebe notificações de conexão de rede, consulte [recebendo notificações de conexão](receiving-connection-notifications.md) e [registrando para receber notificações de conexão](registering-to-receive-connection-notifications.md).

 

 
