---
description: Especifica o idioma usado por um fluxo em um arquivo ASF (Advanced Systems Format).
ms.assetid: 834cac0a-0c84-49aa-baf2-32bae26e215b
title: Atributo MF_SD_ASF_EXTSTRMPROP_LANGUAGE_ID_INDEX (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2afcf2388d2c0641aede4ff0eaccac9178207fb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748469"
---
# <a name="mf_sd_asf_extstrmprop_language_id_index-attribute"></a><span data-ttu-id="c3a60-103">\_Atributo de índice de ID de linguagem MF SD \_ ASF \_ EXTSTRMPROP \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="c3a60-103">MF\_SD\_ASF\_EXTSTRMPROP\_LANGUAGE\_ID\_INDEX attribute</span></span>

<span data-ttu-id="c3a60-104">Especifica o idioma usado por um fluxo em um arquivo ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="c3a60-104">Specifies the language used by a stream in an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="c3a60-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="c3a60-105">Data type</span></span>

<span data-ttu-id="c3a60-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="c3a60-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="c3a60-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="c3a60-107">Remarks</span></span>

<span data-ttu-id="c3a60-108">Esse atributo se aplica a descritores de fluxo para conteúdo ASF.</span><span class="sxs-lookup"><span data-stu-id="c3a60-108">This attribute applies to stream descriptors for ASF content.</span></span> <span data-ttu-id="c3a60-109">O valor é um índice na lista de idiomas contida no atributo [**MF \_ PD \_ ASF \_ langlist**](mf-pd-asf-langlist-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="c3a60-109">The value is an index into the language list contained in the [**MF\_PD\_ASF\_LANGLIST**](mf-pd-asf-langlist-attribute.md) attribute.</span></span>

<span data-ttu-id="c3a60-110">Esse atributo corresponde ao campo de índice de ID de idioma do fluxo no objeto de propriedades do fluxo estendido.</span><span class="sxs-lookup"><span data-stu-id="c3a60-110">This attribute corresponds to the Stream Language ID Index field in the Extended Stream Properties object.</span></span> <span data-ttu-id="c3a60-111">Para obter mais informações, consulte a especificação do ASF.</span><span class="sxs-lookup"><span data-stu-id="c3a60-111">For more information, refer to the ASF specification.</span></span>

<span data-ttu-id="c3a60-112">O método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) gera esse atributo dos metadados do ASF.</span><span class="sxs-lookup"><span data-stu-id="c3a60-112">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span> <span data-ttu-id="c3a60-113">O aplicativo pode criar o descritor de fluxo para o fluxo do descritor de apresentação chamando [**IMFPresentationDescriptor:: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).</span><span class="sxs-lookup"><span data-stu-id="c3a60-113">The application can create the stream descriptor for the stream from the presentation descriptor by calling [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).</span></span>

<span data-ttu-id="c3a60-114">Você também pode obter a marca de idioma consultando o descritor de fluxo para o atributo de [**\_ \_ linguagem SD MF**](mf-sd-language-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="c3a60-114">You can also get the language tag by querying the stream descriptor for the [**MF\_SD\_LANGUAGE**](mf-sd-language-attribute.md) attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3a60-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3a60-115">Requirements</span></span>



| <span data-ttu-id="c3a60-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3a60-116">Requirement</span></span> | <span data-ttu-id="c3a60-117">Valor</span><span class="sxs-lookup"><span data-stu-id="c3a60-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3a60-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c3a60-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c3a60-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c3a60-119">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c3a60-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c3a60-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c3a60-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c3a60-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c3a60-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c3a60-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3a60-123"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3a60-123"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3a60-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="c3a60-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3a60-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c3a60-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c3a60-126">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="c3a60-126">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="c3a60-127">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="c3a60-127">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="c3a60-128">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="c3a60-128">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="c3a60-129">Atributos do descritor de fluxo</span><span class="sxs-lookup"><span data-stu-id="c3a60-129">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="c3a60-130">Objeto de cabeçalho ASF</span><span class="sxs-lookup"><span data-stu-id="c3a60-130">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




