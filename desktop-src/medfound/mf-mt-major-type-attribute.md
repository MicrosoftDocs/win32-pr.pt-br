---
description: GUID de tipo principal para um tipo de mídia.
ms.assetid: b88b5fcf-8025-4638-930d-9fc5cf0ec8a3
title: Atributo MF_MT_MAJOR_TYPE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98c4cc02df4f89e261605c91b71ac1c80ba38b9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761535"
---
# <a name="mf_mt_major_type-attribute"></a><span data-ttu-id="dd929-103">\_Atributo de \_ tipo principal MF MT \_</span><span class="sxs-lookup"><span data-stu-id="dd929-103">MF\_MT\_MAJOR\_TYPE attribute</span></span>

<span data-ttu-id="dd929-104">GUID de tipo principal para um tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="dd929-104">Major type GUID for a media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="dd929-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="dd929-105">Data type</span></span>

<span data-ttu-id="dd929-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="dd929-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="dd929-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="dd929-107">Remarks</span></span>

<span data-ttu-id="dd929-108">O tipo principal define a categoria geral dos dados de mídia.</span><span class="sxs-lookup"><span data-stu-id="dd929-108">The major type defines the overall category of the media data.</span></span> <span data-ttu-id="dd929-109">Os principais tipos incluem vídeo, áudio, script e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="dd929-109">Major types include video, audio, script, and so forth.</span></span> <span data-ttu-id="dd929-110">Para obter uma lista de valores possíveis, consulte [tipos de mídia principais](media-type-guids.md).</span><span class="sxs-lookup"><span data-stu-id="dd929-110">For a list of possible values, see [Major Media Types](media-type-guids.md).</span></span>

<span data-ttu-id="dd929-111">Uma maneira alternativa de recuperar esse atributo é chamar [**IMFMediaType:: Getmajortype**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype).</span><span class="sxs-lookup"><span data-stu-id="dd929-111">An alternate way to retrieve this attribute is to call [**IMFMediaType::GetMajorType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype).</span></span>

<span data-ttu-id="dd929-112">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="dd929-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd929-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd929-113">Requirements</span></span>



| <span data-ttu-id="dd929-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd929-114">Requirement</span></span> | <span data-ttu-id="dd929-115">Valor</span><span class="sxs-lookup"><span data-stu-id="dd929-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dd929-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dd929-116">Minimum supported client</span></span><br/> | <span data-ttu-id="dd929-117">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="dd929-117">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="dd929-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dd929-118">Minimum supported server</span></span><br/> | <span data-ttu-id="dd929-119">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="dd929-119">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="dd929-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dd929-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd929-121"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd929-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd929-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="dd929-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd929-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="dd929-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="dd929-124">**IMFAttributes:: GetGuid**</span><span class="sxs-lookup"><span data-stu-id="dd929-124">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="dd929-125">**IMFAttributes:: SetGUID**</span><span class="sxs-lookup"><span data-stu-id="dd929-125">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="dd929-126">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="dd929-126">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="dd929-127">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="dd929-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




