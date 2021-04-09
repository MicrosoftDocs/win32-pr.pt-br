---
description: Especifica o idioma de um fluxo.
ms.assetid: b64a9554-a560-4212-8964-b68ebbadc046
title: Atributo MF_SD_LANGUAGE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad13ec4d7d17e715bd2583e499c686de26c7b9da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171028"
---
# <a name="mf_sd_language-attribute"></a><span data-ttu-id="b43c1-103">\_Atributo de \_ linguagem SD MF</span><span class="sxs-lookup"><span data-stu-id="b43c1-103">MF\_SD\_LANGUAGE attribute</span></span>

<span data-ttu-id="b43c1-104">Especifica o idioma de um fluxo.</span><span class="sxs-lookup"><span data-stu-id="b43c1-104">Specifies the language for a stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="b43c1-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="b43c1-105">Data type</span></span>

<span data-ttu-id="b43c1-106">Cadeia de caracteres largos</span><span class="sxs-lookup"><span data-stu-id="b43c1-106">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="b43c1-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="b43c1-107">Remarks</span></span>

<span data-ttu-id="b43c1-108">O valor desse atributo é uma marca de linguagem compatível com RFC 1766.</span><span class="sxs-lookup"><span data-stu-id="b43c1-108">The value of this attribute is an RFC 1766-compliant language tag.</span></span> <span data-ttu-id="b43c1-109">Esse atributo se aplica a descritores de fluxo.</span><span class="sxs-lookup"><span data-stu-id="b43c1-109">This attribute applies to stream descriptors.</span></span>

<span data-ttu-id="b43c1-110">Uma origem de mídia (ou qualquer objeto que cria um descritor de fluxo) pode definir esse atributo se o fluxo tiver um idioma especificado.</span><span class="sxs-lookup"><span data-stu-id="b43c1-110">A media source (or any object that creates a stream descriptor) can set this attribute if the stream has a specified language.</span></span> <span data-ttu-id="b43c1-111">Os aplicativos podem consultar esse atributo para obter o idioma.</span><span class="sxs-lookup"><span data-stu-id="b43c1-111">Applications can query this attribute to get the language.</span></span> <span data-ttu-id="b43c1-112">Se o atributo não estiver definido, o fluxo não terá um idioma especificado.</span><span class="sxs-lookup"><span data-stu-id="b43c1-112">If the attribute is not set, the stream does not have a specified language.</span></span>

<span data-ttu-id="b43c1-113">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="b43c1-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b43c1-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b43c1-114">Requirements</span></span>



| <span data-ttu-id="b43c1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b43c1-115">Requirement</span></span> | <span data-ttu-id="b43c1-116">Valor</span><span class="sxs-lookup"><span data-stu-id="b43c1-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b43c1-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b43c1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b43c1-118">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="b43c1-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="b43c1-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b43c1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b43c1-120">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="b43c1-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="b43c1-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b43c1-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b43c1-122"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b43c1-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b43c1-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="b43c1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b43c1-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b43c1-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b43c1-125">**IMFAttributes:: GetString**</span><span class="sxs-lookup"><span data-stu-id="b43c1-125">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="b43c1-126">**IMFAttributes:: SetString**</span><span class="sxs-lookup"><span data-stu-id="b43c1-126">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="b43c1-127">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="b43c1-127">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="b43c1-128">Atributos do descritor de fluxo</span><span class="sxs-lookup"><span data-stu-id="b43c1-128">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> </dl>

 

 




