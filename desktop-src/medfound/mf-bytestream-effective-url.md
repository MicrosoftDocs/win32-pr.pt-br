---
description: Obtém a URL efetiva de um fluxo de bytes.
ms.assetid: 0A83CFC0-7EAA-464B-BA39-50DF220AF683
title: Atributo MF_BYTESTREAM_EFFECTIVE_URL (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b95e01238f04c30f72d55f940b3f3105863247ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758080"
---
# <a name="mf_bytestream_effective_url-attribute"></a><span data-ttu-id="40636-103">Atributo de URL de bytes de MF em \_ \_ vigor \_</span><span class="sxs-lookup"><span data-stu-id="40636-103">MF\_BYTESTREAM\_EFFECTIVE\_URL attribute</span></span>

<span data-ttu-id="40636-104">Obtém a URL efetiva de um fluxo de bytes.</span><span class="sxs-lookup"><span data-stu-id="40636-104">Gets the effective URL of a byte stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="40636-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="40636-105">Data type</span></span>

## <a name="getset"></a><span data-ttu-id="40636-106">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="40636-106">Get/set</span></span>

<span data-ttu-id="40636-107">Para obter esse atributo, chame [**IMFAttributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="40636-107">To get this attribute, call [**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="40636-108">Para definir esse atributo, chame [**IMFAttributes:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="40636-108">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="applies-to"></a><span data-ttu-id="40636-109">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="40636-109">Applies to</span></span>

[<span data-ttu-id="40636-110">**IMFByteStream**</span><span class="sxs-lookup"><span data-stu-id="40636-110">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)

## <a name="remarks"></a><span data-ttu-id="40636-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="40636-111">Remarks</span></span>

<span data-ttu-id="40636-112">A URL efetiva pode diferir da URL original se a URL original contiver informações adicionais, como cadeias de caracteres de pesquisa ou âncoras, ou se a solicitação tiver sido redirecionada.</span><span class="sxs-lookup"><span data-stu-id="40636-112">The effective URL can differ from the original URL if the original URL contains any extra information, such as search strings or anchors, or if the request was redirected.</span></span>

## <a name="requirements"></a><span data-ttu-id="40636-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40636-113">Requirements</span></span>



| <span data-ttu-id="40636-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="40636-114">Requirement</span></span> | <span data-ttu-id="40636-115">Valor</span><span class="sxs-lookup"><span data-stu-id="40636-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="40636-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="40636-116">Minimum supported client</span></span><br/> | <span data-ttu-id="40636-117">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="40636-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                      |
| <span data-ttu-id="40636-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="40636-118">Minimum supported server</span></span><br/> | <span data-ttu-id="40636-119">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="40636-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                            |
| <span data-ttu-id="40636-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="40636-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="40636-121"><dt>Mfobjects. h</dt></span><span class="sxs-lookup"><span data-stu-id="40636-121"><dt>Mfobjects.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40636-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="40636-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40636-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="40636-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="40636-124">Atributos de fluxo de bytes</span><span class="sxs-lookup"><span data-stu-id="40636-124">Byte Stream Attributes</span></span>](byte-stream-attributes.md)
</dt> <dt>

[<span data-ttu-id="40636-125">**IMFByteStream**</span><span class="sxs-lookup"><span data-stu-id="40636-125">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 




