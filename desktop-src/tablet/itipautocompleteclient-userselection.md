---
description: Notifica o painel de entrada que o usuário selecionou algo na lista de preenchimento automático e para descartar todo o texto restante que ainda não foi inserido.
ms.assetid: 2e6fabe1-7984-4908-bf90-0603d0dad268
title: 'Método ITipAutocompleteClient:: userseleções (TipAutoComplete. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.UserSelection
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 1894db9da3b8e3a36e59eb45150b27facfe0291f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812070"
---
# <a name="itipautocompleteclientuserselection-method"></a><span data-ttu-id="3481d-103">Método ITipAutocompleteClient:: userseleções</span><span class="sxs-lookup"><span data-stu-id="3481d-103">ITipAutocompleteClient::UserSelection method</span></span>

<span data-ttu-id="3481d-104">Notifica o painel de entrada que o usuário selecionou algo na lista de preenchimento automático e para descartar todo o texto restante que ainda não foi inserido.</span><span class="sxs-lookup"><span data-stu-id="3481d-104">Notifies the Input Panel that the user has selected something in the auto complete list and to discard all remaining text that has not yet been inserted.</span></span>

## <a name="syntax"></a><span data-ttu-id="3481d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3481d-105">Syntax</span></span>


```C++
HRESULT UserSelection();
```



## <a name="parameters"></a><span data-ttu-id="3481d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3481d-106">Parameters</span></span>

<span data-ttu-id="3481d-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="3481d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3481d-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3481d-108">Return value</span></span>

<span data-ttu-id="3481d-109">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="3481d-109">This method can return one of these values.</span></span>



| <span data-ttu-id="3481d-110">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="3481d-110">Return code</span></span>                                                                            | <span data-ttu-id="3481d-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="3481d-111">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="3481d-112"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3481d-112"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="3481d-113">Êxito.</span><span class="sxs-lookup"><span data-stu-id="3481d-113">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="3481d-114"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="3481d-114"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="3481d-115">Ocorreu um erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="3481d-115">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3481d-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="3481d-116">Remarks</span></span>

<span data-ttu-id="3481d-117">Esse método é chamado do provedor para notificar o cliente de que uma seleção foi feita pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="3481d-117">This method is called from the provider to notify the client that a selection has been made by the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="3481d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3481d-118">Requirements</span></span>



| <span data-ttu-id="3481d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3481d-119">Requirement</span></span> | <span data-ttu-id="3481d-120">Valor</span><span class="sxs-lookup"><span data-stu-id="3481d-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3481d-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3481d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3481d-122">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="3481d-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="3481d-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3481d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3481d-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="3481d-124">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="3481d-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3481d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3481d-126"><dt>TipAutoComplete. h (também requer PenInputPanel \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="3481d-126"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="3481d-127">DLL</span><span class="sxs-lookup"><span data-stu-id="3481d-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3481d-128"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3481d-128"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="3481d-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="3481d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3481d-130">**Interface ITipAutocompleteClient**</span><span class="sxs-lookup"><span data-stu-id="3481d-130">**ITipAutocompleteClient Interface**</span></span>](itipautocompleteclient.md)
</dt> <dt>

[<span data-ttu-id="3481d-131">Referência do painel de entrada de texto</span><span class="sxs-lookup"><span data-stu-id="3481d-131">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> </dl>

 

 




