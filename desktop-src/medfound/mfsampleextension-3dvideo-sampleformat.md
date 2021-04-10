---
description: Especifica como um quadro de vídeo 3D é armazenado em um exemplo de mídia.
ms.assetid: 1B996B22-C76B-47E5-8937-1E5E672E32EC
title: Atributo MFSampleExtension_3DVideo_SampleFormat (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14829c879c151149edc48bf1635b3a5591ddeac5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091360"
---
# <a name="mfsampleextension_3dvideo_sampleformat-attribute"></a><span data-ttu-id="fb4b2-103">\_Atributo MFSampleExtension 3DVideo \_ SampleFormat</span><span class="sxs-lookup"><span data-stu-id="fb4b2-103">MFSampleExtension\_3DVideo\_SampleFormat attribute</span></span>

<span data-ttu-id="fb4b2-104">Especifica como um quadro de vídeo 3D é armazenado em um exemplo de mídia.</span><span class="sxs-lookup"><span data-stu-id="fb4b2-104">Specifies how a 3D video frame is stored in a media sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="fb4b2-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="fb4b2-105">Data type</span></span>

<span data-ttu-id="fb4b2-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="fb4b2-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="fb4b2-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="fb4b2-107">Remarks</span></span>

<span data-ttu-id="fb4b2-108">O valor desse atributo é um membro da enumeração [**MFVideo3DSampleFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideo3dsampleformat) .</span><span class="sxs-lookup"><span data-stu-id="fb4b2-108">The value of this attribute is a member of the [**MFVideo3DSampleFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideo3dsampleformat) enumeration.</span></span>

<span data-ttu-id="fb4b2-109">Um componente que gera quadros de vídeo 3D deve definir esse atributo como **true** em cada amostra de mídia que contenha um quadro 3D.</span><span class="sxs-lookup"><span data-stu-id="fb4b2-109">A component that generates 3D video frames should set this attribute to **TRUE** on every media sample that contains a 3D frame.</span></span> <span data-ttu-id="fb4b2-110">O atributo será ignorado se o atributo [MFSampleExtension \_ 3DVideo](mfsampleextension-3dvideo.md) for **false** ou não estiver definido.</span><span class="sxs-lookup"><span data-stu-id="fb4b2-110">The attribute is ignored if the [MFSampleExtension\_3DVideo](mfsampleextension-3dvideo.md) attribute is **FALSE** or not set.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb4b2-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb4b2-111">Requirements</span></span>



| <span data-ttu-id="fb4b2-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb4b2-112">Requirement</span></span> | <span data-ttu-id="fb4b2-113">Valor</span><span class="sxs-lookup"><span data-stu-id="fb4b2-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fb4b2-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fb4b2-114">Minimum supported client</span></span><br/> | <span data-ttu-id="fb4b2-115">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="fb4b2-115">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="fb4b2-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fb4b2-116">Minimum supported server</span></span><br/> | <span data-ttu-id="fb4b2-117">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="fb4b2-117">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="fb4b2-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fb4b2-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb4b2-119"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb4b2-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb4b2-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="fb4b2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb4b2-121">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fb4b2-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="fb4b2-122">MFSampleExtension \_ 3DVideo</span><span class="sxs-lookup"><span data-stu-id="fb4b2-122">MFSampleExtension\_3DVideo</span></span>](mfsampleextension-3dvideo.md)
</dt> </dl>

 

 




