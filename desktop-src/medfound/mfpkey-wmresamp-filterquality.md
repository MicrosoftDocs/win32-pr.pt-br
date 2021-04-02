---
description: Especifica a qualidade da saída.
ms.assetid: 7b45633b-7f1c-4951-a462-ad6240b9ca31
title: Propriedade MFPKEY_WMRESAMP_FILTERQUALITY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4027d4bc3c0306240986cf632e171fa9a59ed18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164918"
---
# <a name="mfpkey_wmresamp_filterquality-property"></a><span data-ttu-id="2ebce-103">\_Propriedade MFPKEY WMRESAMP \_ FILTERQUALITY</span><span class="sxs-lookup"><span data-stu-id="2ebce-103">MFPKEY\_WMRESAMP\_FILTERQUALITY Property</span></span>

<span data-ttu-id="2ebce-104">Especifica a qualidade da saída.</span><span class="sxs-lookup"><span data-stu-id="2ebce-104">Specifies the quality of the output.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="2ebce-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="2ebce-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="2ebce-106">Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="2ebce-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="2ebce-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="2ebce-107">Data Type</span></span>

<span data-ttu-id="2ebce-108">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="2ebce-108">VT\_I4</span></span>

## <a name="applies-to"></a><span data-ttu-id="2ebce-109">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="2ebce-109">Applies To</span></span>

-   [<span data-ttu-id="2ebce-110">DSP de reamostragem de áudio</span><span class="sxs-lookup"><span data-stu-id="2ebce-110">Audio Resampler DSP</span></span>](audioresampler.md)

## <a name="remarks"></a><span data-ttu-id="2ebce-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="2ebce-111">Remarks</span></span>

<span data-ttu-id="2ebce-112">O intervalo válido dessa propriedade é de 1 a 60, inclusive.</span><span class="sxs-lookup"><span data-stu-id="2ebce-112">The valid range of this property is 1 to 60, inclusive.</span></span> <span data-ttu-id="2ebce-113">Valores mais altos produzem saída de qualidade mais alta, mas apresentam mais latência.</span><span class="sxs-lookup"><span data-stu-id="2ebce-113">Higher values produce higher-quality output, but introduce more latency.</span></span> <span data-ttu-id="2ebce-114">Um valor de 1 é essencialmente o mesmo que a interpolação linear.</span><span class="sxs-lookup"><span data-stu-id="2ebce-114">A value of 1 is essentially the same as linear interpolation.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ebce-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ebce-115">Requirements</span></span>



| <span data-ttu-id="2ebce-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ebce-116">Requirement</span></span> | <span data-ttu-id="2ebce-117">Valor</span><span class="sxs-lookup"><span data-stu-id="2ebce-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2ebce-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2ebce-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2ebce-119">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2ebce-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2ebce-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2ebce-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2ebce-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2ebce-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2ebce-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2ebce-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ebce-123"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ebce-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ebce-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="2ebce-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ebce-125">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2ebce-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
