---
description: A interface IInstallationJob define os métodos a seguir.
ms.assetid: 4990ef7c-b6cd-46fc-9e7d-8d1d78edc9f2
title: Métodos IInstallationJob
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa0c1a5850f3d71ad1a6a51046fe890ea9bc7426
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090622"
---
# <a name="iinstallationjob-methods"></a><span data-ttu-id="bc035-103">Métodos IInstallationJob</span><span class="sxs-lookup"><span data-stu-id="bc035-103">IInstallationJob Methods</span></span>

<span data-ttu-id="bc035-104">A interface [**IInstallationJob**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationjob) define os métodos a seguir.</span><span class="sxs-lookup"><span data-stu-id="bc035-104">The [**IInstallationJob**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationjob) interface defines the following methods.</span></span>



| <span data-ttu-id="bc035-105">Método</span><span class="sxs-lookup"><span data-stu-id="bc035-105">Method</span></span>                                                | <span data-ttu-id="bc035-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="bc035-106">Description</span></span>                                                                                                                                           |
|-------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bc035-107">**Eliminação**</span><span class="sxs-lookup"><span data-stu-id="bc035-107">**CleanUp**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-cleanup)           | <span data-ttu-id="bc035-108">Aguarda a conclusão de uma operação assíncrona e, em seguida, libera todos os retornos de chamada.</span><span class="sxs-lookup"><span data-stu-id="bc035-108">Waits for an asynchronous operation to be completed and then releases all the callbacks.</span></span>                                                              |
| [<span data-ttu-id="bc035-109">**GetProgress**</span><span class="sxs-lookup"><span data-stu-id="bc035-109">**GetProgress**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-getprogress)   | <span data-ttu-id="bc035-110">Retorna uma interface [**IInstallationProgress**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationprogress) que descreve o progresso atual de uma instalação ou desinstalação.</span><span class="sxs-lookup"><span data-stu-id="bc035-110">Returns an [**IInstallationProgress**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationprogress) interface that describes the current progress of an installation or uninstallation.</span></span> |
| [<span data-ttu-id="bc035-111">**RequestAbort**</span><span class="sxs-lookup"><span data-stu-id="bc035-111">**RequestAbort**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-requestabort) | <span data-ttu-id="bc035-112">Faz uma solicitação para cancelar a instalação ou desinstalação.</span><span class="sxs-lookup"><span data-stu-id="bc035-112">Makes a request to cancel the installation or uninstallation.</span></span>                                                                                         |



 

 

 



