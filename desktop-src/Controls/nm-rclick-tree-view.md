---
title: Código de notificação de NM_RCLICK (exibição em árvore) (commctrl. h)
description: Notifica a janela pai de um controle de exibição de árvore que o usuário clicou com o botão direito do mouse dentro do controle. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 5816d8b8-7f3d-477d-9116-1b3670d99240
keywords:
- Código de notificação de NM_RCLICK (exibição de árvore) controles do Windows
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
ms.openlocfilehash: 58d72ee220bf33189e8954a2e1ef454b22886553
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086535"
---
# <a name="nm_rclick-tree-view-notification-code"></a><span data-ttu-id="3bb66-105">\_Código de notificação nm RCLICK (exibição em árvore)</span><span class="sxs-lookup"><span data-stu-id="3bb66-105">NM\_RCLICK (tree view) notification code</span></span>

<span data-ttu-id="3bb66-106">Notifica a janela pai de um controle de exibição de árvore que o usuário clicou com o botão direito do mouse dentro do controle.</span><span class="sxs-lookup"><span data-stu-id="3bb66-106">Notifies the parent window of a tree-view control that the user has clicked the right mouse button within the control.</span></span> <span data-ttu-id="3bb66-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="3bb66-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RCLICK 

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="3bb66-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3bb66-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bb66-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3bb66-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3bb66-110">Ponteiro para uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém informações adicionais sobre esta notificação.</span><span class="sxs-lookup"><span data-stu-id="3bb66-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bb66-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3bb66-111">Return value</span></span>

<span data-ttu-id="3bb66-112">Retornar um valor diferente de zero para impedir o processamento padrão ou zero para permitir o processamento padrão.</span><span class="sxs-lookup"><span data-stu-id="3bb66-112">Return nonzero to prevent the default processing, or zero to allow the default processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bb66-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3bb66-113">Requirements</span></span>



| <span data-ttu-id="3bb66-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3bb66-114">Requirement</span></span> | <span data-ttu-id="3bb66-115">Valor</span><span class="sxs-lookup"><span data-stu-id="3bb66-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3bb66-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3bb66-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3bb66-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3bb66-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3bb66-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3bb66-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3bb66-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3bb66-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3bb66-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3bb66-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3bb66-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3bb66-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





