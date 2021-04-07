---
title: Código de notificação BN_HILITE (WinUser. h)
description: Enviado quando o usuário seleciona um botão.
ms.assetid: f20ba77e-257c-44ec-a2dd-dbf23cd78d07
keywords:
- BN_HILITE de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- BN_HILITE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5567837c9883c52d99f0ca68d450f7b3538f233b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918170"
---
# <a name="bn_hilite-notification-code"></a><span data-ttu-id="044ba-104">Código de notificação do bilhão \_ HILITE</span><span class="sxs-lookup"><span data-stu-id="044ba-104">BN\_HILITE notification code</span></span>

<span data-ttu-id="044ba-105">Enviado quando o usuário seleciona um botão.</span><span class="sxs-lookup"><span data-stu-id="044ba-105">Sent when the user selects a button.</span></span>

> [!Note]  
> <span data-ttu-id="044ba-106">Este código de notificação é fornecido somente para compatibilidade com versões de 16 bits do Windows anteriores à versão 3,0.</span><span class="sxs-lookup"><span data-stu-id="044ba-106">This notification code is provided only for compatibility with 16-bit versions of Windows earlier than version 3.0.</span></span> <span data-ttu-id="044ba-107">Os aplicativos devem usar o estilo de botão [**\_ OWNERDRAW BS**](button-styles.md) e a estrutura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) para essa tarefa.</span><span class="sxs-lookup"><span data-stu-id="044ba-107">Applications should use the [**BS\_OWNERDRAW**](button-styles.md) button style and the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure for this task.</span></span>

 

<span data-ttu-id="044ba-108">A janela pai do botão recebe esse código de notificação por meio da mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="044ba-108">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_HILITE

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="044ba-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="044ba-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="044ba-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="044ba-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="044ba-111">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o identificador de controle do botão.</span><span class="sxs-lookup"><span data-stu-id="044ba-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="044ba-112">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="044ba-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="044ba-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="044ba-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="044ba-114">Manipular para o botão.</span><span class="sxs-lookup"><span data-stu-id="044ba-114">Handle to the button.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="044ba-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="044ba-115">Remarks</span></span>

<span data-ttu-id="044ba-116">BILHÃO \_ HILITE é o mesmo que o código de notificação [ \_ enviado por bilhão](bn-pushed.md) .</span><span class="sxs-lookup"><span data-stu-id="044ba-116">BN\_HILITE is the same as the [BN\_PUSHED](bn-pushed.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="044ba-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="044ba-117">Requirements</span></span>



| <span data-ttu-id="044ba-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="044ba-118">Requirement</span></span> | <span data-ttu-id="044ba-119">Valor</span><span class="sxs-lookup"><span data-stu-id="044ba-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="044ba-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="044ba-120">Minimum supported client</span></span><br/> | <span data-ttu-id="044ba-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="044ba-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="044ba-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="044ba-122">Minimum supported server</span></span><br/> | <span data-ttu-id="044ba-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="044ba-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="044ba-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="044ba-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="044ba-125"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="044ba-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

