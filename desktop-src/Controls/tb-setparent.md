---
title: Mensagem de TB_SETPARENT (commctrl. h)
description: Define a janela à qual o controle Toolbar envia mensagens de notificação.
ms.assetid: 4863bd9f-021b-4295-9483-459fc19325d9
keywords:
- Controles de TB_SETPARENT de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_SETPARENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8137406c8e6854f86ed81d8d6b96293074ae67b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824719"
---
# <a name="tb_setparent-message"></a><span data-ttu-id="5d560-104">Mensagem de TB \_ SETpai</span><span class="sxs-lookup"><span data-stu-id="5d560-104">TB\_SETPARENT message</span></span>

<span data-ttu-id="5d560-105">Define a janela à qual o controle Toolbar envia mensagens de notificação.</span><span class="sxs-lookup"><span data-stu-id="5d560-105">Sets the window to which the toolbar control sends notification messages.</span></span>

## <a name="parameters"></a><span data-ttu-id="5d560-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5d560-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d560-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5d560-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5d560-108">Manipule a janela para receber mensagens de notificação.</span><span class="sxs-lookup"><span data-stu-id="5d560-108">Handle to the window to receive notification messages.</span></span>

</dd> <dt>

<span data-ttu-id="5d560-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5d560-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="5d560-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="5d560-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d560-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5d560-111">Return value</span></span>

<span data-ttu-id="5d560-112">O valor de retorno é um identificador para a janela de notificação anterior ou **nulo** se não houver nenhuma janela de notificação anterior.</span><span class="sxs-lookup"><span data-stu-id="5d560-112">The return value is a handle to the previous notification window, or **NULL** if there is no previous notification window.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d560-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="5d560-113">Remarks</span></span>

<span data-ttu-id="5d560-114">A mensagem de **TB \_ setpai** não altera a janela pai que foi especificada quando o controle foi criado.</span><span class="sxs-lookup"><span data-stu-id="5d560-114">The **TB\_SETPARENT** message does not change the parent window that was specified when the control was created.</span></span> <span data-ttu-id="5d560-115">Chamar a função [**GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent) para um controle Toolbar retornará a janela pai real, não a janela especificada em **TB \_ setpai**.</span><span class="sxs-lookup"><span data-stu-id="5d560-115">Calling the [**GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent) function for a toolbar control will return the actual parent window, not the window specified in **TB\_SETPARENT**.</span></span> <span data-ttu-id="5d560-116">Para alterar a janela pai do controle, chame a função [**setpai**](/windows/desktop/api/winuser/nf-winuser-setparent) .</span><span class="sxs-lookup"><span data-stu-id="5d560-116">To change the control's parent window, call the [**SetParent**](/windows/desktop/api/winuser/nf-winuser-setparent) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d560-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d560-117">Requirements</span></span>



| <span data-ttu-id="5d560-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d560-118">Requirement</span></span> | <span data-ttu-id="5d560-119">Valor</span><span class="sxs-lookup"><span data-stu-id="5d560-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5d560-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d560-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5d560-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5d560-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5d560-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d560-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5d560-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5d560-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5d560-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5d560-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d560-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d560-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

