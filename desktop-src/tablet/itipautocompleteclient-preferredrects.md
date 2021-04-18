---
description: Permite que o cliente sugira onde posicionar a lista de preenchimento automático para evitar sobreposição do painel de entrada.
ms.assetid: c82ffecb-f3e6-4c50-80bb-8393b39d3b2a
title: 'ITipAutocompleteClient: método referredRects de:P (TipAutoComplete. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.PreferredRects
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 04e935c668e858ae3d22936e8a63f9116ebd6ab2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105802085"
---
# <a name="itipautocompleteclientpreferredrects-method"></a><span data-ttu-id="1ed02-103">ITipAutocompleteClient: método referredRects de:P</span><span class="sxs-lookup"><span data-stu-id="1ed02-103">ITipAutocompleteClient::PreferredRects method</span></span>

<span data-ttu-id="1ed02-104">Permite que o cliente sugira onde posicionar a lista de preenchimento automático para evitar sobreposição do painel de entrada.</span><span class="sxs-lookup"><span data-stu-id="1ed02-104">Allows the client to suggest where to position the auto complete list to avoid overlapping the Input Panel.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ed02-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1ed02-105">Syntax</span></span>


```C++
HRESULT PreferredRects(
  [in]      RECT *prcACList,
  [in]      RECT *prcField,
  [out]     RECT *prcModified,
  [in, out] BOOL *pfShownAboveTip
);
```



## <a name="parameters"></a><span data-ttu-id="1ed02-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1ed02-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ed02-107">*prcACList* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1ed02-107">*prcACList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ed02-108">Um retângulo, em coordenadas da tela, indicando o local preferido do provedor e o tamanho da interface de usuário da lista de preenchimento automático.</span><span class="sxs-lookup"><span data-stu-id="1ed02-108">A rectangle, in screen coordinates, indicating the provider's preferred location and the size of the auto complete list user interface.</span></span>

</dd> <dt>

<span data-ttu-id="1ed02-109">*prcField* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1ed02-109">*prcField* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ed02-110">Um retângulo, em coordenadas da tela, indicando o local e o tamanho do campo focado.</span><span class="sxs-lookup"><span data-stu-id="1ed02-110">A rectangle, in screen coordinates, indicating the location and the size of the focused field.</span></span>

</dd> <dt>

<span data-ttu-id="1ed02-111">*prcModified* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1ed02-111">*prcModified* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1ed02-112">Um retângulo com base no estado atual da TIP e o local e o tamanho da lista de preenchimento automático preferenciais especificados por *prcACList*.</span><span class="sxs-lookup"><span data-stu-id="1ed02-112">A rectangle based on the current state of the TIP and the preferred auto complete list location and size specified by *prcACList*.</span></span>

</dd> <dt>

<span data-ttu-id="1ed02-113">*pfShownAboveTip* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="1ed02-113">*pfShownAboveTip* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1ed02-114">**True** se o retângulo modificado for mostrado acima da área de destino do painel de entrada de texto; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="1ed02-114">**TRUE** if the modified rectangle is to be shown above the Text Input Panel's target area; otherwise, **FALSE**.</span></span> <span data-ttu-id="1ed02-115">Esse valor deve ser inicializado para a orientação preferida do provedor antes de o método ser chamado.</span><span class="sxs-lookup"><span data-stu-id="1ed02-115">This value must be initialized to the provider's preferred orientation before the method is called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ed02-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1ed02-116">Return value</span></span>

<span data-ttu-id="1ed02-117">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="1ed02-117">This method can return one of these values.</span></span>



| <span data-ttu-id="1ed02-118">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="1ed02-118">Return code</span></span>                                                                                  | <span data-ttu-id="1ed02-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="1ed02-119">Description</span></span>                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1ed02-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1ed02-120"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="1ed02-121">Êxito.</span><span class="sxs-lookup"><span data-stu-id="1ed02-121">Success.</span></span><br/>                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="1ed02-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="1ed02-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="1ed02-123">Chame o [**método ITipAutocompleteClient:: RequestShowUI**](itipautocompleteclient-requestshowui.md) para definir a janela de lista de preenchimento automático de pop-up antes de chamar o [**método ITipAutocompleteClient::P referredrects**](itipautocompleteclient-preferredrects.md).</span><span class="sxs-lookup"><span data-stu-id="1ed02-123">Call the [**ITipAutocompleteClient::RequestShowUI Method**](itipautocompleteclient-requestshowui.md) to set the popup auto complete list window before calling the [**ITipAutocompleteClient::PreferredRects Method**](itipautocompleteclient-preferredrects.md).</span></span><br/> |
| <dl> <span data-ttu-id="1ed02-124"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="1ed02-124"><dt>**E\_FAIL**</dt></span></span> </dl>       | <span data-ttu-id="1ed02-125">Ocorreu um erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="1ed02-125">An unspecified error occurred.</span></span><br/>                                                                                                                                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="1ed02-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="1ed02-126">Remarks</span></span>

<span data-ttu-id="1ed02-127">Esse é o método que o provedor de preenchimento automático chama quando está prestes a mostrar a interface do usuário de preenchimento automático.</span><span class="sxs-lookup"><span data-stu-id="1ed02-127">This is the method that the auto complete provider calls when it is about to show the auto complete user interface.</span></span> <span data-ttu-id="1ed02-128">O cliente modifica o retângulo preferencial do provedor especificado por *prcACList* por meio do argumento *prcModified* .</span><span class="sxs-lookup"><span data-stu-id="1ed02-128">The client modifies the provider's preferred rectangle specified by *prcACList* through *prcModified* argument.</span></span>

<span data-ttu-id="1ed02-129">Chame o [**método ITipAutocompleteClient:: RequestShowUI**](itipautocompleteclient-requestshowui.md) para definir o identificador de janela de lista de preenchimento automático de pop-up antes de chamar **PreferredRects**.</span><span class="sxs-lookup"><span data-stu-id="1ed02-129">Call the [**ITipAutocompleteClient::RequestShowUI Method**](itipautocompleteclient-requestshowui.md) to set the popup auto complete list window handle before you call **PreferredRects**.</span></span> <span data-ttu-id="1ed02-130">A falha em fazer isso causará um erro **E \_ INVALIDARG** ao chamar **PreferredRects**.</span><span class="sxs-lookup"><span data-stu-id="1ed02-130">Failure to do so will cause an **E\_INVALIDARG** error when calling **PreferredRects**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ed02-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ed02-131">Requirements</span></span>



| <span data-ttu-id="1ed02-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ed02-132">Requirement</span></span> | <span data-ttu-id="1ed02-133">Valor</span><span class="sxs-lookup"><span data-stu-id="1ed02-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ed02-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ed02-134">Minimum supported client</span></span><br/> | <span data-ttu-id="1ed02-135">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="1ed02-135">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="1ed02-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ed02-136">Minimum supported server</span></span><br/> | <span data-ttu-id="1ed02-137">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="1ed02-137">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="1ed02-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1ed02-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ed02-139"><dt>TipAutoComplete. h (também requer PenInputPanel \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="1ed02-139"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="1ed02-140">DLL</span><span class="sxs-lookup"><span data-stu-id="1ed02-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ed02-141"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ed02-141"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="1ed02-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="1ed02-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ed02-143">**Interface ITipAutocompleteClient**</span><span class="sxs-lookup"><span data-stu-id="1ed02-143">**ITipAutocompleteClient Interface**</span></span>](itipautocompleteclient.md)
</dt> <dt>

[<span data-ttu-id="1ed02-144">**Método ITipAutocompleteClient:: RequestShowUI**</span><span class="sxs-lookup"><span data-stu-id="1ed02-144">**ITipAutocompleteClient::RequestShowUI Method**</span></span>](itipautocompleteclient-requestshowui.md)
</dt> <dt>

[<span data-ttu-id="1ed02-145">Referência do painel de entrada de texto</span><span class="sxs-lookup"><span data-stu-id="1ed02-145">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> </dl>

 

 




