---
title: Código de notificação de NM_KILLFOCUS (exibição em árvore) (commctrl. h)
description: Notifica uma janela pai do controle de exibição de árvore que o controle perdeu o foco de entrada. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: f6646a39-6480-4417-9c1c-ffd2417ca7dd
keywords:
- Código de notificação de NM_KILLFOCUS (exibição de árvore) controles do Windows
topic_type:
- apiref
api_name:
- NM_KILLFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7123f47469a02fcec92805a27d81e173c5e1d10a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103917984"
---
# <a name="nm_killfocus-tree-view-notification-code"></a><span data-ttu-id="4cd24-105">\_Código de notificação nm KILLFOCUS (exibição em árvore)</span><span class="sxs-lookup"><span data-stu-id="4cd24-105">NM\_KILLFOCUS (tree view) notification code</span></span>

<span data-ttu-id="4cd24-106">Notifica uma janela pai do controle de exibição de árvore que o controle perdeu o foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="4cd24-106">Notifies a tree-view control's parent window that the control has lost the input focus.</span></span> <span data-ttu-id="4cd24-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="4cd24-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_KILLFOCUS

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="4cd24-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4cd24-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cd24-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4cd24-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4cd24-110">Ponteiro para uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém informações adicionais sobre esta notificação.</span><span class="sxs-lookup"><span data-stu-id="4cd24-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cd24-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4cd24-111">Return value</span></span>

<span data-ttu-id="4cd24-112">O valor de retorno é ignorado.</span><span class="sxs-lookup"><span data-stu-id="4cd24-112">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cd24-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4cd24-113">Requirements</span></span>



| <span data-ttu-id="4cd24-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4cd24-114">Requirement</span></span> | <span data-ttu-id="4cd24-115">Valor</span><span class="sxs-lookup"><span data-stu-id="4cd24-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4cd24-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4cd24-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4cd24-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4cd24-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4cd24-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4cd24-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4cd24-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4cd24-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4cd24-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4cd24-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4cd24-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4cd24-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





