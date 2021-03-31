---
description: Contém a caixa de descrição de exemplo para um arquivo MP4 ou 3GP.
ms.assetid: ea157988-bd15-465c-bd6a-6d33cc1a0323
title: Atributo MF_MT_MPEG4_SAMPLE_DESCRIPTION (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4620ae0b50a2c6f2dae7663aab0c49f13bc5a162
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829602"
---
# <a name="mf_mt_mpeg4_sample_description-attribute"></a><span data-ttu-id="c24a5-103">Atributo de descrição de exemplo do MF \_ MT \_ MPEG4 \_ \_</span><span class="sxs-lookup"><span data-stu-id="c24a5-103">MF\_MT\_MPEG4\_SAMPLE\_DESCRIPTION attribute</span></span>

<span data-ttu-id="c24a5-104">Contém a caixa de descrição de exemplo para um arquivo MP4 ou 3GP.</span><span class="sxs-lookup"><span data-stu-id="c24a5-104">Contains the sample description box for an MP4 or 3GP file.</span></span>

## <a name="data-type"></a><span data-ttu-id="c24a5-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="c24a5-105">Data type</span></span>

<span data-ttu-id="c24a5-106">**MINUCIOSA\[\]**</span><span class="sxs-lookup"><span data-stu-id="c24a5-106">**BYTE\[\]**</span></span>

## <a name="getset"></a><span data-ttu-id="c24a5-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="c24a5-107">Get/set</span></span>

<span data-ttu-id="c24a5-108">Para obter esse atributo, chame [**IMFAttributes:: getBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span><span class="sxs-lookup"><span data-stu-id="c24a5-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="c24a5-109">Para definir esse atributo, chame [**IMFAttributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span><span class="sxs-lookup"><span data-stu-id="c24a5-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="applies-to"></a><span data-ttu-id="c24a5-110">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="c24a5-110">Applies to</span></span>

[<span data-ttu-id="c24a5-111">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="c24a5-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="c24a5-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="c24a5-112">Remarks</span></span>

<span data-ttu-id="c24a5-113">A caixa Descrição de exemplo descreve a codificação usada para um fluxo no arquivo.</span><span class="sxs-lookup"><span data-stu-id="c24a5-113">The sample description box describes the encoding used for a stream in the file.</span></span>

<span data-ttu-id="c24a5-114">A fonte de arquivos MPEG-4 define esse atributo no tipo de mídia para cada fluxo.</span><span class="sxs-lookup"><span data-stu-id="c24a5-114">The MPEG-4 file source sets this attribute on the media type for each stream.</span></span> <span data-ttu-id="c24a5-115">O valor do atributo são os dados brutos na caixa Descrição de exemplo.</span><span class="sxs-lookup"><span data-stu-id="c24a5-115">The value of the attribute is the raw data in the sample description box.</span></span> <span data-ttu-id="c24a5-116">Se a origem do arquivo MPEG-4 puder analisar a descrição do exemplo, ela também adicionará os detalhes do formato ao tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="c24a5-116">If the MPEG-4 file source can parse the sample description, it also adds the format details to the media type.</span></span> <span data-ttu-id="c24a5-117">Caso contrário, o aplicativo ou o decodificador deve analisar a descrição de exemplo do atributo de descrição de exemplo do MF \_ MT \_ MPEG4 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="c24a5-117">Otherwise, the application or the decoder must parse the sample description from the MF\_MT\_MPEG4\_SAMPLE\_DESCRIPTION attribute.</span></span>

<span data-ttu-id="c24a5-118">Ao definir esse atributo no coletor MPEG-4 através do método [**IMFMediaTypeHandler:: SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) , os dados do atributo exemplo de descrição de MPEG4 do MF \_ MT \_ \_ \_ não devem ser alterados depois que um ou mais exemplos forem enviados para o coletor na interface [**IMFStreamSink::P rocesssample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample) do fluxo correspondente.</span><span class="sxs-lookup"><span data-stu-id="c24a5-118">When setting this attribute on MPEG-4 sink through [**IMFMediaTypeHandler::SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) method, the data for the attribute MF\_MT\_MPEG4\_SAMPLE\_DESCRIPTION should not change after one or more samples have been sent to the sink on the corresponding stream's [**IMFStreamSink::ProcessSample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample) interface.</span></span>

<span data-ttu-id="c24a5-119">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="c24a5-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="c24a5-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c24a5-120">Requirements</span></span>



| <span data-ttu-id="c24a5-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c24a5-121">Requirement</span></span> | <span data-ttu-id="c24a5-122">Valor</span><span class="sxs-lookup"><span data-stu-id="c24a5-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c24a5-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c24a5-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c24a5-124">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c24a5-124">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="c24a5-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c24a5-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c24a5-126">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="c24a5-126">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="c24a5-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c24a5-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c24a5-128"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c24a5-128"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c24a5-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="c24a5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c24a5-130">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c24a5-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c24a5-131">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="c24a5-131">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




