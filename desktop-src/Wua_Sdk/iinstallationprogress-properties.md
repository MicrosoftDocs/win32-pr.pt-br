---
description: A interface IInstallationProgress define as propriedades a seguir.
ms.assetid: f16c682f-3e9f-4767-8f26-d7af0a14d720
title: Propriedades de IInstallationProgress
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcbcdb162c544c81b96326ec7b2b7657d81538a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105794571"
---
# <a name="iinstallationprogress-properties"></a><span data-ttu-id="1ff04-103">Propriedades de IInstallationProgress</span><span class="sxs-lookup"><span data-stu-id="1ff04-103">IInstallationProgress Properties</span></span>

<span data-ttu-id="1ff04-104">A interface [**IInstallationProgress**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationprogress) define as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="1ff04-104">The [**IInstallationProgress**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationprogress) interface defines the following properties.</span></span>



| <span data-ttu-id="1ff04-105">Propriedade</span><span class="sxs-lookup"><span data-stu-id="1ff04-105">Property</span></span>                                                                                   | <span data-ttu-id="1ff04-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="1ff04-106">Description</span></span>                                                                                                                                        |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1ff04-107">**CurrentUpdateIndex**</span><span class="sxs-lookup"><span data-stu-id="1ff04-107">**CurrentUpdateIndex**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationprogress-get_currentupdateindex)                     | <span data-ttu-id="1ff04-108">Obtém um valor de índice com base em zero que especifica a atualização atualmente instalada ou desinstalada quando várias atualizações foram selecionadas.</span><span class="sxs-lookup"><span data-stu-id="1ff04-108">Gets a zero-based index value that specifies the update that is currently being installed or uninstalled when multiple updates have been selected.</span></span> |
| [<span data-ttu-id="1ff04-109">**CurrentUpdatePercentComplete**</span><span class="sxs-lookup"><span data-stu-id="1ff04-109">**CurrentUpdatePercentComplete**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationprogress-get_currentupdatepercentcomplete) | <span data-ttu-id="1ff04-110">Obtém a distância em que o processo de instalação ou desinstalação da atualização atual foi progredido, como uma porcentagem.</span><span class="sxs-lookup"><span data-stu-id="1ff04-110">Gets how far the installation or uninstallation process for the current update has progressed, as a percentage.</span></span>                                    |
| [<span data-ttu-id="1ff04-111">**PercentComplete**</span><span class="sxs-lookup"><span data-stu-id="1ff04-111">**PercentComplete**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationprogress-get_percentcomplete)                           | <span data-ttu-id="1ff04-112">Obtém a distância em que o processo geral de instalação ou desinstalação foi progredido, como uma porcentagem.</span><span class="sxs-lookup"><span data-stu-id="1ff04-112">Gets how far the overall installation or uninstallation process has progressed, as a percentage.</span></span>                                                   |



 

 

 



