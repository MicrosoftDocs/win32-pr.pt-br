---
description: Especifica se o leitor de origem desliga a origem da mídia.
ms.assetid: c85f5994-8005-48c9-8a05-0316f48f4142
title: Atributo MF_SOURCE_READER_DISCONNECT_MEDIASOURCE_ON_SHUTDOWN (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7a9474e7fb19bb6531baf31a97238bbe6b10e46
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104297992"
---
# <a name="mf_source_reader_disconnect_mediasource_on_shutdown-attribute"></a><span data-ttu-id="e7968-103">\_ \_ \_ Arquivo de desconexão \_ do leitor \_ de origem MF no \_ atributo de desligamento</span><span class="sxs-lookup"><span data-stu-id="e7968-103">MF\_SOURCE\_READER\_DISCONNECT\_MEDIASOURCE\_ON\_SHUTDOWN attribute</span></span>

<span data-ttu-id="e7968-104">Especifica se o [leitor de origem](source-reader.md) desliga a origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="e7968-104">Specifies whether the [Source Reader](source-reader.md) shuts down the media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="e7968-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="e7968-105">Data type</span></span>

<span data-ttu-id="e7968-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="e7968-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="e7968-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="e7968-107">Get/set</span></span>

<span data-ttu-id="e7968-108">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="e7968-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="e7968-109">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="e7968-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="e7968-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="e7968-110">Remarks</span></span>

<span data-ttu-id="e7968-111">Esse atributo se aplica somente quando o aplicativo cria o leitor de origem de um objeto de origem de mídia existente chamando [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource) ou chamando [**IMFReadWriteClassFactory:: CreateInstanceFromObject**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromobject).</span><span class="sxs-lookup"><span data-stu-id="e7968-111">This attribute applies only when the application creates the source reader from an existing media source object, either by calling [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource) or by calling [**IMFReadWriteClassFactory::CreateInstanceFromObject**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromobject).</span></span>

<span data-ttu-id="e7968-112">Por padrão, quando o aplicativo libera o leitor de origem, o leitor de origem desliga a origem da mídia chamando [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) na origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="e7968-112">By default, when the application releases the source reader, the source reader shuts down the media source by calling [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) on the media source.</span></span> <span data-ttu-id="e7968-113">Nesse ponto, o aplicativo não poderá mais usar a origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="e7968-113">At that point, the application can no longer use the media source.</span></span>

<span data-ttu-id="e7968-114">No entanto, se o \_ atributo do leitor de origem MF \_ \_ Desconectar \_ MediaName \_ no \_ desligamento for **true**, o leitor de origem não desligará a origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="e7968-114">However, if the MF\_SOURCE\_READER\_DISCONNECT\_MEDIASOURCE\_ON\_SHUTDOWN attribute is **TRUE**, the source reader does not shut down the media source.</span></span> <span data-ttu-id="e7968-115">Isso significa que o aplicativo ainda poderá usar a origem de mídia depois que o aplicativo liberar o leitor de origem.</span><span class="sxs-lookup"><span data-stu-id="e7968-115">That means the application can still use the media source after the application releases the source reader.</span></span> <span data-ttu-id="e7968-116">Isso também significa que o aplicativo é responsável por chamar [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) na origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="e7968-116">It also means the application is responsible for calling [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) on the media source.</span></span>

<span data-ttu-id="e7968-117">Se o aplicativo criar o leitor de origem de uma URL ou de um fluxo de bytes, o leitor de origem sempre desligará a origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="e7968-117">If the application creates the source reader from a URL or from a byte stream, the source reader always shuts down the media source.</span></span> <span data-ttu-id="e7968-118">O \_ atributo de \_ desconexão do leitor de origem MF \_ \_ \_ em \_ desligamento é ignorado nesse caso.</span><span class="sxs-lookup"><span data-stu-id="e7968-118">The MF\_SOURCE\_READER\_DISCONNECT\_MEDIASOURCE\_ON\_SHUTDOWN attribute is ignored in this case.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7968-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7968-119">Requirements</span></span>



| <span data-ttu-id="e7968-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7968-120">Requirement</span></span> | <span data-ttu-id="e7968-121">Valor</span><span class="sxs-lookup"><span data-stu-id="e7968-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7968-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e7968-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e7968-123">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="e7968-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="e7968-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e7968-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e7968-125">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="e7968-125">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="e7968-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e7968-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7968-127"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7968-127"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7968-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="e7968-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7968-129">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e7968-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e7968-130">Leitor de origem</span><span class="sxs-lookup"><span data-stu-id="e7968-130">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="e7968-131">Atributos do leitor de origem</span><span class="sxs-lookup"><span data-stu-id="e7968-131">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




