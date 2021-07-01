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
# <a name="switch-statement"></a>Instrução Switch

Transfere o controle para um bloco de instruções diferente dentro do corpo do comutador, dependendo do valor de um seletor.


\[*Atributo* \] switch ( *seletor* ) {caso 0: { *StatementBlock*;}   interrupção   caso 1: { *StatementBlock*;}   interrupção   caso n: { *StatementBlock*;}   interrupção   padrão: { *StatementBlock*;}   interrupção



 

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribute*
</dt> <dd>

Um parâmetro opcional que controla como a instrução é compilada. Quando nenhum atributo é especificado, o compilador pode usar um comutador de hardware ou emitir uma série de instruções **If** .



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Atributo</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>mesclar</td>
<td>Compile a instrução como uma série de instruções <strong>If</strong> , cada uma com o atributo de <strong>achatamento</strong> .</td>
</tr>
<tr class="even">
<td>branch</td>
<td>Compile a instrução como uma série de instruções <strong>If</strong> com o atributo <strong>Branch</strong> .
<blockquote>
[!Note]<br />
Quando você usa o modelo de <a href="dx-graphics-hlsl-sm2.md">sombreador 2. x</a> ou o <a href="dx-graphics-hlsl-sm3.md">modelo de sombreador 3,0</a>, cada vez que usa a ramificação dinâmica, você consome recursos. Portanto, se você usar a ramificação dinâmica de forma excessiva ao direcionar esses perfis, poderá receber erros de compilação.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>forcecase</td>
<td>Force uma instrução switch no hardware.
<blockquote>
[!Note]<br />
Requer hardware de <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">nível de recurso</a> 10_0 ou posterior.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>chamada</td>
<td>Os corpos dos casos individuais no comutador serão movidos para as sub-rotinas de hardware e o comutador será uma série de chamadas de sub-rotina.
<blockquote>
[!Note]<br />
Requer hardware de <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">nível de recurso</a> 10_0 ou posterior.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span id="Selector"></span><span id="selector"></span><span id="SELECTOR"></span>*Seletor*
</dt> <dd>

Uma variável. As instruções Case dentro das chaves irão verificar essa variável para ver se o SwitchValue corresponde a seu Case específico.

</dd> <dt>

<span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*StatementBlock*
</dt> <dd>

Uma ou mais [instruções](dx-graphics-hlsl-statement-blocks.md).

</dd> </dl>

## <a name="remarks"></a>Comentários


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



É equivalente a:


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



Aqui estão exemplos de usos de forcecase e atributos de controle de fluxo de chamada:


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



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Urlmon. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Controle de fluxo](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

