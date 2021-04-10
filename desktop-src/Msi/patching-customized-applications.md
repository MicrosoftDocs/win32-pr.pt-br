---
description: Ao instalar um patch e uma ou mais transformações de personalização em um aplicativo, o patch é normalmente instalado primeiro, seguido pelas transformações de personalização.
ms.assetid: 39a58174-fa62-42e3-a0aa-4cc541c2e36b
title: Aplicação de patch em aplicativos personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 289685ebc390de750ea9c47ddfae6ef58ec87116
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296759"
---
# <a name="patching-customized-applications"></a><span data-ttu-id="6102d-103">Aplicação de patch em aplicativos personalizados</span><span class="sxs-lookup"><span data-stu-id="6102d-103">Patching Customized Applications</span></span>

<span data-ttu-id="6102d-104">Ao instalar um patch e uma ou mais transformações de personalização em um aplicativo, o patch é normalmente instalado primeiro, seguido pelas transformações de personalização.</span><span class="sxs-lookup"><span data-stu-id="6102d-104">When installing a patch and one or more customization transforms to an application, the patch is typically installed first, followed by the customization transforms.</span></span> <span data-ttu-id="6102d-105">Por design, o patch não é interrompido pela instalação subsequente da personalização.</span><span class="sxs-lookup"><span data-stu-id="6102d-105">By design, the patch is not broken by the subsequent installation of the customization.</span></span> <span data-ttu-id="6102d-106">No entanto, instalar as transformações primeiro e, em seguida, o patch, pode interromper a personalização.</span><span class="sxs-lookup"><span data-stu-id="6102d-106">However, installing the transforms first, and then the patch, may break the customization.</span></span>

<span data-ttu-id="6102d-107">Por exemplo, uma interrupção na personalização pode ocorrer quando um patch é usado para atualizar um produto da versão 1 para a versão 2 e uma transformação de personalização que funciona para a versão 1 não funciona para a versão 2.</span><span class="sxs-lookup"><span data-stu-id="6102d-107">For example, a break in the customization could occur when a patch is used to update a product from version 1 to version 2 and a customization transform that works for version 1 does not work for version 2.</span></span> <span data-ttu-id="6102d-108">Nesse caso, o patch de atualização de versão não pode ser aplicado a um produto personalizado sem primeiro desinstalar e reinstalar o produto original.</span><span class="sxs-lookup"><span data-stu-id="6102d-108">In this case, the version update patch cannot be applied to a customized product without first uninstalling and then reinstalling the original product.</span></span>

 

 



