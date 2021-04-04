---
title: Código de notificação de NM_RDBLCLK (guia) (commctrl. h)
description: Notifica a janela pai de um controle guia de que o usuário clicou duas vezes com o botão direito do mouse dentro do controle. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: cdf0df70-e30b-4353-8c2a-26fffa0596c4
keywords:
- Código de notificação de NM_RDBLCLK (guia) controles do Windows
topic_type:
- apiref
api_name:
- NM_RDBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c4e159e64780f21576aa9e936379c881b32153d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008851"
---
# <a name="nm_rdblclk-tab-notification-code"></a><span data-ttu-id="6aa33-105">\_Código de notificação nm RDBLCLK (guia)</span><span class="sxs-lookup"><span data-stu-id="6aa33-105">NM\_RDBLCLK (tab) notification code</span></span>

<span data-ttu-id="6aa33-106">Notifica a janela pai de um controle guia de que o usuário clicou duas vezes com o botão direito do mouse dentro do controle.</span><span class="sxs-lookup"><span data-stu-id="6aa33-106">Notifies the parent window of a tab control that the user has double-clicked the right mouse button within the control.</span></span> <span data-ttu-id="6aa33-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="6aa33-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RDBLCLK 

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="6aa33-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6aa33-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6aa33-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6aa33-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6aa33-110">Ponteiro para uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém informações adicionais sobre esta notificação.</span><span class="sxs-lookup"><span data-stu-id="6aa33-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6aa33-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6aa33-111">Return value</span></span>

<span data-ttu-id="6aa33-112">Retornar zero para não permitir o processamento padrão ou zero para permitir o processamento padrão.</span><span class="sxs-lookup"><span data-stu-id="6aa33-112">Return nonzero to not allow the default processing, or zero to allow the default processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="6aa33-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6aa33-113">Requirements</span></span>



| <span data-ttu-id="6aa33-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6aa33-114">Requirement</span></span> | <span data-ttu-id="6aa33-115">Valor</span><span class="sxs-lookup"><span data-stu-id="6aa33-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6aa33-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6aa33-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6aa33-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6aa33-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6aa33-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6aa33-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6aa33-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6aa33-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6aa33-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6aa33-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6aa33-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6aa33-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





