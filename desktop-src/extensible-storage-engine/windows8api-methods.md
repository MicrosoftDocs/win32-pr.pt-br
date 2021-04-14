---
description: 'Saiba mais sobre: métodos Windows8Api'
title: Métodos Windows8Api (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: Windows8Api methods
ms:assetid: Methods.T:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api_methods(v=EXCHG.10)
ms:contentKeyID: 55104457
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: d8eb8b822affcbf41c375f7ef23b6a71d03afc64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104564807"
---
# <a name="windows8api-methods"></a>Métodos Windows8Api

Incluir membros protegidos  
Incluir membros herdados  

O tipo [Windows8Api](./windows8api-class.md) expõe os membros a seguir.

## <a name="methods"></a>Métodos

<table>
<thead>
<tr class="header">
<th> </th>
<th>Nome</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn335374(v=exchg.10).md">JetBeginTransaction3</a></td>
<td>Faz com que uma sessão Insira uma transação ou crie um novo ponto de salvamento em uma transação existente.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn335489(v=exchg.10).md">JetCommitTransaction2</a></td>
<td>Confirma as alterações feitas no estado do banco de dados durante o ponto de salvamento atual e os migra para o ponto de salvamento anterior. Se o ponto de salvamento mais externo for confirmado, as alterações feitas durante esse ponto de salvamento serão confirmadas no estado do banco de dados e a sessão sairá da transação.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn335488(v=exchg.10).md">JetCreateIndex4</a></td>
<td>Cria índices em dados em um banco de dado ESE.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn335377(v=exchg.10).md">JetCreateTableColumnIndex4</a></td>
<td>Cria uma tabela, adiciona colunas e índices nessa tabela. <a href="dn292129(v=exchg.10).md">JetCreateTableColumnIndex3 (JET_SESID, JET_DBID, JET_TABLECREATE)</a></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn335493(v=exchg.10).md">JetGetErrorInfo</a></td>
<td>Obtém informações estendidas sobre um erro.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn335378(v=exchg.10).md">JetOpenTemporaryTable2</a></td>
<td>Cria uma tabela temporária com um único índice. Uma tabela temporária armazena e recupera registros, assim como uma tabela comum criada usando JetCreateTableColumnIndex. No entanto, as tabelas temporárias são muito mais rápidas do que as tabelas comuns devido à sua natureza volátil. Eles também podem ser usados para classificar e executar com muita rapidez a remoção de duplicidades em conjuntos de registros quando acessados de forma puramente sequencial. Consulte também <a href="dn292231(v=exchg.10).md">JetOpenTempTable (JET_SESID, [], Int32, TempTableGrbit, JET_TABLEID, [])</a>, &quot; API. JetOpenTempTable2 &quot; , <a href="dn292233(v=exchg.10).md">JetOpenTempTable3 (JET_SESID, [], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, [])</a>. <a href="dn335326(v=exchg.10).md">JetOpenTemporaryTable (JET_SESID, JET_OPENTEMPORARYTABLE)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn335382(v=exchg.10).md">JetPrereadIndexRanges</a></td>
<td>Se os registros com os intervalos de chave especificados não estiverem no cache do buffer, inicie as leituras assíncronas para colocar os registros no cache do buffer de banco de dados.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn335496(v=exchg.10).md">JetResizeDatabase</a></td>
<td>Redimensiona um banco de dados aberto no momento.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn335383(v=exchg.10).md">JetSetCursorFilter</a></td>
<td>Defina uma matriz de filtros simples para <a href="dn292217(v=exchg.10).md">JetMove (JET_SESID, JET_TABLEID, Int32, MoveGrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn335495(v=exchg.10).md">JetSetSessionParameter</a></td>
<td>Define um parâmetro no estado de sessão fornecido, usado para o tempo de vida desta sessão ou até a redefinição.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn335494(v=exchg.10).md">JetStopServiceInstance2</a></td>
<td>Prepara uma instância para encerramento. Também pode ser usado para retomar uma pausa anterior.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn335386(v=exchg.10).md">JetTryPrereadIndexRanges</a></td>
<td>Se os registros com os intervalos de chave especificados não estiverem no cache do buffer, inicie as leituras assíncronas para colocar os registros no cache do buffer de banco de dados.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn335499(v=exchg.10).md">PrereadKeyRanges</a></td>
<td>Se os registros com os intervalos de chave especificados não estiverem no cache do buffer, inicie as leituras assíncronas para colocar os registros no cache do buffer de banco de dados.</td>
</tr>
</tbody>
</table>


Parte superior

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe Windows8Api](./windows8api-class.md)

[Namespace Microsoft. ISAM. ESENT. Interop. windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
