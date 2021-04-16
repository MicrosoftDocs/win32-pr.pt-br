---
description: Gerencia o lado do aplicativo da integração de preenchimento automático do painel de entrada de texto.
ms.assetid: 02601258-d867-4c01-b094-bf9ff96d2f6e
title: Interface ITipAutocompleteProvider (TipAutoComplete. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteProvider
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 3c300e2724ccabbc8388ef647f8f0145531cfc8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105772511"
---
# <a name="itipautocompleteprovider-interface"></a><span data-ttu-id="68854-103">Interface ITipAutocompleteProvider</span><span class="sxs-lookup"><span data-stu-id="68854-103">ITipAutocompleteProvider interface</span></span>

<span data-ttu-id="68854-104">Gerencia o lado do aplicativo da integração de preenchimento automático do painel de entrada de texto.</span><span class="sxs-lookup"><span data-stu-id="68854-104">Manages the application's side of the Text Input Panel auto complete integration.</span></span>

## <a name="members"></a><span data-ttu-id="68854-105">Membros</span><span class="sxs-lookup"><span data-stu-id="68854-105">Members</span></span>

<span data-ttu-id="68854-106">A interface **ITipAutocompleteProvider** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="68854-106">The **ITipAutocompleteProvider** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="68854-107">**ITipAutocompleteProvider** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="68854-107">**ITipAutocompleteProvider** also has these types of members:</span></span>

-   [<span data-ttu-id="68854-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="68854-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="68854-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="68854-109">Methods</span></span>

<span data-ttu-id="68854-110">A interface **ITipAutocompleteProvider** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="68854-110">The **ITipAutocompleteProvider** interface has these methods.</span></span>



| <span data-ttu-id="68854-111">Método</span><span class="sxs-lookup"><span data-stu-id="68854-111">Method</span></span>                                                                  | <span data-ttu-id="68854-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="68854-112">Description</span></span>                                                                                                          |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="68854-113">**programa**</span><span class="sxs-lookup"><span data-stu-id="68854-113">**Show**</span></span>](itipautocompleteprovider-show.md)                           | <span data-ttu-id="68854-114">Exibe ou oculta a lista de preenchimento automático.</span><span class="sxs-lookup"><span data-stu-id="68854-114">Displays or hides the auto complete list.</span></span><br/>                                                                 |
| [<span data-ttu-id="68854-115">**UpdatePendingText**</span><span class="sxs-lookup"><span data-stu-id="68854-115">**UpdatePendingText**</span></span>](itipautocompleteprovider-updatependingtext.md) | <span data-ttu-id="68854-116">Usado pelo cliente de preenchimento automático para notificar o aplicativo sobre o texto que um usuário tem Inked no painel de entrada.</span><span class="sxs-lookup"><span data-stu-id="68854-116">Used by the auto complete client to notify the application of the text a user has inked into Input Panel.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="68854-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68854-117">Requirements</span></span>



| <span data-ttu-id="68854-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="68854-118">Requirement</span></span> | <span data-ttu-id="68854-119">Valor</span><span class="sxs-lookup"><span data-stu-id="68854-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68854-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="68854-120">Minimum supported client</span></span><br/> | <span data-ttu-id="68854-121">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="68854-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="68854-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="68854-122">Minimum supported server</span></span><br/> | <span data-ttu-id="68854-123">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="68854-123">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="68854-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="68854-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="68854-125"><dt>TipAutoComplete. h (também requer PenInputPanel \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="68854-125"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="68854-126">DLL</span><span class="sxs-lookup"><span data-stu-id="68854-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68854-127"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68854-127"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="68854-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="68854-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68854-129">Referência do painel de entrada de texto</span><span class="sxs-lookup"><span data-stu-id="68854-129">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> <dt>

[<span data-ttu-id="68854-130">**Interface ITipAutocompleteClient**</span><span class="sxs-lookup"><span data-stu-id="68854-130">**ITipAutocompleteClient Interface**</span></span>](itipautocompleteclient.md)
</dt> </dl>

 

