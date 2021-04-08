---
title: Código de notificação NM_RELEASEDCAPTURE (TrackBar) (commctrl. h)
description: Notifica uma janela pai do controle TrackBar que o controle está liberando a captura do mouse. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 1e3e4f67-672d-4e3e-84f4-b3fa6221d118
keywords:
- TrackBar (código de notificação de NM_RELEASEDCAPTURE) controles do Windows
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
ms.openlocfilehash: 684f58fb5328cfe0d25fc73ce7c1a2d9a189d86f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086027"
---
# <a name="nm_releasedcapture-trackbar-notification-code"></a><span data-ttu-id="9232c-105">\_Código de notificação nm RELEASEDCAPTURE (TrackBar)</span><span class="sxs-lookup"><span data-stu-id="9232c-105">NM\_RELEASEDCAPTURE (trackbar) notification code</span></span>

<span data-ttu-id="9232c-106">Notifica uma janela pai do controle TrackBar que o controle está liberando a captura do mouse.</span><span class="sxs-lookup"><span data-stu-id="9232c-106">Notifies a trackbar control's parent window that the control is releasing mouse capture.</span></span> <span data-ttu-id="9232c-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="9232c-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RELEASEDCAPTURE

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="9232c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9232c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9232c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9232c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9232c-110">Ponteiro para uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém informações adicionais sobre esta notificação.</span><span class="sxs-lookup"><span data-stu-id="9232c-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9232c-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9232c-111">Return value</span></span>

<span data-ttu-id="9232c-112">O controle ignora o valor de retorno deste código de notificação.</span><span class="sxs-lookup"><span data-stu-id="9232c-112">The control ignores the return value from this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9232c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9232c-113">Requirements</span></span>



| <span data-ttu-id="9232c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="9232c-114">Requirement</span></span> | <span data-ttu-id="9232c-115">Valor</span><span class="sxs-lookup"><span data-stu-id="9232c-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9232c-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9232c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9232c-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9232c-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9232c-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9232c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9232c-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9232c-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9232c-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9232c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9232c-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9232c-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





