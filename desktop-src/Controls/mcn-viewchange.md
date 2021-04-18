---
title: MCN_VIEWCHANGE código de notificação (commctrl. h)
description: Enviado por um controle de calendário mensal quando a exibição atual é alterada. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: ee35ac1d-9aeb-4d75-9cef-016487f23602
keywords:
- MCN_VIEWCHANGE de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- MCN_VIEWCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abbcad3fdda355ac2795dbe49a89fa4e7c2c5cad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454757"
---
# <a name="mcn_viewchange-notification-code"></a><span data-ttu-id="1f52c-105">Código de notificação do MCN \_ VIEWCHANGE</span><span class="sxs-lookup"><span data-stu-id="1f52c-105">MCN\_VIEWCHANGE notification code</span></span>

<span data-ttu-id="1f52c-106">Enviado por um controle de calendário mensal quando a exibição atual é alterada.</span><span class="sxs-lookup"><span data-stu-id="1f52c-106">Sent by a month calendar control when the current view changes.</span></span> <span data-ttu-id="1f52c-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="1f52c-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
MCN_VIEWCHANGE

    lpNMViewChange = (LPNMVIEWCHANGE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="1f52c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1f52c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f52c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1f52c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1f52c-110">Ponteiro para uma estrutura [**NMVIEWCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmviewchange) que contém informações sobre a exibição atual.</span><span class="sxs-lookup"><span data-stu-id="1f52c-110">Pointer to an [**NMVIEWCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmviewchange) structure that contains information about the current view.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f52c-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1f52c-111">Return value</span></span>

<span data-ttu-id="1f52c-112">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="1f52c-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f52c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f52c-113">Requirements</span></span>



| <span data-ttu-id="1f52c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f52c-114">Requirement</span></span> | <span data-ttu-id="1f52c-115">Valor</span><span class="sxs-lookup"><span data-stu-id="1f52c-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1f52c-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f52c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1f52c-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1f52c-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1f52c-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f52c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1f52c-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1f52c-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1f52c-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1f52c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f52c-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f52c-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





