---
title: HDN_FILTERCHANGE código de notificação (commctrl. h)
description: Notifica a janela pai do controle de cabeçalho que os atributos de um filtro de controle de cabeçalho estão sendo alterados ou editados. Esse código de notificação é enviado na forma de uma \_ mensagem de notificação do WM.
ms.assetid: 0a46af14-569a-4119-881f-549a130f9b0d
keywords:
- HDN_FILTERCHANGE de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- HDN_FILTERCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3d5d31b792e909cd79cdc6aa966bfdce450787b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454700"
---
# <a name="hdn_filterchange-notification-code"></a><span data-ttu-id="35a41-105">Código de notificação do HDN \_ FILTERCHANGE</span><span class="sxs-lookup"><span data-stu-id="35a41-105">HDN\_FILTERCHANGE notification code</span></span>

<span data-ttu-id="35a41-106">Notifica a janela pai do controle de cabeçalho que os atributos de um filtro de controle de cabeçalho estão sendo alterados ou editados.</span><span class="sxs-lookup"><span data-stu-id="35a41-106">Notifies the header control's parent window that the attributes of a header control filter are being changed or edited.</span></span> <span data-ttu-id="35a41-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="35a41-107">This notification code sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_FILTERCHANGE

    pNMHeader =  (LPNMHEADER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="35a41-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="35a41-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35a41-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="35a41-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="35a41-110">Um ponteiro para uma estrutura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contém informações sobre o controle de cabeçalho e o item de cabeçalho, incluindo os atributos que estão prestes a ser alterados.</span><span class="sxs-lookup"><span data-stu-id="35a41-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information about the header control and the header item, including the attributes that are about to change.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35a41-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="35a41-111">Return value</span></span>

<span data-ttu-id="35a41-112">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="35a41-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="35a41-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35a41-113">Requirements</span></span>



| <span data-ttu-id="35a41-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="35a41-114">Requirement</span></span> | <span data-ttu-id="35a41-115">Valor</span><span class="sxs-lookup"><span data-stu-id="35a41-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="35a41-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35a41-116">Minimum supported client</span></span><br/> | <span data-ttu-id="35a41-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="35a41-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="35a41-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35a41-118">Minimum supported server</span></span><br/> | <span data-ttu-id="35a41-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="35a41-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="35a41-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="35a41-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="35a41-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="35a41-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35a41-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="35a41-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35a41-123">**HDM \_ SETFILTERCHANGETIMEOUT**</span><span class="sxs-lookup"><span data-stu-id="35a41-123">**HDM\_SETFILTERCHANGETIMEOUT**</span></span>](hdm-setfilterchangetimeout.md)
</dt> </dl>

 

 





