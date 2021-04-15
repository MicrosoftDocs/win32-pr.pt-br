---
title: Mensagem de LVM_SUBITEMHITTEST (commctrl. h)
description: Determina qual item de exibição de lista ou subitem está em uma determinada posição. Você pode enviar essa mensagem explicitamente ou usando a \_ macro SubItemHitTest do ListView.
ms.assetid: 1468febb-af0d-4c04-b0b1-cda5ec77aa2c
keywords:
- Controles de LVM_SUBITEMHITTEST de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_SUBITEMHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c811a3ed85b9eb157920f700b34d5d9c99597e67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454696"
---
# <a name="lvm_subitemhittest-message"></a><span data-ttu-id="725d7-105">\_Mensagem SUBITEMHITTEST LVM</span><span class="sxs-lookup"><span data-stu-id="725d7-105">LVM\_SUBITEMHITTEST message</span></span>

<span data-ttu-id="725d7-106">Determina qual item de exibição de lista ou subitem está em uma determinada posição.</span><span class="sxs-lookup"><span data-stu-id="725d7-106">Determines which list-view item or subitem is at a given position.</span></span> <span data-ttu-id="725d7-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ SubItemHitTest do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_subitemhittest) .</span><span class="sxs-lookup"><span data-stu-id="725d7-107">You can send this message explicitly or by using the [**ListView\_SubItemHitTest**](/windows/desktop/api/Commctrl/nf-commctrl-listview_subitemhittest) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="725d7-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="725d7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="725d7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="725d7-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="725d7-110">Deve ser 0.</span><span class="sxs-lookup"><span data-stu-id="725d7-110">Must be 0.</span></span> <span data-ttu-id="725d7-111">**Windows Vista.**</span><span class="sxs-lookup"><span data-stu-id="725d7-111">**Windows Vista.**</span></span> <span data-ttu-id="725d7-112">Deve ser-1 se o membro **iGroup** de *lParam* for recuperado.</span><span class="sxs-lookup"><span data-stu-id="725d7-112">Should be -1 if the **iGroup** member of *lParam* is to be retrieved.</span></span></dd> <dt>

<span data-ttu-id="725d7-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="725d7-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="725d7-114">Ponteiro para uma estrutura [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) .</span><span class="sxs-lookup"><span data-stu-id="725d7-114">Pointer to an [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) structure.</span></span> <span data-ttu-id="725d7-115">A estrutura de [**ponto**](/previous-versions//dd162805(v=vs.85)) em **LVHITTESTINFO** deve ser definida para as coordenadas do cliente para serem testadas com sucesso.</span><span class="sxs-lookup"><span data-stu-id="725d7-115">The [**POINT**](/previous-versions//dd162805(v=vs.85)) structure within **LVHITTESTINFO** should be set to the client coordinates to be hit-tested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="725d7-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="725d7-116">Return value</span></span>

<span data-ttu-id="725d7-117">Retorna o índice do item ou subitem testado, se houver, ou-1 caso contrário.</span><span class="sxs-lookup"><span data-stu-id="725d7-117">Returns the index of the item or subitem tested, if any, or -1 otherwise.</span></span> <span data-ttu-id="725d7-118">Se um item ou subitem estiver nas coordenadas determinadas, os campos da estrutura [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) serão preenchidos com as informações de acesso aplicáveis.</span><span class="sxs-lookup"><span data-stu-id="725d7-118">If an item or subitem is at the given coordinates, the fields of the [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) structure will be filled with the applicable hit information.</span></span>

## <a name="requirements"></a><span data-ttu-id="725d7-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="725d7-119">Requirements</span></span>



| <span data-ttu-id="725d7-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="725d7-120">Requirement</span></span> | <span data-ttu-id="725d7-121">Valor</span><span class="sxs-lookup"><span data-stu-id="725d7-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="725d7-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="725d7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="725d7-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="725d7-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="725d7-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="725d7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="725d7-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="725d7-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="725d7-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="725d7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="725d7-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="725d7-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

