---
description: 'Saiba mais sobre: função JetPrereadIndexRanges'
title: Função JetPrereadIndexRanges
TOCTitle: JetPrereadIndexRanges Function
ms:assetid: ab49abcc-eaeb-438f-8e6d-b08bc94d7bc3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835045(v=EXCHG.10)
ms:contentKeyID: 49894667
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetPrereadIndexRanges
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7cfdd8d25f7008f5fa854cbee32b54fa01942ce2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089878"
---
# <a name="jetprereadindexranges-function"></a>Função JetPrereadIndexRanges


_**Aplica-se a:** Windows | Windows Server_

A função **JetPrereadIndexRanges** lê índices para melhorar o desempenho.

A função **JetPrereadIndexRanges** foi introduzida no sistema operacional Windows 8.

``` c++
JET_ERR JetPrereadIndexRanges(
  __in          const JET_SESID sesid,
  __in          const JET_TABLEID tableid,
  __in_ecount(cIndexRanges)  const JET_INDEX_RANGE* const rgIndexRanges,
  __in          const unsigned long cIndexRanges,
  __out_opt     unsigned long* const pcRangesPreread,
  __in_ecount(ccolumnidPreread)  const JET_COLUMNID* const rgcolumnidPreread,
  __in          const unsigned long ccolumnidPreread,
  __in          const JET_GRBIT grbit
);
```

### <a name="parameters"></a>Parâmetros

*sesid*

O contexto da sessão de banco de dados a ser usado para a chamada à API.

*TableID*

A tabela na qual os itens são relidos.

*rgIndexRanges*

Os intervalos de chave a serem lidos.

*cIndexRanges*

O número de intervalos de chave a serem lidos, determinados pelo número de elementos em *rgIndexRanges*.

*pcRangesPreread*

O número de intervalos de chave que foram realmente lidos.

*rgcolumnidPreread*

Lista de IDs de coluna para colunas de valor longo a serem lidas. Por padrão, somente o registro na página é de leitura. Se colunas de valor longo fora da página precisarem ser lidas, suas IDs de coluna precisarão ser passadas por esse parâmetro.

*ccolumnidPreread*

O número de IDs de coluna para colunas de valor longo a serem lidas, determinado pelo número de elementos em *rgcolumnidPreread*.

*grbit*

Um grupo de bits que especifica zero ou mais valores de direção de preread listados na tabela a seguir.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valor</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Encaminhar</p></td>
<td><p>Leitura antecipada.</p></td>
</tr>
<tr class="even">
<td><p>Compatibilidade</p></td>
<td><p>Leia o retrocesso.</p></td>
</tr>
<tr class="odd">
<td><p>FirstPageOnly</p></td>
<td><p>Somente Leia a primeira página de qualquer coluna longa.</p></td>
</tr>
<tr class="even">
<td><p>NormalizedKey</p></td>
<td><p>Chave/indicador normalizado fornecido em vez do valor da coluna.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Retornar valor

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno listados na tabela a seguir. Para obter mais informações sobre os possíveis erros do ESE (mecanismo de armazenamento extensível), consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Código de retorno</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>A operação foi concluída com sucesso.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Comentários

Se os registros com os intervalos de chave especificados não estiverem no cache do buffer, você deverá iniciar as leituras assíncronas para colocar os registros no cache do buffer de banco de dados.

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer o Windows 8.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer o Windows Server 2012.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Cabeçalho</strong></p></td>
<td><p>Declarado em ESENT. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Biblioteca</strong></p></td>
<td><p>Use ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Requer ESENT.dll.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Confira também

[JET_ERR](./jet-err.md)
