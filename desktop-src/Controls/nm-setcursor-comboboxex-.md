---
title: Código de notificação NM_SETCURSOR (ComboBoxEx) (commctrl. h)
description: Notifica uma janela pai do controle ComboBoxEx que o controle está definindo o cursor em resposta a uma mensagem do WM \_ SetCursor. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: a1c617fa-8eb2-444f-88d1-9913de7a42d1
keywords:
- ComboBoxEx (código de notificação de NM_SETCURSOR) controles do Windows
topic_type:
- apiref
api_name:
- NM_SETCURSOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fbd5e10f06e74af0778521d31c69e63586a6476
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644941"
---
# <a name="nm_setcursor-comboboxex-notification-code"></a><span data-ttu-id="428af-105">\_Código de notificação do nm SetCursor (ComboBoxEx)</span><span class="sxs-lookup"><span data-stu-id="428af-105">NM\_SETCURSOR (ComboBoxEx) notification code</span></span>

<span data-ttu-id="428af-106">Notifica uma janela pai do controle ComboBoxEx que o controle está definindo o cursor em resposta a uma mensagem do [**WM \_ SetCursor**](/windows/desktop/menurc/wm-setcursor) .</span><span class="sxs-lookup"><span data-stu-id="428af-106">Notifies a ComboBoxEx control's parent window that the control is setting the cursor in response to a [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) message.</span></span> <span data-ttu-id="428af-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="428af-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_SETCURSOR

    lpnmm = (LPNMMOUSE) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="428af-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="428af-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="428af-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="428af-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="428af-110">Um ponteiro para uma estrutura [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) que contém informações adicionais sobre esta notificação.</span><span class="sxs-lookup"><span data-stu-id="428af-110">A pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="428af-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="428af-111">Return value</span></span>

<span data-ttu-id="428af-112">Retornar zero para habilitar o controle para definir o cursor ou diferente de zero para impedir que o controle defina o cursor.</span><span class="sxs-lookup"><span data-stu-id="428af-112">Return zero to enable the control to set the cursor or nonzero to prevent the control from setting the cursor.</span></span>

## <a name="requirements"></a><span data-ttu-id="428af-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="428af-113">Requirements</span></span>



| <span data-ttu-id="428af-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="428af-114">Requirement</span></span> | <span data-ttu-id="428af-115">Valor</span><span class="sxs-lookup"><span data-stu-id="428af-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="428af-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="428af-116">Minimum supported client</span></span><br/> | <span data-ttu-id="428af-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="428af-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="428af-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="428af-118">Minimum supported server</span></span><br/> | <span data-ttu-id="428af-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="428af-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="428af-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="428af-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="428af-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="428af-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

