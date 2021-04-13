---
description: Permite que o leitor de origem use transformações de Media Foundation (MFTs) que são otimizadas para transcodificação.
ms.assetid: 9463EB8C-2CA3-4F8F-8A2A-B1292879DD1B
title: Atributo MF_SOURCE_READER_ENABLE_TRANSCODE_ONLY_TRANSFORMS (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04a9559254216a102613d97824601c004c71bfd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501635"
---
# <a name="mf_source_reader_enable_transcode_only_transforms-attribute"></a><span data-ttu-id="5fcad-103">\_Leitor de origem MF \_ \_ habilitar \_ \_ somente \_ transformações atributo</span><span class="sxs-lookup"><span data-stu-id="5fcad-103">MF\_SOURCE\_READER\_ENABLE\_TRANSCODE\_ONLY\_TRANSFORMS attribute</span></span>

<span data-ttu-id="5fcad-104">Permite que o [leitor de origem](source-reader.md) use transformações de Media Foundation (MFTs) que são otimizadas para transcodificação.</span><span class="sxs-lookup"><span data-stu-id="5fcad-104">Enables the [Source Reader](source-reader.md) to use Media Foundation transforms (MFTs) that are optimized for transcoding.</span></span>

## <a name="data-type"></a><span data-ttu-id="5fcad-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="5fcad-105">Data type</span></span>

<span data-ttu-id="5fcad-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="5fcad-106">**UINT32**</span></span>

<span data-ttu-id="5fcad-107">Tratar como booliano.</span><span class="sxs-lookup"><span data-stu-id="5fcad-107">Treat as Boolean.</span></span>

## <a name="remarks"></a><span data-ttu-id="5fcad-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="5fcad-108">Remarks</span></span>

<span data-ttu-id="5fcad-109">Alguns MFTs, especialmente decodificadores, são otimizados para transcodificação em vez de reprodução.</span><span class="sxs-lookup"><span data-stu-id="5fcad-109">Some MFTs, particularly decoders, are optimized for transcoding rather than playback.</span></span> <span data-ttu-id="5fcad-110">Por padrão, o leitor de origem não carregará essas transformações.</span><span class="sxs-lookup"><span data-stu-id="5fcad-110">By default, the Source Reader will not load such transforms.</span></span> <span data-ttu-id="5fcad-111">Defina esse atributo como **true** se você quiser usar transcodificação de MFTs com o leitor de origem.</span><span class="sxs-lookup"><span data-stu-id="5fcad-111">Set this attribute to **TRUE** if you want to use transcoding MFTs with the Source Reader.</span></span>

<span data-ttu-id="5fcad-112">Um aplicativo poderá definir esse atributo se ele não processar os dados em tempo real (para transcodificação ou cenários semelhantes).</span><span class="sxs-lookup"><span data-stu-id="5fcad-112">An application might set this attribute if it does not process the data in real time (for transcoding or similar scenarios).</span></span> <span data-ttu-id="5fcad-113">Caso contrário, para reprodução em tempo real, use o comportamento padrão.</span><span class="sxs-lookup"><span data-stu-id="5fcad-113">Otherwise, for real-time playback, use the default behavior.</span></span>

<span data-ttu-id="5fcad-114">Internamente, esse atributo faz com que o leitor de origem inclua o sinalizador **\_ enumerador de enumeração de MFT \_ \_ \_ somente para transcodificação** ao chamar [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span><span class="sxs-lookup"><span data-stu-id="5fcad-114">Internally, this attribute causes the Source Reader to include the **MFT\_ENUM\_FLAG\_TRANSCODE\_ONLY** flag when it calls [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span></span>

## <a name="requirements"></a><span data-ttu-id="5fcad-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5fcad-115">Requirements</span></span>



| <span data-ttu-id="5fcad-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5fcad-116">Requirement</span></span> | <span data-ttu-id="5fcad-117">Valor</span><span class="sxs-lookup"><span data-stu-id="5fcad-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fcad-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5fcad-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5fcad-119">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="5fcad-119">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="5fcad-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5fcad-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5fcad-121">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="5fcad-121">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="5fcad-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5fcad-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5fcad-123"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="5fcad-123"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fcad-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="5fcad-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fcad-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5fcad-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5fcad-126">Leitor de origem</span><span class="sxs-lookup"><span data-stu-id="5fcad-126">Source Reader</span></span>](source-reader.md)
</dt> </dl>

 

 




