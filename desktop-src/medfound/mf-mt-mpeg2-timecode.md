---
description: Para um tipo de mídia que descreve um fluxo de transporte MPEG-2 (TS), especifica que os pacotes de transporte contêm um código de tempo de 4 bytes.
ms.assetid: B172E7A8-5757-49B7-A784-FAFC7E904A4C
title: Atributo MF_MT_MPEG2_TIMECODE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bc9db5d7b3c6e94f7845bec2bd98c569d1b1f9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170371"
---
# <a name="mf_mt_mpeg2_timecode-attribute"></a><span data-ttu-id="ca2c8-103">Atributo de código de intróia MF \_ MT \_ \_</span><span class="sxs-lookup"><span data-stu-id="ca2c8-103">MF\_MT\_MPEG2\_TIMECODE attribute</span></span>

<span data-ttu-id="ca2c8-104">Para um tipo de mídia que descreve um fluxo de transporte MPEG-2 (TS), especifica que os pacotes de transporte contêm um código de tempo de 4 bytes.</span><span class="sxs-lookup"><span data-stu-id="ca2c8-104">For a media type that describes an MPEG-2 transport stream (TS), specifies the transport packets contain a 4-byte time code.</span></span>

## <a name="data-type"></a><span data-ttu-id="ca2c8-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="ca2c8-105">Data type</span></span>

<span data-ttu-id="ca2c8-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="ca2c8-106">**UINT32**</span></span>



| <span data-ttu-id="ca2c8-107">Valor</span><span class="sxs-lookup"><span data-stu-id="ca2c8-107">Value</span></span>                                                                                                | <span data-ttu-id="ca2c8-108">Significado</span><span class="sxs-lookup"><span data-stu-id="ca2c8-108">Meaning</span></span>                                                                                                                                        |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="ca2c8-109"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="ca2c8-109"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="ca2c8-110">Nenhum código de tempo é adicionado.</span><span class="sxs-lookup"><span data-stu-id="ca2c8-110">No time code is added.</span></span><br/>                                                                                                              |
| <span id="1"></span><dl> <span data-ttu-id="ca2c8-111"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="ca2c8-111"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="ca2c8-112">Um código de tempo de 4 bytes é adicionado no início de cada pacote de transporte.</span><span class="sxs-lookup"><span data-stu-id="ca2c8-112">A 4-byte time code is added at the start of each transport packet.</span></span> <span data-ttu-id="ca2c8-113">Esse código de tempo é exigido por alguns padrões de televisão digital.</span><span class="sxs-lookup"><span data-stu-id="ca2c8-113">This time code is required by some digital television standards.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ca2c8-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca2c8-114">Requirements</span></span>



| <span data-ttu-id="ca2c8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca2c8-115">Requirement</span></span> | <span data-ttu-id="ca2c8-116">Valor</span><span class="sxs-lookup"><span data-stu-id="ca2c8-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ca2c8-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ca2c8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ca2c8-118">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="ca2c8-118">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="ca2c8-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ca2c8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ca2c8-120">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="ca2c8-120">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="ca2c8-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ca2c8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca2c8-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca2c8-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca2c8-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="ca2c8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca2c8-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ca2c8-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




