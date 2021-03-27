---
title: pack_matrix diretiva pragma
description: Diretiva pragma que especifica o alinhamento de empacotamento para matrizes.
ms.assetid: e77dc007-d915-4d78-9fff-d44d4999e4da
keywords:
- pack_matrix HLSL de diretiva pragma
topic_type:
- apiref
api_name:
- pack_matrix pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4bb5474702a1caba3f772002c34677601715caff
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006543"
---
# <a name="pack_matrix-pragma-directive"></a>Diretiva de pragma de matriz de pacote \_

Diretiva pragma que especifica o alinhamento de empacotamento para matrizes.



| \#\_matriz de pragma Pack ( *alinhamento* ) |
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
<td><span id="alignment"></span><span id="ALIGNMENT"></span><em>sintonia</em><br/></td>
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
<td>Padrão. Define o alinhamento da embalagem de matriz para a coluna principal.</td>
</tr>
<tr class="even">
<td>row_major</td>
<td>Define o alinhamento da embalagem de matriz para a linha principal.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="examples"></a>Exemplos

O exemplo a seguir define o alinhamento da embalagem de matriz para a linha principal.


```
#pragma pack_matrix( row_major )
```



## <a name="see-also"></a>Confira também

<dl> <dt>

[Diretivas de pré-processador (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#Diretiva pragma (DirectX HLSL)](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





