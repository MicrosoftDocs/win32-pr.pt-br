---
title: Código de notificação BN_PUSHED (WinUser. h)
description: Enviado quando o estado de push de um botão é definido como enviado por push.
ms.assetid: 34000def-189c-4a37-bcef-4ca09a67df00
keywords:
- BN_PUSHED de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- BN_PUSHED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d18a27599c770eb55d889a21956312512ca804cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104294785"
---
# <a name="bn_pushed-notification-code"></a><span data-ttu-id="5055c-104">BILHÃO \_ código de notificação enviado por push</span><span class="sxs-lookup"><span data-stu-id="5055c-104">BN\_PUSHED notification code</span></span>

<span data-ttu-id="5055c-105">Enviado quando o estado de push de um botão é definido como enviado por push.</span><span class="sxs-lookup"><span data-stu-id="5055c-105">Sent when the push state of a button is set to pushed.</span></span>

> [!Note]  
> <span data-ttu-id="5055c-106">Este código de notificação é fornecido somente para compatibilidade com versões de 16 bits do Windows anteriores à versão 3,0.</span><span class="sxs-lookup"><span data-stu-id="5055c-106">This notification code is provided only for compatibility with 16-bit versions of Windows earlier than version 3.0.</span></span> <span data-ttu-id="5055c-107">Os aplicativos devem usar o estilo de botão [**\_ OWNERDRAW BS**](button-styles.md) e a estrutura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) para essa tarefa.</span><span class="sxs-lookup"><span data-stu-id="5055c-107">Applications should use the [**BS\_OWNERDRAW**](button-styles.md) button style and the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure for this task.</span></span>

 

<span data-ttu-id="5055c-108">A janela pai do botão recebe esse código de notificação por meio da mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="5055c-108">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_PUSHED

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="5055c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5055c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5055c-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5055c-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5055c-111">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o identificador de controle do botão.</span><span class="sxs-lookup"><span data-stu-id="5055c-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="5055c-112">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="5055c-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="5055c-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5055c-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5055c-114">Um identificador para o botão.</span><span class="sxs-lookup"><span data-stu-id="5055c-114">A handle to the button.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5055c-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="5055c-115">Remarks</span></span>

<span data-ttu-id="5055c-116">BILHÃO \_ enviado por push é o mesmo que o código de notificação [bilhão \_ HILITE](bn-hilite.md) .</span><span class="sxs-lookup"><span data-stu-id="5055c-116">BN\_PUSHED is the same as the [BN\_HILITE](bn-hilite.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5055c-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5055c-117">Requirements</span></span>



| <span data-ttu-id="5055c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5055c-118">Requirement</span></span> | <span data-ttu-id="5055c-119">Valor</span><span class="sxs-lookup"><span data-stu-id="5055c-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5055c-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5055c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5055c-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5055c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5055c-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5055c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5055c-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5055c-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5055c-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5055c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5055c-125"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5055c-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5055c-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="5055c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5055c-127">**BILHÃO não \_ enviado por push**</span><span class="sxs-lookup"><span data-stu-id="5055c-127">**BN\_UNPUSHED**</span></span>](bn-unpushed.md)
</dt> </dl>

 

