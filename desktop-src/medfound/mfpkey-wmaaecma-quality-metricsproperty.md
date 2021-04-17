---
description: Recupera métricas de qualidade no AEC (cancelamento de eco acústico) do DSP de captura de voz.
ms.assetid: de2e86ae-0469-471f-9105-0bb38a59b428
title: Propriedade MFPKEY_WMAAECMA_QUALITY_METRICS (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3740630bc23c4e3e0e824e55b4e34bcd8b1347f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759858"
---
# <a name="mfpkey_wmaaecma_quality_metrics-property"></a><span data-ttu-id="13574-103">\_Propriedade de \_ métricas de qualidade MFPKEY WMAAECMA \_</span><span class="sxs-lookup"><span data-stu-id="13574-103">MFPKEY\_WMAAECMA\_QUALITY\_METRICS Property</span></span>

<span data-ttu-id="13574-104">Recupera métricas de qualidade no AEC (cancelamento de eco acústico) do DSP de captura de voz.</span><span class="sxs-lookup"><span data-stu-id="13574-104">Retrieves quality metrics on acoustic echo cancellation (AEC) from the Voice Capture DSP.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="13574-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="13574-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="13574-106">Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="13574-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="13574-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="13574-107">Data Type</span></span>

<span data-ttu-id="13574-108">\_blob VT</span><span class="sxs-lookup"><span data-stu-id="13574-108">VT\_BLOB</span></span>

## <a name="remarks"></a><span data-ttu-id="13574-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="13574-109">Remarks</span></span>

<span data-ttu-id="13574-110">O valor dessa propriedade é uma estrutura [de \_ struct AecQualityMetrics](/windows/win32/api/wmcodecdsp/ns-wmcodecdsp-aecqualitymetrics_struct) .</span><span class="sxs-lookup"><span data-stu-id="13574-110">The value of this property is an [AecQualityMetrics\_Struct](/windows/win32/api/wmcodecdsp/ns-wmcodecdsp-aecqualitymetrics_struct) structure.</span></span> <span data-ttu-id="13574-111">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="13574-111">This property is read-only.</span></span>

## <a name="requirements"></a><span data-ttu-id="13574-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13574-112">Requirements</span></span>



| <span data-ttu-id="13574-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="13574-113">Requirement</span></span> | <span data-ttu-id="13574-114">Valor</span><span class="sxs-lookup"><span data-stu-id="13574-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="13574-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="13574-115">Minimum supported client</span></span><br/> | <span data-ttu-id="13574-116">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="13574-116">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="13574-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="13574-117">Minimum supported server</span></span><br/> | <span data-ttu-id="13574-118">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="13574-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="13574-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="13574-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="13574-120"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="13574-120"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13574-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="13574-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13574-122">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="13574-122">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="13574-123">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="13574-123">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
