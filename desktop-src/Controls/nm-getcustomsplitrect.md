---
title: NM_GETCUSTOMSPLITRECT código de notificação (commctrl. h)
description: Enviado por um controle de botão para seu pai para obter medidas para os dois retângulos do botão de divisão. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: ce72778d-3cca-46a4-9d05-40954a18681d
keywords:
- NM_GETCUSTOMSPLITRECT de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- NM_GETCUSTOMSPLITRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97b839540da7e07069fdf56ed656ed8772d029eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085163"
---
# <a name="nm_getcustomsplitrect-notification-code"></a><span data-ttu-id="baad2-105">\_Código de notificação nm GETCUSTOMSPLITRECT</span><span class="sxs-lookup"><span data-stu-id="baad2-105">NM\_GETCUSTOMSPLITRECT notification code</span></span>

<span data-ttu-id="baad2-106">Enviado por um controle de botão para seu pai para obter medidas para os dois retângulos do botão de divisão.</span><span class="sxs-lookup"><span data-stu-id="baad2-106">Sent by a button control to its parent to get measurements for the two rectangles of the split button.</span></span> <span data-ttu-id="baad2-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="baad2-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_GETCUSTOMSPLITRECT
        
    nmCustomSplit = (NMCUSTOMSPLITRECTINFO *) lParam;
```



## <a name="parameters"></a><span data-ttu-id="baad2-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="baad2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="baad2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="baad2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="baad2-110">Um ponteiro para um [**NMCUSTOMSPLITRECTINFO**](/windows/win32/api/commctrl/ns-commctrl-nmcustomsplitrectinfo) para receber informações de retângulos delimitadores.</span><span class="sxs-lookup"><span data-stu-id="baad2-110">A pointer to an [**NMCUSTOMSPLITRECTINFO**](/windows/win32/api/commctrl/ns-commctrl-nmcustomsplitrectinfo) to receive bounding rectangles information.</span></span> <span data-ttu-id="baad2-111">A estrutura **NMCUSTOMSPLITRECTINFO** é enviada com o código de notificação como uma solicitação para que o pai forneça medidas para os retângulos do botão de divisão.</span><span class="sxs-lookup"><span data-stu-id="baad2-111">The **NMCUSTOMSPLITRECTINFO** structure is sent with the notification code as a request for the parent to provide measurements for the rectangles of the split button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="baad2-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="baad2-112">Return value</span></span>

<span data-ttu-id="baad2-113">Retorne [**CDRF \_ SKIPDEFAULT**](cdrf-constants.md) para instruir o controle de botão a usar os valores retornados na estrutura [**NMCUSTOMSPLITRECTINFO**](/windows/win32/api/commctrl/ns-commctrl-nmcustomsplitrectinfo) ; caso contrário, retornará [**CDRF \_ dopadrão**](cdrf-constants.md).</span><span class="sxs-lookup"><span data-stu-id="baad2-113">Return [**CDRF\_SKIPDEFAULT**](cdrf-constants.md) to tell the button control to use the values returned in the [**NMCUSTOMSPLITRECTINFO**](/windows/win32/api/commctrl/ns-commctrl-nmcustomsplitrectinfo) structure; otherwise, return [**CDRF\_DODEFAULT**](cdrf-constants.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="baad2-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="baad2-114">Remarks</span></span>

<span data-ttu-id="baad2-115">Esse código de notificação é enviado por um controle de botão antes de ser desenhado.</span><span class="sxs-lookup"><span data-stu-id="baad2-115">This notification code is sent by a button control before it is drawn.</span></span> <span data-ttu-id="baad2-116">O botão deve ser do estilo [**BS \_ SPLITBUTTON**](button-styles.md) ou [**BS \_ DEFSPLITBUTTON**](button-styles.md).</span><span class="sxs-lookup"><span data-stu-id="baad2-116">The button must be of style [**BS\_SPLITBUTTON**](button-styles.md) or [**BS\_DEFSPLITBUTTON**](button-styles.md).</span></span> <span data-ttu-id="baad2-117">Se os retângulos retornados ao controle em *lParam* não forem válidos, eles serão ignorados.</span><span class="sxs-lookup"><span data-stu-id="baad2-117">If the rectangles returned to the control in *lParam* are not valid, they are ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="baad2-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="baad2-118">Requirements</span></span>



| <span data-ttu-id="baad2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="baad2-119">Requirement</span></span> | <span data-ttu-id="baad2-120">Valor</span><span class="sxs-lookup"><span data-stu-id="baad2-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="baad2-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="baad2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="baad2-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="baad2-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="baad2-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="baad2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="baad2-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="baad2-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="baad2-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="baad2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="baad2-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="baad2-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





