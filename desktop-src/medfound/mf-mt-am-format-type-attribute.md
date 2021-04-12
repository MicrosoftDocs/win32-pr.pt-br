---
description: Contém um GUID de formato do DirectShow para um tipo de mídia.
ms.assetid: dc532791-39e1-4acb-9e62-21d8f25be870
title: Atributo MF_MT_AM_FORMAT_TYPE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18a8faf88128075e5c5b51c1b5ace39329d4e1fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296563"
---
# <a name="mf_mt_am_format_type-attribute"></a><span data-ttu-id="a3f08-103">\_Atributo de \_ \_ tipo de formato MF MT am \_</span><span class="sxs-lookup"><span data-stu-id="a3f08-103">MF\_MT\_AM\_FORMAT\_TYPE attribute</span></span>

<span data-ttu-id="a3f08-104">Contém um GUID de formato do DirectShow para um tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="a3f08-104">Contains a DirectShow format GUID for a media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="a3f08-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="a3f08-105">Data type</span></span>

<span data-ttu-id="a3f08-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="a3f08-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="a3f08-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="a3f08-107">Remarks</span></span>

<span data-ttu-id="a3f08-108">Esse atributo pode ser definido quando um tipo de mídia do DirectShow é convertido em um tipo de mídia Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="a3f08-108">This attribute might be set when a DirectShow media type is converted into a Media Foundation media type.</span></span> <span data-ttu-id="a3f08-109">O atributo indica o tipo de formato do DirectShow original.</span><span class="sxs-lookup"><span data-stu-id="a3f08-109">The attribute indicates the original DirectShow format type.</span></span> <span data-ttu-id="a3f08-110">O valor corresponde ao membro formatType da estrutura do [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="a3f08-110">The value corresponds to the formattype member of the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

<span data-ttu-id="a3f08-111">Para um formato de áudio, o atributo de [**\_ dados de \_ usuário \_ MF MT**](mf-mt-user-data-attribute.md) pode conter o bloco de formato original, se o tipo de formato do DirectShow não foi reconhecido.</span><span class="sxs-lookup"><span data-stu-id="a3f08-111">For an audio format, the [**MF\_MT\_USER\_DATA**](mf-mt-user-data-attribute.md) attribute might contain the original format block, if the DirectShow format type was not recognized.</span></span>

<span data-ttu-id="a3f08-112">Não defina esse atributo em um tipo de mídia, a menos que você esteja convertendo uma estrutura de formato do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="a3f08-112">Do not set this attribute on a media type unless you are converting a DirectShow format structure.</span></span>

<span data-ttu-id="a3f08-113">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="a3f08-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3f08-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3f08-114">Requirements</span></span>



| <span data-ttu-id="a3f08-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3f08-115">Requirement</span></span> | <span data-ttu-id="a3f08-116">Valor</span><span class="sxs-lookup"><span data-stu-id="a3f08-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a3f08-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a3f08-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a3f08-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a3f08-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a3f08-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a3f08-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a3f08-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a3f08-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a3f08-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a3f08-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3f08-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3f08-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3f08-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="a3f08-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3f08-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a3f08-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a3f08-125">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="a3f08-125">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="a3f08-126">Conversões de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="a3f08-126">Media Type Conversions</span></span>](media-type-conversions.md)
</dt> <dt>

[<span data-ttu-id="a3f08-127">Tipos de mídia</span><span class="sxs-lookup"><span data-stu-id="a3f08-127">Media Types</span></span>](media-types.md)
</dt> <dt>

[<span data-ttu-id="a3f08-128">**IMFAttributes:: GetGuid**</span><span class="sxs-lookup"><span data-stu-id="a3f08-128">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="a3f08-129">**IMFAttributes:: SetGUID**</span><span class="sxs-lookup"><span data-stu-id="a3f08-129">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="a3f08-130">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="a3f08-130">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="a3f08-131">**MFCreateMediaTypeFromRepresentation**</span><span class="sxs-lookup"><span data-stu-id="a3f08-131">**MFCreateMediaTypeFromRepresentation**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatypefromrepresentation)
</dt> </dl>

 

 
