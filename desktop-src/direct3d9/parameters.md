---
description: Os parâmetros são variáveis de efeito.
ms.assetid: vs|directx_sdk|~\parameters.htm
title: Parâmetros (Direct3D 9)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e5c78a4f6c0518c99b61be10b721d98b17630ab
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104088799"
---
# <a name="parameters-direct3d-9"></a><span data-ttu-id="7787c-103">Parâmetros (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="7787c-103">Parameters (Direct3D 9)</span></span>

<span data-ttu-id="7787c-104">Os parâmetros são variáveis de efeito.</span><span class="sxs-lookup"><span data-stu-id="7787c-104">Parameters are effect variables.</span></span>

## <a name="syntax"></a><span data-ttu-id="7787c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7787c-105">Syntax</span></span>

<span data-ttu-id="7787c-106">*ID do tipo de uso* \[ :  \] \[ < *expressão de anotação semântica (s)* > \] \[ =   \] ;</span><span class="sxs-lookup"><span data-stu-id="7787c-106">*usage type ID* \[: *semantic*\] \[<*annotation(s)*>\] \[= *expression*\];</span></span>

<span data-ttu-id="7787c-107">Os parâmetros podem ser lidos e gravados pelo aplicativo com [**ID3DXEffect**](id3dxeffect.md) ou [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).</span><span class="sxs-lookup"><span data-stu-id="7787c-107">Parameters can be read from and written to by the application with [**ID3DXEffect**](id3dxeffect.md) or [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).</span></span>

<span data-ttu-id="7787c-108">Os parâmetros podem ser referenciados em funções e em técnicas (especificamente, no lado direito das atribuições de estado).</span><span class="sxs-lookup"><span data-stu-id="7787c-108">Parameters can be referenced in functions and in techniques (specifically, in the right side of state assignments).</span></span>



| <span data-ttu-id="7787c-109">Item</span><span class="sxs-lookup"><span data-stu-id="7787c-109">Item</span></span>                                                                                 | <span data-ttu-id="7787c-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="7787c-110">Description</span></span>                                                                                                                                                     |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7787c-111"><span id="usage"></span><span id="USAGE"></span>*usos*</span><span class="sxs-lookup"><span data-stu-id="7787c-111"><span id="usage"></span><span id="USAGE"></span>*usage*</span></span><br/>                   | <span data-ttu-id="7787c-112">Escopo do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="7787c-112">Scope of the parameter.</span></span> <span data-ttu-id="7787c-113">Consulte [usos e literais (Direct3D 9)](usages-and-literals.md).</span><span class="sxs-lookup"><span data-stu-id="7787c-113">See [Usages and Literals (Direct3D 9)](usages-and-literals.md).</span></span><br/>                                                             |
| <span data-ttu-id="7787c-114"><span id="type"></span><span id="TYPE"></span>*Escreva*</span><span class="sxs-lookup"><span data-stu-id="7787c-114"><span id="type"></span><span id="TYPE"></span>*type*</span></span><br/>                      | <span data-ttu-id="7787c-115">Qualquer [referência válida para](../direct3dhlsl/dx-graphics-hlsl-reference.md) o tipo HLSL.</span><span class="sxs-lookup"><span data-stu-id="7787c-115">Any valid [Reference for HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md) type.</span></span><br/>                                                                        |
| <span data-ttu-id="7787c-116"><span id="ID"></span><span id="id"></span>*SESSÃO*</span><span class="sxs-lookup"><span data-stu-id="7787c-116"><span id="ID"></span><span id="id"></span>*ID*</span></span><br/>                            | <span data-ttu-id="7787c-117">Um nome exclusivo.</span><span class="sxs-lookup"><span data-stu-id="7787c-117">A unique name.</span></span><br/>                                                                                                                                       |
| <span data-ttu-id="7787c-118"><span id="semantic"></span><span id="SEMANTIC"></span>*semântico*</span><span class="sxs-lookup"><span data-stu-id="7787c-118"><span id="semantic"></span><span id="SEMANTIC"></span>*semantic*</span></span><br/>          | <span data-ttu-id="7787c-119">Uma marca que segue as regras de identificador que normalmente indicam o uso do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="7787c-119">A tag following identifier rules that typically indicates the usage of the parameter.</span></span> <span data-ttu-id="7787c-120">Deve ser um tipo específico.</span><span class="sxs-lookup"><span data-stu-id="7787c-120">Must be a particular type.</span></span><br/>                                     |
| <span data-ttu-id="7787c-121"><span id="annotations"></span><span id="ANNOTATIONS"></span>*anotações*</span><span class="sxs-lookup"><span data-stu-id="7787c-121"><span id="annotations"></span><span id="ANNOTATIONS"></span>*annotations*</span></span><br/> | <span data-ttu-id="7787c-122">Zero ou mais partes de informações específicas do usuário.</span><span class="sxs-lookup"><span data-stu-id="7787c-122">Zero or more pieces of user-specific information.</span></span> <span data-ttu-id="7787c-123">Pode ser qualquer tipo.</span><span class="sxs-lookup"><span data-stu-id="7787c-123">May be any type.</span></span> <span data-ttu-id="7787c-124">Consulte [adicionar informações para parâmetros de efeito com anotações](using-an-effect.md).</span><span class="sxs-lookup"><span data-stu-id="7787c-124">See [Add Information to Effect Parameters with Annotations](using-an-effect.md).</span></span><br/> |
| <span data-ttu-id="7787c-125"><span id="expression"></span><span id="EXPRESSION"></span>*expressão*</span><span class="sxs-lookup"><span data-stu-id="7787c-125"><span id="expression"></span><span id="EXPRESSION"></span>*expression*</span></span><br/>    | <span data-ttu-id="7787c-126">Inicializa o valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="7787c-126">Initializes the parameter's value.</span></span> <span data-ttu-id="7787c-127">Consulte [Expressions (Direct3D 9)](expressions.md).</span><span class="sxs-lookup"><span data-stu-id="7787c-127">See [Expressions (Direct3D 9)](expressions.md).</span></span><br/>                                                                  |



 

<span data-ttu-id="7787c-128">Os parâmetros podem ser inicializados para qualquer [referência válida para](../direct3dhlsl/dx-graphics-hlsl-reference.md) a expressão HLSL que reduz para um valor literal.</span><span class="sxs-lookup"><span data-stu-id="7787c-128">Parameters can be initialized to any valid [Reference for HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md) expression that reduces to a literal value.</span></span>

<span data-ttu-id="7787c-129">Os valores de parâmetro não são alterados pela execução da atribuição de estado ou chamadas de função.</span><span class="sxs-lookup"><span data-stu-id="7787c-129">Parameter values are not changed by the execution of state assignment or function calls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7787c-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7787c-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7787c-131">Formato do efeito</span><span class="sxs-lookup"><span data-stu-id="7787c-131">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 
