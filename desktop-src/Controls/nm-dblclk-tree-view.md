---
title: Código de notificação de NM_DBLCLK (exibição em árvore) (commctrl. h)
description: Notifica a janela pai de um controle de exibição de árvore que o usuário clicou duas vezes com o botão esquerdo do mouse dentro do controle. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 2ed3b3ad-a252-496a-bfcf-0cec5678f192
keywords:
- Código de notificação de NM_DBLCLK (exibição de árvore) controles do Windows
topic_type:
- apiref
api_name:
- NM_DBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78f89671e1a26962eacf255d4c98ea0baa1578de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008856"
---
# <a name="nm_dblclk-tree-view-notification-code"></a><span data-ttu-id="e9f9a-105">\_Código de notificação nm DBLCLK (exibição em árvore)</span><span class="sxs-lookup"><span data-stu-id="e9f9a-105">NM\_DBLCLK (tree view) notification code</span></span>

<span data-ttu-id="e9f9a-106">Notifica a janela pai de um controle de exibição de árvore que o usuário clicou duas vezes com o botão esquerdo do mouse dentro do controle.</span><span class="sxs-lookup"><span data-stu-id="e9f9a-106">Notifies the parent window of a tree-view control that the user has double-clicked the left mouse button within the control.</span></span> <span data-ttu-id="e9f9a-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="e9f9a-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_DBLCLK
        
    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="e9f9a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e9f9a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9f9a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e9f9a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e9f9a-110">Ponteiro para uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém informações adicionais sobre esta notificação.</span><span class="sxs-lookup"><span data-stu-id="e9f9a-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9f9a-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e9f9a-111">Return value</span></span>

<span data-ttu-id="e9f9a-112">Retornar um valor diferente de zero para impedir o processamento padrão ou zero para permitir o processamento padrão.</span><span class="sxs-lookup"><span data-stu-id="e9f9a-112">Return nonzero to prevent the default processing, or zero to allow the default processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9f9a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9f9a-113">Requirements</span></span>



| <span data-ttu-id="e9f9a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9f9a-114">Requirement</span></span> | <span data-ttu-id="e9f9a-115">Valor</span><span class="sxs-lookup"><span data-stu-id="e9f9a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e9f9a-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e9f9a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e9f9a-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e9f9a-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e9f9a-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e9f9a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e9f9a-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e9f9a-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e9f9a-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e9f9a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9f9a-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9f9a-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





