---
description: Sinaliza que o número de botões de menu do DVD foi alterado ou que a seleção do botão foi alterada.
ms.assetid: af6c841d-ca06-4535-b418-14409fa78c81
title: EC_DVD_BUTTON_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_BUTTON_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 8647c1100e5cca6897e2068b2a20119a8f047396
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750278"
---
# <a name="ec_dvd_button_change"></a><span data-ttu-id="69bff-103">\_alteração do \_ botão de DVD do EC \_</span><span class="sxs-lookup"><span data-stu-id="69bff-103">EC\_DVD\_BUTTON\_CHANGE</span></span>

<span data-ttu-id="69bff-104">Sinaliza que o número de botões de menu do DVD foi alterado ou que a seleção do botão foi alterada.</span><span class="sxs-lookup"><span data-stu-id="69bff-104">Signals that the number of DVD menu buttons has changed, or that the button selection has changed.</span></span>

## <a name="parameters"></a><span data-ttu-id="69bff-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="69bff-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69bff-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="69bff-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="69bff-107">Valor **DWORD** que indica o número de botões disponíveis.</span><span class="sxs-lookup"><span data-stu-id="69bff-107">**DWORD** value indicating the number of available buttons.</span></span>

</dd> <dt>

<span data-ttu-id="69bff-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="69bff-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="69bff-109">Valor **DWORD** que indica o número do botão atualmente selecionado.</span><span class="sxs-lookup"><span data-stu-id="69bff-109">**DWORD** value indicating the currently selected button number.</span></span> <span data-ttu-id="69bff-110">O botão selecionado número zero implica que nenhum botão está selecionado.</span><span class="sxs-lookup"><span data-stu-id="69bff-110">Selected button number zero implies that no button is selected.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="69bff-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="69bff-111">Remarks</span></span>

<span data-ttu-id="69bff-112">Os números de botão variam de 1 a 36.</span><span class="sxs-lookup"><span data-stu-id="69bff-112">Button numbers range from 1 to 36.</span></span>

<span data-ttu-id="69bff-113">O botão selecionado no momento pode ser alterado automaticamente com um comando de navegação criado no disco, bem como por meio do controle de aplicativo usando a interface [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) .</span><span class="sxs-lookup"><span data-stu-id="69bff-113">The currently selected button can change automatically with a navigation command authored on the disc as well as through application control by using [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) interface.</span></span>

<span data-ttu-id="69bff-114">Esse evento pode sinalizar qualquer um dos números de botão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="69bff-114">This event can signal any of the available button numbers.</span></span> <span data-ttu-id="69bff-115">Esses números nem sempre correspondem aos números de botão usados para [**IDvdControl2:: SelectAndActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectandactivatebutton) porque esse método pode ativar apenas um subconjunto de botões.</span><span class="sxs-lookup"><span data-stu-id="69bff-115">These numbers do not always correspond to button numbers used for [**IDvdControl2::SelectAndActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectandactivatebutton) because that method can activate only a subset of buttons.</span></span>

<span data-ttu-id="69bff-116">Esse evento é gerado em todos os domínios.</span><span class="sxs-lookup"><span data-stu-id="69bff-116">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="69bff-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69bff-117">Requirements</span></span>



| <span data-ttu-id="69bff-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="69bff-118">Requirement</span></span> | <span data-ttu-id="69bff-119">Valor</span><span class="sxs-lookup"><span data-stu-id="69bff-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69bff-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="69bff-120">Header</span></span><br/> | <dl> <span data-ttu-id="69bff-121"><dt>Dvdevcode. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="69bff-121"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69bff-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="69bff-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69bff-123">Aplicativos de DVD</span><span class="sxs-lookup"><span data-stu-id="69bff-123">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="69bff-124">Códigos de notificação de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="69bff-124">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="69bff-125">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="69bff-125">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




