---
title: Mensagem de LVM_SETBKCOLOR (commctrl. h)
description: Define a cor da tela de fundo de um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro SetBkColor do ListView.
ms.assetid: d579249d-421d-4e7e-8992-4c7fd7277593
keywords:
- Controles de LVM_SETBKCOLOR de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80977ed6c95a1353889265e52cfc05c26aaa2a5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918701"
---
# <a name="lvm_setbkcolor-message"></a><span data-ttu-id="447f2-105">\_Mensagem SETBKCOLOR LVM</span><span class="sxs-lookup"><span data-stu-id="447f2-105">LVM\_SETBKCOLOR message</span></span>

<span data-ttu-id="447f2-106">Define a cor da tela de fundo de um controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="447f2-106">Sets the background color of a list-view control.</span></span> <span data-ttu-id="447f2-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ SetBkColor do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setbkcolor) .</span><span class="sxs-lookup"><span data-stu-id="447f2-107">You can send this message explicitly or by using the [**ListView\_SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setbkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="447f2-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="447f2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="447f2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="447f2-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="447f2-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="447f2-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="447f2-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="447f2-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="447f2-112">Cor do plano de fundo para definir ou o \_ valor de nenhum CLR para nenhuma cor de plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="447f2-112">Background color to set or the CLR\_NONE value for no background color.</span></span> <span data-ttu-id="447f2-113">Os controles de exibição de lista com cores de plano de fundo redesenham-se significativamente mais rápido do que aqueles sem cores de plano</span><span class="sxs-lookup"><span data-stu-id="447f2-113">List-view controls with background colors redraw themselves significantly faster than those without background colors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="447f2-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="447f2-114">Return value</span></span>

<span data-ttu-id="447f2-115">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="447f2-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="447f2-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="447f2-116">Requirements</span></span>



| <span data-ttu-id="447f2-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="447f2-117">Requirement</span></span> | <span data-ttu-id="447f2-118">Valor</span><span class="sxs-lookup"><span data-stu-id="447f2-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="447f2-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="447f2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="447f2-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="447f2-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="447f2-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="447f2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="447f2-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="447f2-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="447f2-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="447f2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="447f2-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="447f2-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





