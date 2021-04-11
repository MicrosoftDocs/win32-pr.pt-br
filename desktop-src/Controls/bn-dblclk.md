---
title: Código de notificação BN_DBLCLK (WinUser. h)
description: Enviado quando o usuário clica duas vezes em um botão.
ms.assetid: 60cc033f-8b84-4aa5-b625-fdee9deb4757
keywords:
- BN_DBLCLK de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- BN_DBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f04c6bf52e213056d85d3a6d038bedb83754a27e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009133"
---
# <a name="bn_dblclk-notification-code"></a><span data-ttu-id="45bf1-104">Código de notificação do bilhão \_ DBLCLK</span><span class="sxs-lookup"><span data-stu-id="45bf1-104">BN\_DBLCLK notification code</span></span>

<span data-ttu-id="45bf1-105">Enviado quando o usuário clica duas vezes em um botão.</span><span class="sxs-lookup"><span data-stu-id="45bf1-105">Sent when the user double-clicks a button.</span></span> <span data-ttu-id="45bf1-106">Esse código de notificação é enviado automaticamente para os botões de [**\_ UserButton**](button-styles.md), [**BS \_ RadioButton**](button-styles.md)e [**BS \_ OWNERDRAW**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="45bf1-106">This notification code is sent automatically for [**BS\_USERBUTTON**](button-styles.md), [**BS\_RADIOBUTTON**](button-styles.md), and [**BS\_OWNERDRAW**](button-styles.md) buttons.</span></span> <span data-ttu-id="45bf1-107">Outros tipos de botão enviam bilhão \_ DBLCLK somente se tiverem o estilo de [**\_ notificação BS**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="45bf1-107">Other button types send BN\_DBLCLK only if they have the [**BS\_NOTIFY**](button-styles.md) style.</span></span>

<span data-ttu-id="45bf1-108">A janela pai do botão recebe esse código de notificação por meio da mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="45bf1-108">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_DBLCLK

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="45bf1-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="45bf1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45bf1-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="45bf1-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="45bf1-111">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o identificador de controle do botão.</span><span class="sxs-lookup"><span data-stu-id="45bf1-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="45bf1-112">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="45bf1-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="45bf1-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="45bf1-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="45bf1-114">Um identificador para o botão.</span><span class="sxs-lookup"><span data-stu-id="45bf1-114">A handle to the button.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="45bf1-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="45bf1-115">Remarks</span></span>

<span data-ttu-id="45bf1-116">BILHÃO \_ DBLCLK é o mesmo que o código de notificação do [bilhão \_ doubleclickd](bn-doubleclicked.md) .</span><span class="sxs-lookup"><span data-stu-id="45bf1-116">BN\_DBLCLK is the same as the [BN\_DOUBLECLICKED](bn-doubleclicked.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="45bf1-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45bf1-117">Requirements</span></span>



| <span data-ttu-id="45bf1-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="45bf1-118">Requirement</span></span> | <span data-ttu-id="45bf1-119">Valor</span><span class="sxs-lookup"><span data-stu-id="45bf1-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45bf1-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="45bf1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="45bf1-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="45bf1-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="45bf1-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="45bf1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="45bf1-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="45bf1-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="45bf1-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="45bf1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="45bf1-125"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="45bf1-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45bf1-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="45bf1-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="45bf1-127">**Referência**</span><span class="sxs-lookup"><span data-stu-id="45bf1-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="45bf1-128">BILHÃO \_ clicou</span><span class="sxs-lookup"><span data-stu-id="45bf1-128">BN\_CLICKED</span></span>](bn-clicked.md)
</dt> <dt>

[<span data-ttu-id="45bf1-129">BILHÃO com \_ DoubleClick</span><span class="sxs-lookup"><span data-stu-id="45bf1-129">BN\_DOUBLECLICKED</span></span>](bn-doubleclicked.md)
</dt> <dt>

<span data-ttu-id="45bf1-130">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="45bf1-130">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="45bf1-131">**comando do WM \_**</span><span class="sxs-lookup"><span data-stu-id="45bf1-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

