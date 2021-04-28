---
description: Evento InkPicture. NewInAirPackets – ocorre quando um pacote no ar é visto.
ms.assetid: 30bc423d-0642-4515-9e51-a8b8b36aecad
title: Evento InkPicture. NewInAirPackets (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0de8f2423817bada84f83b63de1517393740db4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086554"
---
# <a name="inkpicturenewinairpackets-event"></a><span data-ttu-id="c29c1-103">Evento InkPicture. NewInAirPackets</span><span class="sxs-lookup"><span data-stu-id="c29c1-103">InkPicture.NewInAirPackets event</span></span>

<span data-ttu-id="c29c1-104">Ocorre quando um pacote no ar é visto.</span><span class="sxs-lookup"><span data-stu-id="c29c1-104">Occurs when an in-air packet is seen.</span></span>

## <a name="syntax"></a><span data-ttu-id="c29c1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c29c1-105">Syntax</span></span>


```C++
void NewInAirPackets(
  [in]      IInkCursor *Cursor,
  [in]      long       PacketCount,
  [in, out] VARIANT    *PacketData
);
```



## <a name="parameters"></a><span data-ttu-id="c29c1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c29c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c29c1-107">*Cursor* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c29c1-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c29c1-108">O objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que gerou o evento **NewInAirPackets** .</span><span class="sxs-lookup"><span data-stu-id="c29c1-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **NewInAirPackets** event.</span></span>

</dd> <dt>

<span data-ttu-id="c29c1-109">*PacketCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c29c1-109">*PacketCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c29c1-110">O número de pacotes no ar recebidos.</span><span class="sxs-lookup"><span data-stu-id="c29c1-110">The number of in-air packets received.</span></span>

</dd> <dt>

<span data-ttu-id="c29c1-111">*PacketData* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="c29c1-111">*PacketData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c29c1-112">Uma matriz que contém os dados selecionados para o pacote.</span><span class="sxs-lookup"><span data-stu-id="c29c1-112">An array that contains the selected data for the packet.</span></span>

<span data-ttu-id="c29c1-113">Para obter mais informações sobre a estrutura de VARIAntes, consulte [usando a biblioteca com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="c29c1-113">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c29c1-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="c29c1-114">Return value</span></span>

<span data-ttu-id="c29c1-115">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="c29c1-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c29c1-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="c29c1-116">Remarks</span></span>

<span data-ttu-id="c29c1-117">Um pacote no ar é criado quando um usuário move uma caneta perto do Tablet e o cursor está dentro da janela do objeto do coletor de tinta ou o usuário move um mouse dentro da janela associada do objeto do coletor de tinta.</span><span class="sxs-lookup"><span data-stu-id="c29c1-117">An in-air packet is created when a user moves a pen near the tablet and the cursor is within the ink collector object's window or the user moves a mouse within the ink collector object's associated window.</span></span> <span data-ttu-id="c29c1-118">Os eventos **NewInAirPackets** são gerados rapidamente, e o manipulador de eventos deve ser rápido ou o desempenho sofre.</span><span class="sxs-lookup"><span data-stu-id="c29c1-118">**NewInAirPackets** events are generated rapidly, and the event handler must be fast or performance suffers.</span></span>

<span data-ttu-id="c29c1-119">Esse método de evento é definido nas interfaces somente de expedição **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** (dispinterfaces) com uma ID de ICENewInAirPackets de DISPID \_ .</span><span class="sxs-lookup"><span data-stu-id="c29c1-119">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICENewInAirPackets.</span></span>

<span data-ttu-id="c29c1-120">O evento **NewInAirPackets** é acionado mesmo quando no modo de seleção ou apagamento, não apenas ao inserir tinta.</span><span class="sxs-lookup"><span data-stu-id="c29c1-120">The **NewInAirPackets** event is fired even when in select or erase mode, not just when inserting ink.</span></span> <span data-ttu-id="c29c1-121">Isso requer que você monitore o modo de edição (que é responsável pela configuração) e esteja ciente do modo antes de interpretar o evento.</span><span class="sxs-lookup"><span data-stu-id="c29c1-121">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="c29c1-122">A vantagem desse requisito é maior liberdade para inovar na plataforma por meio de maior conscientização dos eventos da plataforma.</span><span class="sxs-lookup"><span data-stu-id="c29c1-122">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

<span data-ttu-id="c29c1-123">Para definir quais propriedades estão contidas nessa matriz, use a propriedade [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription) do objeto do coletor de tinta.</span><span class="sxs-lookup"><span data-stu-id="c29c1-123">To set which properties are contained in this array, use the [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription) property of the ink collector object.</span></span> <span data-ttu-id="c29c1-124">A matriz que o parâmetro *PacketData* retorna contém os dados para essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c29c1-124">The array that the *PacketData* parameter returns contains the data for those properties.</span></span>

> [!Note]  
> <span data-ttu-id="c29c1-125">Embora você possa modificar os dados do pacote, essas modificações não são persistentes ou usadas.</span><span class="sxs-lookup"><span data-stu-id="c29c1-125">Although you can modify the packet data, these modifications are not persisted or used.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c29c1-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c29c1-126">Requirements</span></span>



| <span data-ttu-id="c29c1-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="c29c1-127">Requirement</span></span> | <span data-ttu-id="c29c1-128">Valor</span><span class="sxs-lookup"><span data-stu-id="c29c1-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c29c1-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c29c1-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c29c1-130">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="c29c1-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="c29c1-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c29c1-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c29c1-132">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="c29c1-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="c29c1-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c29c1-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="c29c1-134"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="c29c1-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c29c1-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c29c1-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="c29c1-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c29c1-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="c29c1-137">Consulte também</span><span class="sxs-lookup"><span data-stu-id="c29c1-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c29c1-138">InkPicture</span><span class="sxs-lookup"><span data-stu-id="c29c1-138">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="c29c1-139">**Propriedade DesiredPacketDescription**</span><span class="sxs-lookup"><span data-stu-id="c29c1-139">**DesiredPacketDescription Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription)
</dt> <dt>

[<span data-ttu-id="c29c1-140">**Evento NewPackets**</span><span class="sxs-lookup"><span data-stu-id="c29c1-140">**NewPackets Event**</span></span>](inkpicture-newpackets.md)
</dt> <dt>

[<span data-ttu-id="c29c1-141">**Interface IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="c29c1-141">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




