---
description: A interface IDownloadJob define as propriedades a seguir.
ms.assetid: 50e672d7-0ad6-402d-878c-4ac79b70a036
title: Propriedades de IDownloadJob
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18c9bd940b4b091f2eeefbaaa2a60d66306a3e14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810807"
---
# <a name="idownloadjob-properties"></a><span data-ttu-id="238c5-103">Propriedades de IDownloadJob</span><span class="sxs-lookup"><span data-stu-id="238c5-103">IDownloadJob Properties</span></span>

<span data-ttu-id="238c5-104">A interface [**IDownloadJob**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadjob) define as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="238c5-104">The [**IDownloadJob**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadjob) interface defines the following properties.</span></span>



| <span data-ttu-id="238c5-105">Propriedade</span><span class="sxs-lookup"><span data-stu-id="238c5-105">Property</span></span>                                        | <span data-ttu-id="238c5-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="238c5-106">Description</span></span>                                                                                                                                              |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="238c5-107">**AsyncState**</span><span class="sxs-lookup"><span data-stu-id="238c5-107">**AsyncState**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-get_asyncstate)   | <span data-ttu-id="238c5-108">Obtém o objeto de estado específico do chamador que é passado para o método [**IUpdateDownloader. BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload) .</span><span class="sxs-lookup"><span data-stu-id="238c5-108">Gets the caller-specific state object that is passed to the [**IUpdateDownloader.BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload) method.</span></span>           |
| [<span data-ttu-id="238c5-109">**IsCompleted**</span><span class="sxs-lookup"><span data-stu-id="238c5-109">**IsCompleted**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-get_iscompleted) | <span data-ttu-id="238c5-110">Obtém a configuração que indica se a chamada para [**IUpdateDownloader. BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload) foi processada completamente.</span><span class="sxs-lookup"><span data-stu-id="238c5-110">Gets the setting that indicates whether the call to [**IUpdateDownloader.BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload) was processed completely.</span></span> |
| [<span data-ttu-id="238c5-111">**Atualizações**</span><span class="sxs-lookup"><span data-stu-id="238c5-111">**Updates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-get_updates)         | <span data-ttu-id="238c5-112">Obtém uma interface que contém uma coleção somente leitura das atualizações que são especificadas em um download.</span><span class="sxs-lookup"><span data-stu-id="238c5-112">Gets an interface that contains a read-only collection of the updates that are specified in a download.</span></span>                                                  |



 

 

 



