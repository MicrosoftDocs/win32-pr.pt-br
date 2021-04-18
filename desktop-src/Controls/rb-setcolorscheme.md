---
title: Mensagem de RB_SETCOLORSCHEME (commctrl. h)
description: Define as informações do esquema de cores para o controle rebar.
ms.assetid: ddf8f3e4-66b7-4b53-a04e-b4dd372f71c4
keywords:
- Controles de RB_SETCOLORSCHEME de mensagens do Windows
topic_type:
- apiref
api_name:
- RB_SETCOLORSCHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9c7725d3c0bc3f3a7a7a72db16e19626a3c4d2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499436"
---
# <a name="rb_setcolorscheme-message"></a><span data-ttu-id="c4045-104">\_Mensagem SETCOLORSCHEME RB</span><span class="sxs-lookup"><span data-stu-id="c4045-104">RB\_SETCOLORSCHEME message</span></span>

<span data-ttu-id="c4045-105">Define as informações do esquema de cores para o controle rebar.</span><span class="sxs-lookup"><span data-stu-id="c4045-105">Sets the color scheme information for the rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="c4045-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c4045-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4045-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c4045-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c4045-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="c4045-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c4045-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c4045-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c4045-110">Ponteiro para uma estrutura [**ColorScheme**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) que contém as informações do esquema de cores.</span><span class="sxs-lookup"><span data-stu-id="c4045-110">Pointer to a [**COLORSCHEME**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) structure that contains the color scheme information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4045-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c4045-111">Return value</span></span>

<span data-ttu-id="c4045-112">O valor retornado para esta mensagem não é usado.</span><span class="sxs-lookup"><span data-stu-id="c4045-112">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4045-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="c4045-113">Remarks</span></span>

<span data-ttu-id="c4045-114">O controle rebar usa as informações do esquema de cores ao desenhar os elementos 3-D no controle e nas faixas.</span><span class="sxs-lookup"><span data-stu-id="c4045-114">The rebar control uses the color scheme information when drawing the 3-D elements in the control and bands.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4045-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4045-115">Requirements</span></span>



| <span data-ttu-id="c4045-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4045-116">Requirement</span></span> | <span data-ttu-id="c4045-117">Valor</span><span class="sxs-lookup"><span data-stu-id="c4045-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c4045-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c4045-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c4045-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c4045-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c4045-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c4045-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c4045-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c4045-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c4045-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c4045-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4045-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4045-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4045-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="c4045-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4045-125">**\_GETCOLORSCHEME RB**</span><span class="sxs-lookup"><span data-stu-id="c4045-125">**RB\_GETCOLORSCHEME**</span></span>](rb-getcolorscheme.md)
</dt> </dl>

 

 





