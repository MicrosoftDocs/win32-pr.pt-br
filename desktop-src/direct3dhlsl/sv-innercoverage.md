---
title: SV_InnerCoverage
description: '\_A InputCoverage de VA representa informações de rasterização conservadora subestimadas (ou seja, se um pixel é garantido para ser totalmente coberto).'
ms.assetid: 5BB3C3FB-E5ED-4395-B389-300DE67C984B
keywords:
- SV_InnerCoverage HLSL
topic_type:
- apiref
api_name:
- SV_InnerCoverage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2f1393a6a11a95c8c08746f57083fe193791a60
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104988700"
---
# <a name="sv_innercoverage"></a><span data-ttu-id="e7dda-104">\_INNERCOVERAGE VA</span><span class="sxs-lookup"><span data-stu-id="e7dda-104">SV\_InnerCoverage</span></span>

<span data-ttu-id="e7dda-105">\_A InputCoverage de VA representa informações de rasterização conservadora subestimadas (ou seja, se um pixel é garantido para ser totalmente coberto).</span><span class="sxs-lookup"><span data-stu-id="e7dda-105">SV\_InputCoverage represents underestimated conservative rasterization information (i.e. whether a pixel is guaranteed-to-be-fully covered).</span></span>

## <a name="type"></a><span data-ttu-id="e7dda-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="e7dda-106">Type</span></span>



|      |
|------|
| <span data-ttu-id="e7dda-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="e7dda-107">Type</span></span> |
| <span data-ttu-id="e7dda-108">uint</span><span class="sxs-lookup"><span data-stu-id="e7dda-108">uint</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="e7dda-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="e7dda-109">Remarks</span></span>

<span data-ttu-id="e7dda-110">Esse valor gerado pelo sistema é necessário para o suporte de camada 3 e só está disponível nessa camada.</span><span class="sxs-lookup"><span data-stu-id="e7dda-110">This system generated value is required for tier 3 support, and is only available in that tier.</span></span> <span data-ttu-id="e7dda-111">Essa entrada é mutuamente exclusiva com \_ cobertura de VA-ambas não podem ser usadas.</span><span class="sxs-lookup"><span data-stu-id="e7dda-111">This input is mutually exclusive with SV\_Coverage - both cannot be used.</span></span>

<span data-ttu-id="e7dda-112">Para acessar a \_ InnerCoverage de VA, ela deve ser declarada como um único componente de um dos registros de entrada do sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="e7dda-112">To access SV\_InnerCoverage, it must be declared as a single component out of one of the pixel shader input registers.</span></span> <span data-ttu-id="e7dda-113">O modo de interpolação na declaração deve ser constante (interpolação não se aplica).</span><span class="sxs-lookup"><span data-stu-id="e7dda-113">The interpolation mode on the declaration must be constant (interpolation does not apply).</span></span>

<span data-ttu-id="e7dda-114">A rasterização conservadora está disponível no D3D 11.3 e no D3D12.</span><span class="sxs-lookup"><span data-stu-id="e7dda-114">Conservative rasterization is available in both D3D11.3 and D3D12.</span></span> <span data-ttu-id="e7dda-115">Consulte:</span><span class="sxs-lookup"><span data-stu-id="e7dda-115">Refer to:</span></span>

-   [<span data-ttu-id="e7dda-116">Rasterização conservadora de D3D 11.3</span><span class="sxs-lookup"><span data-stu-id="e7dda-116">D3D11.3 Conservative Rasterization</span></span>](/windows/desktop/direct3d11/conservative-rasterization)
-   [<span data-ttu-id="e7dda-117">Rasterização D3D12 conservadora</span><span class="sxs-lookup"><span data-stu-id="e7dda-117">D3D12 Conservative Rasterization</span></span>](/windows/desktop/direct3d12/conservative-rasterization)

## <a name="see-also"></a><span data-ttu-id="e7dda-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="e7dda-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7dda-119">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="e7dda-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> <dt>

[<span data-ttu-id="e7dda-120">Valores de sistema do modelo do sombreador 5,1</span><span class="sxs-lookup"><span data-stu-id="e7dda-120">Shader Model 5.1 System Values</span></span>](shader-model-5-1-system-values.md)
</dt> </dl>

 

 