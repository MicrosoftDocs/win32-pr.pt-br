---
title: Código de notificação de NM_RELEASEDCAPTURE (up-down) (commctrl. h)
description: Notifica uma janela pai do controle up que o controle está liberando a captura do mouse. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 88a4a9a2-ba7f-4ccc-b5bf-749f49dc666b
keywords:
- NM_RELEASEDCAPTURE (up) código de notificação controles do Windows
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
ms.openlocfilehash: 4b94f2a61727861cbf47720a41c7255763992b54
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105769033"
---
# <a name="nm_releasedcapture-up-down-notification-code"></a><span data-ttu-id="03b06-105">\_Código de notificação nm RELEASEDCAPTURE (up-down)</span><span class="sxs-lookup"><span data-stu-id="03b06-105">NM\_RELEASEDCAPTURE (up-down) notification code</span></span>

<span data-ttu-id="03b06-106">Notifica uma janela pai do controle up que o controle está liberando a captura do mouse.</span><span class="sxs-lookup"><span data-stu-id="03b06-106">Notifies an up-down control's parent window that the control is releasing mouse capture.</span></span> <span data-ttu-id="03b06-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="03b06-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RELEASEDCAPTURE

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="03b06-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="03b06-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03b06-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="03b06-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="03b06-110">Ponteiro para uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém informações adicionais sobre esta notificação.</span><span class="sxs-lookup"><span data-stu-id="03b06-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03b06-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="03b06-111">Return value</span></span>

<span data-ttu-id="03b06-112">O controle ignora o valor de retorno deste código de notificação.</span><span class="sxs-lookup"><span data-stu-id="03b06-112">The control ignores the return value from this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="03b06-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03b06-113">Requirements</span></span>



| <span data-ttu-id="03b06-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="03b06-114">Requirement</span></span> | <span data-ttu-id="03b06-115">Valor</span><span class="sxs-lookup"><span data-stu-id="03b06-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="03b06-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="03b06-116">Minimum supported client</span></span><br/> | <span data-ttu-id="03b06-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="03b06-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="03b06-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="03b06-118">Minimum supported server</span></span><br/> | <span data-ttu-id="03b06-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="03b06-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="03b06-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="03b06-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="03b06-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="03b06-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





