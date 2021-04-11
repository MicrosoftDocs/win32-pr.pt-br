---
description: 'Saiba mais sobre: função JetAttachDatabase'
title: Função JetAttachDatabase
TOCTitle: JetAttachDatabase Function
ms:assetid: bc4c9a76-203c-424a-ac17-f096e3a6e04e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294074(v=EXCHG.10)
ms:contentKeyID: 32765689
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetAttachDatabase
- JetAttachDatabaseW
- JetAttachDatabaseA
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b5968fe7906ace720dad3f94e278f37d992710d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164262"
---
# <a name="jetattachdatabase-function"></a><span data-ttu-id="6ff44-103">Função JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="6ff44-103">JetAttachDatabase Function</span></span>


<span data-ttu-id="6ff44-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="6ff44-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetattachdatabase-function"></a><span data-ttu-id="6ff44-105">Função JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="6ff44-105">JetAttachDatabase Function</span></span>

<span data-ttu-id="6ff44-106">A função **JetAttachDatabase** anexa um arquivo de banco de dados para uso com uma instância de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6ff44-106">The **JetAttachDatabase** function attaches a database file for use with a database instance.</span></span> <span data-ttu-id="6ff44-107">Para usar o banco de dados, será necessário abri-lo posteriormente com [JetOpenDatabase](./jetopendatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="6ff44-107">In order to use the database, it will need to be subsequently opened with [JetOpenDatabase](./jetopendatabase-function.md).</span></span>

```cpp
    JET_ERR JET_API JetAttachDatabase(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="6ff44-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6ff44-108">Parameters</span></span>

<span data-ttu-id="6ff44-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="6ff44-109">*sesid*</span></span>

<span data-ttu-id="6ff44-110">O contexto da sessão de banco de dados a ser usado para a chamada à API.</span><span class="sxs-lookup"><span data-stu-id="6ff44-110">The database session context to use for the API call.</span></span>

<span data-ttu-id="6ff44-111">*szFilename*</span><span class="sxs-lookup"><span data-stu-id="6ff44-111">*szFilename*</span></span>

<span data-ttu-id="6ff44-112">O nome do banco de dados a ser anexado.</span><span class="sxs-lookup"><span data-stu-id="6ff44-112">The name of the database to attach.</span></span>

<span data-ttu-id="6ff44-113">*grbit*</span><span class="sxs-lookup"><span data-stu-id="6ff44-113">*grbit*</span></span>

<span data-ttu-id="6ff44-114">Um grupo de bits que especifica zero ou mais das opções a seguir.</span><span class="sxs-lookup"><span data-stu-id="6ff44-114">A group of bits that specify zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6ff44-115">Valor</span><span class="sxs-lookup"><span data-stu-id="6ff44-115">Value</span></span></p></th>
<th><p><span data-ttu-id="6ff44-116">Significado</span><span class="sxs-lookup"><span data-stu-id="6ff44-116">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6ff44-117">JET_bitDbDeleteCorruptIndexes</span><span class="sxs-lookup"><span data-stu-id="6ff44-117">JET_bitDbDeleteCorruptIndexes</span></span></p></td>
<td><p><span data-ttu-id="6ff44-118">Se <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a> tiver sido definido, todos os índices sobre dados Unicode serão excluídos.</span><span class="sxs-lookup"><span data-stu-id="6ff44-118">If <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a> has been set, all indexes over Unicode data will be deleted.</span></span> <span data-ttu-id="6ff44-119">Para obter mais detalhes, consulte a seção Comentários.</span><span class="sxs-lookup"><span data-stu-id="6ff44-119">See the Remarks section for more details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ff44-120">JET_bitDbDeleteUnicodeIndexes</span><span class="sxs-lookup"><span data-stu-id="6ff44-120">JET_bitDbDeleteUnicodeIndexes</span></span></p></td>
<td><p><span data-ttu-id="6ff44-121">Todos os índices sobre dados Unicode serão excluídos, independentemente da configuração de <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a>.</span><span class="sxs-lookup"><span data-stu-id="6ff44-121">All indexes over Unicode data will be deleted, regardless of the setting of <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a>.</span></span> <span data-ttu-id="6ff44-122">Para obter mais detalhes, consulte a seção Comentários.</span><span class="sxs-lookup"><span data-stu-id="6ff44-122">See the Remarks section for more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ff44-123">JET_bitDbUpgrade</span><span class="sxs-lookup"><span data-stu-id="6ff44-123">JET_bitDbUpgrade</span></span></p></td>
<td><p><span data-ttu-id="6ff44-124">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="6ff44-124">Obsolete.</span></span> <span data-ttu-id="6ff44-125">Não use.</span><span class="sxs-lookup"><span data-stu-id="6ff44-125">Do not use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ff44-126">JET_bitDbReadOnly</span><span class="sxs-lookup"><span data-stu-id="6ff44-126">JET_bitDbReadOnly</span></span></p></td>
<td><p><span data-ttu-id="6ff44-127">Impede modificações no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6ff44-127">Prevents modifications to the database.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="6ff44-128">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="6ff44-128">Return Value</span></span>

<span data-ttu-id="6ff44-129">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="6ff44-129">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="6ff44-130">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="6ff44-130">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6ff44-131">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="6ff44-131">Return code</span></span></p></th>
<th><p><span data-ttu-id="6ff44-132">Descrição</span><span class="sxs-lookup"><span data-stu-id="6ff44-132">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6ff44-133">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="6ff44-133">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="6ff44-134">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="6ff44-134">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ff44-135">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="6ff44-135">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="6ff44-136">Não é permitido anexar um banco de dados durante um backup.</span><span class="sxs-lookup"><span data-stu-id="6ff44-136">Attaching a database is not allowed during a backup.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ff44-137">JET_errDatabaseFileReadOnly</span><span class="sxs-lookup"><span data-stu-id="6ff44-137">JET_errDatabaseFileReadOnly</span></span></p></td>
<td><p><span data-ttu-id="6ff44-138">O arquivo de banco de dados especificado por <em>szFilename</em> deve ser gravável.</span><span class="sxs-lookup"><span data-stu-id="6ff44-138">The database file specified by <em>szFilename</em> must be writable.</span></span> <span data-ttu-id="6ff44-139">O atributo Read-Only não deve ser definido e o processo em execução deve ter privilégios suficientes para gravar no arquivo.</span><span class="sxs-lookup"><span data-stu-id="6ff44-139">The Read-Only attribute must not be set, and the running process must have sufficient privileges to write to the file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ff44-140">JET_errDatabaseInUse</span><span class="sxs-lookup"><span data-stu-id="6ff44-140">JET_errDatabaseInUse</span></span></p></td>
<td><p><span data-ttu-id="6ff44-141">O arquivo de banco de dados já está aberto por outro processo.</span><span class="sxs-lookup"><span data-stu-id="6ff44-141">The database file is already opened by another process.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ff44-142">JET_errDatabaseInvalidPath</span><span class="sxs-lookup"><span data-stu-id="6ff44-142">JET_errDatabaseInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="6ff44-143">Um caminho inválido foi fornecido em <em>szFilename</em>.</span><span class="sxs-lookup"><span data-stu-id="6ff44-143">An invalid path was given in <em>szFilename</em>.</span></span> <span data-ttu-id="6ff44-144"><em>szFilename</em> deve ser não nulo e referir-se a um caminho válido.</span><span class="sxs-lookup"><span data-stu-id="6ff44-144"><em>szFilename</em> must be non-NULL and refer to a valid path.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ff44-145">JET_errDatabaseSharingViolation</span><span class="sxs-lookup"><span data-stu-id="6ff44-145">JET_errDatabaseSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="6ff44-146">O arquivo de banco de dados já foi anexado por uma sessão diferente.</span><span class="sxs-lookup"><span data-stu-id="6ff44-146">The database file has already been attached by a different session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ff44-147">JET_errFileAccessDenied</span><span class="sxs-lookup"><span data-stu-id="6ff44-147">JET_errFileAccessDenied</span></span></p></td>
<td><p><span data-ttu-id="6ff44-148">O mecanismo de banco de dados não pode abrir o arquivo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6ff44-148">The database engine cannot open the database file.</span></span> <span data-ttu-id="6ff44-149">O arquivo pode estar em uso por outro processo ou o chamador pode não ter privilégios suficientes para abrir o arquivo.</span><span class="sxs-lookup"><span data-stu-id="6ff44-149">The file may be in use by another process or the caller may not have sufficient privileges to open the file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ff44-150">JET_errFileNotFound</span><span class="sxs-lookup"><span data-stu-id="6ff44-150">JET_errFileNotFound</span></span></p></td>
<td><p><span data-ttu-id="6ff44-151">O arquivo fornecido em <em>szFilename</em> não existe.</span><span class="sxs-lookup"><span data-stu-id="6ff44-151">The file given in <em>szFilename</em> does not exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ff44-152">JET_errPrimaryIndexCorrupted</span><span class="sxs-lookup"><span data-stu-id="6ff44-152">JET_errPrimaryIndexCorrupted</span></span></p></td>
<td><p><span data-ttu-id="6ff44-153">Há um erro com o índice primário.</span><span class="sxs-lookup"><span data-stu-id="6ff44-153">There is an error with the primary index.</span></span> <span data-ttu-id="6ff44-154">Isso pode ser de corrupção física (como corrupção de disco ou memória).</span><span class="sxs-lookup"><span data-stu-id="6ff44-154">This may be from physical corruption (such as disk or memory corruption).</span></span> <span data-ttu-id="6ff44-155">Ele também pode ser retornado ao anexar um banco de dados que foi modificado pela última vez em um sistema operacional mais antigo e o índice primário está sobre uma coluna com dado Unicode.</span><span class="sxs-lookup"><span data-stu-id="6ff44-155">It may also be returned when attaching a database last modified on an older operating system and the primary index is over a column with Unicode data.</span></span> <span data-ttu-id="6ff44-156">Consulte os comentários para obter mais informações sobre índices sobre dados Unicode.</span><span class="sxs-lookup"><span data-stu-id="6ff44-156">See the remarks for more information on indexes over Unicode data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ff44-157">JET_errSecondaryIndexCorrupted</span><span class="sxs-lookup"><span data-stu-id="6ff44-157">JET_errSecondaryIndexCorrupted</span></span></p></td>
<td><p><span data-ttu-id="6ff44-158">Há um erro com um índice secundário.</span><span class="sxs-lookup"><span data-stu-id="6ff44-158">There is an error with a secondary index.</span></span> <span data-ttu-id="6ff44-159">Isso pode ser de corrupção física (como corrupção de disco ou memória).</span><span class="sxs-lookup"><span data-stu-id="6ff44-159">This may be from physical corruption (such as disk or memory corruption).</span></span> <span data-ttu-id="6ff44-160">Ele também pode ser retornado ao anexar um banco de dados modificado pela última vez em um sistema operacional mais antigo, e um índice secundário está sobre uma coluna com dado Unicode.</span><span class="sxs-lookup"><span data-stu-id="6ff44-160">It may also be returned when attaching a database last modified on an older operating system and a secondary index is over a column with Unicode data.</span></span> <span data-ttu-id="6ff44-161">Consulte os comentários para obter mais informações sobre índices sobre dados Unicode.</span><span class="sxs-lookup"><span data-stu-id="6ff44-161">See the remarks for more information on indexes over Unicode data.</span></span> <span data-ttu-id="6ff44-162">Os índices secundários são completamente recriados quando um banco de dados é desfragmentado com um utilitário offline usando o seguinte comando: <strong>esentutl-d</strong>.</span><span class="sxs-lookup"><span data-stu-id="6ff44-162">Secondary indexes are completely rebuilt when a database is defragmented with an offline utility using the following command: <strong>esentutl -d</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ff44-163">JET_errTooManyAttachedDatabases</span><span class="sxs-lookup"><span data-stu-id="6ff44-163">JET_errTooManyAttachedDatabases</span></span></p></td>
<td><p><span data-ttu-id="6ff44-164">Somente um número finito de bancos de dados pode ser anexado por instância.</span><span class="sxs-lookup"><span data-stu-id="6ff44-164">Only a finite number of databases can be attached per instance.</span></span> <span data-ttu-id="6ff44-165">Atualmente, o limite é de sete bancos de dados por instância.</span><span class="sxs-lookup"><span data-stu-id="6ff44-165">The limit is currently seven databases per instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ff44-166">JET_wrnDatabaseAttached</span><span class="sxs-lookup"><span data-stu-id="6ff44-166">JET_wrnDatabaseAttached</span></span></p></td>
<td><p><span data-ttu-id="6ff44-167">Um aviso não fatal que indica que o arquivo de banco de dados já foi anexado por esta sessão.</span><span class="sxs-lookup"><span data-stu-id="6ff44-167">A nonfatal warning indicating that the database file has already been attached by this session.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="6ff44-168">Comentários</span><span class="sxs-lookup"><span data-stu-id="6ff44-168">Remarks</span></span>

<span data-ttu-id="6ff44-169">Chamar **JetAttachDatabase** é equivalente a chamar [JetAttachDatabase2](./jetattachdatabase2-function.md) e passar um valor de zero, o que significa que não há nenhum limite para o parâmetro *cpgDatabaseSizeMax* .</span><span class="sxs-lookup"><span data-stu-id="6ff44-169">Calling **JetAttachDatabase** is equivalent to calling [JetAttachDatabase2](./jetattachdatabase2-function.md) and passing a value of zero, meaning there is no limit, for the *cpgDatabaseSizeMax* parameter.</span></span>

<span data-ttu-id="6ff44-170">Anexar um banco de dados gravável (ou seja, se JET_bitDbReadOnly não foi especificado no parâmetro *grbit* ) abrirá o arquivo exclusivamente no nível do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="6ff44-170">Attaching a writable database (that is, if JET_bitDbReadOnly was not specified in the *grbit* parameter) will open the file exclusively at the operating system level.</span></span> <span data-ttu-id="6ff44-171">Nenhum outro processo será capaz de abrir o arquivo.</span><span class="sxs-lookup"><span data-stu-id="6ff44-171">No other process will be able open the file.</span></span> <span data-ttu-id="6ff44-172">É possível que vários processos anexem um banco de dados individual abrindo-os no modo somente leitura.</span><span class="sxs-lookup"><span data-stu-id="6ff44-172">It is possible for multiple processes to attach a single database by opening them in read-only mode.</span></span>

<span data-ttu-id="6ff44-173">O arquivo de banco de dados é desanexado usando [JetDetachDatabase](./jetdetachdatabase-function.md) ou [JetDetachDatabase2](./jetdetachdatabase2-function.md).</span><span class="sxs-lookup"><span data-stu-id="6ff44-173">The database file is detached using [JetDetachDatabase](./jetdetachdatabase-function.md) or [JetDetachDatabase2](./jetdetachdatabase2-function.md).</span></span>

<span data-ttu-id="6ff44-174">Parâmetros de verificação de índice</span><span class="sxs-lookup"><span data-stu-id="6ff44-174">Index-checking parameters</span></span>

<span data-ttu-id="6ff44-175">Versões diferentes do Windows normalizam texto Unicode de maneiras diferentes.</span><span class="sxs-lookup"><span data-stu-id="6ff44-175">Different versions of Windows normalize Unicode text in different ways.</span></span> <span data-ttu-id="6ff44-176">Isso significa que os índices criados em uma versão do Windows podem não funcionar em outras versões.</span><span class="sxs-lookup"><span data-stu-id="6ff44-176">That means indexes built under one version of Windows may not work on other versions.</span></span>

<span data-ttu-id="6ff44-177">Antes do Windows Server 2003, quando a versão do sistema operacional foi alterada (incluindo a instalação de um Service Pack), cada índice sobre dados Unicode estava em um estado potencialmente corrompido.</span><span class="sxs-lookup"><span data-stu-id="6ff44-177">Prior to Windows Server 2003, when the operating system version changed (including installation of a Service Pack), every index over Unicode data was in a potentially corrupt state.</span></span>

<span data-ttu-id="6ff44-178">Os índices criados no Windows Server 2003 e versões posteriores são sinalizados com a versão de normalização Unicode com a qual foram criados.</span><span class="sxs-lookup"><span data-stu-id="6ff44-178">Indexes created in Windows Server 2003 and later are flagged with the version of Unicode normalization with which they were built.</span></span> <span data-ttu-id="6ff44-179">Índices mais antigos não contêm informações de versão.</span><span class="sxs-lookup"><span data-stu-id="6ff44-179">Older indexes contain no version information.</span></span> <span data-ttu-id="6ff44-180">A maioria das alterações de normalização Unicode consiste na adição de novos caracteres, pontos de código que anteriormente não foram definidos agora são definidos e normalizados de forma diferente.</span><span class="sxs-lookup"><span data-stu-id="6ff44-180">Most Unicode normalization changes consist of adding new characters, code points which were previously undefined are now defined and normalize differently.</span></span> <span data-ttu-id="6ff44-181">Portanto, se os dados binários forem armazenados em uma coluna Unicode, eles serão normalizados de forma diferente conforme novos pontos de código são definidos.</span><span class="sxs-lookup"><span data-stu-id="6ff44-181">Thus, if binary data is stored in a Unicode column, it will normalize differently as new code points are defined.</span></span>

<span data-ttu-id="6ff44-182">A partir do Windows Server 2003, o mecanismo de banco de dados ESE rastreia entradas de índice Unicode que contêm pontos de código indefinidos.</span><span class="sxs-lookup"><span data-stu-id="6ff44-182">As of Windows Server 2003, the ESE database engine tracks Unicode index entries that contain undefined code points.</span></span> <span data-ttu-id="6ff44-183">Eles podem ser usados para corrigir um índice quando o conjunto de caracteres Unicode definido for alterado.</span><span class="sxs-lookup"><span data-stu-id="6ff44-183">These can be used to fix an index when the set of defined Unicode characters changes.</span></span>

<span data-ttu-id="6ff44-184">Esses parâmetros controlam o que acontece quando o mecanismo de banco de dados ESE é anexado a um banco de dados que foi usado pela última vez em uma compilação diferente do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="6ff44-184">These parameters control what happens when the ESE database engine attaches to a database that was last used under a different build of the operating system.</span></span> <span data-ttu-id="6ff44-185">A versão do sistema operacional é carimbada no cabeçalho do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6ff44-185">The operating system version is stamped in the database header.</span></span>

<span data-ttu-id="6ff44-186">Se [JET_paramEnableIndexChecking](./database-parameters.md) for definido como **true** e o banco de dados contiver índices potencialmente corrompidos:</span><span class="sxs-lookup"><span data-stu-id="6ff44-186">If [JET_paramEnableIndexChecking](./database-parameters.md) is set to **TRUE**, and the database contains potentially corrupt indexes:</span></span>

  - <span data-ttu-id="6ff44-187">**JetAttachDatabase** excluirá os índices potencialmente corrompidos se *grbit* contiver JET_bitDbDeleteCorruptIndexes</span><span class="sxs-lookup"><span data-stu-id="6ff44-187">**JetAttachDatabase** will delete the potentially corrupt indexes if *grbit* contains JET_bitDbDeleteCorruptIndexes</span></span>

  - <span data-ttu-id="6ff44-188">**JetAttachDatabase** retornará um erro se *grbit* não contiver JET_bitDbDeleteCorruptIndexes e houver índices que precisam de exclusão.</span><span class="sxs-lookup"><span data-stu-id="6ff44-188">**JetAttachDatabase** will return an error if *grbit* does not contain JET_bitDbDeleteCorruptIndexes and there are indexes which need deletion.</span></span>

<span data-ttu-id="6ff44-189">Se [JET_paramEnableIndexChecking](./database-parameters.md) for definido como **false**:</span><span class="sxs-lookup"><span data-stu-id="6ff44-189">If [JET_paramEnableIndexChecking](./database-parameters.md) is set to **FALSE**:</span></span>

  - <span data-ttu-id="6ff44-190">**JetAttachDatabase** ignorará índices potencialmente corrompidos e retornará JET_errSuccess (supondo que não haja nenhum outro erro).</span><span class="sxs-lookup"><span data-stu-id="6ff44-190">**JetAttachDatabase** will ignore potentially corrupt indexes, and return JET_errSuccess (assuming there were no other errors).</span></span>

<span data-ttu-id="6ff44-191">Windows Server 2003 e posterior: se [JET_paramEnableIndexChecking](./database-parameters.md) não tiver sido redefinido, a tabela de correção interna será usada para corrigir entradas de índice.</span><span class="sxs-lookup"><span data-stu-id="6ff44-191">Windows Server 2003 and later: If [JET_paramEnableIndexChecking](./database-parameters.md) has not been reset, the internal fixup table will be used to fixup index entries.</span></span> <span data-ttu-id="6ff44-192">Isso pode não corrigir todas as corrupções de índice, mas será transparente para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6ff44-192">This may not fix all index corruptions but will be transparent to the application.</span></span>

<span data-ttu-id="6ff44-193">Se o banco de dados foi anexado como somente leitura, o índice não pode ser corrigido ou excluído.</span><span class="sxs-lookup"><span data-stu-id="6ff44-193">If the database was attached as read-only the index cannot be fixed or deleted.</span></span> <span data-ttu-id="6ff44-194">Nesse caso, a API retornará, em vez disso, um erro, como JET_errSecondaryIndexCorrupted ou JET_errPrimaryIndexCorrupted.</span><span class="sxs-lookup"><span data-stu-id="6ff44-194">In this case, the API will instead return an error, such as JET_errSecondaryIndexCorrupted or JET_errPrimaryIndexCorrupted.</span></span>

#### <a name="requirements"></a><span data-ttu-id="6ff44-195">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ff44-195">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6ff44-196"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="6ff44-196"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="6ff44-197">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="6ff44-197">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ff44-198"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="6ff44-198"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="6ff44-199">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="6ff44-199">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ff44-200"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="6ff44-200"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="6ff44-201">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="6ff44-201">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ff44-202"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="6ff44-202"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="6ff44-203">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="6ff44-203">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ff44-204"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="6ff44-204"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="6ff44-205">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="6ff44-205">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ff44-206"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="6ff44-206"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="6ff44-207">Implementado como <strong>JetAddColumnW</strong> (Unicode) e <strong>JetAddColumnA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="6ff44-207">Implemented as <strong>JetAddColumnW</strong> (Unicode) and <strong>JetAddColumnA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="6ff44-208">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="6ff44-208">See Also</span></span>

[<span data-ttu-id="6ff44-209">Arquivos do mecanismo de armazenamento extensível</span><span class="sxs-lookup"><span data-stu-id="6ff44-209">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="6ff44-210">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="6ff44-210">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="6ff44-211">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="6ff44-211">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="6ff44-212">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="6ff44-212">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="6ff44-213">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="6ff44-213">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="6ff44-214">JetAttachDatabase2</span><span class="sxs-lookup"><span data-stu-id="6ff44-214">JetAttachDatabase2</span></span>](./jetattachdatabase2-function.md)  
[<span data-ttu-id="6ff44-215">JetCreateDatabase</span><span class="sxs-lookup"><span data-stu-id="6ff44-215">JetCreateDatabase</span></span>](./jetcreatedatabase-function.md)  
[<span data-ttu-id="6ff44-216">JetDetachDatabase</span><span class="sxs-lookup"><span data-stu-id="6ff44-216">JetDetachDatabase</span></span>](./jetdetachdatabase-function.md)  
[<span data-ttu-id="6ff44-217">JetDetachDatabase2</span><span class="sxs-lookup"><span data-stu-id="6ff44-217">JetDetachDatabase2</span></span>](./jetdetachdatabase2-function.md)  
[<span data-ttu-id="6ff44-218">JetOpenDatabase</span><span class="sxs-lookup"><span data-stu-id="6ff44-218">JetOpenDatabase</span></span>](./jetopendatabase-function.md)  
[<span data-ttu-id="6ff44-219">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="6ff44-219">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
