---
description: Controla a sinalização de MFSampleExtension \_ MeanAbsoluteDifference por meio de IMFAttribute em cada exemplo de saída.
ms.assetid: 61C0F431-FBF5-4B17-8F3A-0F6AD2BA33B7
title: Propriedade CODECAPI_AVEncVideoMeanAbsoluteDifference (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f58a7bc0da9fce88c0b8137d800d527d4717801c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781192"
---
# <a name="codecapi_avencvideomeanabsolutedifference-property"></a><span data-ttu-id="6df2c-103">\_Propriedade CODECAPI AVEncVideoMeanAbsoluteDifference</span><span class="sxs-lookup"><span data-stu-id="6df2c-103">CODECAPI\_AVEncVideoMeanAbsoluteDifference property</span></span>

<span data-ttu-id="6df2c-104">Controla a sinalização de [MFSampleExtension \_ MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md) por meio de [**IMFAttribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) em cada exemplo de saída.</span><span class="sxs-lookup"><span data-stu-id="6df2c-104">Controls the signaling of [MFSampleExtension\_MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md) through [**IMFAttribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) on each output sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="6df2c-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="6df2c-105">Data type</span></span>

<span data-ttu-id="6df2c-106">**ULONG** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="6df2c-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="6df2c-107">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="6df2c-107">Property GUID</span></span>

<span data-ttu-id="6df2c-108">**CODECAPI \_ AVEncVideoMeanAbsoluteDifference**</span><span class="sxs-lookup"><span data-stu-id="6df2c-108">**CODECAPI\_AVEncVideoMeanAbsoluteDifference**</span></span>

## <a name="remarks"></a><span data-ttu-id="6df2c-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="6df2c-109">Remarks</span></span>

<span data-ttu-id="6df2c-110">Se o aplicativo definir um valor diferente de zero, o codificador deverá adicionar o atributo de exemplo [MFSampleExtension \_ MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md) a cada exemplo de saída.</span><span class="sxs-lookup"><span data-stu-id="6df2c-110">If the application sets a non-zero value then the encoder should add the [MFSampleExtension\_MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md) sample attribute to each output sample.</span></span> <span data-ttu-id="6df2c-111">O \_ atributo MFSampleExtension MeanAbsoluteDifference indica a diferença absoluta média entre os exemplos de origem e os exemplos previstos no plano Y.</span><span class="sxs-lookup"><span data-stu-id="6df2c-111">The MFSampleExtension\_MeanAbsoluteDifference attribute indicates the mean absolute difference between the source samples and the predicted samples in the Y plane.</span></span>

<span data-ttu-id="6df2c-112">Se o codificador retornar 0 para **GetParameterRange**, o codificador não oferecerá suporte à saída de [MFSampleExtension \_ MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md) nos exemplos de saída.</span><span class="sxs-lookup"><span data-stu-id="6df2c-112">If the encoder returns 0 for **GetParameterRange**, then the encoder does not support the output of [MFSampleExtension\_MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md) on the output samples.</span></span>

<span data-ttu-id="6df2c-113">O valor padrão deve ser 0.</span><span class="sxs-lookup"><span data-stu-id="6df2c-113">The default value should be 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="6df2c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6df2c-114">Requirements</span></span>



| <span data-ttu-id="6df2c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="6df2c-115">Requirement</span></span> | <span data-ttu-id="6df2c-116">Valor</span><span class="sxs-lookup"><span data-stu-id="6df2c-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6df2c-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6df2c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6df2c-118">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6df2c-118">Windows 8.1 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="6df2c-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6df2c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6df2c-120">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="6df2c-120">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6df2c-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6df2c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6df2c-122"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="6df2c-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6df2c-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="6df2c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6df2c-124">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6df2c-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




