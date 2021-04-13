---
title: Mensagem de RB_SETTEXTCOLOR (commctrl. h)
description: Define a cor de texto padrão de um controle rebar.
ms.assetid: 85f120bd-39aa-43f8-a794-3bb4f3fe1cd4
keywords:
- Controles de RB_SETTEXTCOLOR de mensagens do Windows
topic_type:
- apiref
api_name:
- RB_SETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68311572927f2e8dac623c697ac366d37d7ab5fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455527"
---
# <a name="rb_settextcolor-message"></a><span data-ttu-id="1cb79-104">\_Mensagem SETTEXTCOLOR RB</span><span class="sxs-lookup"><span data-stu-id="1cb79-104">RB\_SETTEXTCOLOR message</span></span>

<span data-ttu-id="1cb79-105">Define a cor de texto padrão de um controle rebar.</span><span class="sxs-lookup"><span data-stu-id="1cb79-105">Sets a rebar control's default text color.</span></span>

## <a name="parameters"></a><span data-ttu-id="1cb79-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1cb79-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cb79-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1cb79-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="1cb79-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="1cb79-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="1cb79-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1cb79-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1cb79-110">Valor [**COLORREF**](/windows/desktop/gdi/colorref) que representa a nova cor de texto padrão.</span><span class="sxs-lookup"><span data-stu-id="1cb79-110">[**COLORREF**](/windows/desktop/gdi/colorref) value that represents the new default text color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cb79-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1cb79-111">Return value</span></span>

<span data-ttu-id="1cb79-112">Retorna um valor [**COLORREF**](/windows/desktop/gdi/colorref) que representa a cor de texto padrão anterior.</span><span class="sxs-lookup"><span data-stu-id="1cb79-112">Returns a [**COLORREF**](/windows/desktop/gdi/colorref) value that represents the previous default text color.</span></span>

## <a name="remarks"></a><span data-ttu-id="1cb79-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="1cb79-113">Remarks</span></span>

<span data-ttu-id="1cb79-114">A cor de texto padrão do controle rebar é usada para desenhar o texto em um controle rebar e todas as faixas que são adicionadas depois que essa mensagem é enviada.</span><span class="sxs-lookup"><span data-stu-id="1cb79-114">The rebar control's default text color is used to draw the text in a rebar control and all bands that are added after this message has been sent.</span></span> <span data-ttu-id="1cb79-115">A cor de texto padrão de uma determinada faixa pode ser substituída quando uma faixa é adicionada ou modificada definindo o \_ sinalizador cores RBBIM em **fMask** e definindo **clrBack** na estrutura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) .</span><span class="sxs-lookup"><span data-stu-id="1cb79-115">The default text color for a particular band can be overridden when a band is added or modified by setting the RBBIM\_COLORS flag in **fMask** and setting **clrBack** in the [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="1cb79-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1cb79-116">Requirements</span></span>



| <span data-ttu-id="1cb79-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cb79-117">Requirement</span></span> | <span data-ttu-id="1cb79-118">Valor</span><span class="sxs-lookup"><span data-stu-id="1cb79-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1cb79-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1cb79-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1cb79-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1cb79-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1cb79-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1cb79-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1cb79-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1cb79-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1cb79-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1cb79-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1cb79-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1cb79-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cb79-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="1cb79-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cb79-126">**\_GETTEXTCOLOR RB**</span><span class="sxs-lookup"><span data-stu-id="1cb79-126">**RB\_GETTEXTCOLOR**</span></span>](rb-gettextcolor.md)
</dt> </dl>

 

