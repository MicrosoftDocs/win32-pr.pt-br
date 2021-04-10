---
description: Determina se o painel de entrada está pronto para que a lista de preenchimento automático seja mostrada.
ms.assetid: 1e0d4bc6-e6a3-4123-a381-00a41ed9c848
title: 'Método ITipAutocompleteClient:: RequestShowUI (TipAutoComplete. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.RequestShowUI
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: e547376bf2e9c50c224d1917e00329e8d9555e6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169895"
---
# <a name="itipautocompleteclientrequestshowui-method"></a><span data-ttu-id="7f7c0-103">Método ITipAutocompleteClient:: RequestShowUI</span><span class="sxs-lookup"><span data-stu-id="7f7c0-103">ITipAutocompleteClient::RequestShowUI method</span></span>

<span data-ttu-id="7f7c0-104">Determina se o painel de entrada está pronto para que a lista de preenchimento automático seja mostrada.</span><span class="sxs-lookup"><span data-stu-id="7f7c0-104">Determines whether Input Panel is ready to have the auto complete list shown.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f7c0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7f7c0-105">Syntax</span></span>


```C++
HRESULT RequestShowUI(
  [in]  HWND hWndACList,
  [out] BOOL *pfAllowShowing
);
```



## <a name="parameters"></a><span data-ttu-id="7f7c0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7f7c0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f7c0-107">*hWndACList* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7f7c0-107">*hWndACList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f7c0-108">Identificador de janela da interface do usuário da lista de preenchimento automático.</span><span class="sxs-lookup"><span data-stu-id="7f7c0-108">Window handle of the auto complete list user interface.</span></span>

</dd> <dt>

<span data-ttu-id="7f7c0-109">*pfAllowShowing* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="7f7c0-109">*pfAllowShowing* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7f7c0-110">**False** se o cliente recomendar não mostrar a interface de usuário da lista de preenchimento automático.</span><span class="sxs-lookup"><span data-stu-id="7f7c0-110">**FALSE** if client recommends to not show the auto complete list user interface.</span></span> <span data-ttu-id="7f7c0-111">**True** se o provedor de preenchimento automático puder mostrar a interface do usuário da lista.</span><span class="sxs-lookup"><span data-stu-id="7f7c0-111">**TRUE** if the auto complete provider can show the list user interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f7c0-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7f7c0-112">Return value</span></span>

<span data-ttu-id="7f7c0-113">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="7f7c0-113">This method can return one of these values.</span></span>



| <span data-ttu-id="7f7c0-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="7f7c0-114">Return code</span></span>                                                                            | <span data-ttu-id="7f7c0-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="7f7c0-115">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="7f7c0-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7f7c0-116"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="7f7c0-117">Êxito.</span><span class="sxs-lookup"><span data-stu-id="7f7c0-117">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="7f7c0-118"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="7f7c0-118"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="7f7c0-119">Ocorreu um erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="7f7c0-119">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7f7c0-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="7f7c0-120">Remarks</span></span>

<span data-ttu-id="7f7c0-121">Esse método é chamado pelo provedor de preenchimento automático quando está prestes a mostrar a interface do usuário de preenchimento automático.</span><span class="sxs-lookup"><span data-stu-id="7f7c0-121">This method is called by the auto complete provider when it is about to show the auto complete user interface.</span></span> <span data-ttu-id="7f7c0-122">Se o estado interno do cliente não permitir que o provedor mostre a interface do usuário, *pfAllowShowing* será definido como **false**.</span><span class="sxs-lookup"><span data-stu-id="7f7c0-122">If the client's internal state doesn't allow the provider to show the user interface, *pfAllowShowing* will be set to **FALSE**.</span></span> <span data-ttu-id="7f7c0-123">Por exemplo, quando o texto é enviado para o campo da capa de manuscrito no painel de entrada do Tablet PC e o usuário inicia imediatamente a tinta, o cliente recomendará não mostrar a interface do usuário de preenchimento automático, para evitar a destruição da tinta do usuário, definindo *pfAllowShowing* como **false**.</span><span class="sxs-lookup"><span data-stu-id="7f7c0-123">For example, when the text gets sent to the field from the handwriting skin on the Tablet PC Input Panel and the user immediately starts inking, the client will recommend to not show the auto complete user interface, in order to avoid destructing the user's inking, by setting *pfAllowShowing* to **FALSE**.</span></span>

<span data-ttu-id="7f7c0-124">Chame **RequestShowUI** para definir o identificador de janela de lista de preenchimento automático de pop-up antes de chamar o [**método ITipAutocompleteClient::P referredrects**](itipautocompleteclient-preferredrects.md).</span><span class="sxs-lookup"><span data-stu-id="7f7c0-124">Call **RequestShowUI** to set the popup auto complete list window handle before you call the [**ITipAutocompleteClient::PreferredRects Method**](itipautocompleteclient-preferredrects.md).</span></span> <span data-ttu-id="7f7c0-125">A falha em fazer isso causará um erro **E \_ INVALIDARG** ao chamar **PreferredRects**.</span><span class="sxs-lookup"><span data-stu-id="7f7c0-125">Failure to do so will cause an **E\_INVALIDARG** error when calling **PreferredRects**.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f7c0-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f7c0-126">Requirements</span></span>



| <span data-ttu-id="7f7c0-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f7c0-127">Requirement</span></span> | <span data-ttu-id="7f7c0-128">Valor</span><span class="sxs-lookup"><span data-stu-id="7f7c0-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f7c0-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7f7c0-129">Minimum supported client</span></span><br/> | <span data-ttu-id="7f7c0-130">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="7f7c0-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="7f7c0-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7f7c0-131">Minimum supported server</span></span><br/> | <span data-ttu-id="7f7c0-132">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="7f7c0-132">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="7f7c0-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7f7c0-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f7c0-134"><dt>TipAutoComplete. h (também requer PenInputPanel \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="7f7c0-134"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="7f7c0-135">DLL</span><span class="sxs-lookup"><span data-stu-id="7f7c0-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f7c0-136"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f7c0-136"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="7f7c0-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="7f7c0-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f7c0-138">**Interface ITipAutocompleteClient**</span><span class="sxs-lookup"><span data-stu-id="7f7c0-138">**ITipAutocompleteClient Interface**</span></span>](itipautocompleteclient.md)
</dt> <dt>

[<span data-ttu-id="7f7c0-139">**ITipAutocompleteClient: método referredRects de:P**</span><span class="sxs-lookup"><span data-stu-id="7f7c0-139">**ITipAutocompleteClient::PreferredRects Method**</span></span>](itipautocompleteclient-preferredrects.md)
</dt> <dt>

[<span data-ttu-id="7f7c0-140">Referência do painel de entrada de texto</span><span class="sxs-lookup"><span data-stu-id="7f7c0-140">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> </dl>

 

 




