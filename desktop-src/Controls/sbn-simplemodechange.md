---
title: SBN_SIMPLEMODECHANGE código de notificação (commctrl. h)
description: Enviado por um controle de barra de status quando o modo simples é alterado devido a uma \_ mensagem simples do SB. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: b2df8feb-5028-4488-a99b-4ceff5b48a92
keywords:
- SBN_SIMPLEMODECHANGE de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- SBN_SIMPLEMODECHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b998f0c39ecb00322bf5a423f99b3231338283f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105752938"
---
# <a name="sbn_simplemodechange-notification-code"></a><span data-ttu-id="cb049-105">Código de notificação do SBN \_ SIMPLEMODECHANGE</span><span class="sxs-lookup"><span data-stu-id="cb049-105">SBN\_SIMPLEMODECHANGE notification code</span></span>

<span data-ttu-id="cb049-106">Enviado por um controle de barra de status quando o modo simples é alterado devido a uma mensagem [**\_ simples do SB**](sb-simple.md) .</span><span class="sxs-lookup"><span data-stu-id="cb049-106">Sent by a status bar control when the simple mode changes due to a [**SB\_SIMPLE**](sb-simple.md) message.</span></span> <span data-ttu-id="cb049-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="cb049-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
SBN_SIMPLEMODECHANGE

    lpnmh = (NMHDR*) lParam;
```



## <a name="parameters"></a><span data-ttu-id="cb049-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cb049-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb049-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cb049-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cb049-110">Ponteiro para uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém informações sobre o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="cb049-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb049-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cb049-111">Return value</span></span>

<span data-ttu-id="cb049-112">O valor de retorno é ignorado pela barra de status.</span><span class="sxs-lookup"><span data-stu-id="cb049-112">The return value is ignored by the status bar.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb049-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb049-113">Requirements</span></span>



| <span data-ttu-id="cb049-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb049-114">Requirement</span></span> | <span data-ttu-id="cb049-115">Valor</span><span class="sxs-lookup"><span data-stu-id="cb049-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cb049-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cb049-116">Minimum supported client</span></span><br/> | <span data-ttu-id="cb049-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cb049-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cb049-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cb049-118">Minimum supported server</span></span><br/> | <span data-ttu-id="cb049-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cb049-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cb049-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cb049-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb049-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb049-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





