---
title: Código de notificação BN_UNPUSHED (WinUser. h)
description: Enviado quando o estado de push de um botão é definido como não enviado.
ms.assetid: 1ae7311d-f067-41fe-a117-e0c70d239e9d
keywords:
- BN_UNPUSHED de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- BN_UNPUSHED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7eb8c16d8860274c070c31910254311a897c0f1d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085287"
---
# <a name="bn_unpushed-notification-code"></a><span data-ttu-id="65ed2-104">\_Código de notificação não enviado por bilhão</span><span class="sxs-lookup"><span data-stu-id="65ed2-104">BN\_UNPUSHED notification code</span></span>

<span data-ttu-id="65ed2-105">Enviado quando o estado de push de um botão é definido como não enviado.</span><span class="sxs-lookup"><span data-stu-id="65ed2-105">Sent when the push state of a button is set to unpushed.</span></span>

> [!Note]  
> <span data-ttu-id="65ed2-106">Este código de notificação é fornecido somente para compatibilidade com versões de 16 bits do Windows anteriores à versão 3,0.</span><span class="sxs-lookup"><span data-stu-id="65ed2-106">This notification code is provided only for compatibility with 16-bit versions of Windows earlier than version 3.0.</span></span> <span data-ttu-id="65ed2-107">Os aplicativos devem usar o estilo de botão [**\_ OWNERDRAW BS**](button-styles.md) e a estrutura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) para essa tarefa.</span><span class="sxs-lookup"><span data-stu-id="65ed2-107">Applications should use the [**BS\_OWNERDRAW**](button-styles.md) button style and the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure for this task.</span></span>

 

<span data-ttu-id="65ed2-108">A janela pai do botão recebe esse código de notificação por meio da mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="65ed2-108">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_UNPUSHED

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="65ed2-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="65ed2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65ed2-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="65ed2-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="65ed2-111">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o identificador de controle do botão.</span><span class="sxs-lookup"><span data-stu-id="65ed2-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="65ed2-112">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="65ed2-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="65ed2-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="65ed2-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="65ed2-114">Um identificador para o botão.</span><span class="sxs-lookup"><span data-stu-id="65ed2-114">A handle to the button.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="65ed2-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="65ed2-115">Remarks</span></span>

<span data-ttu-id="65ed2-116">\_O bilhão não enviado é o mesmo que o código de notificação do [bilhão \_ UNHILITE](bn-unhilite.md) .</span><span class="sxs-lookup"><span data-stu-id="65ed2-116">BN\_UNPUSHED is the same as the [BN\_UNHILITE](bn-unhilite.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="65ed2-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65ed2-117">Requirements</span></span>



| <span data-ttu-id="65ed2-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="65ed2-118">Requirement</span></span> | <span data-ttu-id="65ed2-119">Valor</span><span class="sxs-lookup"><span data-stu-id="65ed2-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65ed2-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="65ed2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="65ed2-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="65ed2-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="65ed2-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="65ed2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="65ed2-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="65ed2-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="65ed2-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="65ed2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="65ed2-125"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="65ed2-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65ed2-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="65ed2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65ed2-127">BILHÃO \_ enviado por push</span><span class="sxs-lookup"><span data-stu-id="65ed2-127">BN\_PUSHED</span></span>](bn-pushed.md)
</dt> </dl>

 

