---
title: Mensagem de LVM_ISITEMVISIBLE (commctrl. h)
description: Indica se um item no controle de exibição de lista está visível. Envie essa mensagem explicitamente ou usando a \_ macro IsItemVisible do ListView.
ms.assetid: 355be527-e2b9-46be-96a0-951d72216d92
keywords:
- Controles de LVM_ISITEMVISIBLE de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_ISITEMVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a95116d2d6da6e3554e63a8149c9b91d6c97f76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824662"
---
# <a name="lvm_isitemvisible-message"></a><span data-ttu-id="216bf-105">\_Mensagem ISITEMVISIBLE LVM</span><span class="sxs-lookup"><span data-stu-id="216bf-105">LVM\_ISITEMVISIBLE message</span></span>

<span data-ttu-id="216bf-106">Indica se um item no controle de exibição de lista está visível.</span><span class="sxs-lookup"><span data-stu-id="216bf-106">Indicates if an item in the list-view control is visible.</span></span> <span data-ttu-id="216bf-107">Envie essa mensagem explicitamente ou usando a macro [**\_ IsItemVisible do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_isitemvisible) .</span><span class="sxs-lookup"><span data-stu-id="216bf-107">Send this message explicitly or by using the [**ListView\_IsItemVisible**](/windows/desktop/api/Commctrl/nf-commctrl-listview_isitemvisible) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="216bf-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="216bf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="216bf-109">*wParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="216bf-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="216bf-110">Um índice do item no controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="216bf-110">An index of the item in the list-view control.</span></span>

</dd> <dt>

<span data-ttu-id="216bf-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="216bf-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="216bf-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="216bf-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="216bf-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="216bf-113">Return value</span></span>

<span data-ttu-id="216bf-114">Retorna **verdadeiro** se visível ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="216bf-114">Returns **TRUE** if visible, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="216bf-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="216bf-115">Requirements</span></span>



| <span data-ttu-id="216bf-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="216bf-116">Requirement</span></span> | <span data-ttu-id="216bf-117">Valor</span><span class="sxs-lookup"><span data-stu-id="216bf-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="216bf-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="216bf-118">Minimum supported client</span></span><br/> | <span data-ttu-id="216bf-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="216bf-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="216bf-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="216bf-120">Minimum supported server</span></span><br/> | <span data-ttu-id="216bf-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="216bf-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="216bf-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="216bf-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="216bf-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="216bf-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





