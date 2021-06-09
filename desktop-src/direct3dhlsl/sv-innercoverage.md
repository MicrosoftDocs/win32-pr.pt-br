---
title: SV_InnerCoverage
description: SV InputCoverage representa informações de rasterização falsas (ou seja, se um pixel tem garantia de \_ ser totalmente coberto).
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
ms.openlocfilehash: 168f90c17c9e6837d696ebb6dac8f39dc6dfb366
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826620"
---
# <a name="sv_innercoverage"></a><span data-ttu-id="52cd5-104">SV \_ InnerCoverage</span><span class="sxs-lookup"><span data-stu-id="52cd5-104">SV\_InnerCoverage</span></span>

<span data-ttu-id="52cd5-105">SV InputCoverage representa informações de rasterização falsas (ou seja, se um pixel tem garantia de \_ ser totalmente coberto).</span><span class="sxs-lookup"><span data-stu-id="52cd5-105">SV\_InputCoverage represents underestimated conservative rasterization information (i.e. whether a pixel is guaranteed-to-be-fully covered).</span></span>

## <a name="type"></a><span data-ttu-id="52cd5-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="52cd5-106">Type</span></span>



| <span data-ttu-id="52cd5-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="52cd5-107">Type</span></span>     |
|------|
| <span data-ttu-id="52cd5-108">uint</span><span class="sxs-lookup"><span data-stu-id="52cd5-108">uint</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="52cd5-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="52cd5-109">Remarks</span></span>

<span data-ttu-id="52cd5-110">Esse valor gerado pelo sistema é necessário para suporte de camada 3 e só está disponível nessa camada.</span><span class="sxs-lookup"><span data-stu-id="52cd5-110">This system generated value is required for tier 3 support, and is only available in that tier.</span></span> <span data-ttu-id="52cd5-111">Essa entrada é mutuamente exclusiva com a Cobertura SV \_ – ambas não podem ser usadas.</span><span class="sxs-lookup"><span data-stu-id="52cd5-111">This input is mutually exclusive with SV\_Coverage - both cannot be used.</span></span>

<span data-ttu-id="52cd5-112">Para acessar o InnerCoverage SV, ele deve ser declarado como um único componente de um dos registros de entrada \_ do sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="52cd5-112">To access SV\_InnerCoverage, it must be declared as a single component out of one of the pixel shader input registers.</span></span> <span data-ttu-id="52cd5-113">O modo de interpolação na declaração deve ser constante (a interpolação não se aplica).</span><span class="sxs-lookup"><span data-stu-id="52cd5-113">The interpolation mode on the declaration must be constant (interpolation does not apply).</span></span>

<span data-ttu-id="52cd5-114">A rasterização conservadora está disponível em D3D11.3 e D3D12.</span><span class="sxs-lookup"><span data-stu-id="52cd5-114">Conservative rasterization is available in both D3D11.3 and D3D12.</span></span> <span data-ttu-id="52cd5-115">Consulte:</span><span class="sxs-lookup"><span data-stu-id="52cd5-115">Refer to:</span></span>

-   [<span data-ttu-id="52cd5-116">D3D11.3 Rasterização conservadora</span><span class="sxs-lookup"><span data-stu-id="52cd5-116">D3D11.3 Conservative Rasterization</span></span>](/windows/desktop/direct3d11/conservative-rasterization)
-   [<span data-ttu-id="52cd5-117">D3D12 Rasterização conservadora</span><span class="sxs-lookup"><span data-stu-id="52cd5-117">D3D12 Conservative Rasterization</span></span>](/windows/desktop/direct3d12/conservative-rasterization)

## <a name="see-also"></a><span data-ttu-id="52cd5-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="52cd5-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52cd5-119">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="52cd5-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> <dt>

[<span data-ttu-id="52cd5-120">Valores do sistema do Modelo de Sombreador 5.1</span><span class="sxs-lookup"><span data-stu-id="52cd5-120">Shader Model 5.1 System Values</span></span>](shader-model-5-1-system-values.md)
</dt> </dl>

 

 
