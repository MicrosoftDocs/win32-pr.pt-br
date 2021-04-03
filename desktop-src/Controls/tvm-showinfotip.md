---
title: Mensagem de TVM_SHOWINFOTIP (commctrl. h)
description: Mostra o InfoTip de um item especificado em um controle de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ ShowInfoTip.
ms.assetid: ed5a1bda-5754-4bb3-aa22-8faaf1af1268
keywords:
- Controles de TVM_SHOWINFOTIP de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_SHOWINFOTIP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76f147253800469a800677a242ff0ab0ccdbdfa4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824803"
---
# <a name="tvm_showinfotip-message"></a><span data-ttu-id="bf07c-105">\_Mensagem TVM SHOWINFOTIP</span><span class="sxs-lookup"><span data-stu-id="bf07c-105">TVM\_SHOWINFOTIP message</span></span>

<span data-ttu-id="bf07c-106">Mostra o InfoTip de um item especificado em um controle de exibição de árvore.</span><span class="sxs-lookup"><span data-stu-id="bf07c-106">Shows the infotip for a specified item in a tree-view control.</span></span> <span data-ttu-id="bf07c-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ ShowInfoTip**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_showinfotip) .</span><span class="sxs-lookup"><span data-stu-id="bf07c-107">You can send this message explicitly or by using the [**TreeView\_ShowInfoTip**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_showinfotip) macro..</span></span>

## <a name="parameters"></a><span data-ttu-id="bf07c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bf07c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf07c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bf07c-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="bf07c-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="bf07c-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="bf07c-111">*lParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bf07c-111">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf07c-112">Identificador para o item.</span><span class="sxs-lookup"><span data-stu-id="bf07c-112">Handle to the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf07c-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bf07c-113">Return value</span></span>

<span data-ttu-id="bf07c-114">Retorna zero.</span><span class="sxs-lookup"><span data-stu-id="bf07c-114">Returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf07c-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="bf07c-115">Remarks</span></span>

<span data-ttu-id="bf07c-116">A maioria dos aplicativos não usa essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="bf07c-116">Most applications do not use this message.</span></span> <span data-ttu-id="bf07c-117">Infotips são mostrados automaticamente.</span><span class="sxs-lookup"><span data-stu-id="bf07c-117">Infotips are shown automatically.</span></span> <span data-ttu-id="bf07c-118">Para obter mais informações, consulte usando Tree-View Infotips na visão geral [sobre controles About Tree-View](tree-view-controls.md) .</span><span class="sxs-lookup"><span data-stu-id="bf07c-118">For more information, see Using Tree-view Infotips in the [About Tree-View Controls](tree-view-controls.md) overview.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf07c-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf07c-119">Requirements</span></span>



| <span data-ttu-id="bf07c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf07c-120">Requirement</span></span> | <span data-ttu-id="bf07c-121">Valor</span><span class="sxs-lookup"><span data-stu-id="bf07c-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bf07c-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bf07c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bf07c-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bf07c-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bf07c-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bf07c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bf07c-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bf07c-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bf07c-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bf07c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf07c-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf07c-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





