---
description: Especifica o nível de normalização da caixa de diálogo, em decibéis (dB), em um fluxo de áudio Dolby Digital. Essa propriedade se aplica aos codificadores Dolby Digital Audio.
ms.assetid: c347f8b2-5132-45d6-af66-43d3c409b0d7
title: Propriedade AVEncDDDialogNormalization (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 586f241dc8d032767ecb2678c1ee5704dc20e0ef
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456818"
---
# <a name="avencdddialognormalization-property"></a><span data-ttu-id="d91d7-104">Propriedade AVEncDDDialogNormalization</span><span class="sxs-lookup"><span data-stu-id="d91d7-104">AVEncDDDialogNormalization property</span></span>

<span data-ttu-id="d91d7-105">Especifica o nível de normalização da caixa de diálogo, em decibéis (dB), em um fluxo de áudio Dolby Digital.</span><span class="sxs-lookup"><span data-stu-id="d91d7-105">Specifies the dialog normalization level, in decibels (dB), in a Dolby Digital audio stream.</span></span> <span data-ttu-id="d91d7-106">Essa propriedade se aplica aos codificadores Dolby Digital Audio.</span><span class="sxs-lookup"><span data-stu-id="d91d7-106">This property applies to Dolby Digital audio encoders.</span></span>

<span data-ttu-id="d91d7-107">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="d91d7-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="d91d7-108">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="d91d7-108">Data type</span></span>

<span data-ttu-id="d91d7-109">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="d91d7-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="d91d7-110">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="d91d7-110">Property GUID</span></span>

<span data-ttu-id="d91d7-111">**CODECAPI \_ AVEncDDDialogNormalization**</span><span class="sxs-lookup"><span data-stu-id="d91d7-111">**CODECAPI\_AVEncDDDialogNormalization**</span></span>

## <a name="property-value"></a><span data-ttu-id="d91d7-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="d91d7-112">Property value</span></span>

<span data-ttu-id="d91d7-113">Esta propriedade tem um intervalo linear de valores.</span><span class="sxs-lookup"><span data-stu-id="d91d7-113">This property has a linear range of values.</span></span> <span data-ttu-id="d91d7-114">Para obter o intervalo com suporte, chame [**ICodecAPI:: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="d91d7-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="requirements"></a><span data-ttu-id="d91d7-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d91d7-115">Requirements</span></span>



| <span data-ttu-id="d91d7-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d91d7-116">Requirement</span></span> | <span data-ttu-id="d91d7-117">Valor</span><span class="sxs-lookup"><span data-stu-id="d91d7-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d91d7-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d91d7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d91d7-119">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d91d7-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="d91d7-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d91d7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d91d7-121">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d91d7-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="d91d7-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d91d7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d91d7-123"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d91d7-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d91d7-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="d91d7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d91d7-125">Propriedades da API do codec</span><span class="sxs-lookup"><span data-stu-id="d91d7-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="d91d7-126">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="d91d7-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




