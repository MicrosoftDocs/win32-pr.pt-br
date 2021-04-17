---
description: O método OnDisconnect é chamado quando a página de propriedades deve liberar o objeto associado.
ms.assetid: 55bab0ca-587e-405c-9025-f391cf08a620
title: Método CBasePropertyPage. OnDisconnect (cProp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnDisconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: abd251d20ca82ad0374a613d9ee73f0eaee21d31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811752"
---
# <a name="cbasepropertypageondisconnect-method"></a><span data-ttu-id="592ba-103">Método CBasePropertyPage. OnDisconnect</span><span class="sxs-lookup"><span data-stu-id="592ba-103">CBasePropertyPage.OnDisconnect method</span></span>

<span data-ttu-id="592ba-104">O `OnDisconnect` método é chamado quando a página de propriedades deve liberar o objeto associado.</span><span class="sxs-lookup"><span data-stu-id="592ba-104">The `OnDisconnect` method is called when the property page should release the associated object.</span></span>

## <a name="syntax"></a><span data-ttu-id="592ba-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="592ba-105">Syntax</span></span>


```C++
virtual HRESULT OnDisconnect();
```



## <a name="parameters"></a><span data-ttu-id="592ba-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="592ba-106">Parameters</span></span>

<span data-ttu-id="592ba-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="592ba-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="592ba-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="592ba-108">Return value</span></span>

<span data-ttu-id="592ba-109">A implementação da classe base retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="592ba-109">The base-class implementation returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="592ba-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="592ba-110">Remarks</span></span>

<span data-ttu-id="592ba-111">O método [**CBasePropertyPage:: SetObjects**](cbasepropertypage-setobjects.md) chama o `OnDisconnect` método.</span><span class="sxs-lookup"><span data-stu-id="592ba-111">The [**CBasePropertyPage::SetObjects**](cbasepropertypage-setobjects.md) method calls the `OnDisconnect` method.</span></span> <span data-ttu-id="592ba-112">Substitua `OnDisconnect` para liberar quaisquer ponteiros que foram obtidos no método [**CBasePropertyPage:: OnConnect**](cbasepropertypage-onconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="592ba-112">Override `OnDisconnect` to release any pointers that were obtained in the [**CBasePropertyPage::OnConnect**](cbasepropertypage-onconnect.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="592ba-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="592ba-113">Examples</span></span>


```C++
HRESULT CMyProp::OnDisconnect(void)
{
    if (m_pOwningFilter)
    {
        m_pOwningFilter->Release();
        m_pOwningFilter = NULL;
    }
    return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="592ba-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="592ba-114">Requirements</span></span>



| <span data-ttu-id="592ba-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="592ba-115">Requirement</span></span> | <span data-ttu-id="592ba-116">Valor</span><span class="sxs-lookup"><span data-stu-id="592ba-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="592ba-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="592ba-117">Header</span></span><br/>  | <dl> <span data-ttu-id="592ba-118"><dt>CProp. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="592ba-118"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="592ba-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="592ba-119">Library</span></span><br/> | <dl> <span data-ttu-id="592ba-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="592ba-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="592ba-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="592ba-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="592ba-122">**Classe CBasePropertyPage**</span><span class="sxs-lookup"><span data-stu-id="592ba-122">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




