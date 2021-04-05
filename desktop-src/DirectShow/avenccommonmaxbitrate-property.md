---
description: Especifica a taxa de bits máxima, em bits por segundo. Essa propriedade só se aplica a constantes de taxa de bits constante (CBR) e a taxa de bits variável (VBR).
ms.assetid: 053fdad0-dc5f-4af1-84a6-bb7c0dac7e79
title: Propriedade AVEncCommonMaxBitRate (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d03844935e909591b2fe3c7244db79e77e7936f1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825957"
---
# <a name="avenccommonmaxbitrate-property"></a><span data-ttu-id="a2e92-104">Propriedade AVEncCommonMaxBitRate</span><span class="sxs-lookup"><span data-stu-id="a2e92-104">AVEncCommonMaxBitRate property</span></span>

<span data-ttu-id="a2e92-105">Especifica a taxa de bits máxima, em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="a2e92-105">Specifies the maximum bit rate, in bits per second.</span></span> <span data-ttu-id="a2e92-106">Essa propriedade só se aplica a constantes de taxa de bits constante (CBR) e a taxa de bits variável (VBR).</span><span class="sxs-lookup"><span data-stu-id="a2e92-106">This property applies only to constant bit rate (CBR) and variable bit rate (VBR) encoding modes.</span></span>

<span data-ttu-id="a2e92-107">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="a2e92-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="a2e92-108">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="a2e92-108">Data type</span></span>

<span data-ttu-id="a2e92-109">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="a2e92-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="a2e92-110">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="a2e92-110">Property GUID</span></span>

<span data-ttu-id="a2e92-111">**CODECAPI \_ AVEncCommonMaxBitRate**</span><span class="sxs-lookup"><span data-stu-id="a2e92-111">**CODECAPI\_AVEncCommonMaxBitRate**</span></span>

## <a name="property-value"></a><span data-ttu-id="a2e92-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="a2e92-112">Property value</span></span>

<span data-ttu-id="a2e92-113">Esta propriedade tem um intervalo linear de valores.</span><span class="sxs-lookup"><span data-stu-id="a2e92-113">This property has a linear range of values.</span></span> <span data-ttu-id="a2e92-114">Para obter o intervalo com suporte, chame [**ICodecAPI:: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="a2e92-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="requirements"></a><span data-ttu-id="a2e92-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2e92-115">Requirements</span></span>



| <span data-ttu-id="a2e92-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2e92-116">Requirement</span></span> | <span data-ttu-id="a2e92-117">Valor</span><span class="sxs-lookup"><span data-stu-id="a2e92-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a2e92-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a2e92-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a2e92-119">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="a2e92-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="a2e92-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a2e92-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a2e92-121">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="a2e92-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="a2e92-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a2e92-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2e92-123"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2e92-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2e92-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="a2e92-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2e92-125">Propriedades da API do codec</span><span class="sxs-lookup"><span data-stu-id="a2e92-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="a2e92-126">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="a2e92-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




