---
description: 'Contém um ponteiro para o token que foi fornecido ao método IMFMediaStream:: RequestSample.'
ms.assetid: 9403bb15-e912-4aa3-9af1-fef4a4f9b242
title: Atributo MFSampleExtension_Token (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d17331ad098f80c2676e9d057e1688a776cee305
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105808351"
---
# <a name="mfsampleextension_token-attribute"></a><span data-ttu-id="b7cfa-103">\_Atributo de token MFSampleExtension</span><span class="sxs-lookup"><span data-stu-id="b7cfa-103">MFSampleExtension\_Token attribute</span></span>

<span data-ttu-id="b7cfa-104">Contém um ponteiro para o token que foi fornecido ao método [**IMFMediaStream:: RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) .</span><span class="sxs-lookup"><span data-stu-id="b7cfa-104">Contains a pointer to the token that was provided to the [**IMFMediaStream::RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) method.</span></span>

## <a name="data-type"></a><span data-ttu-id="b7cfa-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="b7cfa-105">Data type</span></span>

<span data-ttu-id="b7cfa-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="b7cfa-106">\**IUnknown\** _</span></span>

## <a name="getset"></a><span data-ttu-id="b7cfa-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="b7cfa-107">Get/set</span></span>

<span data-ttu-id="b7cfa-108">Para obter esse atributo, chame [_ *IMFAttributes:: getunknown* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="b7cfa-108">To get this attribute, call [_ *IMFAttributes::GetUnknown*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="b7cfa-109">Para definir esse atributo, chame [**IMFAttributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="b7cfa-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="applies-to"></a><span data-ttu-id="b7cfa-110">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="b7cfa-110">Applies to</span></span>

[<span data-ttu-id="b7cfa-111">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="b7cfa-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="b7cfa-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="b7cfa-112">Remarks</span></span>

<span data-ttu-id="b7cfa-113">Esse atributo se aplica a exemplos de mídia.</span><span class="sxs-lookup"><span data-stu-id="b7cfa-113">This attribute applies to media samples.</span></span> <span data-ttu-id="b7cfa-114">O valor do atributo é o ponteiro **IUnknown** que é passado para o parâmetro *PToken* do método [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) .</span><span class="sxs-lookup"><span data-stu-id="b7cfa-114">The value of the attribute is the **IUnknown** pointer that is passed to the *pToken* parameter of the [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) method.</span></span> <span data-ttu-id="b7cfa-115">O chamador usa esse atributo para acompanhar o status da solicitação.</span><span class="sxs-lookup"><span data-stu-id="b7cfa-115">The caller uses this attribute to track the status of the request.</span></span>

<span data-ttu-id="b7cfa-116">Se você estiver escrevendo uma fonte de mídia personalizada, defina esse atributo no exemplo quando o fluxo de mídia fornecer um exemplo em resposta ao método [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) , a menos que o valor de *pToken* seja **nulo**.</span><span class="sxs-lookup"><span data-stu-id="b7cfa-116">If you are writing a custom media source, set this attribute on the sample when the media stream delivers a sample in response to the [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) method, unless the value of *pToken* is **NULL**.</span></span>

<span data-ttu-id="b7cfa-117">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="b7cfa-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7cfa-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7cfa-118">Requirements</span></span>



| <span data-ttu-id="b7cfa-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7cfa-119">Requirement</span></span> | <span data-ttu-id="b7cfa-120">Valor</span><span class="sxs-lookup"><span data-stu-id="b7cfa-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b7cfa-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7cfa-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b7cfa-122">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="b7cfa-122">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="b7cfa-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7cfa-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b7cfa-124">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="b7cfa-124">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="b7cfa-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b7cfa-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7cfa-126"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7cfa-126"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7cfa-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="b7cfa-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7cfa-128">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b7cfa-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b7cfa-129">Atributos de exemplo</span><span class="sxs-lookup"><span data-stu-id="b7cfa-129">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="b7cfa-130">Amostras de mídia</span><span class="sxs-lookup"><span data-stu-id="b7cfa-130">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 




