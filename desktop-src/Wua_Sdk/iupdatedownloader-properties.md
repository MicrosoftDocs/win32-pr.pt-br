---
description: A interface IUpdateDownloader define as propriedades a seguir.
ms.assetid: b6a30356-f97d-408f-becd-a467e9f8e79f
title: Propriedades de IUpdateDownloader
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99c16aa762bcc14dc1919ef91d162752652c327e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647295"
---
# <a name="iupdatedownloader-properties"></a><span data-ttu-id="b5487-103">Propriedades de IUpdateDownloader</span><span class="sxs-lookup"><span data-stu-id="b5487-103">IUpdateDownloader Properties</span></span>

<span data-ttu-id="b5487-104">A interface [**IUpdateDownloader**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader) define as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="b5487-104">The [**IUpdateDownloader**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader) interface defines the following properties.</span></span>



| <span data-ttu-id="b5487-105">Propriedade</span><span class="sxs-lookup"><span data-stu-id="b5487-105">Property</span></span>                                                             | <span data-ttu-id="b5487-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="b5487-106">Description</span></span>                                                                                                                                                                |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b5487-107">**ClientApplicationID**</span><span class="sxs-lookup"><span data-stu-id="b5487-107">**ClientApplicationID**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_clientapplicationid) | <span data-ttu-id="b5487-108">Obtém e define o aplicativo cliente atual.</span><span class="sxs-lookup"><span data-stu-id="b5487-108">Gets and sets the current client application.</span></span>                                                                                                                              |
| [<span data-ttu-id="b5487-109">**Isforced**</span><span class="sxs-lookup"><span data-stu-id="b5487-109">**IsForced**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_isforced)                       | <span data-ttu-id="b5487-110">Obtém e define um valor booliano que indica se o WUA (agente de Windows Update) força o download de atualizações que já estão instaladas ou que não podem ser instaladas.</span><span class="sxs-lookup"><span data-stu-id="b5487-110">Gets and sets a Boolean value that indicates whether the Windows Update Agent (WUA) forces the download of updates that are already installed or that cannot be installed.</span></span> |
| [<span data-ttu-id="b5487-111">**Priority**</span><span class="sxs-lookup"><span data-stu-id="b5487-111">**Priority**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_priority)                       | <span data-ttu-id="b5487-112">Obtém e define o nível de prioridade do download.</span><span class="sxs-lookup"><span data-stu-id="b5487-112">Gets and sets the priority level of the download.</span></span>                                                                                                                          |
| [<span data-ttu-id="b5487-113">**Atualizações**</span><span class="sxs-lookup"><span data-stu-id="b5487-113">**Updates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_updates)                         | <span data-ttu-id="b5487-114">Obtém e define uma interface que contém uma coleção somente leitura das atualizações que são especificadas para download.</span><span class="sxs-lookup"><span data-stu-id="b5487-114">Gets and sets an interface that contains a read-only collection of the updates that are specified for download.</span></span>                                                            |



 

 

 



