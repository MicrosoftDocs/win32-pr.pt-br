---
description: Contém o carimbo de data/hora de decodificação (DTS) para o exemplo.
ms.assetid: 4E0B8266-FF48-49A1-AB7B-A47C4F96AECD
title: Atributo MFSampleExtension_DecodeTimestamp (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9676b295eb16e7cb2bb607ef4a5074d24b276d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781111"
---
# <a name="mfsampleextension_decodetimestamp-attribute"></a><span data-ttu-id="e8cab-103">\_Atributo MFSampleExtension DecodeTimestamp</span><span class="sxs-lookup"><span data-stu-id="e8cab-103">MFSampleExtension\_DecodeTimestamp attribute</span></span>

<span data-ttu-id="e8cab-104">Contém o carimbo de data/hora de decodificação (DTS) para o exemplo.</span><span class="sxs-lookup"><span data-stu-id="e8cab-104">Contains the decode time stamp (DTS) for the sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="e8cab-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="e8cab-105">Data type</span></span>

<span data-ttu-id="e8cab-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="e8cab-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="e8cab-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="e8cab-107">Remarks</span></span>

<span data-ttu-id="e8cab-108">O valor do atributo é o DTS em unidades de 100 nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="e8cab-108">The value of the attribute is the DTS in 100-nanosecond units.</span></span> <span data-ttu-id="e8cab-109">O DTS é definido em alguns padrões de codificação, incluindo MPEG.</span><span class="sxs-lookup"><span data-stu-id="e8cab-109">The DTS is defined in some encoding standards, including MPEG.</span></span> <span data-ttu-id="e8cab-110">O DTS especifica quando a imagem codificada deve ser decodificada.</span><span class="sxs-lookup"><span data-stu-id="e8cab-110">The DTS specifies when the encoded picture should be decoded.</span></span> <span data-ttu-id="e8cab-111">Se o vídeo codificado contiver quadros B, o DTS poderá ser diferente do horário da apresentação, porque as imagens B aparecem fora de ordem temporal no fragmentado.</span><span class="sxs-lookup"><span data-stu-id="e8cab-111">If the encoded video contains B frames, the DTS can differ from the presentation time, because B pictures appear out of temporal order in the bitstream.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8cab-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8cab-112">Requirements</span></span>



| <span data-ttu-id="e8cab-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8cab-113">Requirement</span></span> | <span data-ttu-id="e8cab-114">Valor</span><span class="sxs-lookup"><span data-stu-id="e8cab-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e8cab-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e8cab-115">Minimum supported client</span></span><br/> | <span data-ttu-id="e8cab-116">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="e8cab-116">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="e8cab-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e8cab-117">Minimum supported server</span></span><br/> | <span data-ttu-id="e8cab-118">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="e8cab-118">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="e8cab-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e8cab-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8cab-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8cab-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8cab-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="e8cab-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8cab-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e8cab-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e8cab-123">Atributos de exemplo</span><span class="sxs-lookup"><span data-stu-id="e8cab-123">Sample Attributes</span></span>](sample-attributes.md)
</dt> </dl>

 

 




