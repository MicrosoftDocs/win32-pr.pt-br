---
title: EN_ALIGNRTL código de notificação (RichEdit. h)
description: Notifica uma janela pai do controle de edição rico que a direção do parágrafo foi alterada da direita para a esquerda. Um controle de edição rico envia esse código de notificação na forma de uma \_ mensagem de comando do WM.
ms.assetid: 2db5fd49-9ecd-49d7-8199-1706648255ca
keywords:
- EN_ALIGNRTL de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- EN_ALIGNRTL
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fac2adaa629d00ef940f02f1ed69eb778cdc7813
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454939"
---
# <a name="en_alignrtl-notification-code"></a><span data-ttu-id="d5916-105">\_Código de notificação en ALIGNRTL</span><span class="sxs-lookup"><span data-stu-id="d5916-105">EN\_ALIGNRTL notification code</span></span>

<span data-ttu-id="d5916-106">Notifica uma janela pai do controle de edição rico que a direção do parágrafo foi alterada da direita para a esquerda.</span><span class="sxs-lookup"><span data-stu-id="d5916-106">Notifies a rich edit control's parent window that the paragraph direction changed to right-to-left.</span></span> <span data-ttu-id="d5916-107">Um controle de edição rico envia esse código de notificação na forma de uma mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="d5916-107">A rich edit control sends this notification code in the form of a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
EN_ALIGNRTL

    WPARAM wParam
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="d5916-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d5916-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5916-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d5916-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d5916-110">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o identificador do controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="d5916-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the rich edit control.</span></span> <span data-ttu-id="d5916-111">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="d5916-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="d5916-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d5916-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d5916-113">Manipular para o controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="d5916-113">Handle to the rich edit control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5916-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d5916-114">Return value</span></span>

<span data-ttu-id="d5916-115">Este código de notificação não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="d5916-115">This notification code does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5916-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5916-116">Requirements</span></span>



| <span data-ttu-id="d5916-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5916-117">Requirement</span></span> | <span data-ttu-id="d5916-118">Valor</span><span class="sxs-lookup"><span data-stu-id="d5916-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d5916-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d5916-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d5916-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d5916-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d5916-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d5916-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d5916-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d5916-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d5916-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d5916-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5916-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5916-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5916-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="d5916-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="d5916-126">**Referência**</span><span class="sxs-lookup"><span data-stu-id="d5916-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d5916-127">**ALIGNLTR de EN \_**</span><span class="sxs-lookup"><span data-stu-id="d5916-127">**EN\_ALIGNLTR**</span></span>](en-alignltr.md)
</dt> <dt>

<span data-ttu-id="d5916-128">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="d5916-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="d5916-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d5916-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="d5916-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d5916-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d5916-131">**comando do WM \_**</span><span class="sxs-lookup"><span data-stu-id="d5916-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

