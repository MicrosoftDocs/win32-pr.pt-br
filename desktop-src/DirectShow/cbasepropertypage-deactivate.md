---
description: O método Deactivate destrói a janela da caixa de diálogo. Esse método implementa o método IPropertyPage::D eactivate.
ms.assetid: f2d2f15f-15f6-4902-bafc-f58a684ff193
title: Método CBasePropertyPage. Deactivate (cProp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Deactivate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 63a843502fc735cc41ff3656e83ef3d6cb839a19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748221"
---
# <a name="cbasepropertypagedeactivate-method"></a><span data-ttu-id="56a3e-104">Método CBasePropertyPage. Deactivate</span><span class="sxs-lookup"><span data-stu-id="56a3e-104">CBasePropertyPage.Deactivate method</span></span>

<span data-ttu-id="56a3e-105">O `Deactivate` método destrói a janela da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="56a3e-105">The `Deactivate` method destroys the dialog window.</span></span> <span data-ttu-id="56a3e-106">Esse método implementa o método **IPropertyPage::D eactivate** .</span><span class="sxs-lookup"><span data-stu-id="56a3e-106">This method implements the **IPropertyPage::Deactivate** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="56a3e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="56a3e-107">Syntax</span></span>


```C++
HRESULT Deactivate();
```



## <a name="parameters"></a><span data-ttu-id="56a3e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="56a3e-108">Parameters</span></span>

<span data-ttu-id="56a3e-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="56a3e-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="56a3e-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="56a3e-110">Return value</span></span>

<span data-ttu-id="56a3e-111">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="56a3e-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="56a3e-112">Os possíveis valores incluem os seguintes.</span><span class="sxs-lookup"><span data-stu-id="56a3e-112">Possible values include the following.</span></span>



| <span data-ttu-id="56a3e-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="56a3e-113">Return code</span></span>                                                                                  | <span data-ttu-id="56a3e-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="56a3e-114">Description</span></span>                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="56a3e-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="56a3e-115"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="56a3e-116">Êxito.</span><span class="sxs-lookup"><span data-stu-id="56a3e-116">Success.</span></span><br/>            |
| <dl> <span data-ttu-id="56a3e-117"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="56a3e-117"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="56a3e-118">Falha inesperada.</span><span class="sxs-lookup"><span data-stu-id="56a3e-118">Unexpected failure.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="56a3e-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56a3e-119">Requirements</span></span>



| <span data-ttu-id="56a3e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="56a3e-120">Requirement</span></span> | <span data-ttu-id="56a3e-121">Valor</span><span class="sxs-lookup"><span data-stu-id="56a3e-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56a3e-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="56a3e-122">Header</span></span><br/>  | <dl> <span data-ttu-id="56a3e-123"><dt>CProp. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="56a3e-123"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="56a3e-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="56a3e-124">Library</span></span><br/> | <dl> <span data-ttu-id="56a3e-125"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="56a3e-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56a3e-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="56a3e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56a3e-127">**Classe CBasePropertyPage**</span><span class="sxs-lookup"><span data-stu-id="56a3e-127">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> <dt>

[<span data-ttu-id="56a3e-128">**CBasePropertyPage:: OnActivate**</span><span class="sxs-lookup"><span data-stu-id="56a3e-128">**CBasePropertyPage::OnDeactivate**</span></span>](cbasepropertypage-ondeactivate.md)
</dt> </dl>

 

 




