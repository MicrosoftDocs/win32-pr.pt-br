---
description: 'O método Apply aplica os valores da página de propriedades atual ao objeto associado à página de propriedades. Esse método implementa o método IPropertyPage:: apply.'
ms.assetid: 9fe759d1-2b46-4489-b7b8-b5a35330091d
title: Método CBasePropertyPage. Apply (cProp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Apply
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21d1208979cca167b059cb720c492ac51c362c39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749631"
---
# <a name="cbasepropertypageapply-method"></a><span data-ttu-id="37fc6-104">Método CBasePropertyPage. Apply</span><span class="sxs-lookup"><span data-stu-id="37fc6-104">CBasePropertyPage.Apply method</span></span>

<span data-ttu-id="37fc6-105">O `Apply` método aplica os valores da página de propriedades atual ao objeto associado à página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="37fc6-105">The `Apply` method applies the current property page values to the object associated with the property page.</span></span> <span data-ttu-id="37fc6-106">Esse método implementa o método **IPropertyPage:: apply** .</span><span class="sxs-lookup"><span data-stu-id="37fc6-106">This method implements the **IPropertyPage::Apply** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="37fc6-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="37fc6-107">Syntax</span></span>


```C++
HRESULT Apply();
```



## <a name="parameters"></a><span data-ttu-id="37fc6-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="37fc6-108">Parameters</span></span>

<span data-ttu-id="37fc6-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="37fc6-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="37fc6-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="37fc6-110">Return value</span></span>

<span data-ttu-id="37fc6-111">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="37fc6-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="37fc6-112">Os possíveis valores incluem os seguintes.</span><span class="sxs-lookup"><span data-stu-id="37fc6-112">Possible values include the following.</span></span>



| <span data-ttu-id="37fc6-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="37fc6-113">Return code</span></span>                                                                                  | <span data-ttu-id="37fc6-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="37fc6-114">Description</span></span>                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="37fc6-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="37fc6-115"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="37fc6-116">Êxito.</span><span class="sxs-lookup"><span data-stu-id="37fc6-116">Success.</span></span><br/>            |
| <dl> <span data-ttu-id="37fc6-117"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="37fc6-117"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="37fc6-118">Falha inesperada.</span><span class="sxs-lookup"><span data-stu-id="37fc6-118">Unexpected failure.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="37fc6-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="37fc6-119">Remarks</span></span>

<span data-ttu-id="37fc6-120">Se o sinalizador [**CBasePropertyPage:: m \_ BDirty**](cbasepropertypage-m-bdirty.md) for **true**, esse método chamará o método [**CBasePropertyPage:: OnApplyChanges**](cbasepropertypage-onapplychanges.md) .</span><span class="sxs-lookup"><span data-stu-id="37fc6-120">If the [**CBasePropertyPage::m\_bDirty**](cbasepropertypage-m-bdirty.md) flag is **TRUE**, this method calls the [**CBasePropertyPage::OnApplyChanges**](cbasepropertypage-onapplychanges.md) method.</span></span> <span data-ttu-id="37fc6-121">Substitua **OnApplyChanges** para aplicar as alterações ao objeto.</span><span class="sxs-lookup"><span data-stu-id="37fc6-121">Override **OnApplyChanges** to apply the changes to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="37fc6-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37fc6-122">Requirements</span></span>



| <span data-ttu-id="37fc6-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="37fc6-123">Requirement</span></span> | <span data-ttu-id="37fc6-124">Valor</span><span class="sxs-lookup"><span data-stu-id="37fc6-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37fc6-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="37fc6-125">Header</span></span><br/>  | <dl> <span data-ttu-id="37fc6-126"><dt>CProp. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="37fc6-126"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="37fc6-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="37fc6-127">Library</span></span><br/> | <dl> <span data-ttu-id="37fc6-128"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="37fc6-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37fc6-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="37fc6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37fc6-130">**Classe CBasePropertyPage**</span><span class="sxs-lookup"><span data-stu-id="37fc6-130">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




