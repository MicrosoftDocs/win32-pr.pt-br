---
description: Evento InkPicture. NewPackets – ocorre quando o coletor de tinta recebe um pacote.
ms.assetid: 7d120198-c016-4452-b8a8-22c4ad87d526
title: Evento InkPicture. NewPackets (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 194fb9bffae07cca561fbfc11ff8a185d63bb9e6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086474"
---
# <a name="inkpicturenewpackets-event"></a><span data-ttu-id="52fa0-103">Evento InkPicture. NewPackets</span><span class="sxs-lookup"><span data-stu-id="52fa0-103">InkPicture.NewPackets event</span></span>

<span data-ttu-id="52fa0-104">Ocorre quando o coletor de tinta recebe um pacote.</span><span class="sxs-lookup"><span data-stu-id="52fa0-104">Occurs when the ink collector receives a packet.</span></span>

## <a name="syntax"></a><span data-ttu-id="52fa0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="52fa0-105">Syntax</span></span>


```C++
void NewPackets(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in]      long           PacketCount,
  [in, out] VARIANT        *PacketData
);
```



## <a name="parameters"></a><span data-ttu-id="52fa0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="52fa0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52fa0-107">*Cursor* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="52fa0-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52fa0-108">O objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que gerou o evento [**NewInAirPackets**](inkpicture-newinairpackets.md) .</span><span class="sxs-lookup"><span data-stu-id="52fa0-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**NewInAirPackets**](inkpicture-newinairpackets.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="52fa0-109">*Traço* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="52fa0-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52fa0-110">O objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) .</span><span class="sxs-lookup"><span data-stu-id="52fa0-110">The [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="52fa0-111">*PacketCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="52fa0-111">*PacketCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52fa0-112">O número de pacotes recebidos para um objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) .</span><span class="sxs-lookup"><span data-stu-id="52fa0-112">The number of packets received for a [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="52fa0-113">*PacketData* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="52fa0-113">*PacketData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="52fa0-114">Uma matriz que contém os dados selecionados para o pacote.</span><span class="sxs-lookup"><span data-stu-id="52fa0-114">An array that contains the selected data for the packet.</span></span>

<span data-ttu-id="52fa0-115">Para obter mais informações sobre a estrutura de VARIAntes, consulte [usando a biblioteca com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="52fa0-115">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52fa0-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="52fa0-116">Return value</span></span>

<span data-ttu-id="52fa0-117">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="52fa0-117">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="52fa0-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="52fa0-118">Remarks</span></span>

<span data-ttu-id="52fa0-119">Os pacotes são recebidos enquanto um traço está sendo coletado.</span><span class="sxs-lookup"><span data-stu-id="52fa0-119">Packets are received while a stroke is being collected.</span></span> <span data-ttu-id="52fa0-120">Os eventos de pacote ocorrem rapidamente e um manipulador de eventos **NewPackets** deve ser rápido ou o desempenho sofre.</span><span class="sxs-lookup"><span data-stu-id="52fa0-120">Packet events occur rapidly, and a **NewPackets** event handler must be fast or performance suffers.</span></span>

<span data-ttu-id="52fa0-121">Esse método de evento é definido nas interfaces somente de expedição **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** (dispinterfaces) com uma ID de ICENewPackets de DISPID \_ .</span><span class="sxs-lookup"><span data-stu-id="52fa0-121">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICENewPackets.</span></span>

<span data-ttu-id="52fa0-122">Esse evento deve ser usado com cuidado, pois ele pode ter um efeito adverso no desempenho da tinta se um código excessivo for executado nos manipuladores de eventos.</span><span class="sxs-lookup"><span data-stu-id="52fa0-122">This event should be used carefully as it could have an adverse effect on ink performance if too much code is executed in the event handlers.</span></span>

<span data-ttu-id="52fa0-123">Para definir quais propriedades estão contidas nessa matriz, use a propriedade [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) do objeto do coletor de tinta.</span><span class="sxs-lookup"><span data-stu-id="52fa0-123">To set which properties are contained in this array, use the [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) property of the ink collector object.</span></span> <span data-ttu-id="52fa0-124">A matriz que o parâmetro *PacketData* retorna contém os dados para essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="52fa0-124">The array that the *PacketData* parameter returns contains the data for those properties.</span></span>

> [!Note]  
> <span data-ttu-id="52fa0-125">Embora você possa modificar os dados do pacote, essas modificações não são persistentes ou usadas.</span><span class="sxs-lookup"><span data-stu-id="52fa0-125">Although you can modify the packet data, these modifications are not persisted or used.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="52fa0-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52fa0-126">Requirements</span></span>



| <span data-ttu-id="52fa0-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="52fa0-127">Requirement</span></span> | <span data-ttu-id="52fa0-128">Valor</span><span class="sxs-lookup"><span data-stu-id="52fa0-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52fa0-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="52fa0-129">Minimum supported client</span></span><br/> | <span data-ttu-id="52fa0-130">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="52fa0-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="52fa0-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="52fa0-131">Minimum supported server</span></span><br/> | <span data-ttu-id="52fa0-132">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="52fa0-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="52fa0-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="52fa0-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="52fa0-134"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="52fa0-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="52fa0-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="52fa0-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="52fa0-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52fa0-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="52fa0-137">Consulte também</span><span class="sxs-lookup"><span data-stu-id="52fa0-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52fa0-138">InkPicture</span><span class="sxs-lookup"><span data-stu-id="52fa0-138">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="52fa0-139">**Evento NewInAirPackets**</span><span class="sxs-lookup"><span data-stu-id="52fa0-139">**NewInAirPackets Event**</span></span>](inkpicture-newinairpackets.md)
</dt> <dt>

[<span data-ttu-id="52fa0-140">**Interface IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="52fa0-140">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="52fa0-141">**Interface IInkStrokeDisp**</span><span class="sxs-lookup"><span data-stu-id="52fa0-141">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

 




