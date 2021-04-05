---
title: Código de notificação BN_UNHILITE (WinUser. h)
description: Enviado quando o realce deve ser removido de um botão.
ms.assetid: 9839a55b-9e9c-4c9c-8e92-347007ea27be
keywords:
- BN_UNHILITE de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- BN_UNHILITE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 395901548103a7a678b4873e1fde52e259297ebb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918120"
---
# <a name="bn_unhilite-notification-code"></a><span data-ttu-id="2b324-104">Código de notificação do bilhão \_ UNHILITE</span><span class="sxs-lookup"><span data-stu-id="2b324-104">BN\_UNHILITE notification code</span></span>

<span data-ttu-id="2b324-105">Enviado quando o realce deve ser removido de um botão.</span><span class="sxs-lookup"><span data-stu-id="2b324-105">Sent when the highlight should be removed from a button.</span></span>

> [!Note]  
> <span data-ttu-id="2b324-106">Este código de notificação é fornecido somente para compatibilidade com versões de 16 bits do Windows anteriores à versão 3,0.</span><span class="sxs-lookup"><span data-stu-id="2b324-106">This notification code is provided only for compatibility with 16-bit versions of Windows earlier than version 3.0.</span></span> <span data-ttu-id="2b324-107">Os aplicativos devem usar o estilo de botão [**\_ OWNERDRAW BS**](button-styles.md) e a estrutura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) para essa tarefa.</span><span class="sxs-lookup"><span data-stu-id="2b324-107">Applications should use the [**BS\_OWNERDRAW**](button-styles.md) button style and the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure for this task.</span></span>

 

<span data-ttu-id="2b324-108">A janela pai do botão recebe esse código de notificação por meio da mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="2b324-108">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_UNHILITE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="2b324-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2b324-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b324-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2b324-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2b324-111">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o identificador de controle do botão.</span><span class="sxs-lookup"><span data-stu-id="2b324-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="2b324-112">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="2b324-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="2b324-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2b324-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2b324-114">Um identificador para o botão.</span><span class="sxs-lookup"><span data-stu-id="2b324-114">A handle to the button.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2b324-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="2b324-115">Remarks</span></span>

<span data-ttu-id="2b324-116">BILHÃO \_ UNHILITE é o mesmo que o código de notificação não [ \_ enviado por bilhão](bn-unpushed.md) .</span><span class="sxs-lookup"><span data-stu-id="2b324-116">BN\_UNHILITE is the same as the [BN\_UNPUSHED](bn-unpushed.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b324-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b324-117">Requirements</span></span>



| <span data-ttu-id="2b324-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b324-118">Requirement</span></span> | <span data-ttu-id="2b324-119">Valor</span><span class="sxs-lookup"><span data-stu-id="2b324-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b324-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2b324-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2b324-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2b324-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2b324-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2b324-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2b324-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2b324-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2b324-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2b324-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b324-125"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2b324-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

