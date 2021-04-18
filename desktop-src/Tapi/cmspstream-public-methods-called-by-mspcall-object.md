---
description: A lista a seguir contém os métodos CMSPStream chamados pelo objeto MSPCall.
ms.assetid: 7a59ca78-b5e8-45e9-8fdb-89402ffef916
title: Métodos CMSPStream chamados por objeto MSPCall
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89744f9e4cf2739fa11f07edc4be7e331beb620a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760167"
---
# <a name="cmspstream-public-methods-called-by-mspcall-object"></a><span data-ttu-id="3288c-103">Métodos públicos CMSPStream chamados por objeto MSPCall</span><span class="sxs-lookup"><span data-stu-id="3288c-103">CMSPStream Public Methods Called by MSPCall Object</span></span>



| <span data-ttu-id="3288c-104">Métodos públicos CMSPStream</span><span class="sxs-lookup"><span data-stu-id="3288c-104">CMSPStream public methods</span></span>                                 | <span data-ttu-id="3288c-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="3288c-105">Description</span></span>                                                                             |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="3288c-106">**Init**</span><span class="sxs-lookup"><span data-stu-id="3288c-106">**Init**</span></span>](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-init)                           | <span data-ttu-id="3288c-107">Chamado pelo **MSPCall** quando o fluxo é criado.</span><span class="sxs-lookup"><span data-stu-id="3288c-107">Called by the **MSPCall** when the stream is created.</span></span>                                   |
| [<span data-ttu-id="3288c-108">**Desligar**</span><span class="sxs-lookup"><span data-stu-id="3288c-108">**ShutDown**</span></span>](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-shutdown)                   | <span data-ttu-id="3288c-109">Chamado pelo **MSPCall** para cancelar a seleção de todos os objetos de terminal e liberar o objeto de chamada.</span><span class="sxs-lookup"><span data-stu-id="3288c-109">Called by the **MSPCall** to unselect all terminal objects and release the call object.</span></span> |
| [<span data-ttu-id="3288c-110">**GetState**</span><span class="sxs-lookup"><span data-stu-id="3288c-110">**GetState**</span></span>](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-getstate)                   | <span data-ttu-id="3288c-111">Chamado pelo objeto MSPCall para obter o status atual do fluxo.</span><span class="sxs-lookup"><span data-stu-id="3288c-111">Called by the MSPCall object to get the current status of the stream.</span></span>                   |
| [<span data-ttu-id="3288c-112">**HandleTSPData**</span><span class="sxs-lookup"><span data-stu-id="3288c-112">**HandleTSPData**</span></span>](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-handletspdata)         | <span data-ttu-id="3288c-113">O objeto de chamada derivada pode chamar esse método para permitir que o fluxo manipule os comandos do TSP.</span><span class="sxs-lookup"><span data-stu-id="3288c-113">Derived call object may call this method to let the stream handle the TSP commands.</span></span>     |
| [<span data-ttu-id="3288c-114">**ProcessGraphEvent**</span><span class="sxs-lookup"><span data-stu-id="3288c-114">**ProcessGraphEvent**</span></span>](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-processgraphevent) | <span data-ttu-id="3288c-115">Chamado pelo objeto MSPCall para permitir que o fluxo manipule eventos de grafo.</span><span class="sxs-lookup"><span data-stu-id="3288c-115">Called by the MSPCall object to let the stream handle graph events.</span></span>                     |



 

 

 



