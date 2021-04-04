---
description: Contém um ponteiro para a interface de retorno de chamada de aplicativos para o gravador de coletor.
ms.assetid: 22df1fa0-469d-4501-aaf0-a0379b7ed096
title: Atributo MF_SINK_WRITER_ASYNC_CALLBACK (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f11bed051df9107ca3a2247b6c3d0cf2058224c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663178"
---
# <a name="mf_sink_writer_async_callback-attribute"></a><span data-ttu-id="0b397-103">\_Atributo de \_ retorno de \_ chamada assíncrono do gravador de coletor MF \_</span><span class="sxs-lookup"><span data-stu-id="0b397-103">MF\_SINK\_WRITER\_ASYNC\_CALLBACK attribute</span></span>

<span data-ttu-id="0b397-104">Contém um ponteiro para a interface de retorno de chamada do aplicativo para o gravador do coletor.</span><span class="sxs-lookup"><span data-stu-id="0b397-104">Contains a pointer to the application's callback interface for the sink writer.</span></span>

## <a name="data-type"></a><span data-ttu-id="0b397-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="0b397-105">Data type</span></span>

<span data-ttu-id="0b397-106">**[](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback) IMFSinkWriterCallback \** _ armazenado como _*IUnknown \*\*_</span><span class="sxs-lookup"><span data-stu-id="0b397-106">**[**IMFSinkWriterCallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback)\** _ stored as _*IUnknown\*\*_</span></span>

## <a name="getset"></a><span data-ttu-id="0b397-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="0b397-107">Get/set</span></span>

<span data-ttu-id="0b397-108">Para obter esse atributo, chame [_ *IMFAttributes:: getunknown* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="0b397-108">To get this attribute, call [_ *IMFAttributes::GetUnknown*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="0b397-109">Para definir esse atributo, chame [**IMFAttributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="0b397-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="0b397-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="0b397-110">Remarks</span></span>

<span data-ttu-id="0b397-111">O valor desse atributo é um ponteiro para a interface [**IMFSinkWriterCallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback) do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0b397-111">The value of this attribute is a pointer to the application's [**IMFSinkWriterCallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback) interface.</span></span>

<span data-ttu-id="0b397-112">Use este atributo com as seguintes funções:</span><span class="sxs-lookup"><span data-stu-id="0b397-112">Use this attribute with the following functions:</span></span>

-   [<span data-ttu-id="0b397-113">**MFCreateSinkWriterFromMediaSink**</span><span class="sxs-lookup"><span data-stu-id="0b397-113">**MFCreateSinkWriterFromMediaSink**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [<span data-ttu-id="0b397-114">**MFCreateSinkWriterFromURL**</span><span class="sxs-lookup"><span data-stu-id="0b397-114">**MFCreateSinkWriterFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

## <a name="requirements"></a><span data-ttu-id="0b397-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b397-115">Requirements</span></span>



| <span data-ttu-id="0b397-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b397-116">Requirement</span></span> | <span data-ttu-id="0b397-117">Valor</span><span class="sxs-lookup"><span data-stu-id="0b397-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b397-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b397-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0b397-119">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="0b397-119">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="0b397-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b397-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0b397-121">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="0b397-121">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="0b397-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0b397-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b397-123"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b397-123"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b397-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="0b397-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b397-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0b397-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0b397-126">Atributos do gravador de coletor</span><span class="sxs-lookup"><span data-stu-id="0b397-126">Sink Writer Attributes</span></span>](sink-writer-attributes.md)
</dt> </dl>

 

 




