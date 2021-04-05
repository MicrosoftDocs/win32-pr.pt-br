---
title: HDN_BEGINFILTEREDIT código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de cabeçalho que uma edição de filtro foi iniciada. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 93964453-bb94-4127-8ed4-41acb226b8e2
keywords:
- HDN_BEGINFILTEREDIT de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- HDN_BEGINFILTEREDIT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0527427752b5621e626add17d61e60a675958f42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919251"
---
# <a name="hdn_beginfilteredit-notification-code"></a><span data-ttu-id="e16fc-105">Código de notificação do HDN \_ BEGINFILTEREDIT</span><span class="sxs-lookup"><span data-stu-id="e16fc-105">HDN\_BEGINFILTEREDIT notification code</span></span>

<span data-ttu-id="e16fc-106">Notifica uma janela pai do controle de cabeçalho que uma edição de filtro foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="e16fc-106">Notifies a header control's parent window that a filter edit has begun.</span></span> <span data-ttu-id="e16fc-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="e16fc-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_BEGINFILTEREDIT

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="e16fc-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e16fc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e16fc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e16fc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e16fc-110">Um ponteiro para uma estrutura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contém informações adicionais sobre o filtro que está sendo editado.</span><span class="sxs-lookup"><span data-stu-id="e16fc-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains additional information about the filter that is being edited.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e16fc-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e16fc-111">Return value</span></span>

<span data-ttu-id="e16fc-112">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="e16fc-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e16fc-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e16fc-113">Requirements</span></span>



| <span data-ttu-id="e16fc-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e16fc-114">Requirement</span></span> | <span data-ttu-id="e16fc-115">Valor</span><span class="sxs-lookup"><span data-stu-id="e16fc-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e16fc-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e16fc-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e16fc-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e16fc-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e16fc-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e16fc-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e16fc-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e16fc-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e16fc-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e16fc-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e16fc-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e16fc-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





