---
description: Especifica o formato de saída preferencial para um codificador.
ms.assetid: 36a09696-3fe7-41a0-93f1-712220f88b04
title: Atributo MFT_PREFERRED_OUTPUTTYPE_Attribute (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13cd079bee65f5324987d9b38dca845ec5b85f83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827808"
---
# <a name="mft_preferred_outputtype_attribute-attribute"></a><span data-ttu-id="338a2-103">\_Atributo de \_ atributo OutputType de MFT preferencial \_</span><span class="sxs-lookup"><span data-stu-id="338a2-103">MFT\_PREFERRED\_OUTPUTTYPE\_Attribute attribute</span></span>

<span data-ttu-id="338a2-104">Especifica o formato de saída preferencial para um codificador.</span><span class="sxs-lookup"><span data-stu-id="338a2-104">Specifies the preferred output format for an encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="338a2-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="338a2-105">Data type</span></span>

<span data-ttu-id="338a2-106">**[](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) IMFAttributes \** _ armazenado como _*IUnknown \*\*_</span><span class="sxs-lookup"><span data-stu-id="338a2-106">**[**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)\** _ stored as _*IUnknown\*\*_</span></span>

## <a name="getset"></a><span data-ttu-id="338a2-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="338a2-107">Get/set</span></span>

<span data-ttu-id="338a2-108">Para obter esse atributo, chame [_ *IMFAttributes:: getunknown* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="338a2-108">To get this attribute, call [_ *IMFAttributes::GetUnknown*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="338a2-109">Para definir esse atributo, chame [**IMFAttributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="338a2-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="applies-to"></a><span data-ttu-id="338a2-110">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="338a2-110">Applies to</span></span>

[<span data-ttu-id="338a2-111">**IMFActivate**</span><span class="sxs-lookup"><span data-stu-id="338a2-111">**IMFActivate**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)

## <a name="remarks"></a><span data-ttu-id="338a2-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="338a2-112">Remarks</span></span>

<span data-ttu-id="338a2-113">Esse atributo pode ser definido no objeto de ativação retornado pela função [**MFCreateTransformActivate**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate) .</span><span class="sxs-lookup"><span data-stu-id="338a2-113">This attribute can be set on the activation object returned by the [**MFCreateTransformActivate**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate) function.</span></span> <span data-ttu-id="338a2-114">O atributo se aplica somente quando o objeto de ativação é configurado para criar um codificador.</span><span class="sxs-lookup"><span data-stu-id="338a2-114">The attribute applies only when the activation object is configured to create an encoder.</span></span> <span data-ttu-id="338a2-115">O valor do atributo é um tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="338a2-115">The value of the attribute is a media type.</span></span> <span data-ttu-id="338a2-116">O objeto de ativação define esse tipo de saída no codificador.</span><span class="sxs-lookup"><span data-stu-id="338a2-116">The activation object sets this output type on the encoder.</span></span>

<span data-ttu-id="338a2-117">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="338a2-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="338a2-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="338a2-118">Requirements</span></span>



| <span data-ttu-id="338a2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="338a2-119">Requirement</span></span> | <span data-ttu-id="338a2-120">Valor</span><span class="sxs-lookup"><span data-stu-id="338a2-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="338a2-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="338a2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="338a2-122">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="338a2-122">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="338a2-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="338a2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="338a2-124">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="338a2-124">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="338a2-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="338a2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="338a2-126"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="338a2-126"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="338a2-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="338a2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="338a2-128">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="338a2-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="338a2-129">**MFCreateTransformActivate**</span><span class="sxs-lookup"><span data-stu-id="338a2-129">**MFCreateTransformActivate**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate)
</dt> <dt>

[<span data-ttu-id="338a2-130">Atributos de transformação</span><span class="sxs-lookup"><span data-stu-id="338a2-130">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




