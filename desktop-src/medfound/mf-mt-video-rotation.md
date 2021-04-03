---
description: Especifica a rotação de um quadro de vídeo na direção do sentido anti-horário.
ms.assetid: 7C0911A6-6D7C-4510-891F-A6F56CE1EC2B
title: Atributo MF_MT_VIDEO_ROTATION (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f46a67c9861b8094e909e5c6fd7bc82e46166dc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837348"
---
# <a name="mf_mt_video_rotation-attribute"></a><span data-ttu-id="c97ee-103">\_Atributo de \_ rotação de vídeo MF MT \_</span><span class="sxs-lookup"><span data-stu-id="c97ee-103">MF\_MT\_VIDEO\_ROTATION attribute</span></span>

<span data-ttu-id="c97ee-104">Especifica a rotação de um quadro de vídeo na direção do sentido anti-horário.</span><span class="sxs-lookup"><span data-stu-id="c97ee-104">Specifies the rotation of a video frame in the counter-clockwise direction.</span></span>

## <a name="data-type"></a><span data-ttu-id="c97ee-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="c97ee-105">Data type</span></span>

<span data-ttu-id="c97ee-106">**MFVideoRotationFormat** armazenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="c97ee-106">**MFVideoRotationFormat** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="c97ee-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="c97ee-107">Remarks</span></span>

<span data-ttu-id="c97ee-108">O vídeo de um dispositivo portátil, como um telefone celular, geralmente é girado por 90, 180 ou 270 graus.</span><span class="sxs-lookup"><span data-stu-id="c97ee-108">Video from a handheld device, such as a mobile phone, is often rotated by 90, 180, or 270 degrees.</span></span> <span data-ttu-id="c97ee-109">Se a câmera armazenar a orientação como metadados no arquivo de vídeo, a imagem poderá ser ajustada no momento da reprodução.</span><span class="sxs-lookup"><span data-stu-id="c97ee-109">If the camera stores the orientation as metadata in the video file, the image can be adjusted at the time of playback.</span></span>

<span data-ttu-id="c97ee-110">Se esse atributo estiver definido como **MFVideoRotationFormat \_ 90**, isso significa que o conteúdo foi girado 90 graus na direção do sentido anti-horário.</span><span class="sxs-lookup"><span data-stu-id="c97ee-110">If this attribute set to **MFVideoRotationFormat\_90**, it means that the content has been rotated 90 degrees in the counter-clockwise direction.</span></span> <span data-ttu-id="c97ee-111">Se o conteúdo foi girado 90 graus na direção do sentido horário, o valor do atributo seria **MFVideoRotationFormat \_ 270**.</span><span class="sxs-lookup"><span data-stu-id="c97ee-111">If the content was rotated 90 degrees in the clockwise direction, the attribute value would be **MFVideoRotationFormat\_270**.</span></span>

<span data-ttu-id="c97ee-112">Os valores com suporte para esse atributo são enumerados em [**MFVideoRotationFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideorotationformat).</span><span class="sxs-lookup"><span data-stu-id="c97ee-112">The supported values for this attribute are enumerated in [**MFVideoRotationFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideorotationformat).</span></span>

<span data-ttu-id="c97ee-113">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="c97ee-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="c97ee-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c97ee-114">Requirements</span></span>



| <span data-ttu-id="c97ee-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c97ee-115">Requirement</span></span> | <span data-ttu-id="c97ee-116">Valor</span><span class="sxs-lookup"><span data-stu-id="c97ee-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c97ee-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c97ee-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c97ee-118">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c97ee-118">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="c97ee-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c97ee-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c97ee-120">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c97ee-120">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="c97ee-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c97ee-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c97ee-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c97ee-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c97ee-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="c97ee-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c97ee-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c97ee-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c97ee-125">Tipos de mídia</span><span class="sxs-lookup"><span data-stu-id="c97ee-125">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 




