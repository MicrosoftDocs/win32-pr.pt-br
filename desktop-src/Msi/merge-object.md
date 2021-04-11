---
description: O objeto de mesclagem fornece acesso a outros objetos de nível superior. Um objeto de mesclagem deve ser criado antes do carregamento do suporte de automação exigido pelo COM para acessar as funções no Mergemod.dll.
ms.assetid: 3f76ee8a-d195-4a69-99a3-31ef2c1c72d5
title: Mesclar objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1379202d4f252560a381f8af09b30741faa060ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171831"
---
# <a name="merge-object"></a><span data-ttu-id="99f96-104">Mesclar objeto</span><span class="sxs-lookup"><span data-stu-id="99f96-104">Merge Object</span></span>

<span data-ttu-id="99f96-105">O objeto de **mesclagem** fornece acesso a outros objetos de nível superior.</span><span class="sxs-lookup"><span data-stu-id="99f96-105">The **Merge** object provides access to other top-level objects.</span></span> <span data-ttu-id="99f96-106">Um objeto de **mesclagem** deve ser criado antes do carregamento do suporte de automação exigido pelo com para acessar as funções no Mergemod.dll.</span><span class="sxs-lookup"><span data-stu-id="99f96-106">A **Merge** object must be created before loading the automation support required by COM to access the functions in Mergemod.dll.</span></span>

<span data-ttu-id="99f96-107">Mergemod.dll fornece acesso à funcionalidade estendida no momento da compilação por meio de uma segunda versão do CLSID existente.</span><span class="sxs-lookup"><span data-stu-id="99f96-107">Mergemod.dll provides access to the extended functionality at build time through a second version of the existing CLSID.</span></span> <span data-ttu-id="99f96-108">Esse CLSID dá suporte à funcionalidade existente disponível por meio da interface [**IMsmMerge**](/windows/win32/api/mergemod/nn-mergemod-imsmmerge) , mas a interface padrão no objeto (e a interface dupla associada) é a interface [**IMsmMerge2**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) em vez da interface **IMsmMerge** .</span><span class="sxs-lookup"><span data-stu-id="99f96-108">This CLSID supports existing functionality available through the [**IMsmMerge**](/windows/win32/api/mergemod/nn-mergemod-imsmmerge) interface, but the default interface on the object (and the associated dual interface) is the [**IMsmMerge2**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) interface instead of the **IMsmMerge** interface.</span></span>

 

 
