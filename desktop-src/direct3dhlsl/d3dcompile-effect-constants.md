---
title: Constantes de D3DCOMPILE_EFFECT (D3DCompiler. h)
description: Essas constantes direcionam como o compilador compila um arquivo de efeito ou como o tempo de execução processa o arquivo de efeito.
ms.assetid: AA46E5ED-92DD-4327-B852-8DD23A878562
topic_type:
- apiref
api_name:
- D3DCOMPILE_EFFECT_CHILD_EFFECT
- D3DCOMPILE_EFFECT_ALLOW_SLOW_OPS
api_location:
- D3DCompiler.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69f0597341a331af82ed279a6030126d222b70f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968555"
---
# <a name="d3dcompile_effect-constants"></a><span data-ttu-id="aac70-103">Constantes de efeito de D3DCOMPILE \_</span><span class="sxs-lookup"><span data-stu-id="aac70-103">D3DCOMPILE\_EFFECT Constants</span></span>

<span data-ttu-id="aac70-104">Essas constantes direcionam como o compilador compila um arquivo de efeito ou como o tempo de execução processa o arquivo de efeito.</span><span class="sxs-lookup"><span data-stu-id="aac70-104">These constants direct how the compiler compiles an effect file or how the runtime processes the effect file.</span></span>

<dl> <dt>

<span data-ttu-id="aac70-105"><span id="D3DCOMPILE_EFFECT_CHILD_EFFECT"></span><span id="d3dcompile_effect_child_effect"></span>**\_ \_ Efeito filho de efeito de D3DCOMPILE \_**</span><span class="sxs-lookup"><span data-stu-id="aac70-105"><span id="D3DCOMPILE_EFFECT_CHILD_EFFECT"></span><span id="d3dcompile_effect_child_effect"></span>**D3DCOMPILE\_EFFECT\_CHILD\_EFFECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aac70-106">(1 << 0)</span><span class="sxs-lookup"><span data-stu-id="aac70-106">(1 << 0)</span></span>
</dt> <dt>



<span data-ttu-id="aac70-107">Compile o arquivo de efeitos (. FX) para um efeito filho.</span><span class="sxs-lookup"><span data-stu-id="aac70-107">Compile the effects (.fx) file to a child effect.</span></span> <span data-ttu-id="aac70-108">Os efeitos filho não têm inicializadores para nenhum valor compartilhado porque esses efeitos filho são inicializados no efeito mestre (o pool de efeitos).</span><span class="sxs-lookup"><span data-stu-id="aac70-108">Child effects have no initializers for any shared values because these child effects are initialized in the master effect (the effect pool).</span></span>

> [!Note]  
> <span data-ttu-id="aac70-109">Os pools de efeitos têm suporte dos efeitos 10 (FX10), mas não dos efeitos 11 (FX11).</span><span class="sxs-lookup"><span data-stu-id="aac70-109">Effect pools are supported by Effects 10 (FX10) but not by Effects 11 (FX11).</span></span> <span data-ttu-id="aac70-110">Para obter mais informações sobre as diferenças entre pools de efeito no Direct3D 10 e em grupos de efeitos no Direct3D 11, consulte [pools de efeitos e grupos](/windows/desktop/direct3d11/d3d11-graphics-programming-guide-effects-differences).</span><span class="sxs-lookup"><span data-stu-id="aac70-110">For more info about differences between effect pools in Direct3D 10 and effect groups in Direct3D 11, see [Effect Pools and Groups](/windows/desktop/direct3d11/d3d11-graphics-programming-guide-effects-differences).</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="aac70-111"><span id="D3DCOMPILE_EFFECT_ALLOW_SLOW_OPS"></span><span id="d3dcompile_effect_allow_slow_ops"></span>**\_Efeito D3DCOMPILE \_ permitir \_ operações lentas \_**</span><span class="sxs-lookup"><span data-stu-id="aac70-111"><span id="D3DCOMPILE_EFFECT_ALLOW_SLOW_OPS"></span><span id="d3dcompile_effect_allow_slow_ops"></span>**D3DCOMPILE\_EFFECT\_ALLOW\_SLOW\_OPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aac70-112">(1 << 1)</span><span class="sxs-lookup"><span data-stu-id="aac70-112">(1 << 1)</span></span>
</dt> <dt>



<span data-ttu-id="aac70-113">Desabilita o modo de desempenho e permite objetos de estado mutável.</span><span class="sxs-lookup"><span data-stu-id="aac70-113">Disables performance mode and allows for mutable state objects.</span></span>

<span data-ttu-id="aac70-114">Por padrão, o modo de desempenho está habilitado.</span><span class="sxs-lookup"><span data-stu-id="aac70-114">By default, performance mode is enabled.</span></span> <span data-ttu-id="aac70-115">O modo de desempenho não permite objetos de estado mutável, impedindo que expressões não literais apareçam nas definições de objeto de estado.</span><span class="sxs-lookup"><span data-stu-id="aac70-115">Performance mode disallows mutable state objects by preventing non-literal expressions from appearing in state object definitions.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="aac70-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aac70-116">Requirements</span></span>



| <span data-ttu-id="aac70-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="aac70-117">Requirement</span></span> | <span data-ttu-id="aac70-118">Valor</span><span class="sxs-lookup"><span data-stu-id="aac70-118">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="aac70-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="aac70-119">Header</span></span><br/> | <dl> <span data-ttu-id="aac70-120"><dt>D3DCompiler. h</dt></span><span class="sxs-lookup"><span data-stu-id="aac70-120"><dt>D3DCompiler.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aac70-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="aac70-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aac70-122">Constantes D3DCompiler</span><span class="sxs-lookup"><span data-stu-id="aac70-122">D3DCompiler Constants</span></span>](dx-graphics-d3dcompiler-reference-constants.md)
</dt> </dl>

 

