---
title: Código de notificação de NM_RCLICK (cabeçalho) (commctrl. h)
description: Notifica uma janela pai do controle de exibição de árvore que o usuário clicou com o botão direito do mouse dentro do controle. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: b453db51-9c41-4a85-8bc0-72bec10f8646
keywords:
- Código de notificação de NM_RCLICK (cabeçalho) controles do Windows
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
ms.openlocfilehash: bab91d3e35f4da74657faa2fce0e9a9881577087
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918878"
---
# <a name="nm_rclick-header-notification-code"></a><span data-ttu-id="77e1d-105">\_Código de notificação nm RCLICK (Header)</span><span class="sxs-lookup"><span data-stu-id="77e1d-105">NM\_RCLICK (header) notification code</span></span>

<span data-ttu-id="77e1d-106">Notifica uma janela pai do controle de exibição de árvore que o usuário clicou com o botão direito do mouse dentro do controle.</span><span class="sxs-lookup"><span data-stu-id="77e1d-106">Notifies a tree-view control's parent window that the user has clicked the right mouse button within the control.</span></span> <span data-ttu-id="77e1d-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="77e1d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RCLICK

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="77e1d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="77e1d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77e1d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="77e1d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="77e1d-110">Um ponteiro para uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém informações adicionais sobre esta notificação.</span><span class="sxs-lookup"><span data-stu-id="77e1d-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77e1d-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="77e1d-111">Return value</span></span>

<span data-ttu-id="77e1d-112">Retornar zero para não permitir o processamento padrão ou zero para permitir o processamento padrão.</span><span class="sxs-lookup"><span data-stu-id="77e1d-112">Return nonzero to not allow the default processing, or zero to allow the default processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="77e1d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77e1d-113">Requirements</span></span>



| <span data-ttu-id="77e1d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="77e1d-114">Requirement</span></span> | <span data-ttu-id="77e1d-115">Valor</span><span class="sxs-lookup"><span data-stu-id="77e1d-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="77e1d-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77e1d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="77e1d-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="77e1d-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="77e1d-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77e1d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="77e1d-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="77e1d-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="77e1d-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="77e1d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="77e1d-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="77e1d-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





