---
description: O desligamento adequado das sessões de comunicação e de um aplicativo inteiro é necessário para impedir que os recursos permaneçam ligados em chamadas ou aplicativos que não precisam mais deles.
ms.assetid: 40694b7f-474b-41aa-be3f-48e4ca517a6f
title: Desligamento TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 661273a3d72559d965fa1ea6066f1090f8e6b6e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782898"
---
# <a name="tapi-shutdown"></a><span data-ttu-id="677f5-103">Desligamento TAPI</span><span class="sxs-lookup"><span data-stu-id="677f5-103">TAPI Shutdown</span></span>

<span data-ttu-id="677f5-104">O desligamento adequado das sessões de comunicação e de um aplicativo inteiro é necessário para impedir que os recursos permaneçam ligados em chamadas ou aplicativos que não precisam mais deles.</span><span class="sxs-lookup"><span data-stu-id="677f5-104">Proper shutdown of communications sessions and of an entire application is required to prevent resources from remaining tied up in calls or applications that no longer need them.</span></span>

<span data-ttu-id="677f5-105">A TAPI fornece uma série de funções e métodos para ajudar no processo.</span><span class="sxs-lookup"><span data-stu-id="677f5-105">TAPI provides a series of functions and methods to assist in the process.</span></span> <span data-ttu-id="677f5-106">Obviamente, o aplicativo também deve assumir a responsabilidade de liberar corretamente a memória alocada, seja na forma de estruturas de dados ou referências COM.</span><span class="sxs-lookup"><span data-stu-id="677f5-106">Obviously, the application must also take responsibility for properly releasing allocated memory, whether in the form of data structures or COM references.</span></span>



| <span data-ttu-id="677f5-107">Funções TAPI 2. x</span><span class="sxs-lookup"><span data-stu-id="677f5-107">TAPI 2.x functions</span></span>                                                            | <span data-ttu-id="677f5-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="677f5-108">Description</span></span>                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="677f5-109">**lineRegisterRequestRecipient**</span><span class="sxs-lookup"><span data-stu-id="677f5-109">**lineRegisterRequestRecipient**</span></span>](/windows/win32/api/tapi/nf-tapi-lineregisterrequestrecipient) | <span data-ttu-id="677f5-110">Cancela o registro do aplicativo como um manipulador para chamadas telefônicas assistidas.</span><span class="sxs-lookup"><span data-stu-id="677f5-110">Unregisters the application as a handler for assisted telephony calls.</span></span> |
| [<span data-ttu-id="677f5-111">**lineClose**</span><span class="sxs-lookup"><span data-stu-id="677f5-111">**lineClose**</span></span>](/windows/win32/api/tapi/nf-tapi-lineclose)                                       | <span data-ttu-id="677f5-112">Desconecta o aplicativo como um gerente para chamadas na linha especificada.</span><span class="sxs-lookup"><span data-stu-id="677f5-112">Disconnects the application as a manager for calls on the given line.</span></span>  |
| [<span data-ttu-id="677f5-113">**lineShutdown**</span><span class="sxs-lookup"><span data-stu-id="677f5-113">**lineShutdown**</span></span>](/windows/win32/api/tapi/nf-tapi-lineshutdown)                                 | <span data-ttu-id="677f5-114">Desliga o uso do aplicativo da abstração de linha.</span><span class="sxs-lookup"><span data-stu-id="677f5-114">Shuts down the application's usage of the line abstraction.</span></span>            |



 



| <span data-ttu-id="677f5-115">Interfaces ou métodos TAPI 3. x</span><span class="sxs-lookup"><span data-stu-id="677f5-115">TAPI 3.x interfaces or methods</span></span>                                            | <span data-ttu-id="677f5-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="677f5-116">Description</span></span>                                                                |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="677f5-117">**ITTAPI::UnregisterNotifications**</span><span class="sxs-lookup"><span data-stu-id="677f5-117">**ITTAPI::UnregisterNotifications**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-unregisternotifications) | <span data-ttu-id="677f5-118">Remove todos os registros de notificação de eventos executados pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="677f5-118">Removes any event notification registrations performed by the application.</span></span> |
| [<span data-ttu-id="677f5-119">**ITTAPI:: Shutdown**</span><span class="sxs-lookup"><span data-stu-id="677f5-119">**ITTAPI::Shutdown**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-shutdown)                               | <span data-ttu-id="677f5-120">Desconecta o aplicativo como um Gerenciador de chamadas.</span><span class="sxs-lookup"><span data-stu-id="677f5-120">Disconnects the application as a call manager.</span></span>                             |



 

 

 
