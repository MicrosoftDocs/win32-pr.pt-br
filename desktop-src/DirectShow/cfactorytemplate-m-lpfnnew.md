---
description: 'CFactoryTemplate:: m_lpfnNew ponteiro de membro para uma função que cria uma instância do objeto.'
ms.assetid: 86859bf9-e16a-4494-bf1b-1d8ddbc1c805
title: 'Membro CFactoryTemplate:: m_lpfnNew (combase. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lpfnNew
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ee4ec8e1503d3b260e025d154624b2d7c09bb49b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095644"
---
# <a name="cfactorytemplatem_lpfnnew-member"></a><span data-ttu-id="faf72-103">Membro de CFactoryTemplate:: m \_ lpfnNew</span><span class="sxs-lookup"><span data-stu-id="faf72-103">CFactoryTemplate::m\_lpfnNew member</span></span>

<span data-ttu-id="faf72-104">Ponteiro para uma função que cria uma instância do objeto.</span><span class="sxs-lookup"><span data-stu-id="faf72-104">Pointer to a function that creates an instance of the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="faf72-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="faf72-105">Syntax</span></span>


```C++
LPFNNewCOMObject m_lpfnNew;
```



## <a name="remarks"></a><span data-ttu-id="faf72-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="faf72-106">Remarks</span></span>

<span data-ttu-id="faf72-107">Em sua DLL, declare uma função estática que retorna um ponteiro para uma nova instância do objeto.</span><span class="sxs-lookup"><span data-stu-id="faf72-107">In your DLL, declare a static function that returns a pointer to a new instance of the object.</span></span> <span data-ttu-id="faf72-108">No modelo de fábrica, defina a variável de membro **m \_ lpfnNew** como o endereço dessa função estática.</span><span class="sxs-lookup"><span data-stu-id="faf72-108">In the factory template, set the **m\_lpfnNew** member variable to the address of this static function.</span></span>

<span data-ttu-id="faf72-109">O tipo de ponteiro de função é [**LPFNNewCOMObject**](lpfnnewcomobject.md).</span><span class="sxs-lookup"><span data-stu-id="faf72-109">The function pointer type is [**LPFNNewCOMObject**](lpfnnewcomobject.md).</span></span>

<span data-ttu-id="faf72-110">O exemplo a seguir mostra uma função típica para **m \_ lpfnNew**:</span><span class="sxs-lookup"><span data-stu-id="faf72-110">The following example shows a typical function for **m\_lpfnNew**:</span></span>


```C++
CUnknown * WINAPI CMyComponent::CreateInstance(LPUNKNOWN pUnk, HRESULT *pHr) 
{
    CMyComponent *pNewObject = 
        new CMyComponent(NAME("My Component"), pUnk, pHr );

    if (pNewObject == NULL)  
    {
        *phr = E_OUTOFMEMORY;
    }
    return pNewObject;
}
```



## <a name="requirements"></a><span data-ttu-id="faf72-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="faf72-111">Requirements</span></span>



| <span data-ttu-id="faf72-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="faf72-112">Requirement</span></span> | <span data-ttu-id="faf72-113">Valor</span><span class="sxs-lookup"><span data-stu-id="faf72-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="faf72-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="faf72-114">Header</span></span><br/>  | <dl> <span data-ttu-id="faf72-115"><dt>Combase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="faf72-115"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="faf72-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="faf72-116">Library</span></span><br/> | <dl> <span data-ttu-id="faf72-117"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="faf72-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="faf72-118">Consulte também</span><span class="sxs-lookup"><span data-stu-id="faf72-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="faf72-119">**Classe CFactoryTemplate**</span><span class="sxs-lookup"><span data-stu-id="faf72-119">**CFactoryTemplate Class**</span></span>](cfactorytemplate.md)
</dt> </dl>

 

 




