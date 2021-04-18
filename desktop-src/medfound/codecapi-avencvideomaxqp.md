---
description: Especifica o máximo de QP com suporte pelo codificador.
ms.assetid: 2C02F82B-E645-4C5B-9526-5E130A6E2F67
title: Propriedade CODECAPI_AVEncVideoMaxQP (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9bcf23866da5530d2edc1203be359071e5e33e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763229"
---
# <a name="codecapi_avencvideomaxqp-property"></a><span data-ttu-id="cfd96-103">\_Propriedade CODECAPI AVEncVideoMaxQP</span><span class="sxs-lookup"><span data-stu-id="cfd96-103">CODECAPI\_AVEncVideoMaxQP property</span></span>

<span data-ttu-id="cfd96-104">Especifica o máximo de QP com suporte pelo codificador.</span><span class="sxs-lookup"><span data-stu-id="cfd96-104">Specifies the maximum QP supported by the encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="cfd96-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="cfd96-105">Data type</span></span>

<span data-ttu-id="cfd96-106">**ULONG** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="cfd96-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="cfd96-107">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="cfd96-107">Property GUID</span></span>

<span data-ttu-id="cfd96-108">**CODECAPI \_ AVEncVideoMaxQP**</span><span class="sxs-lookup"><span data-stu-id="cfd96-108">**CODECAPI\_AVEncVideoMaxQP**</span></span>

## <a name="remarks"></a><span data-ttu-id="cfd96-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="cfd96-109">Remarks</span></span>

<span data-ttu-id="cfd96-110">**Codificadores H. 264/AVC:**</span><span class="sxs-lookup"><span data-stu-id="cfd96-110">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="cfd96-111">O codificador deve dar suporte a [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**DefinirValor**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)e [**GetParameterRange**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="cfd96-111">The encoder shall support [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue), and [**GetParameterRange**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

<span data-ttu-id="cfd96-112">Essa é uma propriedade estática, o que significa que ela só pode ser definida antes do início da sessão de codificação.</span><span class="sxs-lookup"><span data-stu-id="cfd96-112">This is a static property meaning that it can only be set before the encoding session starts.</span></span>

<span data-ttu-id="cfd96-113">O valor padrão deve ser o máximo QP permitido pelo padrão de codificação correspondente.</span><span class="sxs-lookup"><span data-stu-id="cfd96-113">Default value shall be the max QP allowed by the corresponding coding standard.</span></span> <span data-ttu-id="cfd96-114">Por exemplo, os codificadores H. 264 devem ter um valor padrão de 51.</span><span class="sxs-lookup"><span data-stu-id="cfd96-114">For example, H.264 encoders shall have a default value of 51.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfd96-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cfd96-115">Requirements</span></span>



| <span data-ttu-id="cfd96-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="cfd96-116">Requirement</span></span> | <span data-ttu-id="cfd96-117">Valor</span><span class="sxs-lookup"><span data-stu-id="cfd96-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cfd96-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cfd96-118">Minimum supported client</span></span><br/> | <span data-ttu-id="cfd96-119">Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="cfd96-119">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="cfd96-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cfd96-120">Minimum supported server</span></span><br/> | <span data-ttu-id="cfd96-121">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="cfd96-121">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="cfd96-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cfd96-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfd96-123"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="cfd96-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfd96-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="cfd96-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfd96-125">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cfd96-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="cfd96-126">CODECAPI \_ AVEncVideoMinQP</span><span class="sxs-lookup"><span data-stu-id="cfd96-126">CODECAPI\_AVEncVideoMinQP</span></span>](codecapi-avencvideominqp.md)
</dt> </dl>

 

