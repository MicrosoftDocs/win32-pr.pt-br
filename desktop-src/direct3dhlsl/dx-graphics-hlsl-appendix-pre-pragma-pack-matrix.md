---
title: diretiva pack_matrix pragma
description: Diretiva Pragma que especifica o alinhamento de empacotamento para matrizes.
ms.assetid: e77dc007-d915-4d78-9fff-d44d4999e4da
keywords:
- pack_matrix diretiva pragma HLSL
topic_type:
- apiref
api_name:
- pack_matrix pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1c12129b6840197b21d1d259cc13bd07e75620176bdc797e6828c10d71e1c95d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118514779"
---
# <a name="pack_matrix-pragma-directive"></a>Diretiva \_ de pragma de matriz de pacotes

Diretiva Pragma que especifica o alinhamento de empacotamento para matrizes.



| \#pragma pack \_ matrix( *alignment* ) |
|--------------------------------------|



 

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
<td><span id="alignment"></span><span id="ALIGNMENT"></span><em>Alinhamento</em><br/></td>
<td>Alinhamento a ser definido para matrizes. Esse parâmetro pode usar um dos valores listados na tabela a seguir. <br/> 
<table>
<thead>
<tr class="header">
<th>Valor</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>column_major</td>
<td>Padrão. Define o alinhamento do empacotamento de matriz para a coluna principal.</td>
</tr>
<tr class="even">
<td>row_major</td>
<td>Define o alinhamento do empacotamento de matriz para a linha principal.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="examples"></a>Exemplos

O exemplo a seguir define o alinhamento de empacotamento de matriz para a linha principal.


```
#pragma pack_matrix( row_major )
```



## <a name="see-also"></a>Confira também

<dl> <dt>

[Diretivas de pré-processador (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#Diretiva pragma (DirectX HLSL)](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





