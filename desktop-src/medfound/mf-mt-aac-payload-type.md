---
description: Especifica o tipo de carga de um fluxo AAC (codificação de áudio avançado).
ms.assetid: a032fcf4-2584-4047-adbd-d94d4fc4e841
title: Atributo MF_MT_AAC_PAYLOAD_TYPE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd3edba98bdac54b12fb6e3e44fb67373f7fce6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105772687"
---
# <a name="mf_mt_aac_payload_type-attribute"></a><span data-ttu-id="11d50-103">\_Atributo de \_ \_ tipo de conteúdo MF MT AAC \_</span><span class="sxs-lookup"><span data-stu-id="11d50-103">MF\_MT\_AAC\_PAYLOAD\_TYPE attribute</span></span>

<span data-ttu-id="11d50-104">Especifica o tipo de carga de um fluxo AAC (codificação de áudio avançado).</span><span class="sxs-lookup"><span data-stu-id="11d50-104">Specifies the payload type of an Advanced Audio Coding (AAC) stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="11d50-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="11d50-105">Data type</span></span>

<span data-ttu-id="11d50-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="11d50-106">**UINT32**</span></span>

<span data-ttu-id="11d50-107">Os valores a seguir são possíveis.</span><span class="sxs-lookup"><span data-stu-id="11d50-107">The following values are possible.</span></span>



| <span data-ttu-id="11d50-108">Valor</span><span class="sxs-lookup"><span data-stu-id="11d50-108">Value</span></span>                                                                        | <span data-ttu-id="11d50-109">Significado</span><span class="sxs-lookup"><span data-stu-id="11d50-109">Meaning</span></span>                                                                                                                           |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="11d50-110"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="11d50-110"><dt>0</dt></span></span> </dl> | <span data-ttu-id="11d50-111">O fluxo contém \_ apenas elementos de bloco de dados brutos \_ .</span><span class="sxs-lookup"><span data-stu-id="11d50-111">The stream contains raw\_data\_block elements only.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="11d50-112"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="11d50-112"><dt>1</dt></span></span> </dl> | <span data-ttu-id="11d50-113">Fluxo de transporte de dados de áudio (ADTS).</span><span class="sxs-lookup"><span data-stu-id="11d50-113">Audio Data Transport Stream (ADTS).</span></span> <span data-ttu-id="11d50-114">O fluxo contém uma \_ sequência ADTS, conforme definido por MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="11d50-114">The stream contains an adts\_sequence, as defined by MPEG-2.</span></span><br/>                       |
| <dl> <span data-ttu-id="11d50-115"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="11d50-115"><dt>2</dt></span></span> </dl> | <span data-ttu-id="11d50-116">Formato de intercâmbio de dados de áudio (ADIF).</span><span class="sxs-lookup"><span data-stu-id="11d50-116">Audio Data Interchange Format (ADIF).</span></span> <span data-ttu-id="11d50-117">O fluxo contém uma \_ sequência ADIF, conforme definido por MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="11d50-117">The stream contains an adif\_sequence, as defined by MPEG-2.</span></span><br/>                     |
| <dl> <span data-ttu-id="11d50-118"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="11d50-118"><dt>3</dt></span></span> </dl> | <span data-ttu-id="11d50-119">O fluxo contém um fluxo de transporte de áudio MPEG-4 com uma camada de sincronização (LOAS) e uma camada de Multiplex (LATM).</span><span class="sxs-lookup"><span data-stu-id="11d50-119">The stream contains an MPEG-4 audio transport stream with a synchronization layer (LOAS) and a multiplex layer (LATM).</span></span><br/> |



 

## <a name="getset"></a><span data-ttu-id="11d50-120">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="11d50-120">Get/set</span></span>

<span data-ttu-id="11d50-121">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="11d50-121">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="11d50-122">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="11d50-122">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="11d50-123">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="11d50-123">Applies To</span></span>

[<span data-ttu-id="11d50-124">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="11d50-124">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="11d50-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="11d50-125">Remarks</span></span>

<span data-ttu-id="11d50-126">O \_ tipo de conteúdo MF MT \_ AAC \_ \_ é opcional.</span><span class="sxs-lookup"><span data-stu-id="11d50-126">MF\_MT\_AAC\_PAYLOAD\_TYPE is optional.</span></span> <span data-ttu-id="11d50-127">Se esse atributo não for especificado, o valor padrão 0 será usado, o que especificará que o fluxo contém \_ apenas elementos de bloco de dados brutos \_ .</span><span class="sxs-lookup"><span data-stu-id="11d50-127">If this attribute is not specified, the default value 0 is used, which specifies the stream contains raw\_data\_block elements only.</span></span>

<span data-ttu-id="11d50-128">Aplica-se somente ao **MFAudioFormat \_ AAC**.</span><span class="sxs-lookup"><span data-stu-id="11d50-128">Applies only to **MFAudioFormat\_AAC**.</span></span>

<span data-ttu-id="11d50-129">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="11d50-129">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="11d50-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11d50-130">Requirements</span></span>



| <span data-ttu-id="11d50-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="11d50-131">Requirement</span></span> | <span data-ttu-id="11d50-132">Valor</span><span class="sxs-lookup"><span data-stu-id="11d50-132">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="11d50-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="11d50-133">Header</span></span><br/> | <dl> <span data-ttu-id="11d50-134"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="11d50-134"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11d50-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="11d50-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11d50-136">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="11d50-136">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="11d50-137">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="11d50-137">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




