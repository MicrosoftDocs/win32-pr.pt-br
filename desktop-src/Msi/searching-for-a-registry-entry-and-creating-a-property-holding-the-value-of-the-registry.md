---
description: Durante uma instalação de Windows Installer, o instalador pode pesquisar uma entrada de registro e criar uma propriedade que contém o valor do registro.
ms.assetid: 3a663fc7-cdcf-4ac3-8251-836ba0d3cc11
title: Procurando uma entrada de registro e criando uma propriedade que contém o valor do registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82bd7572c0176f4870eed199800715190d9bbbf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826849"
---
# <a name="searching-for-a-registry-entry-and-creating-a-property-holding-the-value-of-the-registry"></a><span data-ttu-id="3f97c-103">Procurando uma entrada de registro e criando uma propriedade que contém o valor do registro</span><span class="sxs-lookup"><span data-stu-id="3f97c-103">Searching for a Registry Entry and Creating a Property Holding the Value of the Registry</span></span>

<span data-ttu-id="3f97c-104">**Para procurar uma entrada de registro e criar uma propriedade que contém o valor desse arquivo**</span><span class="sxs-lookup"><span data-stu-id="3f97c-104">**To search for a registry entry and create a property holding the value of that file**</span></span>

1.  <span data-ttu-id="3f97c-105">Não adicione a assinatura à tabela de [assinatura](signature-table.md) ou à [tabela CompLocator](complocator-table.md).</span><span class="sxs-lookup"><span data-stu-id="3f97c-105">Do not add the signature to the [Signature Table](signature-table.md) or the [CompLocator Table](complocator-table.md).</span></span> <span data-ttu-id="3f97c-106">Se uma assinatura de arquivo estiver listada na [tabela AppSearch](appsearch-table.md) e não estiver listada nas tabelas Signature ou CompLocator, o instalador procurará na [tabela RegLocator](reglocator-table.md).</span><span class="sxs-lookup"><span data-stu-id="3f97c-106">If a file signature is listed in the [AppSearch Table](appsearch-table.md) and is not listed in the Signature or CompLocator tables, the Installer looks in the [RegLocator Table](reglocator-table.md).</span></span>

2.  <span data-ttu-id="3f97c-107">Especifique a entrada do registro a ser pesquisada na [tabela RegLocator](reglocator-table.md).</span><span class="sxs-lookup"><span data-stu-id="3f97c-107">Specify the registry entry to be searched for in the [RegLocator Table](reglocator-table.md).</span></span> <span data-ttu-id="3f97c-108">Se a assinatura estiver ausente da [tabela de assinatura](signature-table.md) e o valor da coluna de tipo for **msidbLocatorTypeRawValue**, a pesquisa será considerada para o nome da chave do registro específico apontado pela tabela RegLocator.</span><span class="sxs-lookup"><span data-stu-id="3f97c-108">If the signature is absent from the [Signature Table](signature-table.md) and the value of the Type column is **msidbLocatorTypeRawValue**, then the search is assumed to be for the specific registry key name pointed to by the RegLocator Table.</span></span>

    <span data-ttu-id="3f97c-109">[Tabela RegLocator](reglocator-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="3f97c-109">[RegLocator Table](reglocator-table.md) (partial)</span></span>

    

    | <span data-ttu-id="3f97c-110">Signature\_</span><span class="sxs-lookup"><span data-stu-id="3f97c-110">Signature\_</span></span>         | <span data-ttu-id="3f97c-111">Root</span><span class="sxs-lookup"><span data-stu-id="3f97c-111">Root</span></span>         | <span data-ttu-id="3f97c-112">Chave</span><span class="sxs-lookup"><span data-stu-id="3f97c-112">Key</span></span>                                                           | <span data-ttu-id="3f97c-113">Nome</span><span class="sxs-lookup"><span data-stu-id="3f97c-113">Name</span></span>                  | <span data-ttu-id="3f97c-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="3f97c-114">Type</span></span>                                    |
    |---------------------|--------------|---------------------------------------------------------------|-----------------------|-----------------------------------------|
    | <span data-ttu-id="3f97c-115">AppValue</span><span class="sxs-lookup"><span data-stu-id="3f97c-115">AppValue</span></span><br/> | <span data-ttu-id="3f97c-116">2</span><span class="sxs-lookup"><span data-stu-id="3f97c-116">2</span></span><br/> | <span data-ttu-id="3f97c-117">**Software** \\ **Microsoft** \\ **MyApp**</span><span class="sxs-lookup"><span data-stu-id="3f97c-117">**SOFTWARE**\\**Microsoft**\\**MyApp**</span></span><br/> <br/> | <span data-ttu-id="3f97c-118">**Myname**</span><span class="sxs-lookup"><span data-stu-id="3f97c-118">**Myname**</span></span><br/> | <span data-ttu-id="3f97c-119">**msidbLocatorTypeRawValue**</span><span class="sxs-lookup"><span data-stu-id="3f97c-119">**msidbLocatorTypeRawValue**</span></span><br/> |

    

     

3.  <span data-ttu-id="3f97c-120">Por fim, preencha a [tabela AppSearch](appsearch-table.md) para que a [ação AppSearch](appsearch-action.md) retorne o valor de AppValue.</span><span class="sxs-lookup"><span data-stu-id="3f97c-120">Finally, populate the [AppSearch Table](appsearch-table.md) so that the [AppSearch Action](appsearch-action.md) returns the value of AppValue.</span></span> <span data-ttu-id="3f97c-121">Depois que o instalador executa a ação AppSearch, o valor de MYREGVAL é o valor de AppValue.</span><span class="sxs-lookup"><span data-stu-id="3f97c-121">After the Installer executes the AppSearch Action, the value of MYREGVAL is the value of AppValue.</span></span>

    <span data-ttu-id="3f97c-122">[Tabela AppSearch](appsearch-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="3f97c-122">[AppSearch Table](appsearch-table.md) (partial)</span></span>

    

    | <span data-ttu-id="3f97c-123">Propriedade</span><span class="sxs-lookup"><span data-stu-id="3f97c-123">Property</span></span>            | <span data-ttu-id="3f97c-124">Assinatura</span><span class="sxs-lookup"><span data-stu-id="3f97c-124">Signature</span></span>           |
    |---------------------|---------------------|
    | <span data-ttu-id="3f97c-125">MYREGVAL</span><span class="sxs-lookup"><span data-stu-id="3f97c-125">MYREGVAL</span></span><br/> | <span data-ttu-id="3f97c-126">AppValue</span><span class="sxs-lookup"><span data-stu-id="3f97c-126">AppValue</span></span><br/> |

    

     

 

 




