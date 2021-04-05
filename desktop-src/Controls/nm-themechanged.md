---
title: NM_THEMECHANGED código de notificação (commctrl. h)
description: Notifica uma janela pai do controle que o tema foi alterado. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 5e6a039e-9c35-4476-8cf1-5aea8977ed2d
keywords:
- NM_THEMECHANGED de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- NM_THEMECHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dab2a133da2ff1fed0949f2bc97ce294168febc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009560"
---
# <a name="nm_themechanged-notification-code"></a><span data-ttu-id="648b3-105">Código de notificação do tema do NMchanged \_</span><span class="sxs-lookup"><span data-stu-id="648b3-105">NM\_THEMECHANGED notification code</span></span>

<span data-ttu-id="648b3-106">Notifica uma janela pai do controle que o tema foi alterado.</span><span class="sxs-lookup"><span data-stu-id="648b3-106">Notifies a control's parent window that the theme has changed.</span></span> <span data-ttu-id="648b3-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="648b3-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_THEMECHANGED

    lpnmhdr = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="648b3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="648b3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="648b3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="648b3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="648b3-110">Um ponteiro para uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém informações adicionais sobre esta notificação.</span><span class="sxs-lookup"><span data-stu-id="648b3-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="648b3-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="648b3-111">Return value</span></span>

<span data-ttu-id="648b3-112">O valor de retorno é ignorado pelo controle.</span><span class="sxs-lookup"><span data-stu-id="648b3-112">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="648b3-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="648b3-113">Requirements</span></span>



| <span data-ttu-id="648b3-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="648b3-114">Requirement</span></span> | <span data-ttu-id="648b3-115">Valor</span><span class="sxs-lookup"><span data-stu-id="648b3-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="648b3-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="648b3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="648b3-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="648b3-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="648b3-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="648b3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="648b3-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="648b3-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="648b3-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="648b3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="648b3-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="648b3-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





