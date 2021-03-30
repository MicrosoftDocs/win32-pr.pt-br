---
title: Mensagem de TB_GETCOLORSCHEME (commctrl. h)
description: Recupera as informações do esquema de cores do controle ToolBar.
ms.assetid: af172631-309e-4181-a690-05946cd6e143
keywords:
- Controles de TB_GETCOLORSCHEME de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_GETCOLORSCHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61344439ae8bc2b3a9ecd47472174577d652aa96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455276"
---
# <a name="tb_getcolorscheme-message"></a><span data-ttu-id="12ea8-104">TB de \_ mensagem GETCOLORSCHEME</span><span class="sxs-lookup"><span data-stu-id="12ea8-104">TB\_GETCOLORSCHEME message</span></span>

<span data-ttu-id="12ea8-105">Recupera as informações do esquema de cores do controle ToolBar.</span><span class="sxs-lookup"><span data-stu-id="12ea8-105">Retrieves the color scheme information from the toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="12ea8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="12ea8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12ea8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="12ea8-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="12ea8-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="12ea8-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="12ea8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="12ea8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="12ea8-110">Ponteiro para uma estrutura [**ColorScheme**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) que receberá as informações do esquema de cores.</span><span class="sxs-lookup"><span data-stu-id="12ea8-110">Pointer to a [**COLORSCHEME**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) structure that will receive the color scheme information.</span></span> <span data-ttu-id="12ea8-111">Você deve definir o membro **cbSize** dessa estrutura como **sizeof**(ColorScheme) antes de enviar esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="12ea8-111">You must set the **cbSize** member of this structure to **sizeof**(COLORSCHEME) before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12ea8-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="12ea8-112">Return value</span></span>

<span data-ttu-id="12ea8-113">Retornará zero se for bem-sucedido ou nenhum outro.</span><span class="sxs-lookup"><span data-stu-id="12ea8-113">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="12ea8-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12ea8-114">Requirements</span></span>



| <span data-ttu-id="12ea8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="12ea8-115">Requirement</span></span> | <span data-ttu-id="12ea8-116">Valor</span><span class="sxs-lookup"><span data-stu-id="12ea8-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="12ea8-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12ea8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="12ea8-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="12ea8-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="12ea8-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12ea8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="12ea8-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="12ea8-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="12ea8-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="12ea8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="12ea8-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="12ea8-122"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12ea8-123">Consulte também</span><span class="sxs-lookup"><span data-stu-id="12ea8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12ea8-124">**TB de \_ SETCOLORSCHEME**</span><span class="sxs-lookup"><span data-stu-id="12ea8-124">**TB\_SETCOLORSCHEME**</span></span>](tb-setcolorscheme.md)
</dt> </dl>

 

 





