---
title: Código de notificação BN_DBLCLK (WinUser. h)
description: BN_DBLCLK código de notificação-enviado quando o usuário clica duas vezes em um botão.
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
ms.openlocfilehash: fdb403f37b8fee9ea36023a7cd2511bbaaa2af81
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096844"
---
# <a name="bn_dblclk-notification-code"></a><span data-ttu-id="32db4-104">Código de notificação do bilhão \_ DBLCLK</span><span class="sxs-lookup"><span data-stu-id="32db4-104">BN\_DBLCLK notification code</span></span>

<span data-ttu-id="32db4-105">Enviado quando o usuário clica duas vezes em um botão.</span><span class="sxs-lookup"><span data-stu-id="32db4-105">Sent when the user double-clicks a button.</span></span> <span data-ttu-id="32db4-106">Esse código de notificação é enviado automaticamente para os botões de [**\_ UserButton**](button-styles.md), [**BS \_ RadioButton**](button-styles.md)e [**BS \_ OWNERDRAW**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="32db4-106">This notification code is sent automatically for [**BS\_USERBUTTON**](button-styles.md), [**BS\_RADIOBUTTON**](button-styles.md), and [**BS\_OWNERDRAW**](button-styles.md) buttons.</span></span> <span data-ttu-id="32db4-107">Outros tipos de botão enviam bilhão \_ DBLCLK somente se tiverem o estilo de [**\_ notificação BS**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="32db4-107">Other button types send BN\_DBLCLK only if they have the [**BS\_NOTIFY**](button-styles.md) style.</span></span>

<span data-ttu-id="32db4-108">A janela pai do botão recebe esse código de notificação por meio da mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="32db4-108">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_DBLCLK

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="32db4-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="32db4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32db4-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="32db4-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="32db4-111">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o identificador de controle do botão.</span><span class="sxs-lookup"><span data-stu-id="32db4-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="32db4-112">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="32db4-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="32db4-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="32db4-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="32db4-114">Um identificador para o botão.</span><span class="sxs-lookup"><span data-stu-id="32db4-114">A handle to the button.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="32db4-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="32db4-115">Remarks</span></span>

<span data-ttu-id="32db4-116">BILHÃO \_ DBLCLK é o mesmo que o código de notificação do [bilhão \_ doubleclickd](bn-doubleclicked.md) .</span><span class="sxs-lookup"><span data-stu-id="32db4-116">BN\_DBLCLK is the same as the [BN\_DOUBLECLICKED](bn-doubleclicked.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="32db4-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32db4-117">Requirements</span></span>



| <span data-ttu-id="32db4-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="32db4-118">Requirement</span></span> | <span data-ttu-id="32db4-119">Valor</span><span class="sxs-lookup"><span data-stu-id="32db4-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32db4-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="32db4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="32db4-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="32db4-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="32db4-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="32db4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="32db4-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="32db4-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="32db4-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="32db4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="32db4-125"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="32db4-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32db4-126">Consulte também</span><span class="sxs-lookup"><span data-stu-id="32db4-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="32db4-127">**Referência**</span><span class="sxs-lookup"><span data-stu-id="32db4-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="32db4-128">BILHÃO \_ clicou</span><span class="sxs-lookup"><span data-stu-id="32db4-128">BN\_CLICKED</span></span>](bn-clicked.md)
</dt> <dt>

[<span data-ttu-id="32db4-129">BILHÃO com \_ DoubleClick</span><span class="sxs-lookup"><span data-stu-id="32db4-129">BN\_DOUBLECLICKED</span></span>](bn-doubleclicked.md)
</dt> <dt>

<span data-ttu-id="32db4-130">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="32db4-130">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="32db4-131">**comando do WM \_**</span><span class="sxs-lookup"><span data-stu-id="32db4-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

