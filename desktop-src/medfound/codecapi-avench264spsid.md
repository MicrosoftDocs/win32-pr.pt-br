---
description: Define o identificador do conjunto de parâmetros de sequência (SPS) na unidade da NAL (camada de abstração de rede) do SPS do fluxo de bits H. 264.
ms.assetid: 583DD539-6EE8-4DD4-A0FE-D2BBE1A4302F
title: Propriedade CODECAPI_AVEncH264SPSID (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e06fb78fc128b2eec5db2c61faf70ee10a5eba5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089787"
---
# <a name="codecapi_avench264spsid-property"></a><span data-ttu-id="71a25-103">\_Propriedade CODECAPI AVEncH264SPSID</span><span class="sxs-lookup"><span data-stu-id="71a25-103">CODECAPI\_AVEncH264SPSID property</span></span>

<span data-ttu-id="71a25-104">Define o identificador do conjunto de parâmetros de sequência (SPS) na unidade da NAL (camada de abstração de rede) do SPS do fluxo de bits H. 264.</span><span class="sxs-lookup"><span data-stu-id="71a25-104">Sets the sequence parameter set (SPS) identifier in the SPS network abstraction layer (NAL) unit of the H.264 bit stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="71a25-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="71a25-105">Data type</span></span>

<span data-ttu-id="71a25-106">**ULONG** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="71a25-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="71a25-107">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="71a25-107">Property GUID</span></span>

<span data-ttu-id="71a25-108">**CODECAPI \_ AVEncH264SPSID**</span><span class="sxs-lookup"><span data-stu-id="71a25-108">**CODECAPI\_AVEncH264SPSID**</span></span>

## <a name="property-value"></a><span data-ttu-id="71a25-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="71a25-109">Property value</span></span>

<span data-ttu-id="71a25-110">Especifica o valor da **\_ ID do \_ conjunto \_ de parâmetros Seq** na unidade de nal do SPS.</span><span class="sxs-lookup"><span data-stu-id="71a25-110">Specifies the value of **seq\_parameter\_set\_id** in the SPS NAL unit.</span></span> <span data-ttu-id="71a25-111">O elemento sintaxe de **\_ ID do \_ conjunto \_ de parâmetros Seq** identifica o conjunto de parâmetros de sequência.</span><span class="sxs-lookup"><span data-stu-id="71a25-111">The **seq\_parameter\_set\_id** syntax element identifies the sequence parameter set.</span></span> <span data-ttu-id="71a25-112">O fluxo de bits resultante pode ser concatenado com outros fluxos de bits, para produzir um fluxo de bits mais longo que contenha vários conjuntos de parâmetros de sequência com diferentes identificadores de SPS.</span><span class="sxs-lookup"><span data-stu-id="71a25-112">The resulting bit stream can be concatenated with other bit streams, to produce a longer bit stream that contains multiple sequence parameter sets with different SPS identifiers.</span></span>

<span data-ttu-id="71a25-113">O intervalo válido é de 0 31, conforme especificado na especificação H. 264/AVC.</span><span class="sxs-lookup"><span data-stu-id="71a25-113">The valid range is 0 31, as specified in the H.264/AVC specification.</span></span>

## <a name="requirements"></a><span data-ttu-id="71a25-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71a25-114">Requirements</span></span>



| <span data-ttu-id="71a25-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="71a25-115">Requirement</span></span> | <span data-ttu-id="71a25-116">Valor</span><span class="sxs-lookup"><span data-stu-id="71a25-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="71a25-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71a25-117">Minimum supported client</span></span><br/> | <span data-ttu-id="71a25-118">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="71a25-118">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="71a25-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71a25-119">Minimum supported server</span></span><br/> | <span data-ttu-id="71a25-120">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="71a25-120">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="71a25-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="71a25-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="71a25-122"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="71a25-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71a25-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="71a25-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71a25-124">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="71a25-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="71a25-125">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="71a25-125">**ICodecAPI**</span></span>](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

