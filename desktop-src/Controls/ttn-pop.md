---
title: TTN_POP código de notificação (commctrl. h)
description: Notifica a janela do proprietário de que uma dica de ferramenta está prestes a ser ocultada. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 44a38f1a-f1df-4057-bf76-f87eb467f0d7
keywords:
- TTN_POP de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TTN_POP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 576aa382f571fb6ded7205d2df3b0abd938c704d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644636"
---
# <a name="ttn_pop-notification-code"></a><span data-ttu-id="eb8fb-105">\_Código de notificação pop do TTN</span><span class="sxs-lookup"><span data-stu-id="eb8fb-105">TTN\_POP notification code</span></span>

<span data-ttu-id="eb8fb-106">Notifica a janela do proprietário de que uma dica de ferramenta está prestes a ser ocultada.</span><span class="sxs-lookup"><span data-stu-id="eb8fb-106">Notifies the owner window that a tooltip is about to be hidden.</span></span> <span data-ttu-id="eb8fb-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="eb8fb-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TTN_POP

    pnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="eb8fb-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eb8fb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb8fb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eb8fb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eb8fb-110">Ponteiro para uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) .</span><span class="sxs-lookup"><span data-stu-id="eb8fb-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb8fb-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="eb8fb-111">Return value</span></span>

<span data-ttu-id="eb8fb-112">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="eb8fb-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb8fb-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb8fb-113">Requirements</span></span>



| <span data-ttu-id="eb8fb-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb8fb-114">Requirement</span></span> | <span data-ttu-id="eb8fb-115">Valor</span><span class="sxs-lookup"><span data-stu-id="eb8fb-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eb8fb-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eb8fb-116">Minimum supported client</span></span><br/> | <span data-ttu-id="eb8fb-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="eb8fb-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="eb8fb-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eb8fb-118">Minimum supported server</span></span><br/> | <span data-ttu-id="eb8fb-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="eb8fb-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="eb8fb-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="eb8fb-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb8fb-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb8fb-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





