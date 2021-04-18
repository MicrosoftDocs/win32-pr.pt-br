---
description: Registra o provedor com o cliente para permitir que o cliente chame o objeto de provedor de preenchimento automático do aplicativo.
ms.assetid: 7b761b30-66f7-454a-9e0d-f45c8099f19f
title: 'Método ITipAutocompleteClient:: Aconselheprovider (TipAutoComplete. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.AdviseProvider
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 9ef35ac730089403ac47c14421de96e75a022192
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105814530"
---
# <a name="itipautocompleteclientadviseprovider-method"></a><span data-ttu-id="30089-103">Método ITipAutocompleteClient:: Aconselheprovider</span><span class="sxs-lookup"><span data-stu-id="30089-103">ITipAutocompleteClient::AdviseProvider method</span></span>

<span data-ttu-id="30089-104">Registra o provedor com o cliente para permitir que o cliente chame o objeto de provedor de preenchimento automático do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="30089-104">Registers the provider with the client to enable the client to call the application's auto complete provider object.</span></span>

## <a name="syntax"></a><span data-ttu-id="30089-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="30089-105">Syntax</span></span>


```C++
HRESULT AdviseProvider(
  [in] HWND                     hWndField,
  [in] ITipAutocompleteProvider *pIACProvider
);
```



## <a name="parameters"></a><span data-ttu-id="30089-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="30089-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30089-107">*hwndfield* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="30089-107">*hWndField* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30089-108">O identificador de janela do campo que fornece o recurso de preenchimento automático.</span><span class="sxs-lookup"><span data-stu-id="30089-108">The window handle of the field which provide the auto complete feature.</span></span>

</dd> <dt>

<span data-ttu-id="30089-109">*pIACProvider* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="30089-109">*pIACProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30089-110">O ponteiro de interface para a interface de provedor de preenchimento automático.</span><span class="sxs-lookup"><span data-stu-id="30089-110">The interface pointer to the auto complete provider interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30089-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="30089-111">Return value</span></span>

<span data-ttu-id="30089-112">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="30089-112">This method can return one of these values.</span></span>



| <span data-ttu-id="30089-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="30089-113">Return code</span></span>                                                                            | <span data-ttu-id="30089-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="30089-114">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="30089-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="30089-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="30089-116">Êxito.</span><span class="sxs-lookup"><span data-stu-id="30089-116">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="30089-117"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="30089-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="30089-118">Ocorreu um erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="30089-118">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="30089-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30089-119">Requirements</span></span>



| <span data-ttu-id="30089-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="30089-120">Requirement</span></span> | <span data-ttu-id="30089-121">Valor</span><span class="sxs-lookup"><span data-stu-id="30089-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30089-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="30089-122">Minimum supported client</span></span><br/> | <span data-ttu-id="30089-123">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="30089-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="30089-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="30089-124">Minimum supported server</span></span><br/> | <span data-ttu-id="30089-125">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="30089-125">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="30089-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="30089-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="30089-127"><dt>TipAutoComplete. h (também requer PenInputPanel \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="30089-127"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="30089-128">DLL</span><span class="sxs-lookup"><span data-stu-id="30089-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30089-129"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30089-129"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="30089-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="30089-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30089-131">**Interface ITipAutocompleteClient**</span><span class="sxs-lookup"><span data-stu-id="30089-131">**ITipAutocompleteClient Interface**</span></span>](itipautocompleteclient.md)
</dt> <dt>

[<span data-ttu-id="30089-132">**Método ITipAutocompleteClient:: unaconselheprovider**</span><span class="sxs-lookup"><span data-stu-id="30089-132">**ITipAutocompleteClient::UnadviseProvider Method**</span></span>](itipautocompleteclient-unadviseprovider.md)
</dt> <dt>

[<span data-ttu-id="30089-133">Referência do painel de entrada de texto</span><span class="sxs-lookup"><span data-stu-id="30089-133">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> </dl>

 

 




