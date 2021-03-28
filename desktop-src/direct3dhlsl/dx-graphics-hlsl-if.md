---
title: Instrução if
description: Executar condicionalmente uma série de instruções, com base na avaliação da expressão condicional.
ms.assetid: ed4e347b-b5ee-40bc-a3f8-36e83ccf45b8
keywords:
- Instrução If HLSL
topic_type:
- apiref
api_name:
- if Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8e8a3c20e73b9783d39b4f4cbdb7c0be5b75fcda
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2020
ms.locfileid: "104007046"
---
# <a name="if-statement"></a>Instrução if

Executar condicionalmente uma série de instruções, com base na avaliação da expressão condicional.



|                                                               |
|---------------------------------------------------------------|
| \[*Atributo* \] If ( *condicional* ) { *bloco de instruções*;} |



 

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribute*
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
<td>Avalie apenas um lado da instrução If dependendo da condição fornecida.
<blockquote>
[!Note]<br />
Quando você usa o modelo de <a href="dx-graphics-hlsl-sm2.md">sombreador 2. x</a> ou o <a href="dx-graphics-hlsl-sm3.md">modelo de sombreador 3,0</a>, cada vez que usa a ramificação dinâmica, você consome recursos. Portanto, se você usar a ramificação dinâmica de forma excessiva ao direcionar esses perfis, poderá receber erros de compilação.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>mesclar</td>
<td>Avalie ambos os lados da instrução If e escolha entre os dois valores resultantes.</td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Condiciona*
</dt> <dd>

Uma [expressão](dx-graphics-hlsl-expressions.md)condicional. A expressão é avaliada e, se for true, o bloco de instrução será executado.

</dd> <dt>

<span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Bloco de instrução*
</dt> <dd>

Uma ou mais [instruções HLSL](dx-graphics-hlsl-statement-blocks.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

Quando o compilador usa o método Branch para compilar uma instrução If, ele gerará um código que avaliará apenas um lado da instrução If dependendo da condição fornecida. Por exemplo, na instrução If:


```
[branch] if(x)
{
    x = sqrt(x);
}
```



A instrução **If** tem um bloco de else implícito, que é equivalente a x = x. Como dissemos ao compilador para usar o método Branch com o atributo Branch anterior, o código compilado avaliará x e executará apenas o lado que deve ser executado; se x for zero, ele executará o lado **mais** e, se for diferente de zero, ele executará o lado de **seguida** .

Por outro lado, se o atributo de **achatamento** for usado, o código compilado avaliará ambos os lados da instrução **If** e escolherá entre os dois valores resultantes usando o valor original de x. Aqui está um exemplo de uso do atributo achatar:


```
[flatten] if(x)
{
    x = sqrt(x);
}
```



Há certos casos em que usar os atributos Branch ou achatamento pode gerar um erro de compilação. O atributo Branch poderá falhar se qualquer lado da instrução If contiver uma função de gradiente, como [**tex2D**](dx-graphics-hlsl-tex2d.md). O atributo achata pode falhar se qualquer lado da instrução If contiver uma instrução Stream Append ou qualquer outra instrução que tenha efeitos colaterais.

Uma instrução **If** também pode usar um bloco opcional ELSE. Se a expressão **If** for true, o código no bloco de instrução associado à instrução If será processado. Caso contrário, o bloco de instrução associado ao bloco opcional else será processado.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Controle de fluxo](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





