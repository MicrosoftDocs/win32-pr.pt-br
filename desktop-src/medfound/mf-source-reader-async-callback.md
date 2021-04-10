---
description: Contém um ponteiro para a interface de retorno de chamada de aplicativos para o leitor de origem.
ms.assetid: de226a5a-03c0-4bfe-bb20-8969ce43cf53
title: Atributo MF_SOURCE_READER_ASYNC_CALLBACK (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66542a155fbb6fa3e56958733626b1d0b750ab9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170364"
---
# <a name="mf_source_reader_async_callback-attribute"></a><span data-ttu-id="bf8c8-103">\_Atributo de \_ retorno de \_ chamada assíncrono do leitor de origem MF \_</span><span class="sxs-lookup"><span data-stu-id="bf8c8-103">MF\_SOURCE\_READER\_ASYNC\_CALLBACK attribute</span></span>

<span data-ttu-id="bf8c8-104">Contém um ponteiro para a interface de retorno de chamada do aplicativo para o [leitor de origem](source-reader.md).</span><span class="sxs-lookup"><span data-stu-id="bf8c8-104">Contains a pointer to the application's callback interface for the [Source Reader](source-reader.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="bf8c8-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="bf8c8-105">Data type</span></span>

<span data-ttu-id="bf8c8-106">**IMFSourceReaderCallback \** _ armazenado como _*IUnknown \*\*_</span><span class="sxs-lookup"><span data-stu-id="bf8c8-106">**IMFSourceReaderCallback\** _ stored as _*IUnknown\*\*_</span></span>

## <a name="getset"></a><span data-ttu-id="bf8c8-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="bf8c8-107">Get/set</span></span>

<span data-ttu-id="bf8c8-108">Para obter esse atributo, chame [_ *IMFAttributes:: getunknown* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="bf8c8-108">To get this attribute, call [_ *IMFAttributes::GetUnknown*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="bf8c8-109">Para definir esse atributo, chame [**IMFAttributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="bf8c8-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="bf8c8-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="bf8c8-110">Remarks</span></span>

<span data-ttu-id="bf8c8-111">O valor desse atributo é um ponteiro para a interface [**IMFSourceReaderCallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback) do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bf8c8-111">The value of this attribute is a pointer to the application's [**IMFSourceReaderCallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback) interface.</span></span>

<span data-ttu-id="bf8c8-112">Use este atributo com as seguintes funções:</span><span class="sxs-lookup"><span data-stu-id="bf8c8-112">Use this attribute with the following functions:</span></span>

-   [<span data-ttu-id="bf8c8-113">**MFCreateSourceReaderFromByteStream**</span><span class="sxs-lookup"><span data-stu-id="bf8c8-113">**MFCreateSourceReaderFromByteStream**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [<span data-ttu-id="bf8c8-114">**MFCreateSourceReaderFromMediaSource**</span><span class="sxs-lookup"><span data-stu-id="bf8c8-114">**MFCreateSourceReaderFromMediaSource**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [<span data-ttu-id="bf8c8-115">**MFCreateSourceReaderFromURL**</span><span class="sxs-lookup"><span data-stu-id="bf8c8-115">**MFCreateSourceReaderFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)

## <a name="requirements"></a><span data-ttu-id="bf8c8-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf8c8-116">Requirements</span></span>



| <span data-ttu-id="bf8c8-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf8c8-117">Requirement</span></span> | <span data-ttu-id="bf8c8-118">Valor</span><span class="sxs-lookup"><span data-stu-id="bf8c8-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf8c8-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bf8c8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bf8c8-120">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="bf8c8-120">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="bf8c8-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bf8c8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bf8c8-122">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="bf8c8-122">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="bf8c8-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bf8c8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf8c8-124"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf8c8-124"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf8c8-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="bf8c8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf8c8-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bf8c8-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="bf8c8-127">Leitor de origem</span><span class="sxs-lookup"><span data-stu-id="bf8c8-127">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="bf8c8-128">Atributos do leitor de origem</span><span class="sxs-lookup"><span data-stu-id="bf8c8-128">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




