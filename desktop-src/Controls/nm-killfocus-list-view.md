---
title: Código de notificação de NM_KILLFOCUS (exibição de lista) (commctrl. h)
description: Notifica uma janela pai do controle de exibição de lista que o controle perdeu o foco de entrada. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: f60064da-21e1-4555-ae72-cda8bd76175a
keywords:
- NM_KILLFOCUS de código de notificação (exibição de lista) controles do Windows
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
ms.openlocfilehash: 2d1c031f3ab23d9f79ccf7f29dcfdf5472162214
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454623"
---
# <a name="nm_killfocus-list-view-notification-code"></a><span data-ttu-id="28441-105">\_Código de notificação nm KILLFOCUS (exibição de lista)</span><span class="sxs-lookup"><span data-stu-id="28441-105">NM\_KILLFOCUS (list view) notification code</span></span>

<span data-ttu-id="28441-106">Notifica uma janela pai do controle de exibição de lista que o controle perdeu o foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="28441-106">Notifies a list-view control's parent window that the control has lost the input focus.</span></span> <span data-ttu-id="28441-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="28441-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_KILLFOCUS

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="28441-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="28441-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28441-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="28441-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="28441-110">Ponteiro para uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém informações adicionais sobre esta notificação.</span><span class="sxs-lookup"><span data-stu-id="28441-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28441-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="28441-111">Return value</span></span>

<span data-ttu-id="28441-112">O valor de retorno para essa notificação não é usado.</span><span class="sxs-lookup"><span data-stu-id="28441-112">The return value for this notification is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="28441-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28441-113">Requirements</span></span>



| <span data-ttu-id="28441-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="28441-114">Requirement</span></span> | <span data-ttu-id="28441-115">Valor</span><span class="sxs-lookup"><span data-stu-id="28441-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="28441-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="28441-116">Minimum supported client</span></span><br/> | <span data-ttu-id="28441-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="28441-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="28441-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="28441-118">Minimum supported server</span></span><br/> | <span data-ttu-id="28441-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="28441-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="28441-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="28441-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="28441-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="28441-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





