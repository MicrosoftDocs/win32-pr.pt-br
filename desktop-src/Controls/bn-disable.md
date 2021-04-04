---
title: Código de notificação BN_DISABLE (WinUser. h)
description: Enviado quando um botão é desabilitado.
ms.assetid: 5e2bb434-f20d-42f1-a9e9-46c4d10b8c7e
keywords:
- BN_DISABLE de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- BN_DISABLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faaba622c056366fe0c49683adc2c020a6302929
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918171"
---
# <a name="bn_disable-notification-code"></a><span data-ttu-id="8d199-104">BILHÃO \_ desabilitar código de notificação</span><span class="sxs-lookup"><span data-stu-id="8d199-104">BN\_DISABLE notification code</span></span>

<span data-ttu-id="8d199-105">Enviado quando um botão é desabilitado.</span><span class="sxs-lookup"><span data-stu-id="8d199-105">Sent when a button is disabled.</span></span>

> [!Note]  
> <span data-ttu-id="8d199-106">Este código de notificação é fornecido somente para compatibilidade com versões de 16 bits do Windows anteriores à versão 3,0.</span><span class="sxs-lookup"><span data-stu-id="8d199-106">This notification code is provided only for compatibility with 16-bit versions of Windows earlier than version 3.0.</span></span> <span data-ttu-id="8d199-107">Os aplicativos devem usar o estilo de botão [**\_ OWNERDRAW BS**](button-styles.md) e a estrutura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) para essa tarefa.</span><span class="sxs-lookup"><span data-stu-id="8d199-107">Applications should use the [**BS\_OWNERDRAW**](button-styles.md) button style and the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure for this task.</span></span>

 

<span data-ttu-id="8d199-108">A janela pai do botão recebe esse código de notificação por meio da mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="8d199-108">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_DISABLE

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="8d199-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8d199-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d199-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8d199-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8d199-111">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o identificador de controle do botão.</span><span class="sxs-lookup"><span data-stu-id="8d199-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="8d199-112">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="8d199-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="8d199-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8d199-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8d199-114">Manipular para o botão.</span><span class="sxs-lookup"><span data-stu-id="8d199-114">Handle to the button.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8d199-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d199-115">Requirements</span></span>



| <span data-ttu-id="8d199-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d199-116">Requirement</span></span> | <span data-ttu-id="8d199-117">Valor</span><span class="sxs-lookup"><span data-stu-id="8d199-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d199-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8d199-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8d199-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8d199-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8d199-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8d199-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8d199-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8d199-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8d199-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8d199-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d199-123"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8d199-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

