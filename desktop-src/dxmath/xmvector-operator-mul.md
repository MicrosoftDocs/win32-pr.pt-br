---
description: Operadores de multiplicação.
ms.assetid: f8397999-9956-4d11-8705-c95b788a9f03
title: operadores do operador *
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name: ''
api_type:
- NA
api_location: ''
ms.openlocfilehash: 15cdb9d189d110621461c1623b4fd20eaa9e7f5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091087"
---
# <a name="operator--operators"></a>operadores de operador \*

Operadores de multiplicação

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
<td style="text-align: left;"><a href="/previous-versions/windows/desktop/legacy/ee421390(v=vs.85)"><strong>XMVECTOR:: Operator * (float, XMVECTOR)</strong></a></td>
<td style="text-align: left;">Multiplique um valor de ponto flutuante por uma instância do <code>XMVECTOR</code> , retornando o resultado de uma nova instância do <code>XMVECTOR</code> .<br/> O <code>operator *</code> multiplica um valor de ponto flutuante em relação a cada componente de uma instância do <a href="xmvector-data-type.md"><strong>tipo de dados XMVECTOR</strong></a>, retornando uma nova <code>XMVECTOR</code> instância cujos componentes contêm o resultado. <br/>
<blockquote>
[!Note]<br />
Esse operador só está disponível em C++.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="/previous-versions/windows/desktop/legacy/ee421391(v=vs.85)"><strong>XMVECTOR:: Operator * (XMVECTOR, float)</strong></a></td>
<td style="text-align: left;">Multiplique uma instância de <code>XMVECTOR</code> por um valor de ponto flutuante, retornando o resultado de uma nova instância do <code>XMVECTOR</code> .<br/> O <code>operator *</code> multiplica cada componente de uma instância do <a href="xmvector-data-type.md"><strong>tipo de dados XMVECTOR</strong></a> por um valor de ponto flutuante, retornando uma nova <code>XMVECTOR</code> instância cujos componentes contêm o resultado. <br/>
<blockquote>
[!Note]<br />
Esse operador só está disponível em C++.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="/previous-versions/windows/desktop/legacy/ee421392(v=vs.85)"><strong>XMVECTOR:: Operator * (XMVECTOR, XMVECTOR)</strong></a></td>
<td style="text-align: left;">Multiplica uma instância de <code>XMVECTOR</code> por uma segunda instância, retornando o resultado em uma terceira instância. <br/> O <code>operator *</code> multiplica cada componente de uma instância do <a href="xmvector-data-type.md"><strong>tipo de dados XMVECTOR</strong></a> pelo componente correspondente em uma segunda instância do <code>XMVECTOR</code> , retornando uma nova <code>XMVECTOR</code> instância que contém o resultado. <br/>
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

 

 
