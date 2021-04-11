---
title: Código de notificação de NM_RCLICK (barra de status) (commctrl. h)
description: Notifica a janela pai de um controle de barra de status que o usuário clicou com o botão direito do mouse dentro do controle. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 9a441d32-f4e4-42ae-877f-17079b0188f4
keywords:
- NM_RCLICK (barra de status) controles do Windows do código de notificação
topic_type:
- apiref
api_name:
- NM_RCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a326ac6600716419648ecfacf25cd8423551fd03
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295922"
---
# <a name="nm_rclick-status-bar-notification-code"></a><span data-ttu-id="bd798-105">\_Código de notificação nm RCLICK (barra de status)</span><span class="sxs-lookup"><span data-stu-id="bd798-105">NM\_RCLICK (status bar) notification code</span></span>

<span data-ttu-id="bd798-106">Notifica a janela pai de um controle de barra de status que o usuário clicou com o botão direito do mouse dentro do controle.</span><span class="sxs-lookup"><span data-stu-id="bd798-106">Notifies the parent window of a status bar control that the user has clicked the right mouse button within the control.</span></span> <span data-ttu-id="bd798-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="bd798-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RCLICK

    lpnm = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="bd798-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bd798-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd798-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bd798-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bd798-110">Ponteiro para uma estrutura [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) que contém informações adicionais sobre esta notificação.</span><span class="sxs-lookup"><span data-stu-id="bd798-110">Pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd798-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bd798-111">Return value</span></span>

<span data-ttu-id="bd798-112">Retornar **true** para indicar que o clique do mouse foi tratado e suprimir o processamento padrão pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="bd798-112">Return **TRUE** to indicate that the mouse click was handled and suppress default processing by the system.</span></span> <span data-ttu-id="bd798-113">Retorne **false** para permitir o processamento padrão do clique.</span><span class="sxs-lookup"><span data-stu-id="bd798-113">Return **FALSE** to allow default processing of the click.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd798-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd798-114">Requirements</span></span>



| <span data-ttu-id="bd798-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd798-115">Requirement</span></span> | <span data-ttu-id="bd798-116">Valor</span><span class="sxs-lookup"><span data-stu-id="bd798-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bd798-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bd798-117">Minimum supported client</span></span><br/> | <span data-ttu-id="bd798-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bd798-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bd798-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bd798-119">Minimum supported server</span></span><br/> | <span data-ttu-id="bd798-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bd798-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bd798-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bd798-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd798-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd798-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





