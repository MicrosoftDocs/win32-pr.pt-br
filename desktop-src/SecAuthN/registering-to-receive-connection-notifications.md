---
description: Depois de criar uma DLL para receber notificações de conexão, você deve registrá-la no sistema.
ms.assetid: 1a389de1-367d-4b07-a420-4af431d48b7f
title: Registrando para receber notificações de conexão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 812c47ba43fe13e4908a1812f7c67f38a94bce5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662129"
---
# <a name="registering-to-receive-connection-notifications"></a><span data-ttu-id="64db7-103">Registrando para receber notificações de conexão</span><span class="sxs-lookup"><span data-stu-id="64db7-103">Registering to Receive Connection Notifications</span></span>

<span data-ttu-id="64db7-104">Depois de criar uma DLL para receber notificações de conexão, você deve registrá-la no sistema.</span><span class="sxs-lookup"><span data-stu-id="64db7-104">After you have created a DLL to receive connection notifications, you must register it with the system.</span></span> <span data-ttu-id="64db7-105">Para fazer isso, adicione um valor **reg \_ Expand \_ sz** sob o</span><span class="sxs-lookup"><span data-stu-id="64db7-105">You do this by adding a **REG\_EXPAND\_SZ** value under the</span></span>

<span data-ttu-id="64db7-106">**HKEY \_ Sistema de \_ computador local** \\  \\ **CurrentControlSet** \\ **Control** o \\ **NetworkProvider** \\ **notifica** os</span><span class="sxs-lookup"><span data-stu-id="64db7-106">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Control**\\**NetworkProvider**\\**Notifyees**</span></span>

<span data-ttu-id="64db7-107">chave.</span><span class="sxs-lookup"><span data-stu-id="64db7-107">key.</span></span> <span data-ttu-id="64db7-108">Esse valor especifica o caminho para a DLL que implementa a [API de notificação de conexão](connection-notification-api.md).</span><span class="sxs-lookup"><span data-stu-id="64db7-108">This value specifies the path to the DLL that implements the [Connection Notification API](connection-notification-api.md).</span></span>

<span data-ttu-id="64db7-109">O valor pode ter qualquer nome.</span><span class="sxs-lookup"><span data-stu-id="64db7-109">The value can have any name.</span></span> <span data-ttu-id="64db7-110">Todos os valores na chave **notificadores** são tratados como caminhos para DLLs notificados de eventos de conexão.</span><span class="sxs-lookup"><span data-stu-id="64db7-110">All values under the **Notifyees** key are treated as paths to DLLs that are notified of connection events.</span></span> <span data-ttu-id="64db7-111">É recomendável que você use um nome que identifique sua DLL.</span><span class="sxs-lookup"><span data-stu-id="64db7-111">It is recommended that you use a name that identifies your DLL.</span></span> <span data-ttu-id="64db7-112">Isso diminui a chance de um conflito de nome com outros aplicativos de notificação de conexão.</span><span class="sxs-lookup"><span data-stu-id="64db7-112">This lessens the chance of a name conflict with other connection notification applications.</span></span>

<span data-ttu-id="64db7-113">Para obter mais informações sobre como criar um aplicativo que recebe notificações de conexão, consulte [recebendo notificações de conexão](receiving-connection-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="64db7-113">For more information about how to create an application that receives connection notifications, see [Receiving Connection Notifications](receiving-connection-notifications.md).</span></span>

 

 



