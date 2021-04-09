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
# <a name="connection-notification-api"></a><span data-ttu-id="9c5fe-104">API de notificação de conexão</span><span class="sxs-lookup"><span data-stu-id="9c5fe-104">Connection Notification API</span></span>

<span data-ttu-id="9c5fe-105">O [*roteador de vários provedores*](/windows/desktop/SecGloss/m-gly) (MPR) chama as funções de notificação de conexão ao se conectar ou desconectar um recurso de rede.</span><span class="sxs-lookup"><span data-stu-id="9c5fe-105">The [*Multiple Provider Router*](/windows/desktop/SecGloss/m-gly) (MPR) calls the connection notification functions when it connects or disconnects a network resource.</span></span> <span data-ttu-id="9c5fe-106">Para receber essas notificações, você pode implementar essas funções em uma DLL.</span><span class="sxs-lookup"><span data-stu-id="9c5fe-106">To receive such notifications, you can implement these functions in a DLL.</span></span>

<span data-ttu-id="9c5fe-107">O MPR chama a função [**AddConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-addconnectnotify) antes e depois de tentar cada operação de adição de conexão ([**WNetAddConnection**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnectiona), [**WNetAddConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a)ou [**WNetAddConnection3**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection3a)).</span><span class="sxs-lookup"><span data-stu-id="9c5fe-107">The MPR calls the [**AddConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-addconnectnotify) function before and after attempting each add-connection operation ([**WNetAddConnection**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnectiona), [**WNetAddConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a), or [**WNetAddConnection3**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection3a)).</span></span> <span data-ttu-id="9c5fe-108">Essa função não é chamada quando o MPR está restaurando automaticamente as conexões de rede.</span><span class="sxs-lookup"><span data-stu-id="9c5fe-108">This function is not called when the MPR is automatically restoring network connections.</span></span>

<span data-ttu-id="9c5fe-109">O MPR chama a função [**CancelConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-cancelconnectnotify) antes e depois de tentar cada operação Cancel-Connection ([**WNetCancelConnection**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnectiona) ou [**WNetCancelConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnection2a)).</span><span class="sxs-lookup"><span data-stu-id="9c5fe-109">The MPR calls the [**CancelConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-cancelconnectnotify) function before and after attempting each cancel-connection operation ([**WNetCancelConnection**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnectiona) or [**WNetCancelConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnection2a)).</span></span>

<span data-ttu-id="9c5fe-110">Para obter mais informações sobre as funções do WNet, consulte [sistema de rede do Windows](/windows/desktop/WNet/windows-networking-wnet-).</span><span class="sxs-lookup"><span data-stu-id="9c5fe-110">For more information about WNet functions, see [Windows Networking](/windows/desktop/WNet/windows-networking-wnet-).</span></span>

<span data-ttu-id="9c5fe-111">Para obter mais informações sobre como criar e registrar um aplicativo que recebe notificações de conexão de rede, consulte [recebendo notificações de conexão](receiving-connection-notifications.md) e [registrando para receber notificações de conexão](registering-to-receive-connection-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="9c5fe-111">For more information about how to create and register an application that receives network connection notifications, see [Receiving Connection Notifications](receiving-connection-notifications.md) and [Registering to Receive Connection Notifications](registering-to-receive-connection-notifications.md).</span></span>

 

 
