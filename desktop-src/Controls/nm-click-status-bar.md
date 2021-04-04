---
title: Código de notificação de NM_CLICK (barra de status) (commctrl. h)
description: Notifica a janela pai de um controle de barra de status que o usuário clicou com o botão esquerdo do mouse dentro do controle. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 179ccbe9-f51f-4356-b91a-10d7e3607b09
keywords:
- NM_CLICK (barra de status) controles do Windows do código de notificação
topic_type:
- apiref
api_name:
- NM_CLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6066f76a8cf0b6ca34b5298cfcdcba2b11e3fa5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824854"
---
# <a name="nm_click-status-bar-notification-code"></a><span data-ttu-id="9c188-105">\_Código de notificação de clique (barra de status) nm</span><span class="sxs-lookup"><span data-stu-id="9c188-105">NM\_CLICK (status bar) notification code</span></span>

<span data-ttu-id="9c188-106">Notifica a janela pai de um controle de barra de status que o usuário clicou com o botão esquerdo do mouse dentro do controle.</span><span class="sxs-lookup"><span data-stu-id="9c188-106">Notifies the parent window of a status bar control that the user has clicked the left mouse button within the control.</span></span> <span data-ttu-id="9c188-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="9c188-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CLICK

    lpnm = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="9c188-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9c188-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c188-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9c188-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9c188-110">Ponteiro para uma estrutura [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) que contém informações adicionais sobre esta notificação.</span><span class="sxs-lookup"><span data-stu-id="9c188-110">Pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains additional information about this notification.</span></span> <span data-ttu-id="9c188-111">O membro **dwItemSpec** contém o índice da seção que foi clicada.</span><span class="sxs-lookup"><span data-stu-id="9c188-111">The **dwItemSpec** member contains the index of the section that was clicked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c188-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9c188-112">Return value</span></span>

<span data-ttu-id="9c188-113">Retornar **true** para indicar que o clique do mouse foi tratado e suprimir o processamento padrão pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="9c188-113">Return **TRUE** to indicate that the mouse click was handled and suppress default processing by the system.</span></span> <span data-ttu-id="9c188-114">Retorne **false** para permitir o processamento padrão do clique.</span><span class="sxs-lookup"><span data-stu-id="9c188-114">Return **FALSE** to allow default processing of the click.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c188-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c188-115">Requirements</span></span>



| <span data-ttu-id="9c188-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c188-116">Requirement</span></span> | <span data-ttu-id="9c188-117">Valor</span><span class="sxs-lookup"><span data-stu-id="9c188-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9c188-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9c188-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9c188-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9c188-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9c188-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9c188-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9c188-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9c188-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9c188-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9c188-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c188-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c188-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





