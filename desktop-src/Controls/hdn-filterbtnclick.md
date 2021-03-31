---
title: HDN_FILTERBTNCLICK código de notificação (commctrl. h)
description: Notifica a janela pai do controle de cabeçalho quando o botão de filtro é clicado ou em resposta a uma \_ mensagem HDM SETITEM. Esse código de notificação é enviado na forma de uma \_ mensagem de notificação do WM.
ms.assetid: 36b85cdc-1022-4568-8891-0c919c850fd4
keywords:
- HDN_FILTERBTNCLICK de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- HDN_FILTERBTNCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3dbbdab8adf0bee400d591f3d8b4cec6fa1ea81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824197"
---
# <a name="hdn_filterbtnclick-notification-code"></a><span data-ttu-id="027ca-105">Código de notificação do HDN \_ FILTERBTNCLICK</span><span class="sxs-lookup"><span data-stu-id="027ca-105">HDN\_FILTERBTNCLICK notification code</span></span>

<span data-ttu-id="027ca-106">Notifica a janela pai do controle de cabeçalho quando o botão de filtro é clicado ou em resposta a uma mensagem [**HDM \_ SETITEM**](hdm-setitem.md) .</span><span class="sxs-lookup"><span data-stu-id="027ca-106">Notifies the header control's parent window when the filter button is clicked or in response to an [**HDM\_SETITEM**](hdm-setitem.md) message.</span></span> <span data-ttu-id="027ca-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="027ca-107">This notification code sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_FILTERBTNCLICK

    pNMHDFilterBtnClk = (LPNMHDFILTERBTNCLICK) lParam;
```



## <a name="parameters"></a><span data-ttu-id="027ca-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="027ca-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="027ca-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="027ca-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="027ca-110">Um ponteiro para uma estrutura [**NMHDFILTERBTNCLICK**](/windows/win32/api/commctrl/ns-commctrl-nmhdfilterbtnclick) que contém informações sobre o controle de cabeçalho e o botão de filtro de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="027ca-110">A pointer to an [**NMHDFILTERBTNCLICK**](/windows/win32/api/commctrl/ns-commctrl-nmhdfilterbtnclick) structure that contains information about the header control and the header filter button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="027ca-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="027ca-111">Return value</span></span>

<span data-ttu-id="027ca-112">Se você retornar **true**, um código de notificação [HDN \_ FILTERCHANGE](hdn-filterchange.md) será enviado para a janela pai do controle de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="027ca-112">If you return **TRUE**, an [HDN\_FILTERCHANGE](hdn-filterchange.md) notification code will be sent to the header control's parent window.</span></span> <span data-ttu-id="027ca-113">Esse código de notificação dá à janela pai uma oportunidade de sincronizar seus elementos de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="027ca-113">This notification code gives the parent window an opportunity to synchronize its user interface elements.</span></span> <span data-ttu-id="027ca-114">Retorne **false** se você não quiser que a notificação seja enviada.</span><span class="sxs-lookup"><span data-stu-id="027ca-114">Return **FALSE** if you do not want the notification sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="027ca-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="027ca-115">Requirements</span></span>



| <span data-ttu-id="027ca-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="027ca-116">Requirement</span></span> | <span data-ttu-id="027ca-117">Valor</span><span class="sxs-lookup"><span data-stu-id="027ca-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="027ca-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="027ca-118">Minimum supported client</span></span><br/> | <span data-ttu-id="027ca-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="027ca-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="027ca-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="027ca-120">Minimum supported server</span></span><br/> | <span data-ttu-id="027ca-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="027ca-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="027ca-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="027ca-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="027ca-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="027ca-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="027ca-124">Consulte também</span><span class="sxs-lookup"><span data-stu-id="027ca-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="027ca-125">**NMHDFILTERBTNCLICK**</span><span class="sxs-lookup"><span data-stu-id="027ca-125">**NMHDFILTERBTNCLICK**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmhdfilterbtnclick)
</dt> </dl>

 

 





