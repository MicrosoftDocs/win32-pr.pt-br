---
title: Código de notificação de NM_RELEASEDCAPTURE (guia) (commctrl. h)
description: Notifica uma janela pai do controle guia que o controle está liberando a captura do mouse. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 17f87666-692c-4c2f-9ef5-6d2593e0de97
keywords:
- Código de notificação de NM_RELEASEDCAPTURE (guia) controles do Windows
topic_type:
- apiref
api_name:
- NM_RELEASEDCAPTURE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad9c9049b63afb18413aea9fa77b7947e97e93b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455425"
---
# <a name="nm_releasedcapture-tab-notification-code"></a><span data-ttu-id="a5815-105">\_Código de notificação nm RELEASEDCAPTURE (guia)</span><span class="sxs-lookup"><span data-stu-id="a5815-105">NM\_RELEASEDCAPTURE (tab) notification code</span></span>

<span data-ttu-id="a5815-106">Notifica uma janela pai do controle guia que o controle está liberando a captura do mouse.</span><span class="sxs-lookup"><span data-stu-id="a5815-106">Notifies a tab control's parent window that the control is releasing mouse capture.</span></span> <span data-ttu-id="a5815-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="a5815-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RELEASEDCAPTURE

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="a5815-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a5815-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5815-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a5815-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a5815-110">Ponteiro para uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém informações adicionais sobre esta notificação.</span><span class="sxs-lookup"><span data-stu-id="a5815-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5815-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a5815-111">Return value</span></span>

<span data-ttu-id="a5815-112">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="a5815-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5815-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5815-113">Requirements</span></span>



| <span data-ttu-id="a5815-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5815-114">Requirement</span></span> | <span data-ttu-id="a5815-115">Valor</span><span class="sxs-lookup"><span data-stu-id="a5815-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a5815-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a5815-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a5815-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a5815-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a5815-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a5815-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a5815-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a5815-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a5815-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a5815-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5815-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5815-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





