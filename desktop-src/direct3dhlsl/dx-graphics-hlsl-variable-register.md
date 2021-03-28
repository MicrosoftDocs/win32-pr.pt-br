---
title: register
description: register
ms.assetid: 45149f8c-8b76-4247-98d7-d141d7268da3
keywords:
- registrar HLSL
topic_type:
- apiref
api_name:
- register
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2b378cd97bc9779951d62873d393009c98d32823
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366044"
---
# <a name="register"></a><span data-ttu-id="4a4f0-104">register</span><span class="sxs-lookup"><span data-stu-id="4a4f0-104">register</span></span>

<span data-ttu-id="4a4f0-105">Palavra-chave opcional para atribuir uma variável de sombreador a um registro específico, que usa a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="4a4f0-105">Optional keyword for assigning a shader variable to a particular register, which uses the following syntax:</span></span>



| <span data-ttu-id="4a4f0-106">: Register ( *\[ \_ perfil \] do sombreador*, *tipo \# \[ subcomponente \]* )</span><span class="sxs-lookup"><span data-stu-id="4a4f0-106">: register ( *\[shader\_profile\]*, *Type\#\[subcomponent\]* )</span></span> |
|----------------------------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="4a4f0-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4a4f0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a4f0-108"><span id="register"></span><span id="REGISTER"></span>Registr</span><span class="sxs-lookup"><span data-stu-id="4a4f0-108"><span id="register"></span><span id="REGISTER"></span>register</span></span>
</dt> <dd>

<span data-ttu-id="4a4f0-109">Palavra-chave required.</span><span class="sxs-lookup"><span data-stu-id="4a4f0-109">Required keyword.</span></span>

</dd> <dt>

<span data-ttu-id="4a4f0-110"><span id="_shader_profile_"></span><span id="_SHADER_PROFILE_"></span>*\[perfil do sombreador \_\]*</span><span class="sxs-lookup"><span data-stu-id="4a4f0-110"><span id="_shader_profile_"></span><span id="_SHADER_PROFILE_"></span>*\[shader\_profile\]*</span></span>
</dt> <dd>

<span data-ttu-id="4a4f0-111">[Perfil de sombreador](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax)opcional, que pode ser um alvo de sombreador ou simplesmente **PS** ou **vs**.</span><span class="sxs-lookup"><span data-stu-id="4a4f0-111">Optional [shader profile](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax), which can be a shader target or simply **ps** or **vs**.</span></span>

</dd> <dt>

<span data-ttu-id="4a4f0-112"><span id="Type__subcomponent_"></span><span id="type__subcomponent_"></span><span id="TYPE__SUBCOMPONENT_"></span>*Subcomponente do tipo \# \[\]*</span><span class="sxs-lookup"><span data-stu-id="4a4f0-112"><span id="Type__subcomponent_"></span><span id="type__subcomponent_"></span><span id="TYPE__SUBCOMPONENT_"></span>*Type\#\[subcomponent\]*</span></span>
</dt> <dd>

<span data-ttu-id="4a4f0-113">Tipo de registro, número e declaração de subcomponente.</span><span class="sxs-lookup"><span data-stu-id="4a4f0-113">Register type, number, and subcomponent declaration.</span></span>

-   <span data-ttu-id="4a4f0-114">O tipo é um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="4a4f0-114">Type is one of the following:</span></span>

    

    | <span data-ttu-id="4a4f0-115">Tipo</span><span class="sxs-lookup"><span data-stu-id="4a4f0-115">Type</span></span> | <span data-ttu-id="4a4f0-116">Descrição do registro</span><span class="sxs-lookup"><span data-stu-id="4a4f0-116">Register Description</span></span>       |
    |------|----------------------------|
    | <span data-ttu-id="4a4f0-117">b</span><span class="sxs-lookup"><span data-stu-id="4a4f0-117">b</span></span>    | <span data-ttu-id="4a4f0-118">Buffer constante</span><span class="sxs-lookup"><span data-stu-id="4a4f0-118">Constant buffer</span></span>            |
    | <span data-ttu-id="4a4f0-119">t</span><span class="sxs-lookup"><span data-stu-id="4a4f0-119">t</span></span>    | <span data-ttu-id="4a4f0-120">Buffer de textura e texturização</span><span class="sxs-lookup"><span data-stu-id="4a4f0-120">Texture and texture buffer</span></span> |
    | <span data-ttu-id="4a4f0-121">c</span><span class="sxs-lookup"><span data-stu-id="4a4f0-121">c</span></span>    | <span data-ttu-id="4a4f0-122">Deslocamento do buffer</span><span class="sxs-lookup"><span data-stu-id="4a4f0-122">Buffer offset</span></span>              |
    | <span data-ttu-id="4a4f0-123">s</span><span class="sxs-lookup"><span data-stu-id="4a4f0-123">s</span></span>    | <span data-ttu-id="4a4f0-124">Exemplo</span><span class="sxs-lookup"><span data-stu-id="4a4f0-124">Sampler</span></span>                    |
    | <span data-ttu-id="4a4f0-125">u</span><span class="sxs-lookup"><span data-stu-id="4a4f0-125">u</span></span>    | <span data-ttu-id="4a4f0-126">Modo de exibição de acesso não ordenado</span><span class="sxs-lookup"><span data-stu-id="4a4f0-126">Unordered Access View</span></span>      |

    

     

-   <span data-ttu-id="4a4f0-127">*\#* é o número do registro, que é um número inteiro.</span><span class="sxs-lookup"><span data-stu-id="4a4f0-127">*\#* is the register number, which is an integer number.</span></span>
-   <span data-ttu-id="4a4f0-128">O *subcomponente* é um número inteiro opcional.</span><span class="sxs-lookup"><span data-stu-id="4a4f0-128">The *subcomponent* is an optional integer number.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4a4f0-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="4a4f0-129">Remarks</span></span>

<span data-ttu-id="4a4f0-130">Você pode adicionar uma ou mais atribuições de registro à mesma declaração de variável, separadas por espaços.</span><span class="sxs-lookup"><span data-stu-id="4a4f0-130">You may add one or more register assignments to the same variable declaration, separated by spaces.</span></span>

<span data-ttu-id="4a4f0-131">Para as variáveis do Direct3D 10 no escopo global, a palavra-chave **Register** atua da mesma forma que a palavra-chave [PACKOFFSET (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md) .</span><span class="sxs-lookup"><span data-stu-id="4a4f0-131">For Direct3D 10 variables in global scope, the **register** keyword acts the same as the [packoffset (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md) keyword.</span></span>

## <a name="examples"></a><span data-ttu-id="4a4f0-132">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4a4f0-132">Examples</span></span>

<span data-ttu-id="4a4f0-133">Estes são alguns exemplos:</span><span class="sxs-lookup"><span data-stu-id="4a4f0-133">Here are some examples:</span></span>


```
sampler myVar : register( ps_5_0, s ); 
```




```
sampler myVar : register( vs, s[8] );
```




```
sampler myVar : register( ps, s[2] ) 
              : register( ps_5_0, s[0] ) 
              : register( vs, s[8] );
```



## <a name="see-also"></a><span data-ttu-id="4a4f0-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="4a4f0-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a4f0-135">Sintaxe de Variável</span><span class="sxs-lookup"><span data-stu-id="4a4f0-135">Variable Syntax</span></span>](dx-graphics-hlsl-variable-syntax.md)
</dt> <dt>

[<span data-ttu-id="4a4f0-136">Variáveis (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4a4f0-136">Variables (DirectX HLSL)</span></span>](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

 