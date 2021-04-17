---
description: Especifica se o gravador do coletor limita a taxa de dados de entrada.
ms.assetid: eb79bda7-ece0-4977-a0f9-d40bd5d220ab
title: Atributo MF_SINK_WRITER_DISABLE_THROTTLING (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e01c34b51726135516fb6547679db3ba3d48ebfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105798541"
---
# <a name="mf_sink_writer_disable_throttling-attribute"></a><span data-ttu-id="29ffa-103">\_Atributo de \_ \_ limitação de desabilitação do gravador de coletor MF \_</span><span class="sxs-lookup"><span data-stu-id="29ffa-103">MF\_SINK\_WRITER\_DISABLE\_THROTTLING attribute</span></span>

<span data-ttu-id="29ffa-104">Especifica se o gravador do coletor limita a taxa de dados de entrada.</span><span class="sxs-lookup"><span data-stu-id="29ffa-104">Specifies whether the sink writer limits the rate of incoming data.</span></span>

## <a name="data-type"></a><span data-ttu-id="29ffa-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="29ffa-105">Data type</span></span>

<span data-ttu-id="29ffa-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="29ffa-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="29ffa-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="29ffa-107">Get/set</span></span>

<span data-ttu-id="29ffa-108">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="29ffa-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="29ffa-109">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="29ffa-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="29ffa-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="29ffa-110">Remarks</span></span>

<span data-ttu-id="29ffa-111">Por padrão, o método [**IMFSinkWriter:: WriteSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample) do gravador do coletor limita a taxa de dados bloqueando o thread de chamada.</span><span class="sxs-lookup"><span data-stu-id="29ffa-111">By default, the sink writer's [**IMFSinkWriter::WriteSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample) method limits the data rate by blocking the calling thread.</span></span> <span data-ttu-id="29ffa-112">Isso impede que o aplicativo entregue amostras com muita rapidez.</span><span class="sxs-lookup"><span data-stu-id="29ffa-112">This prevents the application from delivering samples too quickly.</span></span> <span data-ttu-id="29ffa-113">Para desabilitar esse comportamento, defina o \_ atributo de limitação do gravador de coletor MF \_ \_ \_ para **verdadeiro** ao criar o gravador de coletor.</span><span class="sxs-lookup"><span data-stu-id="29ffa-113">To disable this behavior, set the MF\_SINK\_WRITER\_DISABLE\_THROTTLING attribute to **TRUE** when you create the sink writer.</span></span>

<span data-ttu-id="29ffa-114">Use este atributo com as seguintes funções:</span><span class="sxs-lookup"><span data-stu-id="29ffa-114">Use this attribute with the following functions:</span></span>

-   [<span data-ttu-id="29ffa-115">**MFCreateSinkWriterFromMediaSink**</span><span class="sxs-lookup"><span data-stu-id="29ffa-115">**MFCreateSinkWriterFromMediaSink**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [<span data-ttu-id="29ffa-116">**MFCreateSinkWriterFromURL**</span><span class="sxs-lookup"><span data-stu-id="29ffa-116">**MFCreateSinkWriterFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

## <a name="requirements"></a><span data-ttu-id="29ffa-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29ffa-117">Requirements</span></span>



| <span data-ttu-id="29ffa-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="29ffa-118">Requirement</span></span> | <span data-ttu-id="29ffa-119">Valor</span><span class="sxs-lookup"><span data-stu-id="29ffa-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="29ffa-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="29ffa-120">Minimum supported client</span></span><br/> | <span data-ttu-id="29ffa-121">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="29ffa-121">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="29ffa-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="29ffa-122">Minimum supported server</span></span><br/> | <span data-ttu-id="29ffa-123">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="29ffa-123">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="29ffa-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="29ffa-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="29ffa-125"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="29ffa-125"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29ffa-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="29ffa-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29ffa-127">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="29ffa-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="29ffa-128">Atributos do gravador de coletor</span><span class="sxs-lookup"><span data-stu-id="29ffa-128">Sink Writer Attributes</span></span>](sink-writer-attributes.md)
</dt> </dl>

 

 




