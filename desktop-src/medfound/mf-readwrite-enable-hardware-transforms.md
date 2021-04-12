---
description: Permite que o leitor de origem ou o gravador de coletor use transformações de Media Foundation baseadas em hardware (MFTs).
ms.assetid: 03f2fa76-b828-40b1-929d-60e7d5ab49bb
title: Atributo MF_READWRITE_ENABLE_HARDWARE_TRANSFORMS (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 642be732a51f064d07e57609a886810f2a9c40b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297150"
---
# <a name="mf_readwrite_enable_hardware_transforms-attribute"></a><span data-ttu-id="06a29-103">\_Atributo de \_ \_ \_ transformações de hardware MF ReadWrite</span><span class="sxs-lookup"><span data-stu-id="06a29-103">MF\_READWRITE\_ENABLE\_HARDWARE\_TRANSFORMS attribute</span></span>

<span data-ttu-id="06a29-104">Permite que o leitor de origem ou o gravador de coletor use transformações de Media Foundation baseadas em hardware (MFTs).</span><span class="sxs-lookup"><span data-stu-id="06a29-104">Enables the source reader or sink writer to use hardware-based Media Foundation transforms (MFTs).</span></span>

## <a name="data-type"></a><span data-ttu-id="06a29-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="06a29-105">Data type</span></span>

<span data-ttu-id="06a29-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="06a29-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="06a29-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="06a29-107">Get/set</span></span>

<span data-ttu-id="06a29-108">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="06a29-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="06a29-109">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="06a29-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="06a29-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="06a29-110">Remarks</span></span>

<span data-ttu-id="06a29-111">Por padrão, o leitor de origem e o gravador de coletor não usam codificadores de hardware ou codificadores.</span><span class="sxs-lookup"><span data-stu-id="06a29-111">By default, the source reader and sink writer do not use hardware decoders or encoders.</span></span> <span data-ttu-id="06a29-112">Para habilitar o uso de MFTs de hardware, defina esse atributo como **true** ao criar o leitor de origem ou o gravador de coletor.</span><span class="sxs-lookup"><span data-stu-id="06a29-112">To enable the use of hardware MFTs, set this attribute to **TRUE** when you create the source reader or sink writer.</span></span>

<span data-ttu-id="06a29-113">Use este atributo com as seguintes funções:</span><span class="sxs-lookup"><span data-stu-id="06a29-113">Use this attribute with the following functions:</span></span>

-   [<span data-ttu-id="06a29-114">**MFCreateSourceReaderFromByteStream**</span><span class="sxs-lookup"><span data-stu-id="06a29-114">**MFCreateSourceReaderFromByteStream**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [<span data-ttu-id="06a29-115">**MFCreateSourceReaderFromMediaSource**</span><span class="sxs-lookup"><span data-stu-id="06a29-115">**MFCreateSourceReaderFromMediaSource**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [<span data-ttu-id="06a29-116">**MFCreateSourceReaderFromURL**</span><span class="sxs-lookup"><span data-stu-id="06a29-116">**MFCreateSourceReaderFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)
-   [<span data-ttu-id="06a29-117">**MFCreateSinkWriterFromMediaSink**</span><span class="sxs-lookup"><span data-stu-id="06a29-117">**MFCreateSinkWriterFromMediaSink**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [<span data-ttu-id="06a29-118">**MFCreateSinkWriterFromURL**</span><span class="sxs-lookup"><span data-stu-id="06a29-118">**MFCreateSinkWriterFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

<span data-ttu-id="06a29-119">Há uma exceção para o comportamento padrão.</span><span class="sxs-lookup"><span data-stu-id="06a29-119">There is one exception to the default behavior.</span></span> <span data-ttu-id="06a29-120">O leitor de origem e o gravador de coletor usam automaticamente MFTs que são registrados localmente no processo do chamador.</span><span class="sxs-lookup"><span data-stu-id="06a29-120">The source reader and sink writer automatically use MFTs that are registered locally in the caller's process.</span></span> <span data-ttu-id="06a29-121">Para registrar uma MFT localmente, chame [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) ou [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid).</span><span class="sxs-lookup"><span data-stu-id="06a29-121">To register an MFT locally, call [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) or [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid).</span></span> <span data-ttu-id="06a29-122">Os MFTs de hardware registrados localmente são usados mesmo se o atributo **MF \_ ReadWrite habilitar as \_ \_ \_ transformações de hardware** não estiver definido.</span><span class="sxs-lookup"><span data-stu-id="06a29-122">Hardware MFTs that are registered locally are used even if the **MF\_READWRITE\_ENABLE\_HARDWARE\_TRANSFORMS** attribute is not set.</span></span>

<span data-ttu-id="06a29-123">Esse atributo não afeta a decodificação de vídeo acelerada por hardware que usa a DXVA (aceleração de vídeo do DirectX).</span><span class="sxs-lookup"><span data-stu-id="06a29-123">This attribute does not affect hardware-accelerated video decoding that uses DirectX Video Acceleration (DXVA).</span></span> <span data-ttu-id="06a29-124">Para habilitar a decodificação de DXVA no leitor de origem, defina o atributo [Gerenciador de D3D de \_ leitor de origem \_ \_ \_ MF](mf-source-reader-d3d-manager.md) .</span><span class="sxs-lookup"><span data-stu-id="06a29-124">To enable DXVA decoding in the source reader, set the [MF\_SOURCE\_READER\_D3D\_MANAGER](mf-source-reader-d3d-manager.md) attribute.</span></span>

<span data-ttu-id="06a29-125">Se esse atributo for **true**, não defina o atributo [MF \_ ReadWrite \_ Disable \_ Converters](mf-readwrite-disable-converters.md) .</span><span class="sxs-lookup"><span data-stu-id="06a29-125">If this attribute is **TRUE**, do not set the [MF\_READWRITE\_DISABLE\_CONVERTERS](mf-readwrite-disable-converters.md) attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="06a29-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06a29-126">Requirements</span></span>



| <span data-ttu-id="06a29-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="06a29-127">Requirement</span></span> | <span data-ttu-id="06a29-128">Valor</span><span class="sxs-lookup"><span data-stu-id="06a29-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="06a29-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="06a29-129">Minimum supported client</span></span><br/> | <span data-ttu-id="06a29-130">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="06a29-130">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="06a29-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="06a29-131">Minimum supported server</span></span><br/> | <span data-ttu-id="06a29-132">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="06a29-132">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="06a29-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="06a29-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="06a29-134"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="06a29-134"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06a29-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="06a29-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06a29-136">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="06a29-136">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="06a29-137">Atributos do gravador de coletor</span><span class="sxs-lookup"><span data-stu-id="06a29-137">Sink Writer Attributes</span></span>](sink-writer-attributes.md)
</dt> <dt>

[<span data-ttu-id="06a29-138">Atributos do leitor de origem</span><span class="sxs-lookup"><span data-stu-id="06a29-138">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




