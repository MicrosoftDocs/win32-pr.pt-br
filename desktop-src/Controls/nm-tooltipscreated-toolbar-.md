---
title: Código de notificação de NM_TOOLTIPSCREATED (barra de ferramentas) (commctrl. h)
description: Notifica uma janela pai da barra de ferramentas que a barra de ferramentas criou um controle ToolTip. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 0e9517c1-aa3f-4b14-82b4-195a4ce99757
keywords:
- Código de notificação de NM_TOOLTIPSCREATED (barra de ferramentas) controles do Windows
topic_type:
- apiref
api_name:
- NM_TOOLTIPSCREATED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c13366348da075fab48e7a2f12381f51f7d87bf4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454928"
---
# <a name="nm_tooltipscreated-toolbar-notification-code"></a><span data-ttu-id="41a81-105">\_Código de notificação nm TOOLTIPSCREATED (barra de ferramentas)</span><span class="sxs-lookup"><span data-stu-id="41a81-105">NM\_TOOLTIPSCREATED (toolbar) notification code</span></span>

<span data-ttu-id="41a81-106">Notifica uma janela pai da barra de ferramentas que a barra de ferramentas criou um controle ToolTip.</span><span class="sxs-lookup"><span data-stu-id="41a81-106">Notifies a toolbar's parent window that the toolbar has created a tooltip control.</span></span> <span data-ttu-id="41a81-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="41a81-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_TOOLTIPSCREATED

    lpnmttc = (LPNMTOOLTIPSCREATED) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="41a81-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="41a81-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41a81-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="41a81-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="41a81-110">Ponteiro para uma estrutura [**NMTOOLTIPSCREATED**](/windows/win32/api/commctrl/ns-commctrl-nmtooltipscreated) que contém informações adicionais sobre esta notificação.</span><span class="sxs-lookup"><span data-stu-id="41a81-110">Pointer to an [**NMTOOLTIPSCREATED**](/windows/win32/api/commctrl/ns-commctrl-nmtooltipscreated) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41a81-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="41a81-111">Return value</span></span>

<span data-ttu-id="41a81-112">O controle Toolbar ignora o valor de retorno deste código de notificação.</span><span class="sxs-lookup"><span data-stu-id="41a81-112">The toolbar control ignores the return value from this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="41a81-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41a81-113">Requirements</span></span>



| <span data-ttu-id="41a81-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="41a81-114">Requirement</span></span> | <span data-ttu-id="41a81-115">Valor</span><span class="sxs-lookup"><span data-stu-id="41a81-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="41a81-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="41a81-116">Minimum supported client</span></span><br/> | <span data-ttu-id="41a81-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="41a81-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="41a81-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="41a81-118">Minimum supported server</span></span><br/> | <span data-ttu-id="41a81-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="41a81-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="41a81-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="41a81-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="41a81-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="41a81-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





