---
description: Especifica o tipo MIME do conteúdo.
ms.assetid: bbcfb3e6-a86a-4621-b8d9-92ace60e8c10
title: Atributo MF_PD_MIME_TYPE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce1893253af139a73555d3a4fd483e9f59c5ae1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105769085"
---
# <a name="mf_pd_mime_type-attribute"></a><span data-ttu-id="8db0a-103">\_Atributo de \_ \_ tipo MIME do MF PD</span><span class="sxs-lookup"><span data-stu-id="8db0a-103">MF\_PD\_MIME\_TYPE attribute</span></span>

<span data-ttu-id="8db0a-104">Especifica o tipo MIME do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="8db0a-104">Specifies the MIME type of the content.</span></span>

## <a name="data-type"></a><span data-ttu-id="8db0a-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="8db0a-105">Data type</span></span>

<span data-ttu-id="8db0a-106">Cadeia de caracteres largos</span><span class="sxs-lookup"><span data-stu-id="8db0a-106">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="8db0a-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="8db0a-107">Remarks</span></span>

<span data-ttu-id="8db0a-108">Este atributo se aplica aos descritores de apresentação.</span><span class="sxs-lookup"><span data-stu-id="8db0a-108">This attribute applies to presentation descriptors.</span></span>

<span data-ttu-id="8db0a-109">O tipo MIME exposto por meio de [System. MIMEType](../properties/props-system-mimetype.md) para arquivos de mídia pode ter uma tendência de escolher tipos MIME adequados para a DLNA (rede de vida digital).</span><span class="sxs-lookup"><span data-stu-id="8db0a-109">The MIME type exposed through [System.MIMEType](../properties/props-system-mimetype.md) for media files may have a bias towards choosing MIME types suitable for Digital Living Network Alliance (DLNA).</span></span>

<span data-ttu-id="8db0a-110">O \_ tipo MIME do MF PD \_ \_ e o [System. MIMEType](../properties/props-system-mimetype.md) nem sempre podem corresponder.</span><span class="sxs-lookup"><span data-stu-id="8db0a-110">MF\_PD\_MIME\_TYPE and [System.MIMEType](../properties/props-system-mimetype.md) may not always match.</span></span>

<span data-ttu-id="8db0a-111">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="8db0a-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="8db0a-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8db0a-112">Requirements</span></span>



| <span data-ttu-id="8db0a-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="8db0a-113">Requirement</span></span> | <span data-ttu-id="8db0a-114">Valor</span><span class="sxs-lookup"><span data-stu-id="8db0a-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8db0a-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8db0a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="8db0a-116">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="8db0a-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="8db0a-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8db0a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="8db0a-118">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="8db0a-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="8db0a-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8db0a-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="8db0a-120"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8db0a-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8db0a-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="8db0a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8db0a-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8db0a-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="8db0a-123">**IMFAttributes:: GetString**</span><span class="sxs-lookup"><span data-stu-id="8db0a-123">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="8db0a-124">**IMFAttributes:: SetString**</span><span class="sxs-lookup"><span data-stu-id="8db0a-124">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="8db0a-125">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="8db0a-125">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="8db0a-126">Atributos do descritor de apresentação</span><span class="sxs-lookup"><span data-stu-id="8db0a-126">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 
