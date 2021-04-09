---
title: Código de notificação de NM_RCLICK (guia) (commctrl. h)
description: Notifica a janela pai de um controle guia que o usuário clicou com o botão direito do mouse dentro do controle. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: ef2270c0-eef3-4867-8aa3-b6ff7e1a5f0f
keywords:
- Código de notificação de NM_RCLICK (guia) controles do Windows
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
ms.openlocfilehash: 9c74249e2c2984dd11dab7c4eab8147cb572f291
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009778"
---
# <a name="nm_rclick-tab-notification-code"></a><span data-ttu-id="ac3dc-105">\_Código de notificação nm RCLICK (guia)</span><span class="sxs-lookup"><span data-stu-id="ac3dc-105">NM\_RCLICK (tab) notification code</span></span>

<span data-ttu-id="ac3dc-106">Notifica a janela pai de um controle guia que o usuário clicou com o botão direito do mouse dentro do controle.</span><span class="sxs-lookup"><span data-stu-id="ac3dc-106">Notifies the parent window of a tab control that the user has clicked the right mouse button within the control.</span></span> <span data-ttu-id="ac3dc-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="ac3dc-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RCLICK 

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="ac3dc-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ac3dc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac3dc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ac3dc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ac3dc-110">Ponteiro para uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém informações adicionais sobre esta notificação.</span><span class="sxs-lookup"><span data-stu-id="ac3dc-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac3dc-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ac3dc-111">Return value</span></span>

<span data-ttu-id="ac3dc-112">Retornar zero para não permitir o processamento padrão ou zero para permitir o processamento padrão.</span><span class="sxs-lookup"><span data-stu-id="ac3dc-112">Return nonzero to not allow the default processing, or zero to allow the default processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac3dc-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac3dc-113">Requirements</span></span>



| <span data-ttu-id="ac3dc-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac3dc-114">Requirement</span></span> | <span data-ttu-id="ac3dc-115">Valor</span><span class="sxs-lookup"><span data-stu-id="ac3dc-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ac3dc-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ac3dc-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ac3dc-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ac3dc-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ac3dc-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ac3dc-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ac3dc-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ac3dc-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ac3dc-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ac3dc-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac3dc-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac3dc-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





