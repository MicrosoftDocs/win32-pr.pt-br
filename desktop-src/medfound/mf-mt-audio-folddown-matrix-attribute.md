---
description: Especifica como um decodificador de áudio deve transformar áudio de multicanal em saída de estéreo. Esse processo também é chamado de dobra.
ms.assetid: 6dfe2b97-1ebc-4954-b478-85b3bbba89e3
title: Atributo MF_MT_AUDIO_FOLDDOWN_MATRIX (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10bb8aa00835ab31f6c05eaa9a1d0e5d9d126b41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760364"
---
# <a name="mf_mt_audio_folddown_matrix-attribute"></a><span data-ttu-id="2f570-104">\_Atributo de \_ \_ matriz FOLDDOWN de áudio MF MT \_</span><span class="sxs-lookup"><span data-stu-id="2f570-104">MF\_MT\_AUDIO\_FOLDDOWN\_MATRIX attribute</span></span>

<span data-ttu-id="2f570-105">Especifica como um decodificador de áudio deve transformar áudio de multicanal em saída de estéreo.</span><span class="sxs-lookup"><span data-stu-id="2f570-105">Specifies how an audio decoder should transform multichannel audio to stereo output.</span></span> <span data-ttu-id="2f570-106">Esse processo também é chamado *de dobra*.</span><span class="sxs-lookup"><span data-stu-id="2f570-106">This process is also called *fold-down*.</span></span>

## <a name="data-type"></a><span data-ttu-id="2f570-107">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="2f570-107">Data type</span></span>

<span data-ttu-id="2f570-108">Matriz de bytes</span><span class="sxs-lookup"><span data-stu-id="2f570-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="2f570-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="2f570-109">Remarks</span></span>

<span data-ttu-id="2f570-110">Esse atributo se aplica a tipos de mídia de áudio.</span><span class="sxs-lookup"><span data-stu-id="2f570-110">This attribute applies to audio media types.</span></span>

<span data-ttu-id="2f570-111">O valor desse atributo é uma estrutura [**de \_ matriz MFFOLDDOWN**](/windows/desktop/api/mfapi/ns-mfapi-mffolddown_matrix) .</span><span class="sxs-lookup"><span data-stu-id="2f570-111">The value of this attribute is an [**MFFOLDDOWN\_MATRIX**](/windows/desktop/api/mfapi/ns-mfapi-mffolddown_matrix) structure.</span></span>

<span data-ttu-id="2f570-112">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="2f570-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f570-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f570-113">Requirements</span></span>



| <span data-ttu-id="2f570-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f570-114">Requirement</span></span> | <span data-ttu-id="2f570-115">Valor</span><span class="sxs-lookup"><span data-stu-id="2f570-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2f570-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2f570-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2f570-117">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="2f570-117">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="2f570-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2f570-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2f570-119">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="2f570-119">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="2f570-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2f570-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f570-121"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f570-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f570-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="2f570-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f570-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2f570-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="2f570-124">**IMFAttributes:: getBlob**</span><span class="sxs-lookup"><span data-stu-id="2f570-124">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="2f570-125">**IMFAttributes:: setBlob**</span><span class="sxs-lookup"><span data-stu-id="2f570-125">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="2f570-126">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="2f570-126">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="2f570-127">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="2f570-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




