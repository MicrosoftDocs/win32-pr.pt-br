---
title: Mensagem de PGM_RECALCSIZE (commctrl. h)
description: Força o controle de pager a recalcular o tamanho da janela contida. O envio dessa mensagem resultará na envio de uma \_ notificação PGN CALCSIZE. Você pode enviar essa mensagem explicitamente ou usar a \_ macro RecalcSize do pager.
ms.assetid: 51b75ce8-2b41-4f1a-830e-b25e7d77dccb
keywords:
- Controles de PGM_RECALCSIZE de mensagens do Windows
topic_type:
- apiref
api_name:
- PGM_RECALCSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b407221543a42b4dbff4490508a02b570622d69c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455011"
---
# <a name="pgm_recalcsize-message"></a><span data-ttu-id="726e6-106">\_Mensagem RECALCSIZE do PGM</span><span class="sxs-lookup"><span data-stu-id="726e6-106">PGM\_RECALCSIZE message</span></span>

<span data-ttu-id="726e6-107">Força o controle de pager a recalcular o tamanho da janela contida.</span><span class="sxs-lookup"><span data-stu-id="726e6-107">Forces the pager control to recalculate the size of the contained window.</span></span> <span data-ttu-id="726e6-108">O envio dessa mensagem resultará na envio de uma notificação [PGN \_ CALCSIZE](pgn-calcsize.md) .</span><span class="sxs-lookup"><span data-stu-id="726e6-108">Sending this message will result in a [PGN\_CALCSIZE](pgn-calcsize.md) notification being sent.</span></span> <span data-ttu-id="726e6-109">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ RecalcSize do pager**](/windows/desktop/api/Commctrl/nf-commctrl-pager_recalcsize) .</span><span class="sxs-lookup"><span data-stu-id="726e6-109">You can send this message explicitly or use the [**Pager\_RecalcSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_recalcsize) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="726e6-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="726e6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="726e6-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="726e6-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="726e6-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="726e6-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="726e6-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="726e6-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="726e6-114">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="726e6-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="726e6-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="726e6-115">Return value</span></span>

<span data-ttu-id="726e6-116">O valor de retorno não é usado.</span><span class="sxs-lookup"><span data-stu-id="726e6-116">The return value is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="726e6-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="726e6-117">Requirements</span></span>



| <span data-ttu-id="726e6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="726e6-118">Requirement</span></span> | <span data-ttu-id="726e6-119">Valor</span><span class="sxs-lookup"><span data-stu-id="726e6-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="726e6-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="726e6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="726e6-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="726e6-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="726e6-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="726e6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="726e6-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="726e6-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="726e6-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="726e6-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="726e6-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="726e6-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





