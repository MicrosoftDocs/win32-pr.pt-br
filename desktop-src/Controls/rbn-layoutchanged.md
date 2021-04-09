---
title: RBN_LAYOUTCHANGED código de notificação (commctrl. h)
description: Enviado por um controle rebar quando o usuário altera o layout das faixas do controle. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: e937d151-bfaa-41c0-a134-e70ff2f75d07
keywords:
- RBN_LAYOUTCHANGED de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- RBN_LAYOUTCHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d1fc14578435fc786ecc5496cec96eb2224b4d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085919"
---
# <a name="rbn_layoutchanged-notification-code"></a><span data-ttu-id="d9165-105">\_Código de notificação RBN layoutchanged</span><span class="sxs-lookup"><span data-stu-id="d9165-105">RBN\_LAYOUTCHANGED notification code</span></span>

<span data-ttu-id="d9165-106">Enviado por um controle rebar quando o usuário altera o layout das faixas do controle.</span><span class="sxs-lookup"><span data-stu-id="d9165-106">Sent by a rebar control when the user changes the layout of the control's bands.</span></span> <span data-ttu-id="d9165-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d9165-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_LAYOUTCHANGED 

    lpnmhdr = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="d9165-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d9165-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9165-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d9165-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d9165-110">Ponteiro para uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém informações adicionais sobre esta notificação.</span><span class="sxs-lookup"><span data-stu-id="d9165-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9165-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d9165-111">Return value</span></span>

<span data-ttu-id="d9165-112">O valor de retorno para essa notificação não é usado.</span><span class="sxs-lookup"><span data-stu-id="d9165-112">The return value for this notification is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9165-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9165-113">Requirements</span></span>



| <span data-ttu-id="d9165-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9165-114">Requirement</span></span> | <span data-ttu-id="d9165-115">Valor</span><span class="sxs-lookup"><span data-stu-id="d9165-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d9165-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d9165-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d9165-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d9165-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d9165-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d9165-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d9165-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d9165-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d9165-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d9165-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9165-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9165-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





