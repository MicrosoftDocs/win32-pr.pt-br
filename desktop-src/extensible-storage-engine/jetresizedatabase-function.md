---
description: 'Saiba mais sobre: função JetResizeDatabase'
title: Função JetResizeDatabase
TOCTitle: JetResizeDatabase Function
ms:assetid: b6420de7-acff-480e-838b-f0e5acc29c65
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835047(v=EXCHG.10)
ms:contentKeyID: 49894669
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetResizeDatabase
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dadaa7eaa310c5b3a6a2730d316218bc2607d100
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764385"
---
# <a name="jetresizedatabase-function"></a>Função JetResizeDatabase


_**Aplica-se a:** Windows | Windows Server_

A função **JetResizeDatabase** estende ou reduz o tamanho de um banco de dados que está aberto no momento.

A função **JetResizeDatabase** foi introduzida no sistema operacional Windows 8.

``` c++
JET_ERR JET_API JetResizeDatabase(
  __in          JET_SESID sesid,
  __in          JET_DBID dbid,
  __in          unsigned long cpg,
  __out         unsigned long* pcpgActual,
  __in          const JET_GRBIT grbit
);
```

### <a name="parameters"></a>Parâmetros

*sesid*

O contexto da sessão de banco de dados a ser usado para a chamada à API.

*DBID*

O banco de dados que será estendido.

*CPG*

O tamanho solicitado do banco de dados, em páginas.

*pcpgActual*

Um ponteiro para um número que recebe o tamanho do banco de dados, em páginas, após a chamada à API. Se a chamada à API falhar, o conteúdo do parâmetro *pcpgActual* será indefinido.

*grbit*

Um grupo de bits que especifica zero ou mais valores listados na tabela a seguir.

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
<td><p>JET_bitResizeDatabaseOnlyGrow</p></td>
<td><p>Aumentar apenas o banco de dados. Se a chamada de redimensionamento reduzir o banco de dados, não faça nada.</p></td>
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
<tr class="even">
<td><p>JET_errDiskFull</p></td>
<td><p>Não há espaço livre suficiente no volume para executar a operação de crescimento.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDiskIO</p></td>
<td><p>Um erro relacionado a arquivo foi retornado pela função <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a> . Para obter mais informações sobre outros erros relacionados a arquivos que podem ser retornados, consulte <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a>.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Comentários

Se a função **JetResizeDatabase** for chamada antes da inserção de grandes quantidades de dados, o arquivo de banco de dado será aumentado em uma única operação. Isso reduzirá a probabilidade de o arquivo de banco de dados ficar fragmentado no nível do sistema de arquivos e também reduzir o número de vezes que o arquivo de banco de dados precisa ser aumentado. Aumentar o arquivo de banco de dados uma vez pode ser mais rápido do que expandi-lo várias vezes.

Para definir o tamanho de um banco de dados que não está aberto, consulte [JetSetDatabaseSize](./jetsetdatabasesize-function.md).

O tamanho do arquivo pode não corresponder ao número de páginas retornadas no parâmetro *pcpgReal* . Duas páginas reservadas adicionais podem não ser contadas no parâmetro *pcpgReal* .

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
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_OBJECTINFO](./jet-objectinfo-structure.md)  
[JET_OBJECTLIST](./jet-objectlist-structure.md)  
[JetSetDatabaseSize](./jetsetdatabasesize-function.md)
