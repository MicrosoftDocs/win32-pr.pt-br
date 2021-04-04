---
title: Código de notificação BN_PAINT (WinUser. h)
description: Enviado quando um botão deve ser pintado.
ms.assetid: 1c742272-60bb-42f1-a9b3-974e9a8540cd
keywords:
- BN_PAINT de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- BN_PAINT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f142c0c502d92933bf7bbc9cb01e3062c8bba96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008874"
---
# <a name="bn_paint-notification-code"></a><span data-ttu-id="a8af7-104">Código de notificação do bilhão \_ Paint</span><span class="sxs-lookup"><span data-stu-id="a8af7-104">BN\_PAINT notification code</span></span>

<span data-ttu-id="a8af7-105">Enviado quando um botão deve ser pintado.</span><span class="sxs-lookup"><span data-stu-id="a8af7-105">Sent when a button should be painted.</span></span>

> [!Note]  
> <span data-ttu-id="a8af7-106">Este código de notificação é fornecido somente para compatibilidade com versões de 16 bits do Windows anteriores à versão 3,0.</span><span class="sxs-lookup"><span data-stu-id="a8af7-106">This notification code is provided only for compatibility with 16-bit versions of Windows earlier than version 3.0.</span></span> <span data-ttu-id="a8af7-107">Os aplicativos devem usar o estilo de botão [**\_ OWNERDRAW BS**](button-styles.md) e a estrutura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) para essa tarefa.</span><span class="sxs-lookup"><span data-stu-id="a8af7-107">Applications should use the [**BS\_OWNERDRAW**](button-styles.md) button style and the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure for this task.</span></span>

 

<span data-ttu-id="a8af7-108">A janela pai do botão recebe esse código de notificação por meio da mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="a8af7-108">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_PAINT

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="a8af7-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a8af7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8af7-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a8af7-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a8af7-111">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o identificador de controle do botão.</span><span class="sxs-lookup"><span data-stu-id="a8af7-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="a8af7-112">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="a8af7-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="a8af7-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a8af7-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a8af7-114">Um identificador para o botão.</span><span class="sxs-lookup"><span data-stu-id="a8af7-114">A handle to the button.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a8af7-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8af7-115">Requirements</span></span>



| <span data-ttu-id="a8af7-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8af7-116">Requirement</span></span> | <span data-ttu-id="a8af7-117">Valor</span><span class="sxs-lookup"><span data-stu-id="a8af7-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8af7-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a8af7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a8af7-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a8af7-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a8af7-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a8af7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a8af7-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a8af7-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a8af7-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a8af7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8af7-123"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a8af7-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

