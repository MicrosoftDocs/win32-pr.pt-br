---
title: Instrução switch (Urlmon. h)
description: Transfere o controle para um bloco de instruções diferente dentro do corpo do comutador, dependendo do valor de um seletor.
ms.assetid: d1932ee1-d789-4536-b77d-162aacdbb115
keywords:
- Instrução switch HLSL
topic_type:
- apiref
api_name:
- switch Statement
api_location:
- urlmon.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4af131ca3a126cd6f1fd54160418bfbe70cc9cce
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119071"
---
# <a name="switch-statement"></a><span data-ttu-id="dd5e9-104">Instrução Switch</span><span class="sxs-lookup"><span data-stu-id="dd5e9-104">switch Statement</span></span>

<span data-ttu-id="dd5e9-105">Transfere o controle para um bloco de instruções diferente dentro do corpo do comutador, dependendo do valor de um seletor.</span><span class="sxs-lookup"><span data-stu-id="dd5e9-105">Transfer control to a different statement block within the switch body depending on the value of a selector.</span></span>


<span data-ttu-id="dd5e9-106">\[*Atributo* \] switch ( *seletor* ) {caso 0: { *StatementBlock*;}   interrupção   caso 1: { *StatementBlock*;}   interrupção   caso n: { *StatementBlock*;}   interrupção   padrão: { *StatementBlock*;}   interrupção</span><span class="sxs-lookup"><span data-stu-id="dd5e9-106">\[*Attribute*\] switch( *Selector* ) {   case 0 :     { *StatementBlock*; }   break;   case 1 :     { *StatementBlock*; }   break;   case n :     { *StatementBlock*; }   break;   default :     { *StatementBlock*; }   break;</span></span>



 

## <a name="parameters"></a><span data-ttu-id="dd5e9-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dd5e9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd5e9-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribute*</span><span class="sxs-lookup"><span data-stu-id="dd5e9-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribute*</span></span>
</dt> <dd>

<span data-ttu-id="dd5e9-109">Um parâmetro opcional que controla como a instrução é compilada.</span><span class="sxs-lookup"><span data-stu-id="dd5e9-109">An optional parameter that controls how the statement is compiled.</span></span> <span data-ttu-id="dd5e9-110">Quando nenhum atributo é especificado, o compilador pode usar um comutador de hardware ou emitir uma série de instruções **If** .</span><span class="sxs-lookup"><span data-stu-id="dd5e9-110">When no attribute is specified, the compiler may use a hardware switch or emit a series of **if** statements.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dd5e9-111">Atributo</span><span class="sxs-lookup"><span data-stu-id="dd5e9-111">Attribute</span></span></th>
<th><span data-ttu-id="dd5e9-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="dd5e9-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dd5e9-113">mesclar</span><span class="sxs-lookup"><span data-stu-id="dd5e9-113">flatten</span></span></td>
<td><span data-ttu-id="dd5e9-114">Compile a instrução como uma série de instruções <strong>If</strong> , cada uma com o atributo de <strong>achatamento</strong> .</span><span class="sxs-lookup"><span data-stu-id="dd5e9-114">Compile the statement as a series of <strong>if</strong> statements, each with the <strong>flatten</strong> attribute.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dd5e9-115">branch</span><span class="sxs-lookup"><span data-stu-id="dd5e9-115">branch</span></span></td>
<td><span data-ttu-id="dd5e9-116">Compile a instrução como uma série de instruções <strong>If</strong> com o atributo <strong>Branch</strong> .</span><span class="sxs-lookup"><span data-stu-id="dd5e9-116">Compile the statement as a series of <strong>if</strong> statements each with the <strong>branch</strong> attribute.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="dd5e9-117">Quando você usa o modelo de <a href="dx-graphics-hlsl-sm2.md">sombreador 2. x</a> ou o <a href="dx-graphics-hlsl-sm3.md">modelo de sombreador 3,0</a>, cada vez que usa a ramificação dinâmica, você consome recursos.</span><span class="sxs-lookup"><span data-stu-id="dd5e9-117">When you use <a href="dx-graphics-hlsl-sm2.md">Shader Model 2.x</a> or <a href="dx-graphics-hlsl-sm3.md">Shader Model 3.0</a>, each time you use dynamic branching you consume resources.</span></span> <span data-ttu-id="dd5e9-118">Portanto, se você usar a ramificação dinâmica de forma excessiva ao direcionar esses perfis, poderá receber erros de compilação.</span><span class="sxs-lookup"><span data-stu-id="dd5e9-118">So, if you use dynamic branching excessively when you target these profiles, you can receive compilation errors.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dd5e9-119">forcecase</span><span class="sxs-lookup"><span data-stu-id="dd5e9-119">forcecase</span></span></td>
<td><span data-ttu-id="dd5e9-120">Force uma instrução switch no hardware.</span><span class="sxs-lookup"><span data-stu-id="dd5e9-120">Force a switch statement in the hardware.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="dd5e9-121">Requer hardware de <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">nível de recurso</a> 10_0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="dd5e9-121">Requires <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature level</a> 10_0 or later hardware.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dd5e9-122">chamada</span><span class="sxs-lookup"><span data-stu-id="dd5e9-122">call</span></span></td>
<td><span data-ttu-id="dd5e9-123">Os corpos dos casos individuais no comutador serão movidos para as sub-rotinas de hardware e o comutador será uma série de chamadas de sub-rotina.</span><span class="sxs-lookup"><span data-stu-id="dd5e9-123">The bodies of the individual cases in the switch will be moved into hardware subroutines and the switch will be a series of subroutine calls.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="dd5e9-124">Requer hardware de <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">nível de recurso</a> 10_0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="dd5e9-124">Requires <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature level</a> 10_0 or later hardware.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="dd5e9-125"><span id="Selector"></span><span id="selector"></span><span id="SELECTOR"></span>*Seletor*</span><span class="sxs-lookup"><span data-stu-id="dd5e9-125"><span id="Selector"></span><span id="selector"></span><span id="SELECTOR"></span>*Selector*</span></span>
</dt> <dd>

<span data-ttu-id="dd5e9-126">Uma variável.</span><span class="sxs-lookup"><span data-stu-id="dd5e9-126">A variable.</span></span> <span data-ttu-id="dd5e9-127">As instruções Case dentro das chaves irão verificar essa variável para ver se o SwitchValue corresponde a seu Case específico.</span><span class="sxs-lookup"><span data-stu-id="dd5e9-127">The case statements inside the curly brackets will each check this variable to see if the SwitchValue matches their particular CaseValue.</span></span>

</dd> <dt>

<span data-ttu-id="dd5e9-128"><span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*StatementBlock*</span><span class="sxs-lookup"><span data-stu-id="dd5e9-128"><span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*StatementBlock*</span></span>
</dt> <dd>

<span data-ttu-id="dd5e9-129">Uma ou mais [instruções](dx-graphics-hlsl-statement-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="dd5e9-129">One or more [statements](dx-graphics-hlsl-statement-blocks.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dd5e9-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="dd5e9-130">Remarks</span></span>


```
[branch] switch(a)
{
    case 0:
        return 0; 
    case 1:
        return 1; 
    case 2:
        return 3; 
    default:
        return 6; 
}
```



<span data-ttu-id="dd5e9-131">É equivalente a:</span><span class="sxs-lookup"><span data-stu-id="dd5e9-131">Is equivalent to:</span></span>


```
[branch] if( a == 2 )
    return 3;
else if( a == 1 )
    return 1;
else if( a == 0 )
    return 0;
else
    return 6;
```



<span data-ttu-id="dd5e9-132">Aqui estão exemplos de usos de forcecase e atributos de controle de fluxo de chamada:</span><span class="sxs-lookup"><span data-stu-id="dd5e9-132">Here are example usages of forcecase and call flow control attributes:</span></span>


```
[forcecase] switch(a)
{
    case 0:
        return 0; 
    case 1:
        return 1; 
    case 2:
        return 3; 
    default:
        return 6; 
}

[call] switch(a)
{
    case 0:
        return 0; 
    case 1:
        return 1; 
    case 2:
        return 3; 
    default:
        return 6; 
}
```



## <a name="requirements"></a><span data-ttu-id="dd5e9-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd5e9-133">Requirements</span></span>



| <span data-ttu-id="dd5e9-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd5e9-134">Requirement</span></span> | <span data-ttu-id="dd5e9-135">Valor</span><span class="sxs-lookup"><span data-stu-id="dd5e9-135">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="dd5e9-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dd5e9-136">Header</span></span><br/> | <dl> <span data-ttu-id="dd5e9-137"><dt>Urlmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd5e9-137"><dt>Urlmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd5e9-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="dd5e9-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd5e9-139">Controle de fluxo</span><span class="sxs-lookup"><span data-stu-id="dd5e9-139">Flow Control</span></span>](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

