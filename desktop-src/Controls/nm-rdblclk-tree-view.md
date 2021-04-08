---
title: Código de notificação de NM_RDBLCLK (exibição em árvore) (commctrl. h)
description: Notifica o pai de um controle de exibição de árvore que o usuário clicou duas vezes com o botão direito do mouse dentro do controle. Essa notificação é enviada na forma de uma mensagem de \_ notificação do WM.
ms.assetid: eb1ae167-32cb-45d6-92e6-7bf5f7e46c2a
keywords:
- Código de notificação de NM_RDBLCLK (exibição de árvore) controles do Windows
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
ms.openlocfilehash: 7ef5b4f1dbaf1031c995028028cc0b44e544f5f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086090"
---
# <a name="nm_rdblclk-tree-view-notification-code"></a><span data-ttu-id="244c3-105">\_Código de notificação nm RDBLCLK (exibição em árvore)</span><span class="sxs-lookup"><span data-stu-id="244c3-105">NM\_RDBLCLK (tree view) notification code</span></span>

<span data-ttu-id="244c3-106">Notifica o pai de um controle de exibição de árvore que o usuário clicou duas vezes com o botão direito do mouse dentro do controle.</span><span class="sxs-lookup"><span data-stu-id="244c3-106">Notifies the parent of a tree-view control that the user has double-clicked the right mouse button within the control.</span></span> <span data-ttu-id="244c3-107">Essa notificação é enviada na forma de uma mensagem [**de \_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="244c3-107">This notification is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RDBLCLK

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="244c3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="244c3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="244c3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="244c3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="244c3-110">Ponteiro para uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém informações adicionais sobre esta notificação.</span><span class="sxs-lookup"><span data-stu-id="244c3-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="244c3-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="244c3-111">Return value</span></span>

<span data-ttu-id="244c3-112">Retornar um valor diferente de zero para impedir o processamento padrão ou zero para permitir o processamento padrão.</span><span class="sxs-lookup"><span data-stu-id="244c3-112">Return nonzero to prevent the default processing, or zero to allow the default processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="244c3-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="244c3-113">Requirements</span></span>



| <span data-ttu-id="244c3-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="244c3-114">Requirement</span></span> | <span data-ttu-id="244c3-115">Valor</span><span class="sxs-lookup"><span data-stu-id="244c3-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="244c3-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="244c3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="244c3-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="244c3-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="244c3-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="244c3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="244c3-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="244c3-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="244c3-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="244c3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="244c3-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="244c3-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





