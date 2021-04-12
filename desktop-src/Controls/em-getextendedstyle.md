---
title: Mensagem de EM_GETEXTENDEDSTYLE (commctrl. h)
description: Recupera o estilo estendido para um controle de edição. Envie essa mensagem explicitamente ou usando a macro ' Editar \_ Extended '.
ms.assetid: 557f796e-c9d1-4ea1-b8a6-44ae0bed5ffc
keywords:
- Controles de EM_GETEXTENDEDSTYLE de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 37dc117bccd57b51098a7ca8c19e8b178037bef8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455548"
---
# <a name="em_getextendedstyle-message-commctrlh"></a><span data-ttu-id="143d5-105">Mensagem de EM_GETEXTENDEDSTYLE (commctrl. h)</span><span class="sxs-lookup"><span data-stu-id="143d5-105">EM_GETEXTENDEDSTYLE message (Commctrl.h)</span></span>

<span data-ttu-id="143d5-106">Recupera o estilo estendido para um controle de exibição de árvore.</span><span class="sxs-lookup"><span data-stu-id="143d5-106">Retrieves the extended style for a tree-view control.</span></span> <span data-ttu-id="143d5-107">Envie essa mensagem explicitamente ou usando a macro ' [**Editar \_ Extended**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getextendedstyle) '.</span><span class="sxs-lookup"><span data-stu-id="143d5-107">Send this message explicitly or by using the [**Edit\_GetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getextendedstyle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="143d5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="143d5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="143d5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="143d5-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="143d5-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="143d5-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="143d5-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="143d5-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="143d5-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="143d5-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="143d5-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="143d5-113">Return value</span></span>

<span data-ttu-id="143d5-114">Retorna o valor do estilo estendido. Para obter mais informações sobre estilos, consulte [Editar estilos estendidos de controle](edit-control-window-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="143d5-114">Returns the value of extended style.For more information on styles, see [Edit Control Extended Styles](edit-control-window-extended-styles.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="143d5-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="143d5-115">Remarks</span></span>

<span data-ttu-id="143d5-116">Os estilos estendidos para um controle de edição não têm nada a ver com os estilos estendidos usados com a função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ou a função [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).</span><span class="sxs-lookup"><span data-stu-id="143d5-116">The extended styles for an edit control have nothing to do with the extended styles used with function [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) or function [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).</span></span>

## <a name="requirements"></a><span data-ttu-id="143d5-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="143d5-117">Requirements</span></span>



| <span data-ttu-id="143d5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="143d5-118">Requirement</span></span> | <span data-ttu-id="143d5-119">Valor</span><span class="sxs-lookup"><span data-stu-id="143d5-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="143d5-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="143d5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="143d5-121">\[Somente aplicativos da área de trabalho do Windows 10, versão 1809\]</span><span class="sxs-lookup"><span data-stu-id="143d5-121">Windows 10, version 1809 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="143d5-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="143d5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="143d5-123">\[Somente aplicativos da área de trabalho do Windows Server 2019\]</span><span class="sxs-lookup"><span data-stu-id="143d5-123">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="143d5-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="143d5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="143d5-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="143d5-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

