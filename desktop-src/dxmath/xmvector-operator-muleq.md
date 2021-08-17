---
description: Operadores de atribuição de multiplicação.
ms.assetid: 4d25cef1-8b39-42db-80df-c749940feb0b
title: operador * = operadores
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name: ''
api_type:
- NA
api_location: ''
ms.openlocfilehash: 69937ab8625e4abbde835929391b1f5e8ee6ccbc2143543a8d8e25760df8d254
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119117846"
---
# <a name="operator--operators"></a>operador \* = operadores

Operadores de atribuição de multiplicação

### <a name="overload-list"></a>Lista de sobrecargas



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Operador</th>
<th style="text-align: left;">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="/previous-versions/windows/desktop/legacy/ff729806(v=vs.85)"><strong>XMVECTOR:: Operator * = (XMVECTOR&, float)</strong></a></td>
<td style="text-align: left;">Multiplica uma <code>XMVECTOR</code> instância por um valor de ponto flutuante e retorna uma referência à instância atualizada. <br/> O <code>operator *=</code> multiplica cada componente da instância atual do tipo de <a href="xmvector-data-type.md"><strong>dados XMVECTOR</strong></a> por um valor de ponto flutuante especificado, retornando uma referência à instância atual atualizada. <br/>
<blockquote>
[!Note]<br />
Esse operador só está disponível em C++.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="/previous-versions/windows/desktop/legacy/ee421388(v=vs.85)"><strong>XMVECTOR:: Operator * = (XMVECTOR&, XMVECTOR)</strong></a></td>
<td style="text-align: left;">Multiplica uma <code>XMVECTOR</code> instância por uma segunda instância, retornando uma referência à instância inicial atualizada. <br/> O <code>operator *=</code> multiplica cada componente da instância atual do tipo de <a href="xmvector-data-type.md"><strong>dados XMVECTOR</strong></a> pelo componente correspondente em uma segunda instância especificada do <code>XMVECTOR</code> , retornando uma referência à instância inicial atualizada. <br/>
<blockquote>
[!Note]<br />
Esse operador só está disponível em C++.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a>Confira também

<dl> <dt>

[Operadores XMVECTOR](ovw-xmvector-operators.md)
</dt> <dt>

**Referência**
</dt> <dt>

[**Tipo de dados XMVECTOR**](xmvector-data-type.md)
</dt> </dl>

 

 
