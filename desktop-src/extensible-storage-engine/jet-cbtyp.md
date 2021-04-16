---
description: 'Saiba mais sobre: JET_CBTYP'
title: JET_CBTYP
TOCTitle: JET_CBTYP
ms:assetid: babbfa11-01a7-477b-a525-cff27a983b60
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294071(v=EXCHG.10)
ms:contentKeyID: 32765686
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0b01bafad091ed17e018793ea701596aef6d0d72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768531"
---
# <a name="jet_cbtyp"></a>JET_CBTYP


_**Aplica-se a:** Windows | Windows Server_

## <a name="jet_cbtyp"></a>JET_CBTYP

O **JET_CBTYP** grupo de constantes descreve todos os pontos possíveis em uma operação que o mecanismo de banco de dados notificará um aplicativo chamando a função de retorno de chamada [JET_CALLBACK](./jet-callback-callback-function.md) . O mecanismo de banco de dados passa uma dessas constantes no parâmetro *cbtyp* da função de retorno de chamada. O significado dos outros parâmetros passados pelo mecanismo de banco de dados nessa chamada depende do **JET_CBTYP** específico passado.

**Windows XP:**  O **JET_CBTYP** grupo de constantes é introduzido no Windows XP.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante/valor</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_cbtypNull<br />
0x00000000</p></td>
<td><p>Esse retorno de chamada é reservado e sempre considerado inválido.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbtypFinalize<br />
0x00000001</p></td>
<td><p>Esse retorno de chamada é reservado para uso futuro.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypBeforeInsert<br />
0x00000002</p></td>
<td><p>Esse retorno de chamada ocorrerá logo antes de um novo registro ser inserido em uma tabela por uma chamada para <a href="gg269288(v=exchg.10).md">JetUpdate</a>.</p>
<p>O ponteiro de função para esse motivo de retorno de chamada é passado para <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> por meio de <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> ou é configurado em tempo de execução por meio de <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>. Para obter mais informações, consulte <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> ou <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</p>
<p>Os parâmetros de retorno de chamada terão os seguintes valores:</p>
<ul>
<li><p><em>sesid</em>: a sessão que tem o registro a ser inserido.</p></li>
<li><p><em>DBID</em>: a ID do banco de dados da tabela que contém o registro a ser inserido.</p></li>
<li><p><em>TableName</em>: o cursor que preparou o novo registro a ser inserido. É importante observar que o valor de qualquer versão ou colunas de incremento automático podem não estar corretos no momento.</p></li>
<li><p><em>pvArg1</em>: <strong>nulo</strong></p></li>
<li><p><em>pvArg2</em>: <strong>nulo</strong></p></li>
<li><p><em>pvContext</em>: o ponteiro de contexto passado para <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> ou <strong>NULL</strong>.</p></li>
<li><p><em>ulUnused</em>: <strong>NULL</strong> se um erro for retornado pelo retorno de chamada, a operação que originou o retorno de chamada falhará com esse erro.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_cbtypAfterInsert<br />
0x00000004</p></td>
<td><p>Esse retorno de chamada ocorrerá apenas depois que um novo registro tiver sido inserido em uma tabela por uma chamada para <a href="gg269288(v=exchg.10).md">JetUpdate</a> , mas antes de <a href="gg269288(v=exchg.10).md">JetUpdate</a> retornar ao chamador.</p>
<p>O ponteiro de função para esse motivo de retorno de chamada é passado para <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> por meio de <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> ou é configurado em tempo de execução por meio de <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>. Para obter mais informações, consulte <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> ou <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</p>
<p>Os parâmetros de retorno de chamada terão os seguintes valores:</p>
<ul>
<li><p><em>sesid</em>: a sessão que tem o registro que acabou de ser inserido.</p></li>
<li><p><em>DBID</em>: a ID do banco de dados da tabela que contém o registro que acabou de ser inserido.</p></li>
<li><p><em>TableName</em>: um cursor na tabela no qual o registro acabou de ser inserido. Observe que o cursor ainda está posicionado na mesma entrada de índice que era no retorno de chamada antes de inserir. Observe ainda que essa entrada de índice pode não estar relacionada de nenhuma forma ao registro que está sendo inserido.</p></li>
<li><p><em>pvArg1</em>: <strong>nulo</strong></p></li>
<li><p><em>pvArg2</em>: <strong>nulo</strong></p></li>
<li><p><em>pvContext</em>: o ponteiro de contexto passado para <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> ou <strong>NULL</strong>.</p></li>
<li><p><em>ulUnused</em>: <strong>NULL</strong> se um erro for retornado pelo retorno de chamada, ele será ignorado.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypBeforeReplace<br />
0x00000008</p></td>
<td><p>Esse retorno de chamada ocorrerá logo antes de um registro existente em uma tabela que está sendo alterada por uma chamada para <a href="gg269288(v=exchg.10).md">JetUpdate</a>.</p>
<p>O ponteiro de função para esse motivo de retorno de chamada é passado para <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> por meio de <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> ou é configurado em tempo de execução por meio de <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>. Para obter mais informações, consulte <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> ou <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</p>
<p>Os parâmetros de retorno de chamada terão os seguintes valores:</p>
<ul>
<li><p><em>sesid</em>: a sessão que tem o registro a ser alterado.</p></li>
<li><p><em>DBID</em>: a ID do banco de dados da tabela que contém o registro a ser alterado.</p></li>
<li><p><em>TableName</em>: um cursor posicionado em uma entrada de índice associada ao registro a ser alterado. É importante observar que o valor de qualquer versão ou colunas de incremento automático podem não estar corretos no momento.</p></li>
<li><p><em>pvArg1</em>: <strong>nulo</strong></p></li>
<li><p><em>pvArg2</em>: <strong>nulo</strong></p></li>
<li><p><em>pvContext</em>: o ponteiro de contexto passado para <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> ou <strong>NULL</strong>.</p></li>
<li><p><em>ulUnused</em>: <strong>NULL</strong> se um erro for retornado pelo retorno de chamada, a operação que originou o retorno de chamada falhará com esse erro.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_cbtypAfterReplace<br />
0x00000010</p></td>
<td><p>Esse retorno de chamada ocorrerá apenas depois que um registro existente em uma tabela tiver sido alterado por uma chamada para <a href="gg269288(v=exchg.10).md">JetUpdate</a> , mas antes de <a href="gg269288(v=exchg.10).md">JetUpdate</a> retornar ao seu chamador.</p>
<p>O ponteiro de função para esse motivo de retorno de chamada é passado para <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> por meio de <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> ou é configurado em tempo de execução por meio de <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>. Para obter mais informações, consulte <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> ou <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</p>
<p>Os parâmetros de retorno de chamada terão os seguintes valores:</p>
<ul>
<li><p><em>sesid</em>: a sessão que tem o registro que acabou de ser alterado.</p></li>
<li><p><em>DBID</em>: a ID do banco de dados da tabela que contém o registro que acabou de ser alterado.</p></li>
<li><p><em>TableName</em>: um cursor posicionado em uma entrada de índice associada ao registro que acabou de ser alterado.</p></li>
<li><p><em>pvArg1</em>: <strong>nulo</strong></p></li>
<li><p><em>pvArg2</em>: <strong>nulo</strong></p></li>
<li><p><em>pvContext</em>: o ponteiro de contexto passado para <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> ou <strong>NULL</strong>.</p></li>
<li><p><em>ulUnused</em>: <strong>NULL</strong> se um erro for retornado pelo retorno de chamada, ele será ignorado.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypBeforeDelete<br />
0x00000020</p></td>
<td><p>Esse retorno de chamada ocorrerá logo antes de um registro existente em uma tabela ser excluído por uma chamada para <a href="gg269315(v=exchg.10).md">JetDelete</a>.</p>
<p>O ponteiro de função para esse motivo de retorno de chamada é passado para <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> por meio de <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> ou é configurado em tempo de execução por meio de <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>. Para obter mais informações, consulte <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> ou <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</p>
<p>Os parâmetros de retorno de chamada terão os seguintes valores:</p>
<ul>
<li><p><em>sesid</em>: a sessão que tem o registro a ser excluído.</p></li>
<li><p><em>DBID</em>: a ID do banco de dados da tabela que contém o registro a ser excluído.</p></li>
<li><p><em>TableName</em>: um cursor posicionado em uma entrada de índice associada ao registro a ser excluído.</p></li>
<li><p><em>pvArg1</em>: <strong>nulo</strong></p></li>
<li><p><em>pvArg2</em>: <strong>nulo</strong></p></li>
<li><p><em>pvContext</em>: o ponteiro de contexto passado para <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> ou <strong>NULL</strong>.</p></li>
<li><p><em>ulUnused</em>: <strong>NULL</strong> se um erro for retornado pelo retorno de chamada, a operação que originou o retorno de chamada falhará com esse erro.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_cbtypAfterDelete<br />
0x00000040</p></td>
<td><p>Esse retorno de chamada ocorrerá apenas depois que um registro existente em uma tabela tiver sido excluído por uma chamada para <a href="gg269315(v=exchg.10).md">JetDelete</a> , mas antes de <a href="gg269315(v=exchg.10).md">JetDelete</a> retornar ao chamador.</p>
<p>O ponteiro de função para esse motivo de retorno de chamada é passado para <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> por meio de <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> ou é configurado em tempo de execução por meio de <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>. Para obter mais informações, consulte <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> ou <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</p>
<p>Os parâmetros de retorno de chamada terão os seguintes valores:</p>
<ul>
<li><p><em>sesid</em>: a sessão que tem o registro que acabou de ser excluído.</p></li>
<li><p><em>DBID</em>: a ID do banco de dados da tabela que contém o registro que acabou de ser excluído.</p></li>
<li><p><em>TableName</em>: um cursor posicionado em uma entrada de índice associada ao registro que acabou de ser excluído.</p></li>
<li><p><em>pvArg1</em>: <strong>nulo</strong></p></li>
<li><p><em>pvArg2</em>: <strong>nulo</strong></p></li>
<li><p><em>pvContext</em>: o ponteiro de contexto passado para <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> ou <strong>NULL</strong>.</p></li>
<li><p><em>ulUnused</em>: <strong>nulo</strong></p></li>
</ul>
<p>Se um erro for retornado pelo retorno de chamada, ele será ignorado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypUserDefinedDefaultValue<br />
0x00000080</p></td>
<td><p>Esse retorno de chamada ocorrerá quando o mecanismo precisar recuperar o valor padrão definido pelo usuário de uma coluna do aplicativo. Esse retorno de chamada é essencialmente uma implementação limitada de <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> que é avaliada pelo aplicativo. Um máximo de um valor de coluna pode ser retornado para um valor padrão definido pelo usuário.</p>
<p>O ponteiro de função para esse motivo de retorno de chamada é passado para <a href="gg294122(v=exchg.10).md">JetAddColumn</a> por meio de uma estrutura de <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> ou passado para <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> por meio de uma estrutura de <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> em uma estrutura de <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> em uma estrutura de <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> .</p>
<p>Os parâmetros de retorno de chamada terão os seguintes valores:</p>
<ul>
<li><p><em>sesid</em>: a sessão que está computando o valor padrão definido pelo usuário</p></li>
<li><p><em>DBID</em>: a ID do banco de dados da tabela que contém o valor padrão definido pelo usuário</p></li>
<li><p><em>TableName</em>: um cursor posicionado no registro para o qual o valor padrão definido pelo usuário está sendo recuperado</p></li>
<li><p><em>pvArg1</em>: o buffer de saída para o valor padrão definido pelo usuário</p></li>
<li><p><em>pvArg2</em>: on Input, esse é o tamanho do buffer de saída. Na saída, esse é o tamanho real do valor padrão definido pelo usuário. em ambos os casos, o tamanho é um inteiro sem sinal de 32 bits.</p></li>
<li><p><em>pvContext</em>: um ponteiro para um buffer que contém os dados de usuário especificados na estrutura de <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> quando a coluna foi criada ou nula se nenhum contexto foi fornecido.</p></li>
<li><p><em>ulUnused</em>: a ID de coluna da coluna para a qual o valor padrão definido pelo usuário está sendo recuperado.</p></li>
</ul>
<p>Se um erro for retornado pelo retorno de chamada, a operação que originou o retorno de chamada falhará com esse erro.</p>
<p>Se JET_wrnBufferTruncated for retornado pelo retorno de chamada, a operação continuará, mas o valor inteiro não será recuperado durante o retorno de chamada.</p>
<p>Se JET_wrnColumnNull for retornado pelo retorno de chamada, a operação continuará, mas o valor padrão definido pelo usuário para a coluna será nulo.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbtypOnlineDefragCompleted<br />
0x00000100</p></td>
<td><p>Esse retorno de chamada ocorrerá quando a desfragmentação online de um banco de dados como iniciado pelo <a href="gg269317(v=exchg.10).md">JetDefragment</a> tiver sido interrompida devido à conclusão do processo ou ao limite de tempo que está sendo atingido.</p>
<p>O ponteiro de função para esse motivo de retorno de chamada é passado para <a href="gg269317(v=exchg.10).md">JetDefragment</a>. Para obter mais informações, consulte <a href="gg269317(v=exchg.10).md">JetDefragment</a>.</p>
<p>Os parâmetros de retorno de chamada terão os seguintes valores:</p>
<ul>
<li><p><em>sesid</em>: a sessão usada para executar a desfragmentação online do banco de dados ou JET_sesidNil para um arquivo de streaming.</p></li>
<li><p><em>DBID</em>: a ID do banco de dados que está sendo desfragmentado ou JET_dbidNil para um arquivo de streaming.</p></li>
<li><p><em>TableName</em>: JET_tableidNil</p></li>
<li><p><em>pvArg1</em>: <strong>nulo</strong></p></li>
<li><p><em>pvArg2</em>: <strong>nulo</strong></p></li>
<li><p><em>pvContext</em>: <strong>nulo</strong></p></li>
<li><p><em>ulUnused</em>: <strong>nulo</strong></p></li>
</ul>
<p>Se um erro for retornado pelo retorno de chamada, ele será ignorado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypFreeCursorLS<br />
0x00000200</p></td>
<td><p>Esse retorno de chamada ocorrerá quando o aplicativo precisar limpar o identificador de contexto para o armazenamento local associado a um cursor que está sendo liberado pelo mecanismo de banco de dados. Para obter mais informações, consulte <a href="gg269243(v=exchg.10).md">JetSetLS</a>.</p>
<p>O ponteiro de função para esse motivo de retorno de chamada é configurado por meio de <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> com <a href="gg269310(v=exchg.10).md">JET_paramRuntimeCallback</a>.</p>
<p>Os parâmetros de retorno de chamada terão os seguintes valores:</p>
<ul>
<li><p><em>sesid</em>: JET_sesidNil</p></li>
<li><p><em>DBID</em>: JET_dbidNil</p></li>
<li><p><em>TableName</em>: JET_tableidNil</p></li>
<li><p><em>pvArg1</em>: o conjunto de identificadores de contexto usando <a href="gg269243(v=exchg.10).md">JetSetLS</a></p></li>
<li><p><em>pvArg2</em>: <strong>nulo</strong></p></li>
<li><p><em>pvContext</em>: <strong>nulo</strong></p></li>
<li><p><em>ulUnused</em>: <strong>nulo</strong></p></li>
</ul>
<p>Se um erro for retornado pelo retorno de chamada, ele será ignorado.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbtypFreeTableLS<br />
0x00000400</p></td>
<td><p>Esse retorno de chamada ocorrerá como resultado da necessidade do aplicativo para limpar o identificador de contexto do armazenamento local associado a uma tabela que está sendo liberada pelo mecanismo de banco de dados. Para obter mais informações, consulte <a href="gg269243(v=exchg.10).md">JetSetLS</a>.</p>
<p>O ponteiro de função para esse motivo de retorno de chamada é configurado por meio de <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> com <a href="gg269310(v=exchg.10).md">JET_paramRuntimeCallback</a>.</p>
<p>Os parâmetros de retorno de chamada terão os seguintes valores:</p>
<ul>
<li><p><em>sesid</em>: JET_sesidNil</p></li>
<li><p><em>DBID</em>: JET_dbidNil</p></li>
<li><p><em>TableName</em>: JET_tableidNil</p></li>
<li><p><em>pvArg1</em>: o identificador de contexto definido usando <a href="gg269243(v=exchg.10).md">JetSetLS</a>.</p></li>
<li><p><em>pvArg2</em>: <strong>nulo</strong></p></li>
<li><p><em>pvContext</em>: <strong>nulo</strong></p></li>
<li><p><em>ulUnused</em>: <strong>nulo</strong></p></li>
</ul>
<p>Se um erro for retornado pelo retorno de chamada, ele será ignorado.</p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer o Windows Vista ou o Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer o Windows Server 2008 ou o Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Cabeçalho</strong></p></td>
<td><p>Declarado em ESENT. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte Também

[JET_CALLBACK](./jet-callback-callback-function.md)
