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
ms.openlocfilehash: e1ac278f0524446b5171ef278e169fbe7c3a082f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996963"
---
# <a name="sv_innercoverage"></a><span data-ttu-id="1e306-104">\_INNERCOVERAGE VA</span><span class="sxs-lookup"><span data-stu-id="1e306-104">SV\_InnerCoverage</span></span>

<span data-ttu-id="1e306-105">\_A InputCoverage de VA representa informações de rasterização conservadora subestimadas (ou seja, se um pixel é garantido para ser totalmente coberto).</span><span class="sxs-lookup"><span data-stu-id="1e306-105">SV\_InputCoverage represents underestimated conservative rasterization information (i.e. whether a pixel is guaranteed-to-be-fully covered).</span></span>

## <a name="type"></a><span data-ttu-id="1e306-106">Digite</span><span class="sxs-lookup"><span data-stu-id="1e306-106">Type</span></span>



|      |
|------|
| <span data-ttu-id="1e306-107">Digite</span><span class="sxs-lookup"><span data-stu-id="1e306-107">Type</span></span> |
| <span data-ttu-id="1e306-108">uint</span><span class="sxs-lookup"><span data-stu-id="1e306-108">uint</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="1e306-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="1e306-109">Remarks</span></span>

<span data-ttu-id="1e306-110">Esse valor gerado pelo sistema é necessário para o suporte de camada 3 e só está disponível nessa camada.</span><span class="sxs-lookup"><span data-stu-id="1e306-110">This system generated value is required for tier 3 support, and is only available in that tier.</span></span> <span data-ttu-id="1e306-111">Essa entrada é mutuamente exclusiva com \_ cobertura de VA-ambas não podem ser usadas.</span><span class="sxs-lookup"><span data-stu-id="1e306-111">This input is mutually exclusive with SV\_Coverage - both cannot be used.</span></span>

<span data-ttu-id="1e306-112">Para acessar a \_ InnerCoverage de VA, ela deve ser declarada como um único componente de um dos registros de entrada do sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="1e306-112">To access SV\_InnerCoverage, it must be declared as a single component out of one of the pixel shader input registers.</span></span> <span data-ttu-id="1e306-113">O modo de interpolação na declaração deve ser constante (interpolação não se aplica).</span><span class="sxs-lookup"><span data-stu-id="1e306-113">The interpolation mode on the declaration must be constant (interpolation does not apply).</span></span>

<span data-ttu-id="1e306-114">A rasterização conservadora está disponível no D3D 11.3 e no D3D12.</span><span class="sxs-lookup"><span data-stu-id="1e306-114">Conservative rasterization is available in both D3D11.3 and D3D12.</span></span> <span data-ttu-id="1e306-115">Consulte:</span><span class="sxs-lookup"><span data-stu-id="1e306-115">Refer to:</span></span>

-   [<span data-ttu-id="1e306-116">Rasterização conservadora de D3D 11.3</span><span class="sxs-lookup"><span data-stu-id="1e306-116">D3D11.3 Conservative Rasterization</span></span>](/windows/desktop/direct3d11/conservative-rasterization)
-   [<span data-ttu-id="1e306-117">Rasterização D3D12 conservadora</span><span class="sxs-lookup"><span data-stu-id="1e306-117">D3D12 Conservative Rasterization</span></span>](/windows/desktop/direct3d12/conservative-rasterization)

## <a name="see-also"></a><span data-ttu-id="1e306-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="1e306-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e306-119">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="1e306-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> <dt>

[<span data-ttu-id="1e306-120">Valores de sistema do modelo do sombreador 5,1</span><span class="sxs-lookup"><span data-stu-id="1e306-120">Shader Model 5.1 System Values</span></span>](shader-model-5-1-system-values.md)
</dt> </dl>

 

 
