---
description: 'Saiba mais sobre: função JetCompact'
title: Função JetCompact
TOCTitle: JetCompact Function
ms:assetid: 6944bd61-893d-4269-869b-56590e22580a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269284(v=EXCHG.10)
ms:contentKeyID: 32765576
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCompactW
- JetCompactA
- JetCompact
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ebac7fe4f09a6c4456b5370af03ea24f2334cff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105791296"
---
# <a name="jetcompact-function"></a><span data-ttu-id="070ec-103">Função JetCompact</span><span class="sxs-lookup"><span data-stu-id="070ec-103">JetCompact Function</span></span>


<span data-ttu-id="070ec-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="070ec-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcompact-function"></a><span data-ttu-id="070ec-105">Função JetCompact</span><span class="sxs-lookup"><span data-stu-id="070ec-105">JetCompact Function</span></span>

<span data-ttu-id="070ec-106">A função **JetCompact** faz uma cópia de um banco de dados existente.</span><span class="sxs-lookup"><span data-stu-id="070ec-106">The **JetCompact** function makes a copy of an existing database.</span></span> <span data-ttu-id="070ec-107">A cópia é compactada para um estado ideal para uso.</span><span class="sxs-lookup"><span data-stu-id="070ec-107">The copy is compacted to a state optimal for usage.</span></span> <span data-ttu-id="070ec-108">Os dados nos dados copiados serão empacotados de acordo com as medidas escolhidas para os índices na criação do índice.</span><span class="sxs-lookup"><span data-stu-id="070ec-108">Data in the copied data will be packed according to the measures chosen for the indexes at index create.</span></span> <span data-ttu-id="070ec-109">Dessa forma, os dados compactados podem ser armazenados da maneira mais densa possível.</span><span class="sxs-lookup"><span data-stu-id="070ec-109">In this way, compacted data may be stored as densely as possible.</span></span> <span data-ttu-id="070ec-110">Como alternativa, os dados compactados podem reservar espaço para o aumento de registro subsequente ou inserções de índice.</span><span class="sxs-lookup"><span data-stu-id="070ec-110">Alternatively, compacted data may reserve space for subsequent record growth or index insertions.</span></span>

```cpp
    JET_ERR JET_API JetCompact(
      __in          JET_SESID sesid,
      __in          JET_PCSTR szDatabaseSrc,
      __in          JET_PCSTR szDatabaseDest,
      __in          JET_PFNSTATUS pfnStatus,
      __in_opt      JET_CONVERT* pconvert,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="070ec-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="070ec-111">Parameters</span></span>

<span data-ttu-id="070ec-112">*sesid*</span><span class="sxs-lookup"><span data-stu-id="070ec-112">*sesid*</span></span>

<span data-ttu-id="070ec-113">A sessão a ser usada para esta chamada.</span><span class="sxs-lookup"><span data-stu-id="070ec-113">The session to use for this call.</span></span>

<span data-ttu-id="070ec-114">*szDatabaseSrc*</span><span class="sxs-lookup"><span data-stu-id="070ec-114">*szDatabaseSrc*</span></span>

<span data-ttu-id="070ec-115">O banco de dados de origem que será compactado.</span><span class="sxs-lookup"><span data-stu-id="070ec-115">The source database that will be compacted.</span></span>

<span data-ttu-id="070ec-116">*szDatabaseDest*</span><span class="sxs-lookup"><span data-stu-id="070ec-116">*szDatabaseDest*</span></span>

<span data-ttu-id="070ec-117">O nome a ser usado para o banco de dados compactado.</span><span class="sxs-lookup"><span data-stu-id="070ec-117">The name to use for the compacted database.</span></span>

<span data-ttu-id="070ec-118">*pfnStatus*</span><span class="sxs-lookup"><span data-stu-id="070ec-118">*pfnStatus*</span></span>

<span data-ttu-id="070ec-119">Uma função de retorno de chamada que pode ser chamada periodicamente por meio da operação Compact do banco de dados para relatar o progresso.</span><span class="sxs-lookup"><span data-stu-id="070ec-119">A callback function that can be called periodically through the database compact operation to report progress.</span></span>

<span data-ttu-id="070ec-120">*pconvert*</span><span class="sxs-lookup"><span data-stu-id="070ec-120">*pconvert*</span></span>

<span data-ttu-id="070ec-121">Um ponteiro usado para designar uma DLL do ESE alternativa que pode ser usada para ler o banco de dados de origem e fornecer parâmetros opcionais para uma operação **JetCompact** que está convertendo um banco de dados de um anterior para um formato de versão posterior.</span><span class="sxs-lookup"><span data-stu-id="070ec-121">A pointer used to designate an alternative ESE DLL that can be used to read the source database, and to provide optional parameters for a **JetCompact** operation that is converting a database from an earlier to a later version format.</span></span> <span data-ttu-id="070ec-122">Este recurso foi descontinuado no Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="070ec-122">This feature was discontinued in Windows Server 2003.</span></span>

<span data-ttu-id="070ec-123">*grbit*</span><span class="sxs-lookup"><span data-stu-id="070ec-123">*grbit*</span></span>

<span data-ttu-id="070ec-124">Um grupo de bits que especifica zero ou mais das opções a seguir.</span><span class="sxs-lookup"><span data-stu-id="070ec-124">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="070ec-125">Valor</span><span class="sxs-lookup"><span data-stu-id="070ec-125">Value</span></span></p></th>
<th><p><span data-ttu-id="070ec-126">Significado</span><span class="sxs-lookup"><span data-stu-id="070ec-126">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="070ec-127">JET_bitCompactRepair</span><span class="sxs-lookup"><span data-stu-id="070ec-127">JET_bitCompactRepair</span></span></p></td>
<td><p><span data-ttu-id="070ec-128">Usado quando o banco de dados de origem é conhecido como corrompido.</span><span class="sxs-lookup"><span data-stu-id="070ec-128">Used when the source database is known to be corrupt.</span></span> <span data-ttu-id="070ec-129">Ele permite que um conjunto completo de novos comportamentos se destinasse a recuperar o máximo de dados possível do banco de dado de origem.</span><span class="sxs-lookup"><span data-stu-id="070ec-129">It enables a whole set of new behaviors intended to salvage as much data as possible from the source database.</span></span> <span data-ttu-id="070ec-130"><strong>JetCompact</strong> com esse conjunto de opções pode retornar JET_errSuccess, mas não copiar todos os dados criados no banco de dado de origem.</span><span class="sxs-lookup"><span data-stu-id="070ec-130"><strong>JetCompact</strong> with this option set may return JET_errSuccess but not copy all of the data created in the source database.</span></span> <span data-ttu-id="070ec-131">Os dados que estavam em partes danificadas do banco de dados de origem serão ignorados.</span><span class="sxs-lookup"><span data-stu-id="070ec-131">Data that was in damaged portions of the source database will be skipped.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="070ec-132">JET_bitCompactStats</span><span class="sxs-lookup"><span data-stu-id="070ec-132">JET_bitCompactStats</span></span></p></td>
<td><p><span data-ttu-id="070ec-133">Faz com que o <strong>JetCompact</strong> despeje estatísticas no banco de dados de origem em um arquivo chamado DFRGINFO.TXT.</span><span class="sxs-lookup"><span data-stu-id="070ec-133">Causes <strong>JetCompact</strong> to dump statistics on the source database to a file named DFRGINFO.TXT.</span></span> <span data-ttu-id="070ec-134">As estatísticas incluem o nome de cada tabela no banco de dados de origem, o número de linhas em cada tabela, o tamanho total em bytes de todas as linhas em cada tabela, tamanho total em bytes de todas as colunas do tipo <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> ou <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> que foram grandes o suficiente para serem armazenados separados do registro, número de páginas de folha de índice clusterizado e número de páginas de folha de valor longo</span><span class="sxs-lookup"><span data-stu-id="070ec-134">Statistics include the name of each table in source database, number of rows in each table, total size in bytes of all rows in each table, total size in bytes of all columns of type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> that were large enough to be stored separate from the record, number of clustered index leaf pages, and the number of long value leaf pages.</span></span> <span data-ttu-id="070ec-135">Além disso, estatísticas de resumo, incluindo o tamanho do banco de dados de origem, banco de dados de destino, tempo necessário para compactação de banco de dados, o espaço de banco de dados temporário também são todos despejados.</span><span class="sxs-lookup"><span data-stu-id="070ec-135">In addition, summary statistics including the size of the source database, destination database, time required for database compaction, temporary database space are all dumped as well.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="070ec-136">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="070ec-136">Return Value</span></span>

<span data-ttu-id="070ec-137">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="070ec-137">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="070ec-138">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="070ec-138">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="070ec-139">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="070ec-139">Return code</span></span></p></th>
<th><p><span data-ttu-id="070ec-140">Descrição</span><span class="sxs-lookup"><span data-stu-id="070ec-140">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="070ec-141">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="070ec-141">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="070ec-142">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="070ec-142">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="070ec-143">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="070ec-143">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="070ec-144">Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="070ec-144">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="070ec-145">JET_errFeatureNotAvailable</span><span class="sxs-lookup"><span data-stu-id="070ec-145">JET_errFeatureNotAvailable</span></span></p></td>
<td><p><span data-ttu-id="070ec-146">Um ponteiro <em>pconvert</em> não nulo foi fornecido, mas a versão do ESE que está sendo usada não oferece suporte ao recurso Convert.</span><span class="sxs-lookup"><span data-stu-id="070ec-146">A non-NULL <em>pconvert</em> pointer has been supplied but the version of ESE being used does not support the convert feature.</span></span> <span data-ttu-id="070ec-147">Esse recurso foi removido na versão 2003 do Windows Server do ESE.</span><span class="sxs-lookup"><span data-stu-id="070ec-147">This feature was removed in the Windows Server 2003 version of ESE.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="070ec-148">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="070ec-148">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="070ec-149">Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</span><span class="sxs-lookup"><span data-stu-id="070ec-149">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="070ec-150">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="070ec-150">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="070ec-151">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="070ec-151">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="070ec-152">A sessão de chamada está dentro de uma transação.</span><span class="sxs-lookup"><span data-stu-id="070ec-152">The calling session is within a transaction.</span></span> <span data-ttu-id="070ec-153"><strong>JetCompact</strong> deve ser chamado por uma sessão fora de qualquer transação.</span><span class="sxs-lookup"><span data-stu-id="070ec-153"><strong>JetCompact</strong> must be called by a session outside of any transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="070ec-154">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="070ec-154">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="070ec-155">Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="070ec-155">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="070ec-156">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="070ec-156">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="070ec-157">Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</span><span class="sxs-lookup"><span data-stu-id="070ec-157">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="070ec-158">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="070ec-158">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="070ec-159">A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="070ec-159">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="070ec-160">Esse erro só será retornado pelo Windows XP e por versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="070ec-160">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="070ec-161">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="070ec-161">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="070ec-162">Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="070ec-162">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="070ec-163">Em caso de sucesso, o banco de dados de origem é copiado no banco de dados de destino.</span><span class="sxs-lookup"><span data-stu-id="070ec-163">On success, the source database is copied to the destination database.</span></span> <span data-ttu-id="070ec-164">O banco de dados de destino está em um estado ideal, por exemplo, todos os índices de tabela estão localizados em espaço em disco lógico adjacente.</span><span class="sxs-lookup"><span data-stu-id="070ec-164">The destination database is in an optimal state, for example, all table indexes are located in adjacent logical disk space.</span></span> <span data-ttu-id="070ec-165">Cada página de índice é preenchida para o valor configurado quando os índices foram originalmente criados no banco de dados de origem.</span><span class="sxs-lookup"><span data-stu-id="070ec-165">Each index page is padded to the amount configured when the indexes were originally created in the source database.</span></span> <span data-ttu-id="070ec-166">Todas as configurações de dados e metadados são copiadas com fidelidade total, a menos que a opção de reparo tenha sido especificada.</span><span class="sxs-lookup"><span data-stu-id="070ec-166">All data and metadata settings are copied with full fidelity, unless the repair option was specified.</span></span> <span data-ttu-id="070ec-167">Se a opção de reparo tiver sido especificada, alguns dados do banco de dado de origem podem não ter sido copiados.</span><span class="sxs-lookup"><span data-stu-id="070ec-167">If the repair option was specified, some data from the source database may not have been copied.</span></span>

<span data-ttu-id="070ec-168">Em caso de falha, o banco de dados de destino pode existir, mas não é uma cópia completa do banco de dados de origem.</span><span class="sxs-lookup"><span data-stu-id="070ec-168">On failure, the destination database may exist but is not a full copy of the source database.</span></span>

#### <a name="remarks"></a><span data-ttu-id="070ec-169">Comentários</span><span class="sxs-lookup"><span data-stu-id="070ec-169">Remarks</span></span>

<span data-ttu-id="070ec-170">A compactação de um banco de dados também é usada para atualizar um banco de dados de um formato de versão anterior para uma versão mais moderna.</span><span class="sxs-lookup"><span data-stu-id="070ec-170">Compacting a database is also used to upgrade a database from an earlier version format to a more modern version.</span></span> <span data-ttu-id="070ec-171">Um parâmetro opcional é *pconvert*, que contém uma estrutura que pode conter uma descrição para uma DLL de versão anterior a ser usada para ler o formato do banco de dados de origem.</span><span class="sxs-lookup"><span data-stu-id="070ec-171">An optional parameter is *pconvert*, which contains a structure that can hold a description for an earlier version DLL to use for reading the source database format.</span></span> <span data-ttu-id="070ec-172">Este recurso foi descontinuado no Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="070ec-172">This feature was discontinued in Windows Server 2003.</span></span> <span data-ttu-id="070ec-173">Subsequentemente para o Windows Server 2003, as novas versões do ESE sempre podem ler versões mais antigas do formato de banco de dados e, portanto, esse recurso não é necessário.</span><span class="sxs-lookup"><span data-stu-id="070ec-173">Subsequent to Windows Server 2003, new versions of ESE are always able to read older versions of the database format and hence this feature is not needed.</span></span>

<span data-ttu-id="070ec-174">A densidade de dados desejada após uma operação de compactação é especificada quando tabelas e índices são criados.</span><span class="sxs-lookup"><span data-stu-id="070ec-174">The desired density of data after a compact operation is specified when tables and indexes are created.</span></span> <span data-ttu-id="070ec-175">A densidade deve estar entre 20% e 100%.</span><span class="sxs-lookup"><span data-stu-id="070ec-175">The density must be between 20% and 100%.</span></span> <span data-ttu-id="070ec-176">Se um banco de dados for basicamente lido e não atualizado, os aplicativos definirão a densidade como 100% para reduzir o número de operações de e/s durante o processamento da consulta.</span><span class="sxs-lookup"><span data-stu-id="070ec-176">If a database is primarily read and not updated, applications will set the density to 100% to reduce the number of I/O operations during query processing.</span></span> <span data-ttu-id="070ec-177">No entanto, se os dados forem atualizados com frequência com operações que aumentam o tamanho dos dados armazenados junto com o registro, ou se novos dados forem inseridos com frequência, o aplicativo escolherá uma densidade mais baixa para que as atualizações mais frequentemente encontrem os recursos necessários disponíveis.</span><span class="sxs-lookup"><span data-stu-id="070ec-177">However, if the data is updated frequently with operations that increase the size of data stored together with the record, or new data is frequently inserted, the application will choose a lower density so that updates will more often find needed resources available.</span></span> <span data-ttu-id="070ec-178">A operação de compactação do banco de dados faz com que o banco de dados seja idealmente disposto de acordo com o preenchimento escolhido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="070ec-178">The operation of compacting the database causes the database to be ideally laid out according to the fill chosen by the application.</span></span>

<span data-ttu-id="070ec-179">A compactação de banco de dados é uma operação off-line.</span><span class="sxs-lookup"><span data-stu-id="070ec-179">Database compaction is an off-line operation.</span></span> <span data-ttu-id="070ec-180">Ele não pode ser executado enquanto o banco de dados está em uso.</span><span class="sxs-lookup"><span data-stu-id="070ec-180">It cannot be performed while the database is in use.</span></span> <span data-ttu-id="070ec-181">Como resultado, normalmente é feito como parte de um processo de compilação do desenvolvimento de um aplicativo que fornece um conjunto de dados como parte de si mesmo.</span><span class="sxs-lookup"><span data-stu-id="070ec-181">As a result, it is typically done as part of a build process of developing an application which delivers a data set as part of itself.</span></span>

<span data-ttu-id="070ec-182">A compactação de banco de dados offline toca em todos os bits de um banco e pode ser usada como um meio de verificar a consistência de um banco de dado.</span><span class="sxs-lookup"><span data-stu-id="070ec-182">Offline database compaction touches every bit of data in a database and can be used as a means of checking the consistency of a database.</span></span> <span data-ttu-id="070ec-183">Se um banco de dados for suspeito, ele poderá ser compactado.</span><span class="sxs-lookup"><span data-stu-id="070ec-183">If a database is suspect then it can be compacted.</span></span> <span data-ttu-id="070ec-184">Se nenhum erro for encontrado na compactação, será conhecido que o banco de dados esteja em um estado válido para o ESE.</span><span class="sxs-lookup"><span data-stu-id="070ec-184">If no error is found from compaction then it will be known that the database is in a valid state for ESE.</span></span>

#### <a name="requirements"></a><span data-ttu-id="070ec-185">Requisitos</span><span class="sxs-lookup"><span data-stu-id="070ec-185">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="070ec-186"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="070ec-186"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="070ec-187">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="070ec-187">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="070ec-188"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="070ec-188"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="070ec-189">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="070ec-189">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="070ec-190"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="070ec-190"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="070ec-191">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="070ec-191">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="070ec-192"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="070ec-192"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="070ec-193">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="070ec-193">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="070ec-194"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="070ec-194"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="070ec-195">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="070ec-195">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="070ec-196"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="070ec-196"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="070ec-197">Implementado como <strong>JetCompactW</strong> (Unicode) e <strong>JetCompactA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="070ec-197">Implemented as <strong>JetCompactW</strong> (Unicode) and <strong>JetCompactA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="070ec-198">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="070ec-198">See Also</span></span>

[<span data-ttu-id="070ec-199">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="070ec-199">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="070ec-200">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="070ec-200">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="070ec-201">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="070ec-201">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="070ec-202">JetDefragment</span><span class="sxs-lookup"><span data-stu-id="070ec-202">JetDefragment</span></span>](./jetdefragment-function.md)  
[<span data-ttu-id="070ec-203">JetStopService</span><span class="sxs-lookup"><span data-stu-id="070ec-203">JetStopService</span></span>](./jetstopservice-function.md)
