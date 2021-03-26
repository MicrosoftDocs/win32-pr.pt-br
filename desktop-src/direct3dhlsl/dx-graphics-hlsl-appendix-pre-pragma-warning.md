---
title: Diretiva de pragma de aviso
description: A diretiva pragma que modifica o comportamento das mensagens de aviso do compilador.
ms.assetid: 69488014-36e3-4c87-8b65-6123b5e87bcb
keywords:
- aviso de diretiva pragma HLSL
topic_type:
- apiref
api_name:
- warning pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7599886b47830b33c69f11c0c341c7775c644dd3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103916754"
---
# <a name="warning-pragma-directive"></a>Diretiva de pragma de aviso

A diretiva pragma que modifica o comportamento das mensagens de aviso do compilador.



| \#pragma warning ( *aviso-especificador* : *aviso-número-lista* \[ ; *aviso-especificador* : *aviso-número-lista*... \] ) |
|----------------------------------------------------------------------------------------------------------------------|



 

## <a name="parameters"></a>Parâmetros



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Item</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="warning-specifier"></span><span id="WARNING-SPECIFIER"></span><em>especificador de aviso</em><br/></td>
<td>Comportamento a ser definido para os avisos especificados. Esse parâmetro pode usar um dos valores listados na tabela a seguir. <br/> 
<table>
<thead>
<tr class="header">
<th>Valor</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>uma vez</td>
<td>Exiba a mensagem dos avisos com os números especificados apenas uma vez.</td>
</tr>
<tr class="even">
<td>padrão</td>
<td>Redefina o comportamento dos avisos com os números especificados para o valor padrão. Isso também tem o efeito de ativar um aviso por padrão. O aviso será gerado em seu nível padrão.</td>
</tr>
<tr class="odd">
<td>1, 2, 3, 4</td>
<td>Aplique o nível especificado aos avisos com os números especificados. Isso também tem o efeito de ativar um aviso por padrão.</td>
</tr>
<tr class="even">
<td>disable</td>
<td>Não emita os avisos com os números especificados.</td>
</tr>
<tr class="odd">
<td>erro</td>
<td>Relatar os avisos com os números especificados como erros.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span id="warning-number-list"></span><span id="WARNING-NUMBER-LIST"></span><em>aviso-lista de números</em></p></td>
<td><p>Lista delimitada por espaço em branco dos números dos avisos para modificar o comportamento de.</p></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Comentários

Você pode especificar qualquer número de alterações de comportamento de aviso distintas no mesmo pragma de aviso, separando as alterações com ponto e vírgula.

O compilador adicionará 4000 a qualquer número de aviso que esteja entre 0 e 999. Para números de aviso maiores que 4699 (aqueles associados à geração de código), o pragma de aviso só tem efeito quando colocado fora das definições de função. O pragma será ignorado se ele especificar um número maior que 4699 e for usado dentro de uma função.

O pragma de aviso HLSL não dá suporte à funcionalidade **Push** e **pop** do pragma de aviso incluído no compilador C++.

## <a name="examples"></a>Exemplos

O exemplo a seguir desabilita os avisos 4507 e 4034, exibe o aviso 4385 uma vez e relata o aviso de 4164 como um erro.


```
#pragma warning( disable : 4507 34; once : 4385; error : 164 )
```



O exemplo anterior é funcionalmente equivalente ao seguinte:


```
#pragma warning( disable : 4507 34 )
#pragma warning( once : 4385 )
#pragma warning( error : 164 )
```



## <a name="see-also"></a>Confira também

<dl> <dt>

[Diretivas de pré-processador (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#Diretiva pragma (DirectX HLSL)](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





