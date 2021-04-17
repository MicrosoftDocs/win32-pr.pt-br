---
description: O instalador define as propriedades usando a ordem de precedência a seguir. Um valor de propriedade nessa lista pode substituir um valor que vem depois dele e ser substituído por um valor que vem antes dele na lista.
ms.assetid: ba9240fe-2e5a-43f5-8cdf-59dd6348092b
title: Ordem de precedência de propriedade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90c114594b9a825a3847db37f5b98dc990211d9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760837"
---
# <a name="order-of-property-precedence"></a><span data-ttu-id="e87c1-104">Ordem de precedência de propriedade</span><span class="sxs-lookup"><span data-stu-id="e87c1-104">Order of Property Precedence</span></span>

<span data-ttu-id="e87c1-105">O instalador define as propriedades usando a ordem de precedência a seguir.</span><span class="sxs-lookup"><span data-stu-id="e87c1-105">The installer sets properties using the following order of precedence.</span></span> <span data-ttu-id="e87c1-106">Um valor de propriedade nessa lista pode substituir um valor que vem depois dele e ser substituído por um valor que vem antes dele na lista.</span><span class="sxs-lookup"><span data-stu-id="e87c1-106">A property value in this list can override a value that comes after it and be overridden by a value coming before it in the list.</span></span>

1.  <span data-ttu-id="e87c1-107">Propriedades especificadas pelo ambiente operacional.</span><span class="sxs-lookup"><span data-stu-id="e87c1-107">Properties specified by the operating environment.</span></span>
2.  <span data-ttu-id="e87c1-108">[Propriedades públicas](public-properties.md) definidas na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="e87c1-108">[Public properties](public-properties.md) set on the command line.</span></span>
3.  <span data-ttu-id="e87c1-109">Propriedades públicas listadas pelo propriedade [**adminproperties**](adminproperties.md) durante uma [instalação administrativa](administrative-installation.md) .</span><span class="sxs-lookup"><span data-stu-id="e87c1-109">Public properties listed by the [**AdminProperties**](adminproperties.md) propertyset during an [administrative installation](administrative-installation.md) .</span></span>
4.  <span data-ttu-id="e87c1-110">Propriedades públicas ou privadas definidas durante a aplicação de uma [*transformação*](t-gly.md).</span><span class="sxs-lookup"><span data-stu-id="e87c1-110">Public or private properties set during the application of a [*transform*](t-gly.md).</span></span>
5.  <span data-ttu-id="e87c1-111">Propriedade pública ou privada que é definida pela criação da [tabela de propriedades](property-table.md) do arquivo. msi.</span><span class="sxs-lookup"><span data-stu-id="e87c1-111">Public or private property that set by authoring the [Property table](property-table.md) of the .msi file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e87c1-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e87c1-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e87c1-113">Sobre propriedades</span><span class="sxs-lookup"><span data-stu-id="e87c1-113">About Properties</span></span>](about-properties.md)
</dt> </dl>

 

 



