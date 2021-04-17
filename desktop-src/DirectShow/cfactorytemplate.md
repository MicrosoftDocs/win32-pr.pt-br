---
description: Fornece um modelo para criar fábricas de classes.
ms.assetid: 3dbe6402-15f8-4490-9fe2-bebaa4e79170
title: Classe CFactoryTemplate (combase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CFactoryTemplate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: be5ca9b8319eeddf777cbf0071c1930f21524369
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747594"
---
# <a name="cfactorytemplate-class"></a><span data-ttu-id="3e74a-103">Classe CFactoryTemplate</span><span class="sxs-lookup"><span data-stu-id="3e74a-103">CFactoryTemplate class</span></span>

<span data-ttu-id="3e74a-104">Fornece um modelo para criar fábricas de classes.</span><span class="sxs-lookup"><span data-stu-id="3e74a-104">Provides a template for creating class factories.</span></span>

<span data-ttu-id="3e74a-105">No DirectShow, as fábricas de classes são especializadas usando a classe **CFactoryTemplate** , também chamada de *modelo de fábrica*.</span><span class="sxs-lookup"><span data-stu-id="3e74a-105">In DirectShow, class factories are specialized using the **CFactoryTemplate** class, also called the *factory template*.</span></span> <span data-ttu-id="3e74a-106">Cada fábrica de classe mantém um ponteiro para um modelo de fábrica.</span><span class="sxs-lookup"><span data-stu-id="3e74a-106">Each class factory holds a pointer to a factory template.</span></span> <span data-ttu-id="3e74a-107">O modelo de fábrica contém informações sobre um objeto COM, incluindo o identificador de classe do objeto (CLSID) e um ponteiro para uma função que cria o objeto.</span><span class="sxs-lookup"><span data-stu-id="3e74a-107">The factory template contains information about a COM object, including the object's class identifier (CLSID) and a pointer to a function that creates the object.</span></span>

<span data-ttu-id="3e74a-108">Em sua DLL, declare uma matriz global de modelos de fábrica chamada *g \_ templates*.</span><span class="sxs-lookup"><span data-stu-id="3e74a-108">In your DLL, declare a global array of factory templates named *g\_Templates*.</span></span> <span data-ttu-id="3e74a-109">Inclua um modelo de fábrica para cada objeto na DLL.</span><span class="sxs-lookup"><span data-stu-id="3e74a-109">Include one factory template for each object in the DLL.</span></span> <span data-ttu-id="3e74a-110">Quando a função [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) cria uma nova fábrica de classes, ela pesquisa a matriz em busca de um modelo com um CLSID correspondente.</span><span class="sxs-lookup"><span data-stu-id="3e74a-110">When the [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) function makes a new class factory, it searches the array for a template with a matching CLSID.</span></span> <span data-ttu-id="3e74a-111">Supondo que ele encontre um, ele cria uma fábrica de classes que mantém um ponteiro para o modelo correspondente.</span><span class="sxs-lookup"><span data-stu-id="3e74a-111">Assuming it finds one, it creates a class factory that holds a pointer to the matching template.</span></span> <span data-ttu-id="3e74a-112">Quando o cliente chama **IClassFactory:: CreateInstance**, a fábrica de classes chama a função de instanciação definida no modelo.</span><span class="sxs-lookup"><span data-stu-id="3e74a-112">When the client calls **IClassFactory::CreateInstance**, the class factory calls the instantiation function defined in the template.</span></span>

<span data-ttu-id="3e74a-113">Para obter mais informações, consulte [como criar uma DLL de filtro do DirectShow](how-to-create-a-dll.md).</span><span class="sxs-lookup"><span data-stu-id="3e74a-113">For more information, see [How to Create a DirectShow Filter DLL](how-to-create-a-dll.md).</span></span>



| <span data-ttu-id="3e74a-114">Variáveis de membro público</span><span class="sxs-lookup"><span data-stu-id="3e74a-114">Public Member Variables</span></span>                                                   | <span data-ttu-id="3e74a-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="3e74a-115">Description</span></span>                                                                |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="3e74a-116">**\_nome m**</span><span class="sxs-lookup"><span data-stu-id="3e74a-116">**m\_Name**</span></span>](cfactorytemplate-m-name.md)                                | <span data-ttu-id="3e74a-117">Nome do filtro.</span><span class="sxs-lookup"><span data-stu-id="3e74a-117">Name of the filter.</span></span>                                                        |
| [<span data-ttu-id="3e74a-118">**ClsID do m \_**</span><span class="sxs-lookup"><span data-stu-id="3e74a-118">**m\_ClsID**</span></span>](cfactorytemplate-m-clsid.md)                              | <span data-ttu-id="3e74a-119">Ponteiro para o CLSID do objeto.</span><span class="sxs-lookup"><span data-stu-id="3e74a-119">Pointer to the CLSID of the object.</span></span>                                        |
| [<span data-ttu-id="3e74a-120">**\_lpfnNew m**</span><span class="sxs-lookup"><span data-stu-id="3e74a-120">**m\_lpfnNew**</span></span>](cfactorytemplate-m-lpfnnew.md)                          | <span data-ttu-id="3e74a-121">Ponteiro para uma função que cria uma instância do objeto.</span><span class="sxs-lookup"><span data-stu-id="3e74a-121">Pointer to a function that creates an instance of the object.</span></span>              |
| [<span data-ttu-id="3e74a-122">**\_lpfnInit m**</span><span class="sxs-lookup"><span data-stu-id="3e74a-122">**m\_lpfnInit**</span></span>](cfactorytemplate-m-lpfninit.md)                        | <span data-ttu-id="3e74a-123">Ponteiro para uma função que é chamada a partir do ponto de entrada de DLL.</span><span class="sxs-lookup"><span data-stu-id="3e74a-123">Pointer to a function that gets called from the DLL entry point.</span></span>           |
| [<span data-ttu-id="3e74a-124">**\_filtro de pAMovieSetup m \_**</span><span class="sxs-lookup"><span data-stu-id="3e74a-124">**m\_pAMovieSetup\_Filter**</span></span>](cfactorytemplate-m-pamoviesetup-filter.md) | <span data-ttu-id="3e74a-125">Ponteiro para uma estrutura de [**\_ filtro AMOVIESETUP**](amoviesetup-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="3e74a-125">Pointer to an [**AMOVIESETUP\_FILTER**](amoviesetup-filter.md) structure.</span></span> |
| <span data-ttu-id="3e74a-126">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="3e74a-126">Public Methods</span></span>                                                            | <span data-ttu-id="3e74a-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="3e74a-127">Description</span></span>                                                                |
| [<span data-ttu-id="3e74a-128">**Isclassidid**</span><span class="sxs-lookup"><span data-stu-id="3e74a-128">**IsClassID**</span></span>](cfactorytemplate-isclassid.md)                           | <span data-ttu-id="3e74a-129">Determina se um CLSID corresponde a este modelo de classe.</span><span class="sxs-lookup"><span data-stu-id="3e74a-129">Determines whether a CLSID matches this class template.</span></span>                    |
| [<span data-ttu-id="3e74a-130">**CreateInstance**</span><span class="sxs-lookup"><span data-stu-id="3e74a-130">**CreateInstance**</span></span>](cfactorytemplate-createinstance.md)                 | <span data-ttu-id="3e74a-131">Chama a função de criação de objeto para a classe.</span><span class="sxs-lookup"><span data-stu-id="3e74a-131">Calls the object-creation function for the class.</span></span>                          |



 

## <a name="requirements"></a><span data-ttu-id="3e74a-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e74a-132">Requirements</span></span>



| <span data-ttu-id="3e74a-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e74a-133">Requirement</span></span> | <span data-ttu-id="3e74a-134">Valor</span><span class="sxs-lookup"><span data-stu-id="3e74a-134">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e74a-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3e74a-135">Header</span></span><br/>  | <dl> <span data-ttu-id="3e74a-136"><dt>Combase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3e74a-136"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="3e74a-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3e74a-137">Library</span></span><br/> | <dl> <span data-ttu-id="3e74a-138"><dt>Strmbase. lib; </dt> <dt>Strmbasd. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3e74a-138"><dt>Strmbase.lib; </dt> <dt>Strmbasd.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e74a-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="3e74a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e74a-140">Referência de classe base</span><span class="sxs-lookup"><span data-stu-id="3e74a-140">Base Class Reference</span></span>](base-class-reference.md)
</dt> </dl>

 

