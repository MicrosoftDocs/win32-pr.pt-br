---
description: A interface IDownloadJob define os métodos a seguir.
ms.assetid: b9a6b722-2e32-4177-bcef-514412e132ec
title: Métodos IDownloadJob
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f68acd6d7fef37c4ce9309c559a1de1b4d516dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501872"
---
# <a name="idownloadjob-methods"></a><span data-ttu-id="b3a13-103">Métodos IDownloadJob</span><span class="sxs-lookup"><span data-stu-id="b3a13-103">IDownloadJob Methods</span></span>

<span data-ttu-id="b3a13-104">A interface [**IDownloadJob**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadjob) define os métodos a seguir.</span><span class="sxs-lookup"><span data-stu-id="b3a13-104">The [**IDownloadJob**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadjob) interface defines the following methods.</span></span>



| <span data-ttu-id="b3a13-105">Método</span><span class="sxs-lookup"><span data-stu-id="b3a13-105">Method</span></span>                                            | <span data-ttu-id="b3a13-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="b3a13-106">Description</span></span>                                                                                                            |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b3a13-107">**Eliminação**</span><span class="sxs-lookup"><span data-stu-id="b3a13-107">**CleanUp**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-cleanup)           | <span data-ttu-id="b3a13-108">Aguarda a conclusão de uma operação assíncrona e libera todos os retornos de chamada.</span><span class="sxs-lookup"><span data-stu-id="b3a13-108">Waits for an asynchronous operation to be completed and releases all callbacks.</span></span>                                        |
| [<span data-ttu-id="b3a13-109">**GetProgress**</span><span class="sxs-lookup"><span data-stu-id="b3a13-109">**GetProgress**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-getprogress)   | <span data-ttu-id="b3a13-110">Retorna uma interface [**IDownloadProgress**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadprogress) que descreve o progresso atual de um download.</span><span class="sxs-lookup"><span data-stu-id="b3a13-110">Returns an [**IDownloadProgress**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadprogress) interface that describes the current progress of a download.</span></span> |
| [<span data-ttu-id="b3a13-111">**RequestAbort**</span><span class="sxs-lookup"><span data-stu-id="b3a13-111">**RequestAbort**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-requestabort) | <span data-ttu-id="b3a13-112">Faz uma solicitação para finalizar um download assíncrono.</span><span class="sxs-lookup"><span data-stu-id="b3a13-112">Makes a request to end an asynchronous download.</span></span>                                                                       |



 

 

 



