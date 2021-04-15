---
title: Mensagem de LVM_DELETEALLITEMS (commctrl. h)
description: Remove todos os itens de um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro DeleteAllItems do ListView.
ms.assetid: 816bf565-79e9-4f5d-b5b4-5cdecce8a61c
keywords:
- Controles de LVM_DELETEALLITEMS de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_DELETEALLITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e92344e3cccf7578b8953206a9550022f6c6095
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454641"
---
# <a name="lvm_deleteallitems-message"></a><span data-ttu-id="9a97c-105">\_Mensagem DELETEALLITEMS LVM</span><span class="sxs-lookup"><span data-stu-id="9a97c-105">LVM\_DELETEALLITEMS message</span></span>

<span data-ttu-id="9a97c-106">Remove todos os itens de um controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="9a97c-106">Removes all items from a list-view control.</span></span> <span data-ttu-id="9a97c-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ DeleteAllItems do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deleteallitems) .</span><span class="sxs-lookup"><span data-stu-id="9a97c-107">You can send this message explicitly or by using the [**ListView\_DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deleteallitems) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9a97c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9a97c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a97c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9a97c-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9a97c-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="9a97c-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="9a97c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9a97c-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9a97c-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="9a97c-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a97c-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9a97c-113">Return value</span></span>

<span data-ttu-id="9a97c-114">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="9a97c-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a97c-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="9a97c-115">Remarks</span></span>

<span data-ttu-id="9a97c-116">Quando um controle de exibição de lista recebe a mensagem **\_ DELETEALLITEMS LVM** , ele envia o código de notificação [**LVN \_ DELETEALLITEMS**](lvn-deleteallitems.md) para sua janela pai.</span><span class="sxs-lookup"><span data-stu-id="9a97c-116">When a list-view control receives the **LVM\_DELETEALLITEMS** message, it sends the [**LVN\_DELETEALLITEMS**](lvn-deleteallitems.md) notification code to its parent window.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a97c-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a97c-117">Requirements</span></span>



| <span data-ttu-id="9a97c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a97c-118">Requirement</span></span> | <span data-ttu-id="9a97c-119">Valor</span><span class="sxs-lookup"><span data-stu-id="9a97c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9a97c-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9a97c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9a97c-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9a97c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9a97c-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9a97c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9a97c-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9a97c-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9a97c-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9a97c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a97c-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a97c-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





