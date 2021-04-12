---
title: Código de notificação de NM_RELEASEDCAPTURE (exibição de lista) (commctrl. h)
description: Notifica uma janela pai do controle de exibição de lista que o controle está liberando a captura do mouse. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: a43879d9-1465-4c25-936f-cda9b8b8b465
keywords:
- NM_RELEASEDCAPTURE de código de notificação (exibição de lista) controles do Windows
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
ms.openlocfilehash: f42af9dddf6f9864251eff5e2f5a6aebbfa9cd20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455657"
---
# <a name="nm_releasedcapture-list-view-notification-code"></a><span data-ttu-id="17bda-105">\_Código de notificação nm RELEASEDCAPTURE (exibição de lista)</span><span class="sxs-lookup"><span data-stu-id="17bda-105">NM\_RELEASEDCAPTURE (list view) notification code</span></span>

<span data-ttu-id="17bda-106">Notifica uma janela pai do controle de exibição de lista que o controle está liberando a captura do mouse.</span><span class="sxs-lookup"><span data-stu-id="17bda-106">Notifies a list-view control's parent window that the control is releasing mouse capture.</span></span> <span data-ttu-id="17bda-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="17bda-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RELEASEDCAPTURE

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="17bda-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="17bda-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17bda-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="17bda-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="17bda-110">Ponteiro para uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém informações adicionais sobre esta notificação.</span><span class="sxs-lookup"><span data-stu-id="17bda-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17bda-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="17bda-111">Return value</span></span>

<span data-ttu-id="17bda-112">O controle ignora o valor de retorno deste código de notificação.</span><span class="sxs-lookup"><span data-stu-id="17bda-112">The control ignores the return value from this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="17bda-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17bda-113">Requirements</span></span>



| <span data-ttu-id="17bda-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="17bda-114">Requirement</span></span> | <span data-ttu-id="17bda-115">Valor</span><span class="sxs-lookup"><span data-stu-id="17bda-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="17bda-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="17bda-116">Minimum supported client</span></span><br/> | <span data-ttu-id="17bda-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="17bda-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="17bda-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="17bda-118">Minimum supported server</span></span><br/> | <span data-ttu-id="17bda-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="17bda-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="17bda-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="17bda-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="17bda-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="17bda-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





