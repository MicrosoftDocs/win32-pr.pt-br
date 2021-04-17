---
description: Ponteiro para uma função que cria uma instância do objeto.
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
ms.openlocfilehash: 2299f7a87f348ac8a5fa6c6d83b6a17fbf97ca28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748447"
---
# <a name="cfactorytemplatem_lpfnnew-member"></a><span data-ttu-id="79011-103">Membro de CFactoryTemplate:: m \_ lpfnNew</span><span class="sxs-lookup"><span data-stu-id="79011-103">CFactoryTemplate::m\_lpfnNew member</span></span>

<span data-ttu-id="79011-104">Ponteiro para uma função que cria uma instância do objeto.</span><span class="sxs-lookup"><span data-stu-id="79011-104">Pointer to a function that creates an instance of the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="79011-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="79011-105">Syntax</span></span>


```C++
LPFNNewCOMObject m_lpfnNew;
```



## <a name="remarks"></a><span data-ttu-id="79011-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="79011-106">Remarks</span></span>

<span data-ttu-id="79011-107">Em sua DLL, declare uma função estática que retorna um ponteiro para uma nova instância do objeto.</span><span class="sxs-lookup"><span data-stu-id="79011-107">In your DLL, declare a static function that returns a pointer to a new instance of the object.</span></span> <span data-ttu-id="79011-108">No modelo de fábrica, defina a variável de membro **m \_ lpfnNew** como o endereço dessa função estática.</span><span class="sxs-lookup"><span data-stu-id="79011-108">In the factory template, set the **m\_lpfnNew** member variable to the address of this static function.</span></span>

<span data-ttu-id="79011-109">O tipo de ponteiro de função é [**LPFNNewCOMObject**](lpfnnewcomobject.md).</span><span class="sxs-lookup"><span data-stu-id="79011-109">The function pointer type is [**LPFNNewCOMObject**](lpfnnewcomobject.md).</span></span>

<span data-ttu-id="79011-110">O exemplo a seguir mostra uma função típica para **m \_ lpfnNew**:</span><span class="sxs-lookup"><span data-stu-id="79011-110">The following example shows a typical function for **m\_lpfnNew**:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="79011-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79011-111">Requirements</span></span>



| <span data-ttu-id="79011-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="79011-112">Requirement</span></span> | <span data-ttu-id="79011-113">Valor</span><span class="sxs-lookup"><span data-stu-id="79011-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79011-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="79011-114">Header</span></span><br/>  | <dl> <span data-ttu-id="79011-115"><dt>Combase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="79011-115"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="79011-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="79011-116">Library</span></span><br/> | <dl> <span data-ttu-id="79011-117"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="79011-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79011-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="79011-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79011-119">**Classe CFactoryTemplate**</span><span class="sxs-lookup"><span data-stu-id="79011-119">**CFactoryTemplate Class**</span></span>](cfactorytemplate.md)
</dt> </dl>

 

 




