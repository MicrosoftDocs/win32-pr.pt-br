---
description: Ocorre quando o coletor de tinta rreceives um pacote.
ms.assetid: 26d5a3eb-430a-4e21-8a3f-fdec5005cd6e
title: Evento InkOverlay. NewPackets (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43743b47d007b44d4f2460266e7198266c36afd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171537"
---
# <a name="inkoverlaynewpackets-event"></a><span data-ttu-id="b017c-103">Evento InkOverlay. NewPackets</span><span class="sxs-lookup"><span data-stu-id="b017c-103">InkOverlay.NewPackets event</span></span>

<span data-ttu-id="b017c-104">Ocorre quando o coletor de tinta rreceives um pacote</span><span class="sxs-lookup"><span data-stu-id="b017c-104">Occurs when the ink collecto rreceives a packet</span></span>

## <a name="syntax"></a><span data-ttu-id="b017c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b017c-105">Syntax</span></span>


```C++
void NewPackets(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in]      long           PacketCount,
  [in, out] VARIANT        *PacketData
);
```



## <a name="parameters"></a><span data-ttu-id="b017c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b017c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b017c-107">*Cursor* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b017c-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b017c-108">O objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que gerou o evento [**NewInAirPackets**](inkcollector-newinairpackets.md) .</span><span class="sxs-lookup"><span data-stu-id="b017c-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**NewInAirPackets**](inkcollector-newinairpackets.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="b017c-109">*Traço* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b017c-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b017c-110">Especifica o objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) .</span><span class="sxs-lookup"><span data-stu-id="b017c-110">Specifies the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="b017c-111">*PacketCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b017c-111">*PacketCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b017c-112">O número de pacotes recebidos para um objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) .</span><span class="sxs-lookup"><span data-stu-id="b017c-112">The number of packets received for a [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="b017c-113">*PacketData* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="b017c-113">*PacketData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b017c-114">Uma matriz que contém os dados selecionados para o pacote.</span><span class="sxs-lookup"><span data-stu-id="b017c-114">An array that contains the selected data for the packet.</span></span>

<span data-ttu-id="b017c-115">Para obter mais informações sobre a estrutura de VARIAntes, consulte [usando a biblioteca com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="b017c-115">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b017c-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b017c-116">Return value</span></span>

<span data-ttu-id="b017c-117">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="b017c-117">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b017c-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="b017c-118">Remarks</span></span>

<span data-ttu-id="b017c-119">Os pacotes são recebidos enquanto um traço está sendo coletado.</span><span class="sxs-lookup"><span data-stu-id="b017c-119">Packets are received while a stroke is being collected.</span></span> <span data-ttu-id="b017c-120">Os eventos de pacote ocorrem rapidamente e um manipulador de eventos [**NewPackets**](inkcollector-newpackets.md) deve ser rápido ou o desempenho sofre.</span><span class="sxs-lookup"><span data-stu-id="b017c-120">Packet events occur rapidly, and a [**NewPackets**](inkcollector-newpackets.md) event handler must be fast or performance suffers.</span></span>

<span data-ttu-id="b017c-121">Esse método de evento é definido nas \_ \_ interfaces somente de expedição IInkCollectorEvents, IInkOverlayEvents e \_ IInkPictureEvents (dispinterfaces) com uma ID de ICENewPackets de DISPID \_ .</span><span class="sxs-lookup"><span data-stu-id="b017c-121">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICENewPackets.</span></span>

<span data-ttu-id="b017c-122">Esse evento deve ser usado com cuidado, pois ele pode ter um efeito adverso no desempenho da tinta se um código excessivo for executado nos manipuladores de eventos.</span><span class="sxs-lookup"><span data-stu-id="b017c-122">This event should be used carefully as it could have an adverse effect on ink performance if too much code is executed in the event handlers.</span></span>

<span data-ttu-id="b017c-123">Para definir quais propriedades estão contidas nessa matriz, use a propriedade [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) do objeto do coletor de tinta.</span><span class="sxs-lookup"><span data-stu-id="b017c-123">To set which properties are contained in this array, use the [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) property of the ink collector object.</span></span> <span data-ttu-id="b017c-124">A matriz que o parâmetro *PacketData* retorna contém os dados para essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b017c-124">The array that the *PacketData* parameter returns contains the data for those properties.</span></span>

> [!Note]  
> <span data-ttu-id="b017c-125">Embora você possa modificar os dados do pacote, essas modificações não são persistentes ou usadas.</span><span class="sxs-lookup"><span data-stu-id="b017c-125">Although you can modify the packet data, these modifications are not persisted or used.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b017c-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b017c-126">Requirements</span></span>



| <span data-ttu-id="b017c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="b017c-127">Requirement</span></span> | <span data-ttu-id="b017c-128">Valor</span><span class="sxs-lookup"><span data-stu-id="b017c-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b017c-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b017c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b017c-130">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="b017c-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="b017c-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b017c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b017c-132">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b017c-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="b017c-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b017c-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="b017c-134"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b017c-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b017c-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b017c-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="b017c-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b017c-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="b017c-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="b017c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b017c-138">**Classe InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="b017c-138">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="b017c-139">**Evento NewInAirPackets**</span><span class="sxs-lookup"><span data-stu-id="b017c-139">**NewInAirPackets Event**</span></span>](inkcollector-newinairpackets.md)
</dt> <dt>

[<span data-ttu-id="b017c-140">**Interface IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="b017c-140">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="b017c-141">**Interface IInkStrokeDisp**</span><span class="sxs-lookup"><span data-stu-id="b017c-141">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

 




