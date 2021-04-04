---
title: Código de notificação BN_DOUBLECLICKED (WinUser. h)
description: Enviado quando o usuário clica duas vezes em um botão.
ms.assetid: 2fd7363a-5a02-453c-bfab-df5cbf8e42a5
keywords:
- BN_DOUBLECLICKED de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- BN_DOUBLECLICKED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 018df4387b026d68e3f4e9a6c259fb19efd4a0f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824272"
---
# <a name="bn_doubleclicked-notification-code"></a><span data-ttu-id="5b864-104">Código de notificação do bilhão \_ doubleclickd</span><span class="sxs-lookup"><span data-stu-id="5b864-104">BN\_DOUBLECLICKED notification code</span></span>

<span data-ttu-id="5b864-105">Enviado quando o usuário clica duas vezes em um botão.</span><span class="sxs-lookup"><span data-stu-id="5b864-105">Sent when the user double-clicks a button.</span></span> <span data-ttu-id="5b864-106">Esse código de notificação é enviado automaticamente para os botões de [**\_ UserButton**](button-styles.md), [**BS \_ RadioButton**](button-styles.md)e [**BS \_ OWNERDRAW**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="5b864-106">This notification code is sent automatically for [**BS\_USERBUTTON**](button-styles.md), [**BS\_RADIOBUTTON**](button-styles.md), and [**BS\_OWNERDRAW**](button-styles.md) buttons.</span></span> <span data-ttu-id="5b864-107">Outros tipos de botão enviam bilhão \_ doubleclickd somente se eles tiverem o estilo de [**\_ notificação BS**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="5b864-107">Other button types send BN\_DOUBLECLICKED only if they have the [**BS\_NOTIFY**](button-styles.md) style.</span></span>

<span data-ttu-id="5b864-108">A janela pai do botão recebe esse código de notificação por meio da mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="5b864-108">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_DOUBLECLICKED

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="5b864-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5b864-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b864-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5b864-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5b864-111">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o identificador de controle do botão.</span><span class="sxs-lookup"><span data-stu-id="5b864-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="5b864-112">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="5b864-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="5b864-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5b864-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5b864-114">Um identificador para o botão.</span><span class="sxs-lookup"><span data-stu-id="5b864-114">A handle to the button.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5b864-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="5b864-115">Remarks</span></span>

<span data-ttu-id="5b864-116">O bilhão \_ doubleclickd é o mesmo que o código de notificação do [bilhão \_ DBLCLK](bn-dblclk.md) .</span><span class="sxs-lookup"><span data-stu-id="5b864-116">BN\_DOUBLECLICKED is the same as the [BN\_DBLCLK](bn-dblclk.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b864-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b864-117">Requirements</span></span>



| <span data-ttu-id="5b864-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b864-118">Requirement</span></span> | <span data-ttu-id="5b864-119">Valor</span><span class="sxs-lookup"><span data-stu-id="5b864-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b864-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b864-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5b864-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5b864-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5b864-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b864-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5b864-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5b864-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5b864-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5b864-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b864-125"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5b864-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

