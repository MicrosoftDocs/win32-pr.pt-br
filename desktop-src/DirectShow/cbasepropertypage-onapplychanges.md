---
description: O método OnApplyChanges é chamado quando o usuário aplica alterações à página de propriedades.
ms.assetid: 15a55644-b7bf-4c72-8e26-18fc4fb714b9
title: Método CBasePropertyPage. OnApplyChanges (cProp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnApplyChanges
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cbcea308a8daaa8b9fdf15be765dc5d3a0df182c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780886"
---
# <a name="cbasepropertypageonapplychanges-method"></a><span data-ttu-id="82bc2-103">Método CBasePropertyPage. OnApplyChanges</span><span class="sxs-lookup"><span data-stu-id="82bc2-103">CBasePropertyPage.OnApplyChanges method</span></span>

<span data-ttu-id="82bc2-104">O `OnApplyChanges` método é chamado quando o usuário aplica alterações à página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="82bc2-104">The `OnApplyChanges` method is called when the user applies changes to the property page.</span></span>

## <a name="syntax"></a><span data-ttu-id="82bc2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="82bc2-105">Syntax</span></span>


```C++
virtual HRESULT OnApplyChanges();
```



## <a name="parameters"></a><span data-ttu-id="82bc2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="82bc2-106">Parameters</span></span>

<span data-ttu-id="82bc2-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="82bc2-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="82bc2-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="82bc2-108">Return value</span></span>

<span data-ttu-id="82bc2-109">A implementação da classe base retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="82bc2-109">The base-class implementation returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="82bc2-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="82bc2-110">Remarks</span></span>

<span data-ttu-id="82bc2-111">O método [**CBasePropertyPage:: apply**](cbasepropertypage-apply.md) chama `OnApplyChanges` se o sinalizador [**CBasePropertyPage:: m \_ bDirty**](cbasepropertypage-m-bdirty.md) é **true**.</span><span class="sxs-lookup"><span data-stu-id="82bc2-111">The [**CBasePropertyPage::Apply**](cbasepropertypage-apply.md) method calls `OnApplyChanges` if the [**CBasePropertyPage::m\_bDirty**](cbasepropertypage-m-bdirty.md) flag is **TRUE**.</span></span> <span data-ttu-id="82bc2-112">Substitua `OnApplyChanges` para processar as alterações e redefinir **m \_ bDirty** como **false**.</span><span class="sxs-lookup"><span data-stu-id="82bc2-112">Override `OnApplyChanges` to process the changes and reset **m\_bDirty** to **FALSE**.</span></span>

## <a name="examples"></a><span data-ttu-id="82bc2-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="82bc2-113">Examples</span></span>


```C++
HRESULT CMyProp::OnApplyChanges(void)
{
    ASSERT(m_pOwningFilter != NULL);
    return m_pOwningFilter->SetSomeProperty(&m_lNewVal);
}
```



## <a name="requirements"></a><span data-ttu-id="82bc2-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82bc2-114">Requirements</span></span>



| <span data-ttu-id="82bc2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="82bc2-115">Requirement</span></span> | <span data-ttu-id="82bc2-116">Valor</span><span class="sxs-lookup"><span data-stu-id="82bc2-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82bc2-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="82bc2-117">Header</span></span><br/>  | <dl> <span data-ttu-id="82bc2-118"><dt>CProp. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="82bc2-118"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="82bc2-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="82bc2-119">Library</span></span><br/> | <dl> <span data-ttu-id="82bc2-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="82bc2-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82bc2-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="82bc2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82bc2-122">**Classe CBasePropertyPage**</span><span class="sxs-lookup"><span data-stu-id="82bc2-122">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




