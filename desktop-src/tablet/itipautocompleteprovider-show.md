---
description: Exibe ou oculta a lista de preenchimento automático.
ms.assetid: 756ffa3d-03ee-4753-a826-3bc22ab16f5f
title: 'Método ITipAutocompleteProvider:: show (TipAutoComplete. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteProvider.Show
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 950358ae28d1cb68af803ed6b7f520f1bbad8c03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663260"
---
# <a name="itipautocompleteprovidershow-method"></a><span data-ttu-id="378b7-103">Método ITipAutocompleteProvider:: show</span><span class="sxs-lookup"><span data-stu-id="378b7-103">ITipAutocompleteProvider::Show method</span></span>

<span data-ttu-id="378b7-104">Exibe ou oculta a lista de preenchimento automático.</span><span class="sxs-lookup"><span data-stu-id="378b7-104">Displays or hides the auto complete list.</span></span>

## <a name="syntax"></a><span data-ttu-id="378b7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="378b7-105">Syntax</span></span>


```C++
HRESULT Show(
  [in] BOOL fShow
);
```



## <a name="parameters"></a><span data-ttu-id="378b7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="378b7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="378b7-107">*fshow* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="378b7-107">*fShow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="378b7-108">**True** para mostrar a interface do usuário de preenchimento automático, **false** para ocultar a interface do usuário da lista de preenchimento automático.</span><span class="sxs-lookup"><span data-stu-id="378b7-108">**TRUE** to show the auto complete user interface, **FALSE** to hide the auto complete list user interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="378b7-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="378b7-109">Return value</span></span>

<span data-ttu-id="378b7-110">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="378b7-110">This method can return one of these values.</span></span>



| <span data-ttu-id="378b7-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="378b7-111">Return code</span></span>                                                                            | <span data-ttu-id="378b7-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="378b7-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="378b7-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="378b7-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="378b7-114">Êxito.</span><span class="sxs-lookup"><span data-stu-id="378b7-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="378b7-115"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="378b7-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="378b7-116">Ocorreu um erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="378b7-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="378b7-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="378b7-117">Remarks</span></span>

<span data-ttu-id="378b7-118">Esse método é chamado pelo cliente para mostrar ou ocultar a lista de preenchimento automático.</span><span class="sxs-lookup"><span data-stu-id="378b7-118">This method is called by the client to show or hide the auto complete list.</span></span> <span data-ttu-id="378b7-119">Se a lista de preenchimento automático não for exibida e *fshow* for **false**, esse método não fará nada.</span><span class="sxs-lookup"><span data-stu-id="378b7-119">If the auto complete list is not displayed and *fShow* is **FALSE**, this method does nothing.</span></span> <span data-ttu-id="378b7-120">Se a lista de preenchimento automático for exibida e *fshow* for **true**, esse método não fará nada.</span><span class="sxs-lookup"><span data-stu-id="378b7-120">If the auto complete list is displayed and *fShow* is **TRUE**, this method does nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="378b7-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="378b7-121">Requirements</span></span>



| <span data-ttu-id="378b7-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="378b7-122">Requirement</span></span> | <span data-ttu-id="378b7-123">Valor</span><span class="sxs-lookup"><span data-stu-id="378b7-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="378b7-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="378b7-124">Minimum supported client</span></span><br/> | <span data-ttu-id="378b7-125">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="378b7-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="378b7-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="378b7-126">Minimum supported server</span></span><br/> | <span data-ttu-id="378b7-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="378b7-127">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="378b7-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="378b7-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="378b7-129"><dt>TipAutoComplete. h (também requer PenInputPanel \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="378b7-129"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="378b7-130">DLL</span><span class="sxs-lookup"><span data-stu-id="378b7-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="378b7-131"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="378b7-131"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="378b7-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="378b7-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="378b7-133">**Interface ITipAutocompleteProvider**</span><span class="sxs-lookup"><span data-stu-id="378b7-133">**ITipAutocompleteProvider Interface**</span></span>](itipautocompleteprovider.md)
</dt> <dt>

[<span data-ttu-id="378b7-134">Referência do painel de entrada de texto</span><span class="sxs-lookup"><span data-stu-id="378b7-134">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> </dl>

 

 




