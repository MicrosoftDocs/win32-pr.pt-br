---
description: Especifica a precisão dos coeficientes de DC, em bits. Essa propriedade se aplica a codificadores de vídeo MPEG.
ms.assetid: 2b4d11c1-767c-4466-8291-7959d841ae65
title: Propriedade AVEncMPVIntraDCPrecision (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55d4bdd3c08f49586eb2663829271ae4166d917e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825852"
---
# <a name="avencmpvintradcprecision-property"></a><span data-ttu-id="35e34-104">Propriedade AVEncMPVIntraDCPrecision</span><span class="sxs-lookup"><span data-stu-id="35e34-104">AVEncMPVIntraDCPrecision property</span></span>

<span data-ttu-id="35e34-105">Especifica a precisão dos coeficientes de DC, em bits.</span><span class="sxs-lookup"><span data-stu-id="35e34-105">Specifies the precision of the DC coefficients, in bits.</span></span> <span data-ttu-id="35e34-106">Essa propriedade se aplica a codificadores de vídeo MPEG.</span><span class="sxs-lookup"><span data-stu-id="35e34-106">This property applies to MPEG video encoders.</span></span>

<span data-ttu-id="35e34-107">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="35e34-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="35e34-108">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="35e34-108">Data type</span></span>

<span data-ttu-id="35e34-109">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="35e34-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="35e34-110">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="35e34-110">Property GUID</span></span>

<span data-ttu-id="35e34-111">**CODECAPI \_ AVEncMPVIntraDCPrecision**</span><span class="sxs-lookup"><span data-stu-id="35e34-111">**CODECAPI\_AVEncMPVIntraDCPrecision**</span></span>

## <a name="property-value"></a><span data-ttu-id="35e34-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="35e34-112">Property value</span></span>

<span data-ttu-id="35e34-113">Esta propriedade tem um intervalo linear de valores.</span><span class="sxs-lookup"><span data-stu-id="35e34-113">This property has a linear range of values.</span></span> <span data-ttu-id="35e34-114">Para obter o intervalo com suporte, chame [**ICodecAPI:: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="35e34-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="remarks"></a><span data-ttu-id="35e34-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="35e34-115">Remarks</span></span>

<span data-ttu-id="35e34-116">O intervalo usual para essa propriedade é de 8 a 11 bits.</span><span class="sxs-lookup"><span data-stu-id="35e34-116">The usual range for this property is 8 to 11 bits.</span></span> <span data-ttu-id="35e34-117">Se o valor for zero, o codificador selecionará a precisão.</span><span class="sxs-lookup"><span data-stu-id="35e34-117">If the value is zero, the encoder selects the precision.</span></span>

## <a name="requirements"></a><span data-ttu-id="35e34-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35e34-118">Requirements</span></span>



| <span data-ttu-id="35e34-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="35e34-119">Requirement</span></span> | <span data-ttu-id="35e34-120">Valor</span><span class="sxs-lookup"><span data-stu-id="35e34-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="35e34-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35e34-121">Minimum supported client</span></span><br/> | <span data-ttu-id="35e34-122">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="35e34-122">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="35e34-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35e34-123">Minimum supported server</span></span><br/> | <span data-ttu-id="35e34-124">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="35e34-124">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="35e34-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="35e34-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="35e34-126"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="35e34-126"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35e34-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="35e34-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35e34-128">Propriedades da API do codec</span><span class="sxs-lookup"><span data-stu-id="35e34-128">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="35e34-129">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="35e34-129">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




