---
description: A interface IDownloadProgress define as propriedades a seguir.
ms.assetid: 8f64c702-b2b5-4a5f-9365-bc962e35f499
title: Propriedades de IDownloadProgress
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 469246acb59b4aa58efcbf4bb5aa7f04b7e44b6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920969"
---
# <a name="idownloadprogress-properties"></a><span data-ttu-id="94dcd-103">Propriedades de IDownloadProgress</span><span class="sxs-lookup"><span data-stu-id="94dcd-103">IDownloadProgress Properties</span></span>

<span data-ttu-id="94dcd-104">A interface [**IDownloadProgress**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadprogress) define as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="94dcd-104">The [**IDownloadProgress**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadprogress) interface defines the following properties.</span></span>



| <span data-ttu-id="94dcd-105">Propriedade</span><span class="sxs-lookup"><span data-stu-id="94dcd-105">Property</span></span>                                                                               | <span data-ttu-id="94dcd-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="94dcd-106">Description</span></span>                                                                                                                                      |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="94dcd-107">**CurrentUpdateBytesDownloaded**</span><span class="sxs-lookup"><span data-stu-id="94dcd-107">**CurrentUpdateBytesDownloaded**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatebytesdownloaded) | <span data-ttu-id="94dcd-108">Obtém uma cadeia de caracteres que especifica a quantidade de dados que foi transferida para o arquivo de conteúdo ou arquivos da atualização que está sendo baixada, em bytes.</span><span class="sxs-lookup"><span data-stu-id="94dcd-108">Gets a string that specifies how much data has been transferred for the content file or files of the update that is being downloaded, in bytes.</span></span>  |
| [<span data-ttu-id="94dcd-109">**CurrentUpdateBytesToDownload**</span><span class="sxs-lookup"><span data-stu-id="94dcd-109">**CurrentUpdateBytesToDownload**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatebytestodownload) | <span data-ttu-id="94dcd-110">Obtém uma cadeia de caracteres que estima a quantidade de dados que deve ser transferida para o arquivo de conteúdo ou os arquivos da atualização que está sendo baixada, em bytes.</span><span class="sxs-lookup"><span data-stu-id="94dcd-110">Gets a string that estimates how much data should be transferred for the content file or files of the update that is being downloaded, in bytes.</span></span> |
| [<span data-ttu-id="94dcd-111">**CurrentUpdateDownloadPhase**</span><span class="sxs-lookup"><span data-stu-id="94dcd-111">**CurrentUpdateDownloadPhase**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatedownloadphase)     | <span data-ttu-id="94dcd-112">Obtém um valor de enumeração [**DownloadPhase**](/windows/win32/api/wuapi/ne-wuapi-downloadphase) que especifica a fase do download que está em andamento no momento.</span><span class="sxs-lookup"><span data-stu-id="94dcd-112">Gets a [**DownloadPhase**](/windows/win32/api/wuapi/ne-wuapi-downloadphase) enumeration value that specifies the phase of the download that is currently in progress.</span></span>          |
| [<span data-ttu-id="94dcd-113">**CurrentUpdateIndex**</span><span class="sxs-lookup"><span data-stu-id="94dcd-113">**CurrentUpdateIndex**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdateindex)                     | <span data-ttu-id="94dcd-114">Obtém um valor de índice baseado em zero que especifica a atualização que está sendo baixada no momento quando várias atualizações foram selecionadas.</span><span class="sxs-lookup"><span data-stu-id="94dcd-114">Gets a zero-based index value that specifies the update that is currently being downloaded when multiple updates have been selected.</span></span>             |
| [<span data-ttu-id="94dcd-115">**CurrentUpdatePercentComplete**</span><span class="sxs-lookup"><span data-stu-id="94dcd-115">**CurrentUpdatePercentComplete**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatepercentcomplete) | <span data-ttu-id="94dcd-116">Obtém uma estimativa do percentual da atualização atual que foi baixada.</span><span class="sxs-lookup"><span data-stu-id="94dcd-116">Gets an estimate of the percentage of the current update that has been downloaded.</span></span>                                                               |
| [<span data-ttu-id="94dcd-117">**PercentComplete**</span><span class="sxs-lookup"><span data-stu-id="94dcd-117">**PercentComplete**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_percentcomplete)                           | <span data-ttu-id="94dcd-118">Obtém uma estimativa do percentual de todas as atualizações que foram baixadas.</span><span class="sxs-lookup"><span data-stu-id="94dcd-118">Gets an estimate of the percentage of all the updates that have been downloaded.</span></span>                                                                 |
| [<span data-ttu-id="94dcd-119">**TotalBytesDownloaded**</span><span class="sxs-lookup"><span data-stu-id="94dcd-119">**TotalBytesDownloaded**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_totalbytesdownloaded)                 | <span data-ttu-id="94dcd-120">Obtém uma cadeia de caracteres que especifica a quantidade total de dados baixados, em bytes.</span><span class="sxs-lookup"><span data-stu-id="94dcd-120">Gets a string that specifies the total amount of data that has been downloaded, in bytes.</span></span>                                                        |
| [<span data-ttu-id="94dcd-121">**TotalBytesToDownload**</span><span class="sxs-lookup"><span data-stu-id="94dcd-121">**TotalBytesToDownload**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_totalbytestodownload)                 | <span data-ttu-id="94dcd-122">Obtém uma cadeia de caracteres que representa a estimativa da quantidade total de dados que serão baixados, em bytes.</span><span class="sxs-lookup"><span data-stu-id="94dcd-122">Gets a string that represents the estimate of the total amount of data that will be downloaded, in bytes.</span></span>                                        |



 

 

 



