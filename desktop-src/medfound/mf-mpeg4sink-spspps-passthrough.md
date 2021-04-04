---
description: Especifica se o coletor de arquivos MPEG-4 filtra o conjunto de parâmetros de sequência (SPS) e o conjunto de parâmetros de imagem (PPS) NALUs.
ms.assetid: B2574BE5-6334-4ED2-A008-86326CDC13B8
title: Atributo MF_MPEG4SINK_SPSPPS_PASSTHROUGH (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3c02f4f1cdcac17a104b5061c8899c92e0ad824
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661575"
---
# <a name="mf_mpeg4sink_spspps_passthrough-attribute"></a><span data-ttu-id="136aa-103">\_Atributo de passagem MF MPEG4SINK \_ SPSPPS \_</span><span class="sxs-lookup"><span data-stu-id="136aa-103">MF\_MPEG4SINK\_SPSPPS\_PASSTHROUGH attribute</span></span>

<span data-ttu-id="136aa-104">Especifica se o [**coletor de arquivos MPEG-4**](mpeg-4-file-sink.md) filtra o conjunto de parâmetros de sequência (SPS) e o conjunto de parâmetros de imagem (PPS) NALUs.</span><span class="sxs-lookup"><span data-stu-id="136aa-104">Specifies whether the [**MPEG-4 File Sink**](mpeg-4-file-sink.md) filters out sequence parameter set (SPS) and picture parameter set (PPS) NALUs.</span></span>

## <a name="data-type"></a><span data-ttu-id="136aa-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="136aa-105">Data type</span></span>

<span data-ttu-id="136aa-106">**Bool** armazenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="136aa-106">**BOOL** stored as **UINT32**</span></span>

## <a name="applies-to"></a><span data-ttu-id="136aa-107">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="136aa-107">Applies to</span></span>

[<span data-ttu-id="136aa-108">**IMFMediaSink**</span><span class="sxs-lookup"><span data-stu-id="136aa-108">**IMFMediaSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)

## <a name="remarks"></a><span data-ttu-id="136aa-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="136aa-109">Remarks</span></span>

<span data-ttu-id="136aa-110">O [**coletor de arquivos MPEG-4**](mpeg-4-file-sink.md) grava os parâmetros SPS e PPS na caixa de descrição de exemplo do arquivo MP4.</span><span class="sxs-lookup"><span data-stu-id="136aa-110">The [**MPEG-4 File Sink**](mpeg-4-file-sink.md) writes the SPS and PPS parameters into the sample description box of the MP4 file.</span></span> <span data-ttu-id="136aa-111">Por padrão, ele filtra o SPS e o PPS NALUs do fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="136aa-111">By default, it filters out the SPS and PPS NALUs from the video stream.</span></span> <span data-ttu-id="136aa-112">Para substituir esse comportamento, defina o \_ atributo de passagem MF MPEG4SINK \_ SPSPPS \_ como **true**.</span><span class="sxs-lookup"><span data-stu-id="136aa-112">To override this behavior, set the MF\_MPEG4SINK\_SPSPPS\_PASSTHROUGH attribute to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="136aa-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="136aa-113">Requirements</span></span>



| <span data-ttu-id="136aa-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="136aa-114">Requirement</span></span> | <span data-ttu-id="136aa-115">Valor</span><span class="sxs-lookup"><span data-stu-id="136aa-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="136aa-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="136aa-116">Minimum supported client</span></span><br/> | <span data-ttu-id="136aa-117">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="136aa-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="136aa-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="136aa-118">Minimum supported server</span></span><br/> | <span data-ttu-id="136aa-119">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="136aa-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="136aa-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="136aa-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="136aa-121"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="136aa-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="136aa-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="136aa-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="136aa-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="136aa-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




