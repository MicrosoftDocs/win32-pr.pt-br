---
description: Cancela o registro do provedor associado.
ms.assetid: b5edc33d-dfd0-4350-b8cd-eaa30b726771
title: 'Método ITipAutocompleteClient:: unaconselheprovider (TipAutoComplete. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.UnadviseProvider
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 1100ebb700ef2fb769a13f9b62aacf5c1d007e0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828740"
---
# <a name="itipautocompleteclientunadviseprovider-method"></a><span data-ttu-id="1f273-103">Método ITipAutocompleteClient:: unaconselheprovider</span><span class="sxs-lookup"><span data-stu-id="1f273-103">ITipAutocompleteClient::UnadviseProvider method</span></span>

<span data-ttu-id="1f273-104">Cancela o registro do provedor associado.</span><span class="sxs-lookup"><span data-stu-id="1f273-104">Unregisters the associated provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f273-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1f273-105">Syntax</span></span>


```C++
HRESULT UnadviseProvider(
  [in] HWND                   hWndField,
  [in] ITipAutocompleProvider *pIACProvider
);
```



## <a name="parameters"></a><span data-ttu-id="1f273-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1f273-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f273-107">*hwndfield* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1f273-107">*hWndField* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f273-108">Identificador de janela do campo que fornece o recurso de preenchimento automático.</span><span class="sxs-lookup"><span data-stu-id="1f273-108">Window handle of the field which provide the auto complete feature.</span></span>

</dd> <dt>

<span data-ttu-id="1f273-109">*pIACProvider* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1f273-109">*pIACProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f273-110">Ponteiro de interface para o cancelamento do registro da interface do provedor de preenchimento automático.</span><span class="sxs-lookup"><span data-stu-id="1f273-110">Interface pointer to the auto complete provider interface to be unregistered.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f273-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1f273-111">Return value</span></span>

<span data-ttu-id="1f273-112">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="1f273-112">This method can return one of these values.</span></span>



| <span data-ttu-id="1f273-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="1f273-113">Return code</span></span>                                                                            | <span data-ttu-id="1f273-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="1f273-114">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="1f273-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1f273-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="1f273-116">Êxito.</span><span class="sxs-lookup"><span data-stu-id="1f273-116">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="1f273-117"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="1f273-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="1f273-118">Ocorreu um erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="1f273-118">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1f273-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f273-119">Requirements</span></span>



| <span data-ttu-id="1f273-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f273-120">Requirement</span></span> | <span data-ttu-id="1f273-121">Valor</span><span class="sxs-lookup"><span data-stu-id="1f273-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f273-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f273-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1f273-123">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="1f273-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="1f273-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f273-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1f273-125">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="1f273-125">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="1f273-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1f273-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f273-127"><dt>TipAutoComplete. h (também requer PenInputPanel \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="1f273-127"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="1f273-128">DLL</span><span class="sxs-lookup"><span data-stu-id="1f273-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f273-129"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f273-129"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="1f273-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="1f273-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f273-131">**Interface ITipAutocompleteClient**</span><span class="sxs-lookup"><span data-stu-id="1f273-131">**ITipAutocompleteClient Interface**</span></span>](itipautocompleteclient.md)
</dt> <dt>

[<span data-ttu-id="1f273-132">Referência do painel de entrada de texto</span><span class="sxs-lookup"><span data-stu-id="1f273-132">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> </dl>

 

 




