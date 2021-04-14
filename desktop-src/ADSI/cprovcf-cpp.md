---
title: CPROVCF. CPP
description: No componente do provedor de exemplo, um exemplo de código do código de fábrica da classe de objeto do provedor ADs está em cprovcf. cpp.
ms.assetid: 53a4da74-3f36-4e6d-ae93-8d595680bcf3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d086cd79086f40bab6d898b844ed52fc0161bc7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453489"
---
# <a name="cprovcfcpp"></a><span data-ttu-id="12535-103">CPROVCF. CPP</span><span class="sxs-lookup"><span data-stu-id="12535-103">CPROVCF.CPP</span></span>

<span data-ttu-id="12535-104">No componente do provedor de exemplo, um exemplo de código do código de fábrica da classe de objeto do provedor ADs está em cprovcf. cpp.</span><span class="sxs-lookup"><span data-stu-id="12535-104">In the example provider component, one code example of the ADs provider object class factory code is in cprovcf.cpp.</span></span> <span data-ttu-id="12535-105">O componente de provedor nunca cria diretamente uma instância desse objeto a qualquer momento além de quando o objeto é criado automaticamente durante as operações de associação em [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) ou a função interna no método de Visual Basic **GetObject**.</span><span class="sxs-lookup"><span data-stu-id="12535-105">The provider component never directly creates an instance of this object at any time other than when the object is created automatically during the binding operations in [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) or the internal function in the Visual Basic method **GetObject**.</span></span> <span data-ttu-id="12535-106">O método com suporte é listado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="12535-106">The supported method is listed in the following table.</span></span>



| <span data-ttu-id="12535-107">Método</span><span class="sxs-lookup"><span data-stu-id="12535-107">Method</span></span>                                  | <span data-ttu-id="12535-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="12535-108">Description</span></span>                                                           |
|-----------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="12535-109">**CSampleDSProviderCF:: CreateInstance**</span><span class="sxs-lookup"><span data-stu-id="12535-109">**CSampleDSProviderCF::CreateInstance**</span></span> | <span data-ttu-id="12535-110">Cria uma instância da fábrica de classes para o objeto do provedor ADS.</span><span class="sxs-lookup"><span data-stu-id="12535-110">Creates an instance of the class factory for the ADS provider object.</span></span> |



 

 

 




