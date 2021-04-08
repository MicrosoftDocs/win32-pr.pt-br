---
title: Código de notificação de NM_RETURN (exibição em árvore) (commctrl. h)
description: Notifica uma janela pai do controle de exibição de árvore que o controle tem o foco de entrada e que o usuário pressionou a chave. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: e4a048ec-4643-458a-bf75-f5b08163d6c6
keywords:
- Código de notificação de NM_RETURN (exibição de árvore) controles do Windows
topic_type:
- apiref
api_name:
- NM_RETURN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a0abf3152a9236103301f1c74acfcac69d43f07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918872"
---
# <a name="nm_return-tree-view-notification-code"></a><span data-ttu-id="a5e45-105">\_Código de notificação de retorno de nm (exibição de árvore)</span><span class="sxs-lookup"><span data-stu-id="a5e45-105">NM\_RETURN (tree view) notification code</span></span>

<span data-ttu-id="a5e45-106">Notifica uma janela pai do controle de exibição de árvore que o controle tem o foco de entrada e que o usuário pressionou a chave.</span><span class="sxs-lookup"><span data-stu-id="a5e45-106">Notifies a tree-view control's parent window that the control has the input focus and that the user has pressed the key.</span></span> <span data-ttu-id="a5e45-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="a5e45-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RETURN

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="a5e45-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a5e45-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5e45-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a5e45-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a5e45-110">Ponteiro para uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém informações adicionais sobre esta notificação.</span><span class="sxs-lookup"><span data-stu-id="a5e45-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5e45-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a5e45-111">Return value</span></span>

<span data-ttu-id="a5e45-112">Retornar um valor diferente de zero para impedir o processamento padrão ou zero para permitir o processamento padrão.</span><span class="sxs-lookup"><span data-stu-id="a5e45-112">Return nonzero to prevent the default processing, or zero to allow the default processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5e45-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5e45-113">Requirements</span></span>



| <span data-ttu-id="a5e45-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5e45-114">Requirement</span></span> | <span data-ttu-id="a5e45-115">Valor</span><span class="sxs-lookup"><span data-stu-id="a5e45-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a5e45-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a5e45-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a5e45-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a5e45-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a5e45-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a5e45-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a5e45-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a5e45-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a5e45-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a5e45-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5e45-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5e45-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





