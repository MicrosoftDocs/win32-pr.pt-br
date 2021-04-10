---
description: Habilita ou desabilita conversões de formato pelo leitor de fonte ou gravador de coletor.
ms.assetid: 282b70c3-c81c-47dd-bfa2-7e77138ccb91
title: Atributo MF_READWRITE_DISABLE_CONVERTERS (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8532c45ca3aeb272fa6b6ef422e0d82e40bd3e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171726"
---
# <a name="mf_readwrite_disable_converters-attribute"></a><span data-ttu-id="76fca-103">\_Atributo de \_ conversores do MF ReadWrite Disable \_</span><span class="sxs-lookup"><span data-stu-id="76fca-103">MF\_READWRITE\_DISABLE\_CONVERTERS attribute</span></span>

<span data-ttu-id="76fca-104">Habilita ou desabilita conversões de formato pelo leitor de fonte ou gravador de coletor.</span><span class="sxs-lookup"><span data-stu-id="76fca-104">Enables or disables format conversions by the source reader or sink writer.</span></span>

## <a name="data-type"></a><span data-ttu-id="76fca-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="76fca-105">Data type</span></span>

<span data-ttu-id="76fca-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="76fca-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="76fca-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="76fca-107">Get/set</span></span>

<span data-ttu-id="76fca-108">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="76fca-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="76fca-109">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="76fca-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="76fca-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="76fca-110">Remarks</span></span>

<span data-ttu-id="76fca-111">Por padrão, o leitor de origem e o gravador de coletor podem executar algumas conversões de formato em fluxos de vídeo e áudio não compactados.</span><span class="sxs-lookup"><span data-stu-id="76fca-111">By default, the source reader and sink writer can perform some format conversions on uncompressed audio and video streams.</span></span> <span data-ttu-id="76fca-112">Para desabilitar esse comportamento, defina esse atributo como **true** ao criar o leitor de origem ou o gravador de coletor.</span><span class="sxs-lookup"><span data-stu-id="76fca-112">To disable this behavior, set this attribute to **TRUE** when you create the source reader or sink writer.</span></span>

<span data-ttu-id="76fca-113">Use este atributo com as seguintes funções:</span><span class="sxs-lookup"><span data-stu-id="76fca-113">Use this attribute with the following functions:</span></span>

-   [<span data-ttu-id="76fca-114">**MFCreateSourceReaderFromByteStream**</span><span class="sxs-lookup"><span data-stu-id="76fca-114">**MFCreateSourceReaderFromByteStream**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [<span data-ttu-id="76fca-115">**MFCreateSourceReaderFromMediaSource**</span><span class="sxs-lookup"><span data-stu-id="76fca-115">**MFCreateSourceReaderFromMediaSource**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [<span data-ttu-id="76fca-116">**MFCreateSourceReaderFromURL**</span><span class="sxs-lookup"><span data-stu-id="76fca-116">**MFCreateSourceReaderFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)
-   [<span data-ttu-id="76fca-117">**MFCreateSinkWriterFromMediaSink**</span><span class="sxs-lookup"><span data-stu-id="76fca-117">**MFCreateSinkWriterFromMediaSink**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [<span data-ttu-id="76fca-118">**MFCreateSinkWriterFromURL**</span><span class="sxs-lookup"><span data-stu-id="76fca-118">**MFCreateSinkWriterFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

## <a name="requirements"></a><span data-ttu-id="76fca-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="76fca-119">Requirements</span></span>



| <span data-ttu-id="76fca-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="76fca-120">Requirement</span></span> | <span data-ttu-id="76fca-121">Valor</span><span class="sxs-lookup"><span data-stu-id="76fca-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="76fca-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="76fca-122">Minimum supported client</span></span><br/> | <span data-ttu-id="76fca-123">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="76fca-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="76fca-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="76fca-124">Minimum supported server</span></span><br/> | <span data-ttu-id="76fca-125">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="76fca-125">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="76fca-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="76fca-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="76fca-127"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="76fca-127"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76fca-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="76fca-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76fca-129">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="76fca-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="76fca-130">Atributos do gravador de coletor</span><span class="sxs-lookup"><span data-stu-id="76fca-130">Sink Writer Attributes</span></span>](sink-writer-attributes.md)
</dt> <dt>

[<span data-ttu-id="76fca-131">Atributos do leitor de origem</span><span class="sxs-lookup"><span data-stu-id="76fca-131">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




