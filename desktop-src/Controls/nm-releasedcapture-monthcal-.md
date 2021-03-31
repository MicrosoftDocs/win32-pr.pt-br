---
title: Código de notificação NM_RELEASEDCAPTURE (calendário mensal) (commctrl. h)
description: Notifica uma janela pai do controle calendário mensal que o controle está liberando a captura do mouse. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: c05d3331-26f3-41f4-8032-36ed38d47917
keywords:
- Calendário mensal (código de notificação de NM_RELEASEDCAPTURE) controles do Windows
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
ms.openlocfilehash: 0b9c743a076c8046aa57ba4306145248ed00f0fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644254"
---
# <a name="nm_releasedcapture-monthcal-notification-code"></a><span data-ttu-id="99f56-105">\_Código de notificação nm RELEASEDCAPTURE (calendário mensal)</span><span class="sxs-lookup"><span data-stu-id="99f56-105">NM\_RELEASEDCAPTURE (monthcal) notification code</span></span>

<span data-ttu-id="99f56-106">Notifica uma janela pai do controle calendário mensal que o controle está liberando a captura do mouse.</span><span class="sxs-lookup"><span data-stu-id="99f56-106">Notifies a monthcal control's parent window that the control is releasing mouse capture.</span></span> <span data-ttu-id="99f56-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="99f56-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RELEASEDCAPTURE

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="99f56-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="99f56-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99f56-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="99f56-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="99f56-110">Ponteiro para uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém informações adicionais sobre esta notificação.</span><span class="sxs-lookup"><span data-stu-id="99f56-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99f56-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="99f56-111">Return value</span></span>

<span data-ttu-id="99f56-112">O controle ignora o valor de retorno deste código de notificação.</span><span class="sxs-lookup"><span data-stu-id="99f56-112">The control ignores the return value from this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="99f56-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99f56-113">Requirements</span></span>



| <span data-ttu-id="99f56-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="99f56-114">Requirement</span></span> | <span data-ttu-id="99f56-115">Valor</span><span class="sxs-lookup"><span data-stu-id="99f56-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="99f56-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="99f56-116">Minimum supported client</span></span><br/> | <span data-ttu-id="99f56-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="99f56-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="99f56-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="99f56-118">Minimum supported server</span></span><br/> | <span data-ttu-id="99f56-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="99f56-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="99f56-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="99f56-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="99f56-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="99f56-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





