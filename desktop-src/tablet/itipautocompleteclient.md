---
description: Permite que o cliente chame o objeto de provedor de preenchimento automático do painel de entrada de texto do aplicativo.
ms.assetid: 448b8136-ebcb-4116-9a81-a77a37d69e24
title: Interface ITipAutocompleteClient (TipAutoComplete. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 7b9dad38d0e3f169019934b7e60a09096aced1b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105808313"
---
# <a name="itipautocompleteclient-interface"></a><span data-ttu-id="ec337-103">Interface ITipAutocompleteClient</span><span class="sxs-lookup"><span data-stu-id="ec337-103">ITipAutocompleteClient interface</span></span>

<span data-ttu-id="ec337-104">Permite que o cliente chame o objeto de provedor de preenchimento automático do painel de entrada de texto do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ec337-104">Enables the client to call the application's Text Input Panel auto complete provider object.</span></span>

## <a name="members"></a><span data-ttu-id="ec337-105">Membros</span><span class="sxs-lookup"><span data-stu-id="ec337-105">Members</span></span>

<span data-ttu-id="ec337-106">A interface **ITipAutocompleteClient** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="ec337-106">The **ITipAutocompleteClient** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ec337-107">**ITipAutocompleteClient** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ec337-107">**ITipAutocompleteClient** also has these types of members:</span></span>

-   [<span data-ttu-id="ec337-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="ec337-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ec337-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="ec337-109">Methods</span></span>

<span data-ttu-id="ec337-110">A interface **ITipAutocompleteClient** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="ec337-110">The **ITipAutocompleteClient** interface has these methods.</span></span>



| <span data-ttu-id="ec337-111">Método</span><span class="sxs-lookup"><span data-stu-id="ec337-111">Method</span></span>                                                              | <span data-ttu-id="ec337-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="ec337-112">Description</span></span>                                                                                                                                                          |
|:--------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ec337-113">**Aconselheprovider**</span><span class="sxs-lookup"><span data-stu-id="ec337-113">**AdviseProvider**</span></span>](itipautocompleteclient-adviseprovider.md)     | <span data-ttu-id="ec337-114">Registra o provedor com o cliente para permitir que o cliente chame o objeto de provedor de preenchimento automático do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ec337-114">Registers the provider with the client to enable the client to call the application's auto complete provider object.</span></span><br/>                                      |
| [<span data-ttu-id="ec337-115">**PreferredRects**</span><span class="sxs-lookup"><span data-stu-id="ec337-115">**PreferredRects**</span></span>](itipautocompleteclient-preferredrects.md)     | <span data-ttu-id="ec337-116">Permite que o cliente sugira onde posicionar a lista de preenchimento automático para evitar sobreposição do painel de entrada.</span><span class="sxs-lookup"><span data-stu-id="ec337-116">Allows the client to suggest where to position the auto complete list to avoid overlapping the Input Panel.</span></span><br/>                                               |
| [<span data-ttu-id="ec337-117">**RequestShowUI**</span><span class="sxs-lookup"><span data-stu-id="ec337-117">**RequestShowUI**</span></span>](itipautocompleteclient-requestshowui.md)       | <span data-ttu-id="ec337-118">Determina se o painel de entrada está pronto para que a lista de preenchimento automático seja mostrada.</span><span class="sxs-lookup"><span data-stu-id="ec337-118">Determines whether Input Panel is ready to have the auto complete list shown.</span></span><br/>                                                                             |
| [<span data-ttu-id="ec337-119">**Unaconselheprovider**</span><span class="sxs-lookup"><span data-stu-id="ec337-119">**UnadviseProvider**</span></span>](itipautocompleteclient-unadviseprovider.md) | <span data-ttu-id="ec337-120">Cancela o registro do provedor associado.</span><span class="sxs-lookup"><span data-stu-id="ec337-120">Unregisters the associated provider.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="ec337-121">**Userseleções**</span><span class="sxs-lookup"><span data-stu-id="ec337-121">**UserSelection**</span></span>](itipautocompleteclient-userselection.md)       | <span data-ttu-id="ec337-122">Notifica o painel de entrada que o usuário selecionou algo na lista de preenchimento automático e para descartar todo o texto restante que ainda não foi inserido.</span><span class="sxs-lookup"><span data-stu-id="ec337-122">Notifies the Input Panel that the user has selected something in the auto complete list and to discard all remaining text that has not yet been inserted.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ec337-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec337-123">Requirements</span></span>



| <span data-ttu-id="ec337-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec337-124">Requirement</span></span> | <span data-ttu-id="ec337-125">Valor</span><span class="sxs-lookup"><span data-stu-id="ec337-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec337-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ec337-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ec337-127">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="ec337-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="ec337-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ec337-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ec337-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="ec337-129">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="ec337-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ec337-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec337-131"><dt>TipAutoComplete. h (também requer PenInputPanel \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ec337-131"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ec337-132">DLL</span><span class="sxs-lookup"><span data-stu-id="ec337-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec337-133"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec337-133"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



 

