---
description: O roteador de vários provedores (MPR) chama as funções de notificação de conexão ao se conectar ou desconectar um recurso de rede. Para receber essas notificações, você pode implementar essas funções em uma DLL.
ms.assetid: 62559eab-dd2f-43fa-9b09-5e4d82efc879
title: API de notificação de conexão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0afaa2e08e6a88f101e8914d9d98a40d6024bdf942ed4bcb0fd1924bc5800213
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883306"
---
# <a name="connection-notification-api"></a>API de notificação de conexão

O [*roteador de vários provedores*](/windows/desktop/SecGloss/m-gly) (MPR) chama as funções de notificação de conexão ao se conectar ou desconectar um recurso de rede. Para receber essas notificações, você pode implementar essas funções em uma DLL.

O MPR chama a função [**AddConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-addconnectnotify) antes e depois de tentar cada operação de adição de conexão ([**WNetAddConnection**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnectiona), [**WNetAddConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a)ou [**WNetAddConnection3**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection3a)). Essa função não é chamada quando o MPR está restaurando automaticamente as conexões de rede.

O MPR chama a função [**CancelConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-cancelconnectnotify) antes e depois de tentar cada operação Cancel-Connection ([**WNetCancelConnection**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnectiona) ou [**WNetCancelConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnection2a)).

para obter mais informações sobre as funções do WNet, consulte [Windows rede](/windows/desktop/WNet/windows-networking-wnet-).

Para obter mais informações sobre como criar e registrar um aplicativo que recebe notificações de conexão de rede, consulte [recebendo notificações de conexão](receiving-connection-notifications.md) e [registrando para receber notificações de conexão](registering-to-receive-connection-notifications.md).

 

 
