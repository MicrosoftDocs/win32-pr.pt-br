---
title: Instrução if
description: Execute condicionalmente uma série de instruções, com base na avaliação da expressão condicional.
ms.assetid: ed4e347b-b5ee-40bc-a3f8-36e83ccf45b8
keywords:
- Instrução if HLSL
topic_type:
- apiref
api_name:
- if Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: df4a1f049526422f39c3529395481548943c7e84
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118951"
---
# <a name="if-statement"></a>Instrução if

Execute condicionalmente uma série de instruções, com base na avaliação da expressão condicional.

\[*Atributo* \] if ( *Conditional* ) { *Statement Block*; }



 

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Atributo*
</dt> <dd>

Um parâmetro opcional que controla como a instrução é compilada.



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
<td>branch</td>
<td>Avalie apenas um lado da instrução if dependendo da condição determinada.
<blockquote>
[!Note]<br />
Quando você usa o Modelo de Sombreador <a href="dx-graphics-hlsl-sm2.md">2.x</a> ou o Modelo de Sombreador <a href="dx-graphics-hlsl-sm3.md">3.0</a>, sempre que usa a ramificação dinâmica, você consome recursos. Portanto, se você usar a ramificação dinâmica excessivamente ao direcionar esses perfis, poderá receber erros de compilação.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>mesclar</td>
<td>Avalie os dois lados da instrução if e escolha entre os dois valores resultantes.</td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Condicional*
</dt> <dd>

Uma expressão [condicional](dx-graphics-hlsl-expressions.md). A expressão é avaliada e, se true, o bloco de instrução é executado.

</dd> <dt>

<span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Bloco de instrução*
</dt> <dd>

Uma ou mais [instruções HLSL](dx-graphics-hlsl-statement-blocks.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

Quando o compilador usa o método branch para compilar uma instrução if, ele gerará um código que avaliará apenas um lado da instrução if, dependendo da condição determinada. Por exemplo, na instrução if:


```
[branch] if(x)
{
    x = sqrt(x);
}
```



A **instrução if** tem um bloco else implícito, que é equivalente a x = x. Como dissemos ao compilador para usar o método branch com o atributo de branch anterior, o código compilado avaliará x e executará apenas o lado que deve ser executado; se x for zero, ele executará o **outro** lado e, se for diferente de zero, executará o **lado em** seguida.

Por outro lado, se o atributo de nivelamento for usado, o código compilado avaliará os dois lados da instrução **if** e escolherá entre os dois valores resultantes usando o valor original de x.  Aqui está um exemplo de uso do atributo flatten:


```
[flatten] if(x)
{
    x = sqrt(x);
}
```



Há certos casos em que o uso do branch ou atributos de nivelar pode gerar um erro de compilação. O atributo branch poderá falhar se qualquer lado da instrução if contiver uma função de gradiente, como [**o tex2D.**](dx-graphics-hlsl-tex2d.md) O atributo de nivelar poderá falhar se qualquer lado da instrução if contiver uma instrução de anexação de fluxo ou qualquer outra instrução que tenha efeitos colaterais.

Uma **instrução if** também pode usar um bloco else opcional. Se a **expressão if** for true, o código no bloco de instrução associado à instrução if será processado. Caso contrário, o bloco de instrução associado ao bloco opcional else será processado.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Controle de fluxo](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





