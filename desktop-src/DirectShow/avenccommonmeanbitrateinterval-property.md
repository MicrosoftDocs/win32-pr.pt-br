---
description: Especifica o intervalo de tempo durante o qual a taxa de bits média se aplica. Essa propriedade é usada em conjunto com a propriedade AVEncCommonMeanBitRate.
ms.assetid: 3cf26f46-e8ac-448a-a031-800915cad1ef
title: Propriedade AVEncCommonMeanBitRateInterval (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ffee31b0ac54d195051f1cc973d2fdcb058f202
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456825"
---
# <a name="avenccommonmeanbitrateinterval-property"></a><span data-ttu-id="043e2-104">Propriedade AVEncCommonMeanBitRateInterval</span><span class="sxs-lookup"><span data-stu-id="043e2-104">AVEncCommonMeanBitRateInterval property</span></span>

<span data-ttu-id="043e2-105">Especifica o intervalo de tempo durante o qual a taxa de bits média se aplica.</span><span class="sxs-lookup"><span data-stu-id="043e2-105">Specifies the time interval over which the average bit rate applies.</span></span> <span data-ttu-id="043e2-106">Essa propriedade é usada em conjunto com a propriedade [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md) .</span><span class="sxs-lookup"><span data-stu-id="043e2-106">This property is used in conjunction with the [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md) property.</span></span>

<span data-ttu-id="043e2-107">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="043e2-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="043e2-108">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="043e2-108">Data type</span></span>

<span data-ttu-id="043e2-109">**UINT64** (**VT \_ UI8**)</span><span class="sxs-lookup"><span data-stu-id="043e2-109">**UINT64** (**VT\_UI8**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="043e2-110">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="043e2-110">Property GUID</span></span>

<span data-ttu-id="043e2-111">**CODECAPI \_ AVEncCommonMeanBitRateInterval**</span><span class="sxs-lookup"><span data-stu-id="043e2-111">**CODECAPI\_AVEncCommonMeanBitRateInterval**</span></span>

## <a name="property-value"></a><span data-ttu-id="043e2-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="043e2-112">Property value</span></span>

<span data-ttu-id="043e2-113">Esta propriedade tem um intervalo linear de valores.</span><span class="sxs-lookup"><span data-stu-id="043e2-113">This property has a linear range of values.</span></span> <span data-ttu-id="043e2-114">Para obter o intervalo com suporte, chame [**ICodecAPI:: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="043e2-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="remarks"></a><span data-ttu-id="043e2-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="043e2-115">Remarks</span></span>

<span data-ttu-id="043e2-116">Para a codificação de taxa de bits variável (VBR) de duas passagens, o valor zero indica que o intervalo de tempo é a duração total do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="043e2-116">For two-pass variable bit rate (VBR) encoding, the value zero indicates that the time interval is the entire duration of the content.</span></span> <span data-ttu-id="043e2-117">Para a codificação de taxa de bits constante de passagem única (CBR), o valor zero indica que o codificador seleciona o intervalo (normalmente 0,5 segundos).</span><span class="sxs-lookup"><span data-stu-id="043e2-117">For single-pass constant bit rate (CBR) encoding, the value zero indicates that the encoder selects the interval (typically 0.5 seconds).</span></span>

## <a name="requirements"></a><span data-ttu-id="043e2-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="043e2-118">Requirements</span></span>



| <span data-ttu-id="043e2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="043e2-119">Requirement</span></span> | <span data-ttu-id="043e2-120">Valor</span><span class="sxs-lookup"><span data-stu-id="043e2-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="043e2-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="043e2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="043e2-122">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="043e2-122">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="043e2-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="043e2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="043e2-124">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="043e2-124">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="043e2-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="043e2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="043e2-126"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="043e2-126"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="043e2-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="043e2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="043e2-128">Propriedades da API do codec</span><span class="sxs-lookup"><span data-stu-id="043e2-128">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="043e2-129">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="043e2-129">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




