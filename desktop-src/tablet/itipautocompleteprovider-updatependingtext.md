---
description: Usado pelo cliente de preenchimento automático para notificar o aplicativo sobre o texto que um usuário tem Inked no painel de entrada.
ms.assetid: 68413836-321a-4e75-8538-c5a8fc577c0f
title: 'Método ITipAutocompleteProvider:: UpdatePendingText (TipAutoComplete. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteProvider.UpdatePendingText
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 5c66e625639aa7088b1b3934a2f984d0f4097536
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011820"
---
# <a name="itipautocompleteproviderupdatependingtext-method"></a><span data-ttu-id="3c954-103">Método ITipAutocompleteProvider:: UpdatePendingText</span><span class="sxs-lookup"><span data-stu-id="3c954-103">ITipAutocompleteProvider::UpdatePendingText method</span></span>

<span data-ttu-id="3c954-104">Usado pelo cliente de preenchimento automático para notificar o aplicativo sobre o texto que um usuário tem Inked no painel de entrada.</span><span class="sxs-lookup"><span data-stu-id="3c954-104">Used by the auto complete client to notify the application of the text a user has inked into Input Panel.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c954-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3c954-105">Syntax</span></span>


```C++
HRESULT UpdatePendingText(
  [in] BSTR bstrPendingText
);
```



## <a name="parameters"></a><span data-ttu-id="3c954-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3c954-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c954-107">*bstrPendingText* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3c954-107">*bstrPendingText* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c954-108">O texto de origem a ser usado para gerar a lista de preenchimento automático.</span><span class="sxs-lookup"><span data-stu-id="3c954-108">Source text to be used to generate the auto complete list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c954-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3c954-109">Return value</span></span>

<span data-ttu-id="3c954-110">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="3c954-110">This method can return one of these values.</span></span>



| <span data-ttu-id="3c954-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="3c954-111">Return code</span></span>                                                                            | <span data-ttu-id="3c954-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="3c954-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="3c954-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3c954-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="3c954-114">Êxito.</span><span class="sxs-lookup"><span data-stu-id="3c954-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="3c954-115"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="3c954-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="3c954-116">Ocorreu um erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="3c954-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3c954-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="3c954-117">Remarks</span></span>

<span data-ttu-id="3c954-118">Esse texto não conterá o texto já inserido no campo focalizado.</span><span class="sxs-lookup"><span data-stu-id="3c954-118">This text will not contain the text already inserted in the focused field.</span></span> <span data-ttu-id="3c954-119">O provedor de preenchimento automático é responsável por levar em conta o texto do campo atual e a seleção para gerar a lista de preenchimento automático.</span><span class="sxs-lookup"><span data-stu-id="3c954-119">The auto complete provider is responsible for taking into account the current field text and the selection to generate the auto complete list.</span></span> <span data-ttu-id="3c954-120">Quando *bstrPendingText* é **nulo**, a lista de preenchimento automático é gerada com o texto atual à esquerda da seleção no campo.</span><span class="sxs-lookup"><span data-stu-id="3c954-120">When *bstrPendingText* is **NULL**, the auto complete list is generated with the current text to the left of the selection in the field.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c954-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c954-121">Requirements</span></span>



| <span data-ttu-id="3c954-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c954-122">Requirement</span></span> | <span data-ttu-id="3c954-123">Valor</span><span class="sxs-lookup"><span data-stu-id="3c954-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c954-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3c954-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3c954-125">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="3c954-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="3c954-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3c954-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3c954-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="3c954-127">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="3c954-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3c954-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c954-129"><dt>TipAutoComplete. h (também requer PenInputPanel \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="3c954-129"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="3c954-130">DLL</span><span class="sxs-lookup"><span data-stu-id="3c954-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c954-131"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c954-131"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="3c954-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="3c954-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c954-133">**Interface ITipAutocompleteProvider**</span><span class="sxs-lookup"><span data-stu-id="3c954-133">**ITipAutocompleteProvider Interface**</span></span>](itipautocompleteprovider.md)
</dt> <dt>

[<span data-ttu-id="3c954-134">Referência do painel de entrada de texto</span><span class="sxs-lookup"><span data-stu-id="3c954-134">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> </dl>

 

 




