---
description: Especifica se um exemplo de mídia contém um quadro de vídeo 3D.
ms.assetid: 1B0B9DBD-80EB-4876-B2F2-BE419AC84265
title: Atributo MFSampleExtension_3DVideo (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e30ea247f6f12f05414df0ae4305ecaaa6e3e283
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105784511"
---
# <a name="mfsampleextension_3dvideo-attribute"></a><span data-ttu-id="8b746-103">\_Atributo MFSampleExtension 3DVideo</span><span class="sxs-lookup"><span data-stu-id="8b746-103">MFSampleExtension\_3DVideo attribute</span></span>

<span data-ttu-id="8b746-104">Especifica se um exemplo de mídia contém um quadro de vídeo 3D.</span><span class="sxs-lookup"><span data-stu-id="8b746-104">Specifies whether a media sample contains a 3D video frame.</span></span>

## <a name="data-type"></a><span data-ttu-id="8b746-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="8b746-105">Data type</span></span>

<span data-ttu-id="8b746-106">**Bool** armazenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="8b746-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="8b746-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="8b746-107">Remarks</span></span>

<span data-ttu-id="8b746-108">Se esse atributo for **true**, o exemplo de mídia conterá um quadro de vídeo com duas ou mais exibições estereoscópico.</span><span class="sxs-lookup"><span data-stu-id="8b746-108">If this attribute is **TRUE**, the media sample contains a video frame that has two or more stereoscopic views.</span></span> <span data-ttu-id="8b746-109">O valor padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="8b746-109">The default value is **FALSE**.</span></span>

<span data-ttu-id="8b746-110">Um componente que gera quadros de vídeo 3D deve definir esse atributo como **true** em cada amostra de mídia que contenha um quadro 3D.</span><span class="sxs-lookup"><span data-stu-id="8b746-110">A component that generates 3D video frames should set this attribute to **TRUE** on every media sample that contains a 3D frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b746-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b746-111">Requirements</span></span>



| <span data-ttu-id="8b746-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b746-112">Requirement</span></span> | <span data-ttu-id="8b746-113">Valor</span><span class="sxs-lookup"><span data-stu-id="8b746-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8b746-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8b746-114">Minimum supported client</span></span><br/> | <span data-ttu-id="8b746-115">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="8b746-115">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="8b746-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8b746-116">Minimum supported server</span></span><br/> | <span data-ttu-id="8b746-117">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="8b746-117">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="8b746-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8b746-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b746-119"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b746-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b746-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="8b746-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b746-121">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8b746-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="8b746-122">MFSampleExtension \_ 3DVideo \_ SampleFormat</span><span class="sxs-lookup"><span data-stu-id="8b746-122">MFSampleExtension\_3DVideo\_SampleFormat</span></span>](mfsampleextension-3dvideo-sampleformat.md)
</dt> </dl>

 

 




