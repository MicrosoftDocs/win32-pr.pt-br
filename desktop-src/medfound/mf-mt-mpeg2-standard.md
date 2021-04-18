---
description: Para um tipo de mídia que descreve um fluxo de programa MPEG-2 (PS) ou um fluxo de transporte (TS), especifica o padrão usado para multiplexar o fluxo.
ms.assetid: 3D4C1A81-A9BA-427F-93DB-F522A0616EAB
title: Atributo MF_MT_MPEG2_STANDARD (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0650a68975f449ea938b41872005e11d79922393
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752182"
---
# <a name="mf_mt_mpeg2_standard-attribute"></a><span data-ttu-id="11d6d-103">\_ \_ Atributo padrão MF MT MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="11d6d-103">MF\_MT\_MPEG2\_STANDARD attribute</span></span>

<span data-ttu-id="11d6d-104">Para um tipo de mídia que descreve um fluxo de programa MPEG-2 (PS) ou um fluxo de transporte (TS), especifica o padrão usado para multiplexar o fluxo.</span><span class="sxs-lookup"><span data-stu-id="11d6d-104">For a media type that describes an MPEG-2 program stream (PS) or transport stream (TS), specifies the standard that is used to multiplex the stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="11d6d-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="11d6d-105">Data type</span></span>

<span data-ttu-id="11d6d-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="11d6d-106">**UINT32**</span></span>



| <span data-ttu-id="11d6d-107">Valor</span><span class="sxs-lookup"><span data-stu-id="11d6d-107">Value</span></span>                                                                                                | <span data-ttu-id="11d6d-108">Significado</span><span class="sxs-lookup"><span data-stu-id="11d6d-108">Meaning</span></span>                                                                    |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="11d6d-109"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="11d6d-109"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="11d6d-110">Standard MPEG-2 PS ou TS.</span><span class="sxs-lookup"><span data-stu-id="11d6d-110">Standard MPEG-2 PS or TS.</span></span><br/>                                       |
| <span id="1"></span><dl> <span data-ttu-id="11d6d-111"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="11d6d-111"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="11d6d-112">Padrão ATSC (Comitê de sistemas de televisão avançado).</span><span class="sxs-lookup"><span data-stu-id="11d6d-112">Advanced Television Systems Committee (ATSC) standard.</span></span><br/>          |
| <span id="2"></span><dl> <span data-ttu-id="11d6d-113"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="11d6d-113"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="11d6d-114">Padrão de transmissão de vídeo digital (DVB).</span><span class="sxs-lookup"><span data-stu-id="11d6d-114">Digital Video Broadcasting (DVB) standard.</span></span><br/>                      |
| <span id="3"></span><dl> <span data-ttu-id="11d6d-115"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="11d6d-115"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="11d6d-116">Associação de ARIB (setores de rádio e empresas) padrão.</span><span class="sxs-lookup"><span data-stu-id="11d6d-116">Association of Radio Industries and Businesses (ARIB) standard.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="11d6d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11d6d-117">Requirements</span></span>



| <span data-ttu-id="11d6d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="11d6d-118">Requirement</span></span> | <span data-ttu-id="11d6d-119">Valor</span><span class="sxs-lookup"><span data-stu-id="11d6d-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="11d6d-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="11d6d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="11d6d-121">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="11d6d-121">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="11d6d-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="11d6d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="11d6d-123">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="11d6d-123">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="11d6d-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="11d6d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="11d6d-125"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="11d6d-125"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11d6d-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="11d6d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11d6d-127">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="11d6d-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




