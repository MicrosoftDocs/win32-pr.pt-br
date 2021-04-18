---
title: CCLSOBJ. CPP
description: No componente de provedor de exemplo, as funções para o objeto de classe de esquema estão contidas em cclsobj. cpp.
ms.assetid: e8cdef8e-c031-49e0-9496-871064aec8bd
ms.tgt_platform: multiple
keywords:
- CSampleDSClass
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f23c198413819627ce1fcb5a605bd8e45faae0ce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105771762"
---
# <a name="cclsobjcpp"></a><span data-ttu-id="096fb-104">CCLSOBJ. CPP</span><span class="sxs-lookup"><span data-stu-id="096fb-104">CCLSOBJ.CPP</span></span>

<span data-ttu-id="096fb-105">No componente de provedor de exemplo, as funções para o objeto de classe de esquema estão contidas em cclsobj. cpp.</span><span class="sxs-lookup"><span data-stu-id="096fb-105">In the example provider component, the functions for the schema class object are contained in cclsobj.cpp.</span></span>

<span data-ttu-id="096fb-106">A classe **CSampleDSClass** está definida neste arquivo.</span><span class="sxs-lookup"><span data-stu-id="096fb-106">The **CSampleDSClass** class is defined in this file.</span></span> <span data-ttu-id="096fb-107">**CSampleDSClass** é definido com métodos e propriedades listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="096fb-107">**CSampleDSClass** is defined with methods and properties listed in the following table.</span></span>



| <span data-ttu-id="096fb-108">Método</span><span class="sxs-lookup"><span data-stu-id="096fb-108">Method</span></span>                      | <span data-ttu-id="096fb-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="096fb-109">Description</span></span>                                                                                                                                                                                                |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="096fb-110">**CSampleDSClass**</span><span class="sxs-lookup"><span data-stu-id="096fb-110">**CSampleDSClass**</span></span>          | <span data-ttu-id="096fb-111">Construtor padrão.</span><span class="sxs-lookup"><span data-stu-id="096fb-111">Standard constructor.</span></span>                                                                                                                                                                                      |
| <span data-ttu-id="096fb-112">**~ CSampleDSClass**</span><span class="sxs-lookup"><span data-stu-id="096fb-112">**~CSampleDSClass**</span></span>         | <span data-ttu-id="096fb-113">Destruidor padrão.</span><span class="sxs-lookup"><span data-stu-id="096fb-113">Standard destructor.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="096fb-114">**Createclass**</span><span class="sxs-lookup"><span data-stu-id="096fb-114">**CreateClass**</span></span>             | <span data-ttu-id="096fb-115">Crie um objeto de classe de esquema ADs.</span><span class="sxs-lookup"><span data-stu-id="096fb-115">Create an ADs schema class object.</span></span> <span data-ttu-id="096fb-116">Definições de atributo de pesquisa chamando **SampleDSGetClassDefinition**.</span><span class="sxs-lookup"><span data-stu-id="096fb-116">Lookup attribute definitions by calling **SampleDSGetClassDefinition**.</span></span>                                                                                                 |
| <span data-ttu-id="096fb-117">**Createclass**</span><span class="sxs-lookup"><span data-stu-id="096fb-117">**CreateClass**</span></span>             | <span data-ttu-id="096fb-118">Crie um objeto de classe de esquema, dadas as definições de atributo, definindo atributos conhecidos, como aqueles listados em [**IADsClass:: mandatoryattributes**](iadsclass-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="096fb-118">Create a schema class object, given the attribute definitions, setting known attributes, such as those listed in [**IADsClass::MandatoryAttributes**](iadsclass-property-methods.md).</span></span>                     |
| <span data-ttu-id="096fb-119">**AllocateClassObject**</span><span class="sxs-lookup"><span data-stu-id="096fb-119">**AllocateClassObject**</span></span>     | <span data-ttu-id="096fb-120">Crie um objeto de classe de esquema e carregue seus dados de tipo.</span><span class="sxs-lookup"><span data-stu-id="096fb-120">Create a schema class object and load its type data.</span></span>                                                                                                                                                       |
| <span data-ttu-id="096fb-121">**QueryInterface**</span><span class="sxs-lookup"><span data-stu-id="096fb-121">**QueryInterface**</span></span>          | <span data-ttu-id="096fb-122">Retorne o ponteiro de interface solicitado, se disponível.</span><span class="sxs-lookup"><span data-stu-id="096fb-122">Return the requested interface pointer, if available.</span></span>                                                                                                                                                      |
| <span data-ttu-id="096fb-123">Métodos IADs padrão.</span><span class="sxs-lookup"><span data-stu-id="096fb-123">Standard IADs methods.</span></span>      | <span data-ttu-id="096fb-124">Métodos de interface padrão [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) incluídos neste arquivo.</span><span class="sxs-lookup"><span data-stu-id="096fb-124">Standard [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface methods included in this file.</span></span>                                                                                                                                     |
| <span data-ttu-id="096fb-125">Métodos IADsClass padrão.</span><span class="sxs-lookup"><span data-stu-id="096fb-125">Standard IADsClass methods.</span></span> | <span data-ttu-id="096fb-126">Métodos de interface [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) padrão incluídos neste arquivo.</span><span class="sxs-lookup"><span data-stu-id="096fb-126">Standard [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) interface methods included in this file.</span></span>                                                                                                                           |
| <span data-ttu-id="096fb-127">**Createpropertylist**</span><span class="sxs-lookup"><span data-stu-id="096fb-127">**CreatePropertyList**</span></span>      | <span data-ttu-id="096fb-128">Crie uma lista de propriedades associadas a essa classe de esquema chamando **CreatePropertyEntry**.</span><span class="sxs-lookup"><span data-stu-id="096fb-128">Create a list of properties associated with this schema class by calling **CreatePropertyEntry**.</span></span>                                                                                                          |
| <span data-ttu-id="096fb-129">**CreatePropertyEntry**</span><span class="sxs-lookup"><span data-stu-id="096fb-129">**CreatePropertyEntry**</span></span>     | <span data-ttu-id="096fb-130">Crie um objeto de propriedade nesta classe de esquema.</span><span class="sxs-lookup"><span data-stu-id="096fb-130">Create one property object in this schema class.</span></span>                                                                                                                                                           |
| <span data-ttu-id="096fb-131">**FreePropertyEntry**</span><span class="sxs-lookup"><span data-stu-id="096fb-131">**FreePropertyEntry**</span></span>       | <span data-ttu-id="096fb-132">Libere a entrada feita em **CreatePropertyEntry**.</span><span class="sxs-lookup"><span data-stu-id="096fb-132">Free the entry made in **CreatePropertyEntry**.</span></span>                                                                                                                                                            |
| <span data-ttu-id="096fb-133">**MakeVariantFromPropList**</span><span class="sxs-lookup"><span data-stu-id="096fb-133">**MakeVariantFromPropList**</span></span> | <span data-ttu-id="096fb-134">Crie uma matriz de VARIAntes na lista de propriedades criada por **Createpropertylist**.</span><span class="sxs-lookup"><span data-stu-id="096fb-134">Create an array of VARIANTS from the property list created by **CreatePropertyList**.</span></span> <span data-ttu-id="096fb-135">Pode ser usado na implementação de [**IADsClass:: mandatoryattributes**](iadsclass-property-methods.md) e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="096fb-135">Can be used in the implementation of [**IADsClass::MandatoryAttributes**](iadsclass-property-methods.md) and so on.</span></span> |



 

 

 




