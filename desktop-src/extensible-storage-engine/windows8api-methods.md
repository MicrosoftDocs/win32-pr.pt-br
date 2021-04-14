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
# <a name="windows8api-methods"></a><span data-ttu-id="21f81-103">Métodos Windows8Api</span><span class="sxs-lookup"><span data-stu-id="21f81-103">Windows8Api methods</span></span>

<span data-ttu-id="21f81-104">Incluir membros protegidos</span><span class="sxs-lookup"><span data-stu-id="21f81-104">Include protected members</span></span>  
<span data-ttu-id="21f81-105">Incluir membros herdados</span><span class="sxs-lookup"><span data-stu-id="21f81-105">Include inherited members</span></span>  

<span data-ttu-id="21f81-106">O tipo [Windows8Api](./windows8api-class.md) expõe os membros a seguir.</span><span class="sxs-lookup"><span data-stu-id="21f81-106">The [Windows8Api](./windows8api-class.md) type exposes the following members.</span></span>

## <a name="methods"></a><span data-ttu-id="21f81-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="21f81-107">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="21f81-108">Nome</span><span class="sxs-lookup"><span data-stu-id="21f81-108">Name</span></span></th>
<th><span data-ttu-id="21f81-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="21f81-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="21f81-112"><a href="dn335374(v=exchg.10).md">JetBeginTransaction3</a></span><span class="sxs-lookup"><span data-stu-id="21f81-112"><a href="dn335374(v=exchg.10).md">JetBeginTransaction3</a></span></span></td>
<td><span data-ttu-id="21f81-113">Faz com que uma sessão Insira uma transação ou crie um novo ponto de salvamento em uma transação existente.</span><span class="sxs-lookup"><span data-stu-id="21f81-113">Causes a session to enter a transaction or create a new save point in an existing transaction.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="21f81-116"><a href="dn335489(v=exchg.10).md">JetCommitTransaction2</a></span><span class="sxs-lookup"><span data-stu-id="21f81-116"><a href="dn335489(v=exchg.10).md">JetCommitTransaction2</a></span></span></td>
<td><span data-ttu-id="21f81-117">Confirma as alterações feitas no estado do banco de dados durante o ponto de salvamento atual e os migra para o ponto de salvamento anterior.</span><span class="sxs-lookup"><span data-stu-id="21f81-117">Commits the changes made to the state of the database during the current save point and migrates them to the previous save point.</span></span> <span data-ttu-id="21f81-118">Se o ponto de salvamento mais externo for confirmado, as alterações feitas durante esse ponto de salvamento serão confirmadas no estado do banco de dados e a sessão sairá da transação.</span><span class="sxs-lookup"><span data-stu-id="21f81-118">If the outermost save point is committed then the changes made during that save point will be committed to the state of the database and the session will exit the transaction.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="21f81-121"><a href="dn335488(v=exchg.10).md">JetCreateIndex4</a></span><span class="sxs-lookup"><span data-stu-id="21f81-121"><a href="dn335488(v=exchg.10).md">JetCreateIndex4</a></span></span></td>
<td><span data-ttu-id="21f81-122">Cria índices em dados em um banco de dado ESE.</span><span class="sxs-lookup"><span data-stu-id="21f81-122">Creates indexes over data in an ESE database.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="21f81-125"><a href="dn335377(v=exchg.10).md">JetCreateTableColumnIndex4</a></span><span class="sxs-lookup"><span data-stu-id="21f81-125"><a href="dn335377(v=exchg.10).md">JetCreateTableColumnIndex4</a></span></span></td>
<td><span data-ttu-id="21f81-126">Cria uma tabela, adiciona colunas e índices nessa tabela.</span><span class="sxs-lookup"><span data-stu-id="21f81-126">Creates a table, adds columns, and indices on that table.</span></span> <span data-ttu-id="21f81-127"><a href="dn292129(v=exchg.10).md">JetCreateTableColumnIndex3 (JET_SESID, JET_DBID, JET_TABLECREATE)</a></span><span class="sxs-lookup"><span data-stu-id="21f81-127"><a href="dn292129(v=exchg.10).md">JetCreateTableColumnIndex3(JET_SESID, JET_DBID, JET_TABLECREATE)</a></span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="21f81-130"><a href="dn335493(v=exchg.10).md">JetGetErrorInfo</a></span><span class="sxs-lookup"><span data-stu-id="21f81-130"><a href="dn335493(v=exchg.10).md">JetGetErrorInfo</a></span></span></td>
<td><span data-ttu-id="21f81-131">Obtém informações estendidas sobre um erro.</span><span class="sxs-lookup"><span data-stu-id="21f81-131">Gets extended information about an error.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="21f81-134"><a href="dn335378(v=exchg.10).md">JetOpenTemporaryTable2</a></span><span class="sxs-lookup"><span data-stu-id="21f81-134"><a href="dn335378(v=exchg.10).md">JetOpenTemporaryTable2</a></span></span></td>
<td><span data-ttu-id="21f81-135">Cria uma tabela temporária com um único índice.</span><span class="sxs-lookup"><span data-stu-id="21f81-135">Creates a temporary table with a single index.</span></span> <span data-ttu-id="21f81-136">Uma tabela temporária armazena e recupera registros, assim como uma tabela comum criada usando JetCreateTableColumnIndex.</span><span class="sxs-lookup"><span data-stu-id="21f81-136">A temporary table stores and retrieves records just like an ordinary table created using JetCreateTableColumnIndex.</span></span> <span data-ttu-id="21f81-137">No entanto, as tabelas temporárias são muito mais rápidas do que as tabelas comuns devido à sua natureza volátil.</span><span class="sxs-lookup"><span data-stu-id="21f81-137">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="21f81-138">Eles também podem ser usados para classificar e executar com muita rapidez a remoção de duplicidades em conjuntos de registros quando acessados de forma puramente sequencial.</span><span class="sxs-lookup"><span data-stu-id="21f81-138">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span> <span data-ttu-id="21f81-139">Consulte também <a href="dn292231(v=exchg.10).md">JetOpenTempTable (JET_SESID, [], Int32, TempTableGrbit, JET_TABLEID, [])</a>, &quot; API. JetOpenTempTable2 &quot; , <a href="dn292233(v=exchg.10).md">JetOpenTempTable3 (JET_SESID, [], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, [])</a>.</span><span class="sxs-lookup"><span data-stu-id="21f81-139">Also see <a href="dn292231(v=exchg.10).md">JetOpenTempTable(JET_SESID, [], Int32, TempTableGrbit, JET_TABLEID, [])</a>, &quot;Api.JetOpenTempTable2&quot;, <a href="dn292233(v=exchg.10).md">JetOpenTempTable3(JET_SESID, [], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, [])</a>.</span></span> <span data-ttu-id="21f81-140"><a href="dn335326(v=exchg.10).md">JetOpenTemporaryTable (JET_SESID, JET_OPENTEMPORARYTABLE)</a>.</span><span class="sxs-lookup"><span data-stu-id="21f81-140"><a href="dn335326(v=exchg.10).md">JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="21f81-143"><a href="dn335382(v=exchg.10).md">JetPrereadIndexRanges</a></span><span class="sxs-lookup"><span data-stu-id="21f81-143"><a href="dn335382(v=exchg.10).md">JetPrereadIndexRanges</a></span></span></td>
<td><span data-ttu-id="21f81-144">Se os registros com os intervalos de chave especificados não estiverem no cache do buffer, inicie as leituras assíncronas para colocar os registros no cache do buffer de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="21f81-144">If the records with the specified key ranges are not in the buffer cache, then start asynchronous reads to bring the records into the database buffer cache.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="21f81-147"><a href="dn335496(v=exchg.10).md">JetResizeDatabase</a></span><span class="sxs-lookup"><span data-stu-id="21f81-147"><a href="dn335496(v=exchg.10).md">JetResizeDatabase</a></span></span></td>
<td><span data-ttu-id="21f81-148">Redimensiona um banco de dados aberto no momento.</span><span class="sxs-lookup"><span data-stu-id="21f81-148">Resizes a currently open database.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="21f81-151"><a href="dn335383(v=exchg.10).md">JetSetCursorFilter</a></span><span class="sxs-lookup"><span data-stu-id="21f81-151"><a href="dn335383(v=exchg.10).md">JetSetCursorFilter</a></span></span></td>
<td><span data-ttu-id="21f81-152">Defina uma matriz de filtros simples para <a href="dn292217(v=exchg.10).md">JetMove (JET_SESID, JET_TABLEID, Int32, MoveGrbit)</a>.</span><span class="sxs-lookup"><span data-stu-id="21f81-152">Set an array of simple filters for <a href="dn292217(v=exchg.10).md">JetMove(JET_SESID, JET_TABLEID, Int32, MoveGrbit)</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="21f81-155"><a href="dn335495(v=exchg.10).md">JetSetSessionParameter</a></span><span class="sxs-lookup"><span data-stu-id="21f81-155"><a href="dn335495(v=exchg.10).md">JetSetSessionParameter</a></span></span></td>
<td><span data-ttu-id="21f81-156">Define um parâmetro no estado de sessão fornecido, usado para o tempo de vida desta sessão ou até a redefinição.</span><span class="sxs-lookup"><span data-stu-id="21f81-156">Sets a parameter on the provided session state, used for the lifetime of this session or until reset.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="21f81-159"><a href="dn335494(v=exchg.10).md">JetStopServiceInstance2</a></span><span class="sxs-lookup"><span data-stu-id="21f81-159"><a href="dn335494(v=exchg.10).md">JetStopServiceInstance2</a></span></span></td>
<td><span data-ttu-id="21f81-160">Prepara uma instância para encerramento.</span><span class="sxs-lookup"><span data-stu-id="21f81-160">Prepares an instance for termination.</span></span> <span data-ttu-id="21f81-161">Também pode ser usado para retomar uma pausa anterior.</span><span class="sxs-lookup"><span data-stu-id="21f81-161">Can also be used to resume a previous quiescing.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="21f81-164"><a href="dn335386(v=exchg.10).md">JetTryPrereadIndexRanges</a></span><span class="sxs-lookup"><span data-stu-id="21f81-164"><a href="dn335386(v=exchg.10).md">JetTryPrereadIndexRanges</a></span></span></td>
<td><span data-ttu-id="21f81-165">Se os registros com os intervalos de chave especificados não estiverem no cache do buffer, inicie as leituras assíncronas para colocar os registros no cache do buffer de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="21f81-165">If the records with the specified key ranges are not in the buffer cache, then start asynchronous reads to bring the records into the database buffer cache.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="21f81-168"><a href="dn335499(v=exchg.10).md">PrereadKeyRanges</a></span><span class="sxs-lookup"><span data-stu-id="21f81-168"><a href="dn335499(v=exchg.10).md">PrereadKeyRanges</a></span></span></td>
<td><span data-ttu-id="21f81-169">Se os registros com os intervalos de chave especificados não estiverem no cache do buffer, inicie as leituras assíncronas para colocar os registros no cache do buffer de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="21f81-169">If the records with the specified key ranges are not in the buffer cache then start asynchronous reads to bring the records into the database buffer cache.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="21f81-170">Parte superior</span><span class="sxs-lookup"><span data-stu-id="21f81-170">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="21f81-171">Confira também</span><span class="sxs-lookup"><span data-stu-id="21f81-171">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="21f81-172">Referência</span><span class="sxs-lookup"><span data-stu-id="21f81-172">Reference</span></span>

[<span data-ttu-id="21f81-173">Classe Windows8Api</span><span class="sxs-lookup"><span data-stu-id="21f81-173">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="21f81-174">Namespace Microsoft. ISAM. ESENT. Interop. windows8</span><span class="sxs-lookup"><span data-stu-id="21f81-174">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
