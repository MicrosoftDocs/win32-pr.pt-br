---
description: As funções a seguir são usadas por provedores de tempo.
ms.assetid: 05687a67-4e0b-4a44-9c2d-7e097be9008c
title: Funções de provedor de tempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20a24f15bd67751dc09a689078a8a518224267c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755291"
---
# <a name="time-provider-functions"></a><span data-ttu-id="7aeb3-103">Funções de provedor de tempo</span><span class="sxs-lookup"><span data-stu-id="7aeb3-103">Time Provider Functions</span></span>

<span data-ttu-id="7aeb3-104">As funções a seguir são usadas por provedores de tempo.</span><span class="sxs-lookup"><span data-stu-id="7aeb3-104">The following functions are used by time providers.</span></span>



| <span data-ttu-id="7aeb3-105">Função</span><span class="sxs-lookup"><span data-stu-id="7aeb3-105">Function</span></span>                                                               | <span data-ttu-id="7aeb3-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="7aeb3-106">Description</span></span>                                                                                            |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7aeb3-107">**AlertSamplesAvailFunc**</span><span class="sxs-lookup"><span data-stu-id="7aeb3-107">**AlertSamplesAvailFunc**</span></span>](/windows/desktop/api/Timeprov/nc-timeprov-alertsamplesavailfunc)                     | <span data-ttu-id="7aeb3-108">Notifica o sistema de que há novos exemplos disponíveis.</span><span class="sxs-lookup"><span data-stu-id="7aeb3-108">Notifies the system that there are new samples available.</span></span>                                              |
| [<span data-ttu-id="7aeb3-109">**GetTimeSysInfoFunc**</span><span class="sxs-lookup"><span data-stu-id="7aeb3-109">**GetTimeSysInfoFunc**</span></span>](/windows/desktop/api/Timeprov/nc-timeprov-gettimesysinfofunc)                           | <span data-ttu-id="7aeb3-110">Recupera as informações de estado do tempo do sistema.</span><span class="sxs-lookup"><span data-stu-id="7aeb3-110">Retrieves the system time state information.</span></span>                                                           |
| [<span data-ttu-id="7aeb3-111">**LogTimeProvEventFunc**</span><span class="sxs-lookup"><span data-stu-id="7aeb3-111">**LogTimeProvEventFunc**</span></span>](/windows/desktop/api/Timeprov/nc-timeprov-logtimeproveventfunc)                       | <span data-ttu-id="7aeb3-112">Registra um evento de provedor de tempo no log de eventos.</span><span class="sxs-lookup"><span data-stu-id="7aeb3-112">Logs a time provider event in the event log.</span></span>                                                           |
| [<span data-ttu-id="7aeb3-113">**SetProviderStatusFunc**</span><span class="sxs-lookup"><span data-stu-id="7aeb3-113">**SetProviderStatusFunc**</span></span>](/windows/desktop/api/Timeprov/nc-timeprov-setproviderstatusfunc)                 | <span data-ttu-id="7aeb3-114">Define as informações de status do provedor de tempo.</span><span class="sxs-lookup"><span data-stu-id="7aeb3-114">Sets the time provider's status information.</span></span>                                                           |
| [<span data-ttu-id="7aeb3-115">**SetProviderStatusInfoFreeFunc**</span><span class="sxs-lookup"><span data-stu-id="7aeb3-115">**SetProviderStatusInfoFreeFunc**</span></span>](/windows/desktop/api/Timeprov/nc-timeprov-setproviderstatusinfofreefunc) | <span data-ttu-id="7aeb3-116">Libera uma estrutura [**SetProviderStatusInfo**](/windows/desktop/api/Timeprov/ns-timeprov-setproviderstatusinfo) .</span><span class="sxs-lookup"><span data-stu-id="7aeb3-116">Frees a [**SetProviderStatusInfo**](/windows/desktop/api/Timeprov/ns-timeprov-setproviderstatusinfo) structure.</span></span>                          |
| [<span data-ttu-id="7aeb3-117">**TimeProvClose**</span><span class="sxs-lookup"><span data-stu-id="7aeb3-117">**TimeProvClose**</span></span>](/windows/desktop/api/Timeprov/nf-timeprov-timeprovclose)                                 | <span data-ttu-id="7aeb3-118">Uma função de retorno de chamada que é chamada pelo Gerenciador de provedores de tempo para desligar o provedor de tempo.</span><span class="sxs-lookup"><span data-stu-id="7aeb3-118">A callback function that is called by the time provider manager to shut down the time provider.</span></span>        |
| [<span data-ttu-id="7aeb3-119">**TimeProvCommand**</span><span class="sxs-lookup"><span data-stu-id="7aeb3-119">**TimeProvCommand**</span></span>](/windows/desktop/api/Timeprov/nf-timeprov-timeprovcommand)                             | <span data-ttu-id="7aeb3-120">Uma função de retorno de chamada que é chamada pelo Gerenciador de provedores de tempo para enviar comandos para o provedor de tempo.</span><span class="sxs-lookup"><span data-stu-id="7aeb3-120">A callback function that is called by the time provider manager to send commands to the time provider.</span></span> |
| [<span data-ttu-id="7aeb3-121">**TimeProvOpen**</span><span class="sxs-lookup"><span data-stu-id="7aeb3-121">**TimeProvOpen**</span></span>](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen)                                   | <span data-ttu-id="7aeb3-122">Uma função de retorno de chamada que é chamada pelo Gerenciador de provedores de tempo quando a DLL do provedor de tempo é carregada.</span><span class="sxs-lookup"><span data-stu-id="7aeb3-122">A callback function that is called by the time provider manager when the time provider DLL is loaded.</span></span>  |



 

 

 



