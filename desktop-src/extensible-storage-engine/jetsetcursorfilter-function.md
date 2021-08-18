---
description: 'Saiba mais sobre: Função JetSetCursorFilter'
title: Função JetSetCursorFilter
TOCTitle: JetSetCursorFilter Function
ms:assetid: 3cea5beb-2cf8-4053-8e7f-7b8645580ef0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835040(v=EXCHG.10)
ms:contentKeyID: 49894662
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetSetCursorFilter
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 76e92f768fd99cdd755e435caf4ba24dbbba0e3b0ee6338ffe7f49c2f506f2f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118978796"
---
# <a name="jetsetcursorfilter-function"></a>Função JetSetCursorFilter


_**Aplica-se a:** Windows | Windows Servidor_

A **função JetSetCursorFilter** define uma matriz de filtros simples para a [função JetMove.](./jetmove-function.md)

A **função JetSetCursorFilter** foi introduzida no Windows 8 operacional.

``` c++
JET_ERR JET_API JetSetCursorFilter(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in_ecount(cFilters)  JET_INDEX_COLUMN* rgFilters,
  __in          DWORD cFilters,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a>Parâmetros

*sesid*

O contexto de sessão do banco de dados a ser usado para a chamada à API.

*Tableid*

O cursor a ser posicionado.

*rgFilters*

Os filtros de registro simples.

*cFilters*

O número de filtros.

*grbit*

Um grupo de bits que especifica zero ou mais das opções de movimentação listadas na tabela a seguir.

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
<td><p>Nenhum</p></td>
<td><p>Opção padrão.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valor retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno listados na tabela a seguir. Para obter mais informações sobre os possíveis erros de ESE (Extensible Armazenamento Engine), consulte [Extensible Armazenamento Engine Error](./extensible-storage-engine-errors.md) [Handling Parameters](./error-handling-parameters.md).

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


#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer Windows 8.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer Windows Server 2012.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Cabeçalho</strong></p></td>
<td><p>Declarado em Esent.h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Biblioteca</strong></p></td>
<td><p>Use ESENT.lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Requer ESENT.dll.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Confira também

[JetMove](./jetmove-function.md)  
[JET_ERR](./jet-err.md)
