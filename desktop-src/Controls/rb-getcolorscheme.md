---
title: Mensagem de RB_GETCOLORSCHEME (commctrl. h)
description: Recupera as informações do esquema de cores do controle rebar.
ms.assetid: 01f81c4b-bbc9-43ae-a1f5-1e289c6fa278
keywords:
- Controles de RB_GETCOLORSCHEME de mensagens do Windows
topic_type:
- apiref
api_name:
- RB_GETCOLORSCHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a3d154fd14b93127aa22148f2882f70018225cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499541"
---
# <a name="rb_getcolorscheme-message"></a><span data-ttu-id="219c6-104">\_Mensagem GETCOLORSCHEME RB</span><span class="sxs-lookup"><span data-stu-id="219c6-104">RB\_GETCOLORSCHEME message</span></span>

<span data-ttu-id="219c6-105">Recupera as informações do esquema de cores do controle rebar.</span><span class="sxs-lookup"><span data-stu-id="219c6-105">Retrieves the color scheme information from the rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="219c6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="219c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="219c6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="219c6-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="219c6-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="219c6-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="219c6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="219c6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="219c6-110">Ponteiro para uma estrutura [**ColorScheme**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) que receberá as informações do esquema de cores.</span><span class="sxs-lookup"><span data-stu-id="219c6-110">Pointer to a [**COLORSCHEME**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) structure that will receive the color scheme information.</span></span> <span data-ttu-id="219c6-111">Você deve definir o membro **dwSize** dessa estrutura como **sizeof**(ColorScheme) antes de enviar esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="219c6-111">You must set the **dwSize** member of this structure to **sizeof**(COLORSCHEME) before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="219c6-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="219c6-112">Return value</span></span>

<span data-ttu-id="219c6-113">Retornará zero se for bem-sucedido ou nenhum outro.</span><span class="sxs-lookup"><span data-stu-id="219c6-113">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="219c6-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="219c6-114">Requirements</span></span>



| <span data-ttu-id="219c6-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="219c6-115">Requirement</span></span> | <span data-ttu-id="219c6-116">Valor</span><span class="sxs-lookup"><span data-stu-id="219c6-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="219c6-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="219c6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="219c6-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="219c6-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="219c6-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="219c6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="219c6-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="219c6-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="219c6-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="219c6-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="219c6-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="219c6-122"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="219c6-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="219c6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="219c6-124">**\_SETCOLORSCHEME RB**</span><span class="sxs-lookup"><span data-stu-id="219c6-124">**RB\_SETCOLORSCHEME**</span></span>](rb-setcolorscheme.md)
</dt> </dl>

 

 





