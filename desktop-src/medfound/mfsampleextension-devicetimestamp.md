---
description: Contém o carimbo de data/hora do driver de dispositivo.
ms.assetid: 8904d104-ebcc-474d-b6b5-b262b6f62ee9
title: Atributo MFSampleExtension_DeviceTimestamp (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 285b354ecd0e399fc297d3677d29b88847f9eba8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827816"
---
# <a name="mfsampleextension_devicetimestamp-attribute"></a><span data-ttu-id="00a74-103">\_Atributo MFSampleExtension DeviceTimestamp</span><span class="sxs-lookup"><span data-stu-id="00a74-103">MFSampleExtension\_DeviceTimestamp attribute</span></span>

<span data-ttu-id="00a74-104">Contém o carimbo de data/hora do driver de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="00a74-104">Contains the time stamp from the device driver.</span></span>

## <a name="data-type"></a><span data-ttu-id="00a74-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="00a74-105">Data type</span></span>

<span data-ttu-id="00a74-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="00a74-106">**UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="00a74-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="00a74-107">Get/set</span></span>

<span data-ttu-id="00a74-108">Para obter esse atributo, chame [**IMFAttributes:: getuint64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span><span class="sxs-lookup"><span data-stu-id="00a74-108">To get this attribute, call [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span></span>

<span data-ttu-id="00a74-109">Para definir esse atributo, chame [**IMFAttributes:: setuint64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span><span class="sxs-lookup"><span data-stu-id="00a74-109">To set this attribute, call [**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span></span>

## <a name="applies-to"></a><span data-ttu-id="00a74-110">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="00a74-110">Applies to</span></span>

[<span data-ttu-id="00a74-111">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="00a74-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="00a74-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="00a74-112">Remarks</span></span>

<span data-ttu-id="00a74-113">Esse atributo é definido em amostras de mídia criadas por uma fonte de mídia para um dispositivo de captura.</span><span class="sxs-lookup"><span data-stu-id="00a74-113">This attribute is set on media samples created by a media source for a capture device.</span></span> <span data-ttu-id="00a74-114">O valor desse atributo está no domínio [**MFTIME**](mftime.md) , compartilhando uma época com tempo de QPC (contador de desempenho de consulta) e sempre expresso em unidades de 100ns.</span><span class="sxs-lookup"><span data-stu-id="00a74-114">This attribute's value is in the [**MFTIME**](mftime.md) domain, sharing an epoch with query performance counter (QPC) time and always expressed in 100ns units.</span></span> <span data-ttu-id="00a74-115">Esse atributo está disponível para MFTs inserido no pipeline de captura.</span><span class="sxs-lookup"><span data-stu-id="00a74-115">This attribute is available for MFTs inserted into the capture pipeline.</span></span>

<span data-ttu-id="00a74-116">Para obter o carimbo de data/hora em relação ao início do streaming, chame o método [**IMFSample:: Getsampletime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) .</span><span class="sxs-lookup"><span data-stu-id="00a74-116">To get the time stamp relative to the start of streaming, call the [**IMFSample::GetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) method.</span></span>

<span data-ttu-id="00a74-117">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="00a74-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="00a74-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00a74-118">Requirements</span></span>



| <span data-ttu-id="00a74-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="00a74-119">Requirement</span></span> | <span data-ttu-id="00a74-120">Valor</span><span class="sxs-lookup"><span data-stu-id="00a74-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="00a74-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="00a74-121">Minimum supported client</span></span><br/> | <span data-ttu-id="00a74-122">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="00a74-122">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="00a74-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="00a74-123">Minimum supported server</span></span><br/> | <span data-ttu-id="00a74-124">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="00a74-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="00a74-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="00a74-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="00a74-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="00a74-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00a74-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="00a74-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00a74-128">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="00a74-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="00a74-129">Captura de áudio/vídeo no Media Foundation</span><span class="sxs-lookup"><span data-stu-id="00a74-129">Audio/Video Capture in Media Foundation</span></span>](audio-video-capture-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="00a74-130">Atributos de exemplo</span><span class="sxs-lookup"><span data-stu-id="00a74-130">Sample Attributes</span></span>](sample-attributes.md)
</dt> </dl>

 

 




