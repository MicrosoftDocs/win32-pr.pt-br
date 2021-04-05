---
title: MCN_GETDAYSTATE código de notificação (commctrl. h)
description: Enviado por um controle de calendário mensal para solicitar informações sobre como dias individuais devem ser exibidos. Esse código de notificação é enviado somente por controles de calendário de mês que usam o \_ estilo MCS DAYSTATE e é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: dc2608e0-c598-4b26-9195-208f09cd84b7
keywords:
- MCN_GETDAYSTATE de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- MCN_GETDAYSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bff81b9f171884f39063c517cb17299a55b4053b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644697"
---
# <a name="mcn_getdaystate-notification-code"></a><span data-ttu-id="35b5f-105">Código de notificação do MCN \_ GETDAYSTATE</span><span class="sxs-lookup"><span data-stu-id="35b5f-105">MCN\_GETDAYSTATE notification code</span></span>

<span data-ttu-id="35b5f-106">Enviado por um controle de calendário mensal para solicitar informações sobre como dias individuais devem ser exibidos.</span><span class="sxs-lookup"><span data-stu-id="35b5f-106">Sent by a month calendar control to request information about how individual days should be displayed.</span></span> <span data-ttu-id="35b5f-107">Esse código de notificação é enviado somente por controles de calendário de mês que usam o estilo [**MCS \_ DAYSTATE**](month-calendar-control-styles.md) e é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="35b5f-107">This notification code is sent only by month calendar controls that use the [**MCS\_DAYSTATE**](month-calendar-control-styles.md) style, and it is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
MCN_GETDAYSTATE

    lpNMDayState = (LPNMDAYSTATE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="35b5f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="35b5f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35b5f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="35b5f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="35b5f-110">Ponteiro para uma estrutura [**NMDAYSTATE**](/windows/win32/api/commctrl/ns-commctrl-nmdaystate) .</span><span class="sxs-lookup"><span data-stu-id="35b5f-110">Pointer to an [**NMDAYSTATE**](/windows/win32/api/commctrl/ns-commctrl-nmdaystate) structure.</span></span> <span data-ttu-id="35b5f-111">A estrutura contém informações sobre o intervalo de tempo para o qual o controle precisa de informações e recebe o endereço de uma matriz que fornece esses dados.</span><span class="sxs-lookup"><span data-stu-id="35b5f-111">The structure contains information about the time frame for which the control needs information, and it receives the address of an array that provides this data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35b5f-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="35b5f-112">Return value</span></span>

<span data-ttu-id="35b5f-113">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="35b5f-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="35b5f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="35b5f-114">Remarks</span></span>

<span data-ttu-id="35b5f-115">Manipular esse código de notificação permite que seu aplicativo Personalize sua exibição especificando que determinados dias sejam exibidos em negrito.</span><span class="sxs-lookup"><span data-stu-id="35b5f-115">Handling this notification code allows your application to customize its display by specifying that certain days be displayed in bold.</span></span>

## <a name="requirements"></a><span data-ttu-id="35b5f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35b5f-116">Requirements</span></span>



| <span data-ttu-id="35b5f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="35b5f-117">Requirement</span></span> | <span data-ttu-id="35b5f-118">Valor</span><span class="sxs-lookup"><span data-stu-id="35b5f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="35b5f-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35b5f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="35b5f-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="35b5f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="35b5f-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35b5f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="35b5f-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="35b5f-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="35b5f-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="35b5f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="35b5f-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="35b5f-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





