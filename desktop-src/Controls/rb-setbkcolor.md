---
title: Mensagem de RB_SETBKCOLOR (commctrl. h)
description: Define a cor do plano de fundo padrão de um controle rebar.
ms.assetid: 450a1e16-24f6-4f86-8e46-14009da05efc
keywords:
- Controles de RB_SETBKCOLOR de mensagens do Windows
topic_type:
- apiref
api_name:
- RB_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa9365de2d790b1f28b1330c038b69d30b208143
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105749073"
---
# <a name="rb_setbkcolor-message"></a><span data-ttu-id="09f9c-104">\_Mensagem SETBKCOLOR RB</span><span class="sxs-lookup"><span data-stu-id="09f9c-104">RB\_SETBKCOLOR message</span></span>

<span data-ttu-id="09f9c-105">Define a cor do plano de fundo padrão de um controle rebar.</span><span class="sxs-lookup"><span data-stu-id="09f9c-105">Sets a rebar control's default background color.</span></span>

## <a name="parameters"></a><span data-ttu-id="09f9c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="09f9c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09f9c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="09f9c-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="09f9c-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="09f9c-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="09f9c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="09f9c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="09f9c-110">Valor [**COLORREF**](/windows/desktop/gdi/colorref) que representa a nova cor de plano de fundo padrão.</span><span class="sxs-lookup"><span data-stu-id="09f9c-110">[**COLORREF**](/windows/desktop/gdi/colorref) value that represents the new default background color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09f9c-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="09f9c-111">Return value</span></span>

<span data-ttu-id="09f9c-112">Retorna um valor [**COLORREF**](/windows/desktop/gdi/colorref) que representa a cor de plano de fundo padrão anterior.</span><span class="sxs-lookup"><span data-stu-id="09f9c-112">Returns a [**COLORREF**](/windows/desktop/gdi/colorref) value that represents the previous default background color.</span></span>

## <a name="remarks"></a><span data-ttu-id="09f9c-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="09f9c-113">Remarks</span></span>

<span data-ttu-id="09f9c-114">A cor do plano de fundo padrão do controle rebar é usada para desenhar o plano de fundo em um controle rebar e todas as faixas que são adicionadas depois que essa mensagem é enviada.</span><span class="sxs-lookup"><span data-stu-id="09f9c-114">The rebar control's default background color is used to draw the background in a rebar control and all bands that are added after this message has been sent.</span></span> <span data-ttu-id="09f9c-115">A cor de plano de fundo padrão para uma banda específica pode ser substituída quando uma banda é adicionada ou modificada definindo o \_ sinalizador de cores RBBIM em **fMask** e definindo **clrBack** na estrutura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) .</span><span class="sxs-lookup"><span data-stu-id="09f9c-115">The default background color for a particular band can be overridden when a band is added or modified by setting the RBBIM\_COLORS flag in **fMask** and setting **clrBack** in the [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) structure.</span></span>

<span data-ttu-id="09f9c-116">Quando os estilos visuais são habilitados, essa mensagem não tem nenhum efeito.</span><span class="sxs-lookup"><span data-stu-id="09f9c-116">When visual styles are enabled, this message has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="09f9c-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09f9c-117">Requirements</span></span>



| <span data-ttu-id="09f9c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="09f9c-118">Requirement</span></span> | <span data-ttu-id="09f9c-119">Valor</span><span class="sxs-lookup"><span data-stu-id="09f9c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="09f9c-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="09f9c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="09f9c-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="09f9c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="09f9c-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="09f9c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="09f9c-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="09f9c-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="09f9c-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="09f9c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="09f9c-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="09f9c-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09f9c-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="09f9c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09f9c-127">**\_GETBKCOLOR RB**</span><span class="sxs-lookup"><span data-stu-id="09f9c-127">**RB\_GETBKCOLOR**</span></span>](rb-getbkcolor.md)
</dt> </dl>

 

