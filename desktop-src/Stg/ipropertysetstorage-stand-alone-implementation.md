---
title: Implementação IPropertySetStorage-autônoma
description: A implementação autônoma fornecida pelo sistema do IPropertySetStorage inclui uma implementação de IPropertyStorage e IPropertySetStorage.
ms.assetid: 0ea5aadf-0b3f-44ac-9bb7-a7e8292f04c2
keywords:
- IPropertySetStorage Strctd STG, implementações
- IPropertySetStorage Strctd STG, implementações, autônoma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f9fd0afe31775b06b3a5f61f4c79939be976e98
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007655"
---
# <a name="ipropertysetstorage-stand-alone-implementation"></a><span data-ttu-id="924f7-105">Implementação IPropertySetStorage-autônoma</span><span class="sxs-lookup"><span data-stu-id="924f7-105">IPropertySetStorage-Stand-alone Implementation</span></span>

<span data-ttu-id="924f7-106">A implementação autônoma fornecida pelo sistema do [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) inclui uma implementação de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) e **IPropertySetStorage**. [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) é a interface que lê e grava Propriedades em um armazenamento de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="924f7-106">The system-provided, stand-alone implementation of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) includes an implementation of both [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) and **IPropertySetStorage**.[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) is the interface that reads and writes properties in a property set storage.</span></span> <span data-ttu-id="924f7-107">[**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) é a interface que cria e abre conjuntos de propriedades em um armazenamento.</span><span class="sxs-lookup"><span data-stu-id="924f7-107">[**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) is the interface that creates and opens property sets in a storage.</span></span> <span data-ttu-id="924f7-108">As interfaces [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) e [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) também são fornecidas na implementação autônoma.</span><span class="sxs-lookup"><span data-stu-id="924f7-108">The [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) and [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) interfaces are also provided in the stand-alone implementation.</span></span>

<span data-ttu-id="924f7-109">Para usar a implementação autônoma do [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage), primeiro obtenha um ponteiro para a implementação autônoma fornecida pelo sistema e associe a implementação fornecida pelo sistema com o objeto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="924f7-109">To use the stand-alone implementation of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage), first obtain a pointer to the system-provided, stand-alone implementation and associate the system-provided implementation with your storage object.</span></span> <span data-ttu-id="924f7-110">Para obter um ponteiro para a implementação autônoma do **IPropertySetStorage**, chame a função [**StgCreatePropSetStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg) e forneça o parâmetro *pStorage* especificando o objeto de armazenamento que conterá o conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="924f7-110">To get a pointer to the stand-alone implementation of **IPropertySetStorage**, call the [**StgCreatePropSetStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg) function and provide the *pStorage* parameter specifying the storage object that will contain the property set.</span></span> <span data-ttu-id="924f7-111">Essa função fornece um ponteiro para a nova interface **IPropertySetStorage** para o objeto de armazenamento especificado.</span><span class="sxs-lookup"><span data-stu-id="924f7-111">This function provides a pointer to the new **IPropertySetStorage** interface for the specified storage object.</span></span>

<span data-ttu-id="924f7-112">A implementação autônoma do [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) cria conjuntos de propriedades em qualquer objeto de armazenamento, não apenas em armazenamentos de arquivos compostos.</span><span class="sxs-lookup"><span data-stu-id="924f7-112">The stand-alone implementation of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) creates property sets on any storage object, not just on compound file storages.</span></span> <span data-ttu-id="924f7-113">A implementação autônoma não depende de arquivos compostos e pode ser usada com qualquer implementação de armazenamentos estruturados.</span><span class="sxs-lookup"><span data-stu-id="924f7-113">The stand-alone implementation does not depend on compound files and can be used with any implementation of structured storages.</span></span> <span data-ttu-id="924f7-114">Quaisquer restrições nos armazenamentos estruturados fornecidos pelo chamador se aplicam a essa implementação de conjuntos de propriedades.</span><span class="sxs-lookup"><span data-stu-id="924f7-114">Any restrictions on the caller-provided structured storages apply to this implementation of property sets.</span></span> <span data-ttu-id="924f7-115">Por exemplo, se você fornecer um armazenamento de modo simples para [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg), o **IPropertySetStorage** resultante será restringido pelo [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)fornecido.</span><span class="sxs-lookup"><span data-stu-id="924f7-115">For example, if you provide a simple-mode storage to [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg), the resulting **IPropertySetStorage** will be restricted by the supplied [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage).</span></span>

<span data-ttu-id="924f7-116">Para obter mais informações sobre a implementação de arquivo composto dessa interface, consulte a seção [IPropertySetStorage-composição de arquivos](ipropertysetstorage-compound-file-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="924f7-116">For more information about the compound file implementation of this interface, see the section [IPropertySetStorage-Compound File Implementation](ipropertysetstorage-compound-file-implementation.md).</span></span>

## <a name="when-to-use"></a><span data-ttu-id="924f7-117">Quando usar</span><span class="sxs-lookup"><span data-stu-id="924f7-117">When to Use</span></span>

<span data-ttu-id="924f7-118">Chame os métodos de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) para criar, abrir e excluir conjuntos de propriedades em qualquer armazenamento estruturado.</span><span class="sxs-lookup"><span data-stu-id="924f7-118">Call the methods of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) to create, open, and delete property sets in any structured storage.</span></span> <span data-ttu-id="924f7-119">Também há um método que fornece um ponteiro para o enumerador [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) que pode ser usado para enumerar os conjuntos de propriedades no armazenamento.</span><span class="sxs-lookup"><span data-stu-id="924f7-119">There is also a method that supplies a pointer to the [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) enumerator that can be used to enumerate the property sets in the storage.</span></span>

<span data-ttu-id="924f7-120">A implementação autônoma também fornece as funções auxiliares [**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) e [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) , além dos métodos [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) e [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) , para criar e abrir conjuntos de propriedades.</span><span class="sxs-lookup"><span data-stu-id="924f7-120">The stand-alone implementation also provides the [**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) and [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) helper functions, in addition to the [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) and [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) methods, to create and open property sets.</span></span> <span data-ttu-id="924f7-121">Essas duas funções adicionam suporte para o \_ valor sem buffer PROPSETFLAG para que você possa gravar as alterações diretamente no conjunto de propriedades em vez de armazená-las em um cache.</span><span class="sxs-lookup"><span data-stu-id="924f7-121">These two functions add support for the PROPSETFLAG\_UNBUFFERED value so you can write changes directly to the property set instead of buffering them in a cache.</span></span> <span data-ttu-id="924f7-122">Para obter mais informações, consulte [**constantes PROPSETFLAG**](propsetflag-constants.md).</span><span class="sxs-lookup"><span data-stu-id="924f7-122">For more information, see [**PROPSETFLAG Constants**](propsetflag-constants.md).</span></span>

## <a name="methods"></a><span data-ttu-id="924f7-123">Métodos</span><span class="sxs-lookup"><span data-stu-id="924f7-123">Methods</span></span>

<span data-ttu-id="924f7-124">A implementação autônoma do [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) dá suporte aos métodos a seguir.</span><span class="sxs-lookup"><span data-stu-id="924f7-124">The stand-alone implementation of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) supports the following methods.</span></span>

<dl> <dt>

<span data-ttu-id="924f7-125"><span id="IPropertySetStorage__Create"></span><span id="ipropertysetstorage__create"></span><span id="IPROPERTYSETSTORAGE__CREATE"></span>[**IPropertySetStorage:: criar**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)</span><span class="sxs-lookup"><span data-stu-id="924f7-125"><span id="IPropertySetStorage__Create"></span><span id="ipropertysetstorage__create"></span><span id="IPROPERTYSETSTORAGE__CREATE"></span>[**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)</span></span>
</dt> <dd>

<span data-ttu-id="924f7-126">Cria uma nova propriedade definida no armazenamento e retorna um ponteiro para a interface [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) no conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="924f7-126">Creates a new property set in the storage and returns a pointer to the [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) interface on the property set.</span></span>

<span data-ttu-id="924f7-127">Se você planeja usar o valor sem \_ buffer PROPSETFLAG, use a função [**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) em vez disso para criar e abrir o novo conjunto de propriedades e obter um ponteiro para a implementação autônoma da interface [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) no conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="924f7-127">If you plan to use the PROPSETFLAG\_UNBUFFERED value, use the [**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) function instead to create and open the new property set and to obtain a pointer to the stand-alone implementation for the [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) interface on the property set.</span></span>

</dd> <dt>

<span data-ttu-id="924f7-128"><span id="IPropertySetStorage__Open"></span><span id="ipropertysetstorage__open"></span><span id="IPROPERTYSETSTORAGE__OPEN"></span>[**IPropertySetStorage:: abrir**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)</span><span class="sxs-lookup"><span data-stu-id="924f7-128"><span id="IPropertySetStorage__Open"></span><span id="ipropertysetstorage__open"></span><span id="IPROPERTYSETSTORAGE__OPEN"></span>[**IPropertySetStorage::Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)</span></span>
</dt> <dd>

<span data-ttu-id="924f7-129">Abre um conjunto de propriedades existente no armazenamento e retorna um ponteiro para a interface [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) no conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="924f7-129">Opens an existing property set in the storage and returns a pointer to the [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) interface on the property set.</span></span>

<span data-ttu-id="924f7-130">Se você planeja usar o valor sem \_ buffer PROPSETFLAG, use a função [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) em vez disso, para obter um ponteiro para a implementação autônoma de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) no conjunto de propriedades especificado.</span><span class="sxs-lookup"><span data-stu-id="924f7-130">If you plan to use the PROPSETFLAG\_UNBUFFERED value, use the [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) function instead to obtain a pointer to the stand-alone implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) on the specified property set.</span></span>

</dd> <dt>

<span data-ttu-id="924f7-131"><span id="IPropertySetStorage__Delete"></span><span id="ipropertysetstorage__delete"></span><span id="IPROPERTYSETSTORAGE__DELETE"></span>[**IPropertySetStorage::D excluir**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-delete)</span><span class="sxs-lookup"><span data-stu-id="924f7-131"><span id="IPropertySetStorage__Delete"></span><span id="ipropertysetstorage__delete"></span><span id="IPROPERTYSETSTORAGE__DELETE"></span>[**IPropertySetStorage::Delete**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-delete)</span></span>
</dt> <dd>

<span data-ttu-id="924f7-132">Exclui um conjunto de propriedades neste armazenamento de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="924f7-132">Deletes a property set in this property set storage.</span></span>

</dd> <dt>

<span data-ttu-id="924f7-133"><span id="IPropertySetStorage__Enum"></span><span id="ipropertysetstorage__enum"></span><span id="IPROPERTYSETSTORAGE__ENUM"></span>[**IPropertySetStorage:: enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum)</span><span class="sxs-lookup"><span data-stu-id="924f7-133"><span id="IPropertySetStorage__Enum"></span><span id="ipropertysetstorage__enum"></span><span id="IPROPERTYSETSTORAGE__ENUM"></span>[**IPropertySetStorage::Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum)</span></span>
</dt> <dd>

<span data-ttu-id="924f7-134">Cria um objeto que pode ser usado para enumerar estruturas [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) .</span><span class="sxs-lookup"><span data-stu-id="924f7-134">Creates an object that can be used to enumerate [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) structures.</span></span> <span data-ttu-id="924f7-135">Cada estrutura **STATPROPSETSTG** fornece dados sobre um único conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="924f7-135">Each **STATPROPSETSTG** structure provides data about a single property set.</span></span>

> [!Note]  
> <span data-ttu-id="924f7-136">O conjunto de propriedades DocumentSummaryInformation e UserDefined é exclusivo, pois ele pode ter duas seções de conjunto de propriedades em um único fluxo subjacente.</span><span class="sxs-lookup"><span data-stu-id="924f7-136">The DocumentSummaryInformation and UserDefined property set is unique in that it may have two property set sections in a single underlying stream.</span></span> <span data-ttu-id="924f7-137">Para obter mais informações, consulte [os conjuntos de propriedades DocumentSummaryInformation e UserDefined](the-documentsummaryinformation-and-userdefined-property-sets.md) .</span><span class="sxs-lookup"><span data-stu-id="924f7-137">For more information, see [The DocumentSummaryInformation and UserDefined Property Sets](the-documentsummaryinformation-and-userdefined-property-sets.md) .</span></span>

 

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="924f7-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="924f7-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="924f7-139">Implementação IPropertyStorage-autônoma</span><span class="sxs-lookup"><span data-stu-id="924f7-139">IPropertyStorage-Stand-alone Implementation</span></span>](ipropertystorage-stand-alone-implementation.md)
</dt> <dt>

[<span data-ttu-id="924f7-140">**IPropertySetStorage**</span><span class="sxs-lookup"><span data-stu-id="924f7-140">**IPropertySetStorage**</span></span>](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)
</dt> <dt>

[<span data-ttu-id="924f7-141">**IPropertyStorage**</span><span class="sxs-lookup"><span data-stu-id="924f7-141">**IPropertyStorage**</span></span>](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[<span data-ttu-id="924f7-142">**IStorage:: EnumElements**</span><span class="sxs-lookup"><span data-stu-id="924f7-142">**IStorage::EnumElements**</span></span>](/windows/desktop/api/Objidl/nf-objidl-istorage-enumelements)
</dt> <dt>

[<span data-ttu-id="924f7-143">**Constantes PROPSETFLAG**</span><span class="sxs-lookup"><span data-stu-id="924f7-143">**PROPSETFLAG Constants**</span></span>](propsetflag-constants.md)
</dt> <dt>

[<span data-ttu-id="924f7-144">**STATPROPSETSTG**</span><span class="sxs-lookup"><span data-stu-id="924f7-144">**STATPROPSETSTG**</span></span>](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)
</dt> <dt>

[<span data-ttu-id="924f7-145">**StgCreatePropSetStg**</span><span class="sxs-lookup"><span data-stu-id="924f7-145">**StgCreatePropSetStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg)
</dt> <dt>

[<span data-ttu-id="924f7-146">**StgCreatePropStg**</span><span class="sxs-lookup"><span data-stu-id="924f7-146">**StgCreatePropStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg)
</dt> <dt>

[<span data-ttu-id="924f7-147">**StgOpenPropStg**</span><span class="sxs-lookup"><span data-stu-id="924f7-147">**StgOpenPropStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg)
</dt> <dt>

[<span data-ttu-id="924f7-148">**Constantes STGM**</span><span class="sxs-lookup"><span data-stu-id="924f7-148">**STGM Constants**</span></span>](stgm-constants.md)
</dt> </dl>

 

 