---
description: Ocorre quando um pacote no ar é visto.
ms.assetid: 10dc1909-bfbc-4ea0-b77a-e33149205107
title: Evento InkOverlay. NewInAirPackets (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ac030a2e32ecf662d811a3c91ccdc2dd3c5fd03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171166"
---
# <a name="inkoverlaynewinairpackets-event"></a><span data-ttu-id="3a773-103">Evento InkOverlay. NewInAirPackets</span><span class="sxs-lookup"><span data-stu-id="3a773-103">InkOverlay.NewInAirPackets event</span></span>

<span data-ttu-id="3a773-104">Ocorre quando um pacote no ar é visto.</span><span class="sxs-lookup"><span data-stu-id="3a773-104">Occurs when an in-air packet is seen.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a773-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3a773-105">Syntax</span></span>


```C++
void NewInAirPackets(
  [in]      IInkCursor *Cursor,
  [in]      long       PacketCount,
  [in, out] VARIANT    *PacketData
);
```



## <a name="parameters"></a><span data-ttu-id="3a773-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3a773-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a773-107">*Cursor* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3a773-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a773-108">O objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que gerou o evento [**NewInAirPackets**](inkcollector-newinairpackets.md) .</span><span class="sxs-lookup"><span data-stu-id="3a773-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**NewInAirPackets**](inkcollector-newinairpackets.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="3a773-109">*PacketCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3a773-109">*PacketCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a773-110">O número de pacotes no ar recebidos.</span><span class="sxs-lookup"><span data-stu-id="3a773-110">The number of in-air packets received.</span></span>

</dd> <dt>

<span data-ttu-id="3a773-111">*PacketData* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="3a773-111">*PacketData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3a773-112">Uma matriz que contém os dados selecionados para o pacote.</span><span class="sxs-lookup"><span data-stu-id="3a773-112">An array that contains the selected data for the packet.</span></span>

<span data-ttu-id="3a773-113">Para obter mais informações sobre a estrutura de VARIAntes, consulte [usando a biblioteca com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="3a773-113">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a773-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3a773-114">Return value</span></span>

<span data-ttu-id="3a773-115">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="3a773-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a773-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="3a773-116">Remarks</span></span>

<span data-ttu-id="3a773-117">Um pacote no ar é criado quando um usuário move uma caneta perto do Tablet e o cursor está dentro da janela do objeto do coletor de tinta ou o usuário move um mouse dentro da janela associada do objeto do coletor de tinta.</span><span class="sxs-lookup"><span data-stu-id="3a773-117">An in-air packet is created when a user moves a pen near the tablet and the cursor is within the ink collector object's window or the user moves a mouse within the ink collector object's associated window.</span></span> <span data-ttu-id="3a773-118">Os eventos [**NewInAirPackets**](inkcollector-newinairpackets.md) são gerados rapidamente, e o manipulador de eventos deve ser rápido ou o desempenho sofre.</span><span class="sxs-lookup"><span data-stu-id="3a773-118">[**NewInAirPackets**](inkcollector-newinairpackets.md) events are generated rapidly, and the event handler must be fast or performance suffers.</span></span>

<span data-ttu-id="3a773-119">Esse método de evento é definido nas \_ \_ interfaces somente de expedição IInkCollectorEvents, IInkOverlayEvents e \_ IInkPictureEvents (dispinterfaces) com uma ID de ICENewInAirPackets de DISPID \_ .</span><span class="sxs-lookup"><span data-stu-id="3a773-119">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICENewInAirPackets.</span></span>

<span data-ttu-id="3a773-120">O evento [**NewInAirPackets**](inkcollector-newinairpackets.md) é acionado mesmo quando no modo de seleção ou apagamento, não apenas ao inserir tinta.</span><span class="sxs-lookup"><span data-stu-id="3a773-120">The [**NewInAirPackets**](inkcollector-newinairpackets.md) event is fired even when in select or erase mode, not just when inserting ink.</span></span> <span data-ttu-id="3a773-121">Isso requer que você monitore o modo de edição (que é responsável pela configuração) e esteja ciente do modo antes de interpretar o evento.</span><span class="sxs-lookup"><span data-stu-id="3a773-121">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="3a773-122">A vantagem desse requisito é maior liberdade para inovar na plataforma por meio de maior conscientização dos eventos da plataforma.</span><span class="sxs-lookup"><span data-stu-id="3a773-122">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

<span data-ttu-id="3a773-123">Para definir quais propriedades estão contidas nessa matriz, use a propriedade [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) do objeto do coletor de tinta.</span><span class="sxs-lookup"><span data-stu-id="3a773-123">To set which properties are contained in this array, use the [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) property of the ink collector object.</span></span> <span data-ttu-id="3a773-124">A matriz que o parâmetro *PacketData* retorna contém os dados para essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="3a773-124">The array that the *PacketData* parameter returns contains the data for those properties.</span></span>

> [!Note]  
> <span data-ttu-id="3a773-125">Embora você possa modificar os dados do pacote, essas modificações não são persistentes ou usadas.</span><span class="sxs-lookup"><span data-stu-id="3a773-125">Although you can modify the packet data, these modifications are not persisted or used.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3a773-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a773-126">Requirements</span></span>



| <span data-ttu-id="3a773-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a773-127">Requirement</span></span> | <span data-ttu-id="3a773-128">Valor</span><span class="sxs-lookup"><span data-stu-id="3a773-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a773-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a773-129">Minimum supported client</span></span><br/> | <span data-ttu-id="3a773-130">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="3a773-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="3a773-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a773-131">Minimum supported server</span></span><br/> | <span data-ttu-id="3a773-132">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="3a773-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="3a773-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3a773-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a773-134"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="3a773-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="3a773-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3a773-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="3a773-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a773-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="3a773-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="3a773-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a773-138">**Classe InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="3a773-138">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="3a773-139">**Propriedade DesiredPacketDescription**</span><span class="sxs-lookup"><span data-stu-id="3a773-139">**DesiredPacketDescription Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription)
</dt> <dt>

[<span data-ttu-id="3a773-140">**Evento NewPackets**</span><span class="sxs-lookup"><span data-stu-id="3a773-140">**NewPackets Event**</span></span>](inkcollector-newpackets.md)
</dt> <dt>

[<span data-ttu-id="3a773-141">**Interface IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="3a773-141">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




