---
description: 'O método Activate cria a janela da caixa de diálogo. Esse método implementa o método IPropertyPage:: Activate.'
ms.assetid: 8f030dc5-1d14-46b5-9d40-7f07a1177dbe
title: Método CBasePropertyPage. Activate (cProp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Activate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4b851cfc4490d25e7e30dfd2cf0e7c33b0e76224
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756638"
---
# <a name="cbasepropertypageactivate-method"></a><span data-ttu-id="16958-104">Método CBasePropertyPage. Activate</span><span class="sxs-lookup"><span data-stu-id="16958-104">CBasePropertyPage.Activate method</span></span>

<span data-ttu-id="16958-105">O `Activate` método cria a janela da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="16958-105">The `Activate` method creates the dialog box window.</span></span> <span data-ttu-id="16958-106">Esse método implementa o método **IPropertyPage:: Activate** .</span><span class="sxs-lookup"><span data-stu-id="16958-106">This method implements the **IPropertyPage::Activate** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="16958-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="16958-107">Syntax</span></span>


```C++
HRESULT Activate(
   HWND    hwndParent,
   LPCRECT prect,
   BOOL    fModal
);
```



## <a name="parameters"></a><span data-ttu-id="16958-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="16958-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16958-109">*hwndParent*</span><span class="sxs-lookup"><span data-stu-id="16958-109">*hwndParent*</span></span> 
</dt> <dd>

<span data-ttu-id="16958-110">Identificador para a janela pai da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="16958-110">Handle to the parent window of the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="16958-111">*prect*</span><span class="sxs-lookup"><span data-stu-id="16958-111">*prect*</span></span> 
</dt> <dd>

<span data-ttu-id="16958-112">Ponteiro para uma estrutura **Rect** que contém informações de posicionamento para a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="16958-112">Pointer to a **RECT** structure that contains positioning information for the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="16958-113">*fModal*</span><span class="sxs-lookup"><span data-stu-id="16958-113">*fModal*</span></span> 
</dt> <dd>

<span data-ttu-id="16958-114">Valor booliano que indica se o quadro da caixa de diálogo é modal (**true**) ou sem janela restrita (**false**).</span><span class="sxs-lookup"><span data-stu-id="16958-114">Boolean value indicating whether the dialog box frame is modal (**TRUE**) or modeless (**FALSE**).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16958-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="16958-115">Return value</span></span>

<span data-ttu-id="16958-116">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="16958-116">Returns an **HRESULT** value.</span></span> <span data-ttu-id="16958-117">Os possíveis valores incluem os seguintes.</span><span class="sxs-lookup"><span data-stu-id="16958-117">Possible values include the following.</span></span>



| <span data-ttu-id="16958-118">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="16958-118">Return code</span></span>                                                                                   | <span data-ttu-id="16958-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="16958-119">Description</span></span>                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="16958-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="16958-120"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="16958-121">Êxito.</span><span class="sxs-lookup"><span data-stu-id="16958-121">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="16958-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="16958-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="16958-123">Memória insuficiente.</span><span class="sxs-lookup"><span data-stu-id="16958-123">Insufficient memory.</span></span><br/>       |
| <dl> <span data-ttu-id="16958-124"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="16958-124"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="16958-125">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="16958-125">**NULL** pointer argument.</span></span><br/> |
| <dl> <span data-ttu-id="16958-126"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="16958-126"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>  | <span data-ttu-id="16958-127">Falha inesperada.</span><span class="sxs-lookup"><span data-stu-id="16958-127">Unexpected failure.</span></span><br/>        |



 

## <a name="requirements"></a><span data-ttu-id="16958-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16958-128">Requirements</span></span>



| <span data-ttu-id="16958-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="16958-129">Requirement</span></span> | <span data-ttu-id="16958-130">Valor</span><span class="sxs-lookup"><span data-stu-id="16958-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16958-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="16958-131">Header</span></span><br/>  | <dl> <span data-ttu-id="16958-132"><dt>CProp. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="16958-132"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="16958-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="16958-133">Library</span></span><br/> | <dl> <span data-ttu-id="16958-134"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="16958-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16958-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="16958-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16958-136">**Classe CBasePropertyPage**</span><span class="sxs-lookup"><span data-stu-id="16958-136">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> <dt>

[<span data-ttu-id="16958-137">**CBasePropertyPage:: OnActivate**</span><span class="sxs-lookup"><span data-stu-id="16958-137">**CBasePropertyPage::OnActivate**</span></span>](cbasepropertypage-onactivate.md)
</dt> </dl>

 

 




