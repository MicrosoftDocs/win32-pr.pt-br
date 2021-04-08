---
title: DL_CANCELDRAG código de notificação (commctrl. h)
description: Sinaliza que o usuário cancelou uma operação de arrastar clicando com o botão direito do mouse ou pressionando a tecla ESC.
ms.assetid: 62c1377f-41b6-449f-a95e-2689dc1913c6
keywords:
- DL_CANCELDRAG de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- DL_CANCELDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab10f7c31184c44fabdffd4f611847e550b62cc7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086559"
---
# <a name="dl_canceldrag-notification-code"></a><span data-ttu-id="04198-104">Código de notificação do DL \_ CANCELDRAG</span><span class="sxs-lookup"><span data-stu-id="04198-104">DL\_CANCELDRAG notification code</span></span>

<span data-ttu-id="04198-105">Sinaliza que o usuário cancelou uma operação de arrastar clicando com o botão direito do mouse ou pressionando a tecla ESC.</span><span class="sxs-lookup"><span data-stu-id="04198-105">Signals that the user has canceled a drag operation by clicking the right mouse button or pressing the ESC key.</span></span> <span data-ttu-id="04198-106">Uma caixa de listagem de arrastar envia esse código de notificação para sua janela pai na forma de uma mensagem de arrastar lista.</span><span class="sxs-lookup"><span data-stu-id="04198-106">A drag list box sends this notification code to its parent window in the form of a drag list message.</span></span> <span data-ttu-id="04198-107">Para obter mais informações, consulte [arrastar mensagens da caixa de listagem](about-list-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="04198-107">For more information, see [Drag List Box Messages](about-list-boxes.md).</span></span>


```C++
DL_CANCELDRAG

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam;
```



## <a name="parameters"></a><span data-ttu-id="04198-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="04198-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04198-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="04198-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="04198-110">Um ponteiro para uma estrutura [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) que contém o \_ código de notificação DL CANCELDRAG, o identificador para a caixa de listagem de arrastar e a posição do cursor.</span><span class="sxs-lookup"><span data-stu-id="04198-110">A pointer to a [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) structure that contains the DL\_CANCELDRAG notification code, the handle to the drag list box, and the cursor position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04198-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="04198-111">Return value</span></span>

<span data-ttu-id="04198-112">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="04198-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="04198-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="04198-113">Remarks</span></span>

<span data-ttu-id="04198-114">Ao processar o \_ código de notificação DL CANCELDRAG, um aplicativo pode redefinir seu estado interno para indicar que arrastar não está em vigor.</span><span class="sxs-lookup"><span data-stu-id="04198-114">By processing the DL\_CANCELDRAG notification code, an application can reset its internal state to indicate that dragging is not in effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="04198-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04198-115">Requirements</span></span>



| <span data-ttu-id="04198-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="04198-116">Requirement</span></span> | <span data-ttu-id="04198-117">Valor</span><span class="sxs-lookup"><span data-stu-id="04198-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="04198-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="04198-118">Minimum supported client</span></span><br/> | <span data-ttu-id="04198-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="04198-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="04198-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="04198-120">Minimum supported server</span></span><br/> | <span data-ttu-id="04198-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="04198-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="04198-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="04198-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="04198-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="04198-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





