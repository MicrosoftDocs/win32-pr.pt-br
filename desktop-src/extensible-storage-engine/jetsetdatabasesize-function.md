---
description: 'Saiba mais sobre: função JetSetDatabaseSize'
title: Função JetSetDatabaseSize
TOCTitle: JetSetDatabaseSize Function
ms:assetid: 4a87bf43-c8f7-4966-9f1f-68c16d1cb558
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269242(v=EXCHG.10)
ms:contentKeyID: 32765544
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetDatabaseSizeW
- JetSetDatabaseSize
- JetSetDatabaseSizeA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cd450a0afed0256b0b80d97a278dccf99418a900
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089872"
---
# <a name="jetsetdatabasesize-function"></a>Função JetSetDatabaseSize


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetsetdatabasesize-function"></a>Função JetSetDatabaseSize

A função **JetSetDatabaseSize** define o tamanho de um arquivo de banco de dados não aberto.

```cpp
    JET_ERR JET_API JetSetDatabaseSize(
      __in          JET_SESID sesid,
      __in          JET_PCSTR szDatabaseName,
      __in          unsigned long cpg,
      __out         unsigned long* pcpgReal
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

Identifica o contexto de sessão de banco de dados a ser usado para a chamada à API.

*szDatabaseName*

Identifica o nome do arquivo de banco de dados cujo tamanho deve ser alterado.

*CPG*

Especifica o tamanho desejado do banco de dados, em páginas.

*pcpgReal*

Ponteiro para um número que recebe o tamanho do banco de dados, em páginas, após a chamada à API. Se a chamada à API não tiver sido bem-sucedida, o conteúdo de *pcpgReal* será indefinido.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).

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
<td><p>JET_errDatabaseInconsistent<br />
JET_errDatabaseDirtyShutdown</p></td>
<td><p>JET_errDatabaseInconsistent e JET_errDatabaseDirtyShutdown são do mesmo valor numérico. O banco de dados cujo tamanho será ajustado deve estar em um desligamento normal, conhecido como um estado consistente. Um banco de dados inconsistente não está corrompido, mas requer que os arquivos de log sejam reproduzidos.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseInvalidPath</p></td>
<td><p><em>szDatabaseName</em> não deve ser uma cadeia de caracteres vazia e não nula.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDiskFull</p></td>
<td><p>Não há espaço livre suficiente no volume para executar a operação de crescimento. O <strong>JetSetDatabaseSize</strong> também pode retornar muitos erros relacionados a arquivos, incluindo, mas não se limitando a:</p>
<ul>
<li><p>JET_errDiskIO</p></li>
<li><p>JET_errFileNotFound</p></li>
<li><p>JET_errInvalidPath</p></li>
<li><p>JET_errFileAccessDenied</p></li>
<li><p>JET_errOutOfFileHandles</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Um dos motivos pelos quais esse erro pode ser retornado é se o <em>CPG</em> atender ao tamanho mínimo do banco de dados. O tamanho mínimo atual do banco de dados é de 256 páginas.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfMemory</p></td>
<td><p>O sistema está com poucos recursos de memória.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Comentários

Se **JetSetDatabaseSize** for chamado antes da inserção de grandes quantidades de dados, o arquivo de banco de dado será aumentado em uma única operação. Isso reduzirá a probabilidade de o arquivo de banco de dados ficar fragmentado no nível do sistema de arquivos e também reduzir o número de vezes que o arquivo de banco de dados precisa ser aumentado. Aumentar o arquivo de banco de dados uma vez pode ser mais rápido do que expandi-lo várias vezes.

No momento, há suporte para o aumento do arquivo. Para reduzir um arquivo, use o recurso de desfragmentação do programa utilitário de esentutl.exe.

Se *CPG* for menor do que o tamanho atual do banco de dados, a operação será ignorada. Se *CPG* for menor que o tamanho mínimo do banco de dados (atualmente 256 páginas), ele retornará JET_errInvalidParameter.

Para definir o tamanho de um banco de dados que está aberto, consulte [JetGrowDatabase](./jetgrowdatabase-function.md).

O tamanho do arquivo pode não corresponder ao número de páginas retornadas em *pcpgReal*. Há duas páginas reservadas adicionais que podem não ser contadas em *pcpgReal*.

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</p></td>
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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementado como <strong>JetSetDatabaseSizeW</strong> (Unicode) e <strong>JetSetDatabaseSizeA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_OBJECTINFO](./jet-objectinfo-structure.md)  
[JET_OBJECTLIST](./jet-objectlist-structure.md)  
[JetGrowDatabase](./jetgrowdatabase-function.md)
