---
description: Contém o valor de mérito de um codec de hardware.
ms.assetid: 1df40a42-4c02-473f-a87f-2ae2d42e4f4e
title: Atributo MFT_CODEC_MERIT_Attribute (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74745244824bc766d0f7c1e691cb5f176d1da6a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754895"
---
# <a name="mft_codec_merit_attribute-attribute"></a><span data-ttu-id="ea2ed-103">\_Atributo de \_ atributo mérito de codec de MFT \_</span><span class="sxs-lookup"><span data-stu-id="ea2ed-103">MFT\_CODEC\_MERIT\_Attribute attribute</span></span>

<span data-ttu-id="ea2ed-104">Contém o valor de mérito de um codec de hardware.</span><span class="sxs-lookup"><span data-stu-id="ea2ed-104">Contains the merit value of a hardware codec.</span></span>

## <a name="data-type"></a><span data-ttu-id="ea2ed-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="ea2ed-105">Data type</span></span>

<span data-ttu-id="ea2ed-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="ea2ed-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="ea2ed-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="ea2ed-107">Get/set</span></span>

<span data-ttu-id="ea2ed-108">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="ea2ed-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="ea2ed-109">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="ea2ed-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="ea2ed-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="ea2ed-110">Remarks</span></span>

<span data-ttu-id="ea2ed-111">Esse atributo é definido no objeto de ativação para uma Media Foundation transformação (MFT) que representa um codec de hardware.</span><span class="sxs-lookup"><span data-stu-id="ea2ed-111">This attribute is set on the activation object for a Media Foundation transform (MFT) that represents a hardware codec.</span></span> <span data-ttu-id="ea2ed-112">O valor do atributo é o valor de mérito do codec.</span><span class="sxs-lookup"><span data-stu-id="ea2ed-112">The value of the attribute is the codec's merit value.</span></span>

<span data-ttu-id="ea2ed-113">Esse atributo controla a ordem na qual a função [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) enumera codecs, se o sinalizador **\_ \_ \_ SORTANDFILTER do sinalizador de enumeração de MFT** estiver definido.</span><span class="sxs-lookup"><span data-stu-id="ea2ed-113">This attribute controls the order in which the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function enumerates codecs, if the **MFT\_ENUM\_FLAG\_SORTANDFILTER** flag is set.</span></span> <span data-ttu-id="ea2ed-114">MFTs com um valor de mérito aparece mais alto na lista que outros MFTs.</span><span class="sxs-lookup"><span data-stu-id="ea2ed-114">MFTs with a merit value appear higher in the list than other MFTs.</span></span>

<span data-ttu-id="ea2ed-115">Este atributo não contém um valor confiável.</span><span class="sxs-lookup"><span data-stu-id="ea2ed-115">This attribute does not contain a trusted value.</span></span> <span data-ttu-id="ea2ed-116">Para verificar o valor do mérito real do codec, chame a função [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) .</span><span class="sxs-lookup"><span data-stu-id="ea2ed-116">To verify the codec's actual merit value, call the [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) function.</span></span>

<span data-ttu-id="ea2ed-117">Se o valor do atributo de \_ atributo de mérito do codec MFT \_ \_ não corresponder ao valor de mérito recuperado por [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit), o método [**IMFActivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) falhará e retornará um **mérito de \_ codec MF e \_ inválido \_ \_**.</span><span class="sxs-lookup"><span data-stu-id="ea2ed-117">If the value of the MFT\_CODEC\_MERIT\_Attribute attribute does not match the merit value retrieved by [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit), the [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) method fails and returns **MF\_E\_INVALID\_CODEC\_MERIT**.</span></span>

<span data-ttu-id="ea2ed-118">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="ea2ed-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea2ed-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea2ed-119">Requirements</span></span>



| <span data-ttu-id="ea2ed-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea2ed-120">Requirement</span></span> | <span data-ttu-id="ea2ed-121">Valor</span><span class="sxs-lookup"><span data-stu-id="ea2ed-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea2ed-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ea2ed-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ea2ed-123">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="ea2ed-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="ea2ed-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ea2ed-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ea2ed-125">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="ea2ed-125">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="ea2ed-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ea2ed-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea2ed-127"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea2ed-127"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea2ed-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="ea2ed-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea2ed-129">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ea2ed-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ea2ed-130">Atributos de transformação</span><span class="sxs-lookup"><span data-stu-id="ea2ed-130">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




