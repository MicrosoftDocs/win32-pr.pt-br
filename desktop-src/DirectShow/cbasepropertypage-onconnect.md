---
description: O método OnConnect fornece um ponteiro IUnknown para o objeto associado à página de propriedades.
ms.assetid: 74cae8e1-5347-4e3d-ba5f-6a4efec2ddae
title: Método CBasePropertyPage. OnConnect (cProp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 38f83a7c491f1591cece8d5d85eb4525a1059d2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755607"
---
# <a name="cbasepropertypageonconnect-method"></a><span data-ttu-id="41d6b-103">Método CBasePropertyPage. OnConnect</span><span class="sxs-lookup"><span data-stu-id="41d6b-103">CBasePropertyPage.OnConnect method</span></span>

<span data-ttu-id="41d6b-104">O `OnConnect` método fornece um ponteiro **IUnknown** para o objeto associado à página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="41d6b-104">The `OnConnect` method provides an **IUnknown** pointer to the object associated with the property page.</span></span>

## <a name="syntax"></a><span data-ttu-id="41d6b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="41d6b-105">Syntax</span></span>


```C++
virtual HRESULT OnConnect(
   IUnknown *pUnknown
);
```



## <a name="parameters"></a><span data-ttu-id="41d6b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="41d6b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41d6b-107">*pUnknown*</span><span class="sxs-lookup"><span data-stu-id="41d6b-107">*pUnknown*</span></span> 
</dt> <dd>

<span data-ttu-id="41d6b-108">Ponteiro para a interface **IUnknown** do objeto.</span><span class="sxs-lookup"><span data-stu-id="41d6b-108">Pointer to the **IUnknown** interface of the object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41d6b-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="41d6b-109">Return value</span></span>

<span data-ttu-id="41d6b-110">A implementação da classe base retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="41d6b-110">The base-class implementation returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="41d6b-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="41d6b-111">Remarks</span></span>

<span data-ttu-id="41d6b-112">O método [**CBasePropertyPage:: SetObjects**](cbasepropertypage-setobjects.md) chama o `OnConnect` método.</span><span class="sxs-lookup"><span data-stu-id="41d6b-112">The [**CBasePropertyPage::SetObjects**](cbasepropertypage-setobjects.md) method calls the `OnConnect` method.</span></span> <span data-ttu-id="41d6b-113">Substitua esse método para armazenar um ponteiro para o objeto especificado por *pUnknown*.</span><span class="sxs-lookup"><span data-stu-id="41d6b-113">Override this method to store a pointer to the object specified by *pUnknown*.</span></span> <span data-ttu-id="41d6b-114">Você pode armazenar o próprio ponteiro *pUnknown* ou consultar o ponteiro para outras interfaces.</span><span class="sxs-lookup"><span data-stu-id="41d6b-114">You can either store the *pUnknown* pointer itself, or query that pointer for other interfaces.</span></span> <span data-ttu-id="41d6b-115">Se você armazenar o ponteiro *pUnknown* , chame **AddRef** antes de `OnConnect` retornar.</span><span class="sxs-lookup"><span data-stu-id="41d6b-115">If you store the *pUnknown* pointer, call **AddRef** before `OnConnect` returns.</span></span>

<span data-ttu-id="41d6b-116">No método [**CBasePropertyPage:: OnActivate**](cbasepropertypage-onactivate.md) , use o ponteiro armazenado (ou ponteiros) para recuperar os valores iniciais das propriedades da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="41d6b-116">In the [**CBasePropertyPage::OnActivate**](cbasepropertypage-onactivate.md) method, use the stored pointer (or pointers) to retrieve initial values for the dialog properties.</span></span> <span data-ttu-id="41d6b-117">No método [**CBasePropertyPage:: OnApplyChanges**](cbasepropertypage-onapplychanges.md) , aplique as alterações de volta ao objeto.</span><span class="sxs-lookup"><span data-stu-id="41d6b-117">In the [**CBasePropertyPage::OnApplyChanges**](cbasepropertypage-onapplychanges.md) method, apply any changes back to the object.</span></span> <span data-ttu-id="41d6b-118">Libere todos os ponteiros no método [**CBasePropertyPage:: OnDisconnect**](cbasepropertypage-ondisconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="41d6b-118">Release all pointers in the [**CBasePropertyPage::OnDisconnect**](cbasepropertypage-ondisconnect.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="41d6b-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="41d6b-119">Examples</span></span>


```C++
HRESULT CMyProp::OnConnect(IUnknown *pUnk)
{
    ASSERT(m_pOwningFilter == NULL);
    HRESULT hr;
    // Query pUnk for the filter's custom interface.
    hr = pUnk->QueryInterface(IID_ISomeCustomInterface,
             reinterpret_cast<void**>(&m_pOwningFilter));
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="41d6b-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41d6b-120">Requirements</span></span>



| <span data-ttu-id="41d6b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="41d6b-121">Requirement</span></span> | <span data-ttu-id="41d6b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="41d6b-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41d6b-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="41d6b-123">Header</span></span><br/>  | <dl> <span data-ttu-id="41d6b-124"><dt>CProp. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="41d6b-124"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="41d6b-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="41d6b-125">Library</span></span><br/> | <dl> <span data-ttu-id="41d6b-126"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="41d6b-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41d6b-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="41d6b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41d6b-128">**Classe CBasePropertyPage**</span><span class="sxs-lookup"><span data-stu-id="41d6b-128">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




