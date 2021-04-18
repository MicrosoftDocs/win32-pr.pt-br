---
description: 'Saiba mais sobre: função JetCreateDatabase2'
title: Função JetCreateDatabase2
TOCTitle: JetCreateDatabase2 Function
ms:assetid: 267ac69f-49d3-4741-b324-d8510d7a36d3
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269208(v=EXCHG.10)
ms:contentKeyID: 32765511
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateDatabase2A
- JetCreateDatabase2W
- JetCreateDatabase2
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a370f88f95a2eb8217dc06124b50c9ed165eb679
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780346"
---
# <a name="jetcreatedatabase2-function"></a><span data-ttu-id="b1e6c-103">Função JetCreateDatabase2</span><span class="sxs-lookup"><span data-stu-id="b1e6c-103">JetCreateDatabase2 Function</span></span>


<span data-ttu-id="b1e6c-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="b1e6c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreatedatabase2-function"></a><span data-ttu-id="b1e6c-105">Função JetCreateDatabase2</span><span class="sxs-lookup"><span data-stu-id="b1e6c-105">JetCreateDatabase2 Function</span></span>

<span data-ttu-id="b1e6c-106">A função **JetCreateDatabase2** cria e anexa um arquivo de banco de dados a ser usado com o mecanismo de banco de dados ESE com um tamanho máximo de banco de dados especificado.</span><span class="sxs-lookup"><span data-stu-id="b1e6c-106">The **JetCreateDatabase2** function creates and attaches a database file to be used with the ESE database engine with a maximum database size specified.</span></span> <span data-ttu-id="b1e6c-107">Chamar **JetCreateDatabase2** com *cpgDatabaseSizeMax* definido como zero é idêntico a chamar [JETCREATEDATABASE](./jetcreatedatabase-function.md) com *szConnect* definido como nulo.</span><span class="sxs-lookup"><span data-stu-id="b1e6c-107">Calling **JetCreateDatabase2** with *cpgDatabaseSizeMax* set to zero is identical to calling [JetCreateDatabase](./jetcreatedatabase-function.md) with *szConnect* set to NULL.</span></span> <span data-ttu-id="b1e6c-108">Atualmente, até sete bancos de dados podem ser criados por instância.</span><span class="sxs-lookup"><span data-stu-id="b1e6c-108">Currently up to seven databases can be created per instance.</span></span>

```cpp
    JET_ERR JET_API JetCreateDatabase2(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          const unsigned long cpgDatabaseSizeMax,
      __out         JET_DBID* pdbid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="b1e6c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b1e6c-109">Parameters</span></span>

<span data-ttu-id="b1e6c-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="b1e6c-110">*sesid*</span></span>

<span data-ttu-id="b1e6c-111">O contexto da sessão de banco de dados a ser usado para a chamada à API.</span><span class="sxs-lookup"><span data-stu-id="b1e6c-111">The database session context to use for the API call.</span></span>

<span data-ttu-id="b1e6c-112">*szFilename*</span><span class="sxs-lookup"><span data-stu-id="b1e6c-112">*szFilename*</span></span>

<span data-ttu-id="b1e6c-113">O nome do banco de dados a ser criado.</span><span class="sxs-lookup"><span data-stu-id="b1e6c-113">The name of the database to be created.</span></span>

<span data-ttu-id="b1e6c-114">*cpgDatabaseSizeMax*</span><span class="sxs-lookup"><span data-stu-id="b1e6c-114">*cpgDatabaseSizeMax*</span></span>

<span data-ttu-id="b1e6c-115">O tamanho máximo, em páginas de banco de dados, para o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="b1e6c-115">The maximum size, in database pages, for the database.</span></span> <span data-ttu-id="b1e6c-116">O tamanho da página do banco de dados padrão é 4 quilobytes e pode ser alterado com [JetSetSystemParameter](./jetsetsystemparameter-function.md) antes de criar um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="b1e6c-116">The default database page size is 4 kilobytes, and can be changed with [JetSetSystemParameter](./jetsetsystemparameter-function.md) prior to creating a database.</span></span>

<span data-ttu-id="b1e6c-117">Passar zero significa que não há nenhum máximo imposto pelo mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="b1e6c-117">Passing zero means that there is no maximum enforced by the database engine.</span></span>

<span data-ttu-id="b1e6c-118">*pdbid*</span><span class="sxs-lookup"><span data-stu-id="b1e6c-118">*pdbid*</span></span>

<span data-ttu-id="b1e6c-119">Ponteiro para um buffer que, em uma chamada bem-sucedida, contém o identificador do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="b1e6c-119">Pointer to a buffer that, on a successful call, contains the identifier of the database.</span></span> <span data-ttu-id="b1e6c-120">Em caso de falha, o valor é indefinido.</span><span class="sxs-lookup"><span data-stu-id="b1e6c-120">On failure, the value is undefined.</span></span>

<span data-ttu-id="b1e6c-121">*grbit*</span><span class="sxs-lookup"><span data-stu-id="b1e6c-121">*grbit*</span></span>

<span data-ttu-id="b1e6c-122">Um grupo de bits que especifica zero ou mais das opções a seguir.</span><span class="sxs-lookup"><span data-stu-id="b1e6c-122">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b1e6c-123">Valor</span><span class="sxs-lookup"><span data-stu-id="b1e6c-123">Value</span></span></p></th>
<th><p><span data-ttu-id="b1e6c-124">Significado</span><span class="sxs-lookup"><span data-stu-id="b1e6c-124">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b1e6c-125">JET_bitDbOverwriteExisting</span><span class="sxs-lookup"><span data-stu-id="b1e6c-125">JET_bitDbOverwriteExisting</span></span></p></td>
<td><p><span data-ttu-id="b1e6c-126">Por padrão, se <a href="gg269212(v=exchg.10).md">JetCreateDatabase</a> ou <strong>JetCreateDatabase2</strong> for chamado e o banco de dados já existir, a chamada à API falhará e o banco de dados original não será substituído.</span><span class="sxs-lookup"><span data-stu-id="b1e6c-126">By default, if <a href="gg269212(v=exchg.10).md">JetCreateDatabase</a> or <strong>JetCreateDatabase2</strong> is called and the database already exists, the API call will fail and the original database will not be overwritten.</span></span> <span data-ttu-id="b1e6c-127">JET_bitDbOverwriteExisting altera esse comportamento e o banco de dados antigo será substituído por um novo.</span><span class="sxs-lookup"><span data-stu-id="b1e6c-127">JET_bitDbOverwriteExisting changes this behavior, and the old database will be overwritten with a new one.</span></span> <span data-ttu-id="b1e6c-128">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="b1e6c-128">Windows XP and later.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1e6c-129">JET_bitDbRecoveryOff</span><span class="sxs-lookup"><span data-stu-id="b1e6c-129">JET_bitDbRecoveryOff</span></span></p></td>
<td><p><span data-ttu-id="b1e6c-130">JET_bitDbRecoveryOff desativa o registro em log.</span><span class="sxs-lookup"><span data-stu-id="b1e6c-130">JET_bitDbRecoveryOff turns off logging.</span></span> <span data-ttu-id="b1e6c-131">A definição desse bit perde a capacidade de reproduzir arquivos de log e recuperar o banco de dados para um estado utilizável consistente após um evento catastrófico.</span><span class="sxs-lookup"><span data-stu-id="b1e6c-131">Setting this bit loses the ability to replay log files and recover the database to a consistent usable state after a catastrophic event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1e6c-132">JET_bitDbShadowingOff</span><span class="sxs-lookup"><span data-stu-id="b1e6c-132">JET_bitDbShadowingOff</span></span></p></td>
<td><p><span data-ttu-id="b1e6c-133">A configuração JET_bitDbShadowingOff desabilitará a duplicação de algumas estruturas de banco de dados internas (sombreamento).</span><span class="sxs-lookup"><span data-stu-id="b1e6c-133">Setting JET_bitDbShadowingOff will disable the duplication of some internal database structures (shadowing).</span></span> <span data-ttu-id="b1e6c-134">A duplicação dessas estruturas é feita para manter a resiliência. portanto, a configuração JET_bitDbShadowingOff removerá essa resiliência.</span><span class="sxs-lookup"><span data-stu-id="b1e6c-134">The duplication of these structures is done for resiliency, so setting JET_bitDbShadowingOff will remove that resiliency.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="b1e6c-135">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="b1e6c-135">Return Value</span></span>

<span data-ttu-id="b1e6c-136">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="b1e6c-136">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="b1e6c-137">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="b1e6c-137">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b1e6c-138">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="b1e6c-138">Return code</span></span></p></th>
<th><p><span data-ttu-id="b1e6c-139">Descrição</span><span class="sxs-lookup"><span data-stu-id="b1e6c-139">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b1e6c-140">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="b1e6c-140">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="b1e6c-141">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="b1e6c-141">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1e6c-142">JET_errDatabaseDuplicate</span><span class="sxs-lookup"><span data-stu-id="b1e6c-142">JET_errDatabaseDuplicate</span></span></p></td>
<td><p><span data-ttu-id="b1e6c-143">O banco de dados nomeado em <em>szFilename</em> já existe.</span><span class="sxs-lookup"><span data-stu-id="b1e6c-143">The database named in <em>szFilename</em> already exists.</span></span> <span data-ttu-id="b1e6c-144">Quando esse erro é retornado, o banco de dados não é anexado.</span><span class="sxs-lookup"><span data-stu-id="b1e6c-144">When this error is returned, the database does not get attached.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1e6c-145">JET_errDatabaseInUse</span><span class="sxs-lookup"><span data-stu-id="b1e6c-145">JET_errDatabaseInUse</span></span></p></td>
<td><p><span data-ttu-id="b1e6c-146">Pode ser retornado se o acesso exclusivo tiver sido solicitado, mas não puder ser concedido ou se outra sessão já tiver aberto o banco de dados exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="b1e6c-146">Can be returned if exclusive access was requested, but could not be granted, or if another session has already opened the database exclusively.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1e6c-147">JET_errDatabaseInvalidPages</span><span class="sxs-lookup"><span data-stu-id="b1e6c-147">JET_errDatabaseInvalidPages</span></span></p></td>
<td><p><span data-ttu-id="b1e6c-148">Retornado quando <em>cpgDatabaseSizeMax</em> é maior do que o número máximo de páginas permitido em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="b1e6c-148">Returned when <em>cpgDatabaseSizeMax</em> is larger than the maximum number of pages allowed in a database.</span></span> <span data-ttu-id="b1e6c-149">O máximo atual é 2147483646 (0x7FFFFFFE).</span><span class="sxs-lookup"><span data-stu-id="b1e6c-149">The current maximum is 2147483646 (0x7ffffffe).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1e6c-150">JET_errDatabaseInvalidPath</span><span class="sxs-lookup"><span data-stu-id="b1e6c-150">JET_errDatabaseInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="b1e6c-151">Um caminho inválido foi fornecido em <em>szFilename</em>.</span><span class="sxs-lookup"><span data-stu-id="b1e6c-151">An invalid path was given in <em>szFilename</em>.</span></span> <span data-ttu-id="b1e6c-152"><em>szFilename</em> deve ser não nulo.</span><span class="sxs-lookup"><span data-stu-id="b1e6c-152"><em>szFilename</em> must be non-NULL.</span></span> <span data-ttu-id="b1e6c-153">Por padrão, <em>szFilename</em> deve apontar para um diretório existente.</span><span class="sxs-lookup"><span data-stu-id="b1e6c-153">By default, <em>szFilename</em> must point to a directory that exists.</span></span> <span data-ttu-id="b1e6c-154">O caminho será criado se <em>JET_paramCreatePathIfNotExist</em> estiver definido (consulte <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a>).</span><span class="sxs-lookup"><span data-stu-id="b1e6c-154">The path will be created if <em>JET_paramCreatePathIfNotExist</em> is set (See <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1e6c-155">JET_errDatabaseLocked</span><span class="sxs-lookup"><span data-stu-id="b1e6c-155">JET_errDatabaseLocked</span></span></p></td>
<td><p><span data-ttu-id="b1e6c-156">Indica que outra sessão já abriu o banco de dados exclusivamente (usando JET_bitDbExclusive).</span><span class="sxs-lookup"><span data-stu-id="b1e6c-156">Indicates that another session has already opened the database exclusively (using JET_bitDbExclusive).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1e6c-157">JET_errDatabaseNotFound</span><span class="sxs-lookup"><span data-stu-id="b1e6c-157">JET_errDatabaseNotFound</span></span></p></td>
<td><p><span data-ttu-id="b1e6c-158">O banco de dados não foi anexado anteriormente (consulte <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a>).</span><span class="sxs-lookup"><span data-stu-id="b1e6c-158">The database was not previously attached (See <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1e6c-159">JET_errDatabaseSharingViolation</span><span class="sxs-lookup"><span data-stu-id="b1e6c-159">JET_errDatabaseSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="b1e6c-160">O arquivo de banco de dados já foi anexado por uma sessão diferente.</span><span class="sxs-lookup"><span data-stu-id="b1e6c-160">The database file has already been attached by a different session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1e6c-161">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="b1e6c-161">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="b1e6c-162">Foi feita uma tentativa de criar um banco de dados em uma transação.</span><span class="sxs-lookup"><span data-stu-id="b1e6c-162">An attempt was made to create a database while in a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1e6c-163">JET_errInvalidDatabase</span><span class="sxs-lookup"><span data-stu-id="b1e6c-163">JET_errInvalidDatabase</span></span></p></td>
<td><p><span data-ttu-id="b1e6c-164">Foi feita uma tentativa de abrir um arquivo que não é um arquivo de banco de dados válido.</span><span class="sxs-lookup"><span data-stu-id="b1e6c-164">An attempt was made to open a file that is not a valid database file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1e6c-165">JET_errOneDatabasePerSession</span><span class="sxs-lookup"><span data-stu-id="b1e6c-165">JET_errOneDatabasePerSession</span></span></p></td>
<td><p><span data-ttu-id="b1e6c-166">Foi feita uma tentativa de abrir mais de um banco de dados e JET_paramOneDatabasePerSession foi definido.</span><span class="sxs-lookup"><span data-stu-id="b1e6c-166">An attempt was made to open more than one database, and JET_paramOneDatabasePerSession was set.</span></span> <span data-ttu-id="b1e6c-167">Consulte <a href="gg294139(v=exchg.10).md">parâmetros do sistema</a>.</span><span class="sxs-lookup"><span data-stu-id="b1e6c-167">See <a href="gg294139(v=exchg.10).md">System Parameters</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1e6c-168">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="b1e6c-168">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="b1e6c-169">O sistema ficou com poucos recursos.</span><span class="sxs-lookup"><span data-stu-id="b1e6c-169">The system ran low on resources.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1e6c-170">JET_errTooManyAttachedDatabases</span><span class="sxs-lookup"><span data-stu-id="b1e6c-170">JET_errTooManyAttachedDatabases</span></span></p></td>
<td><p><span data-ttu-id="b1e6c-171">Somente um número finito de banco de dados pode ser anexado por instância.</span><span class="sxs-lookup"><span data-stu-id="b1e6c-171">Only a finite number of database can be attached per instance.</span></span> <span data-ttu-id="b1e6c-172">Atualmente, o limite é de sete bancos de dados por instância.</span><span class="sxs-lookup"><span data-stu-id="b1e6c-172">The limit is currently seven databases per instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1e6c-173">JET_wrnDatabaseAttached</span><span class="sxs-lookup"><span data-stu-id="b1e6c-173">JET_wrnDatabaseAttached</span></span></p></td>
<td><p><span data-ttu-id="b1e6c-174">Um aviso não fatal que indica que o arquivo de banco de dados já foi anexado por esta sessão.</span><span class="sxs-lookup"><span data-stu-id="b1e6c-174">A nonfatal warning indicating that the database file has already been attached by this session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1e6c-175">JET_wrnFileOpenReadOnly</span><span class="sxs-lookup"><span data-stu-id="b1e6c-175">JET_wrnFileOpenReadOnly</span></span></p></td>
<td><p><span data-ttu-id="b1e6c-176">JET_wrnFileOpenReadOnly indica que o arquivo foi anexado somente leitura, mas <a href="gg269212(v=exchg.10).md">JetCreateDatabase</a> não passou JET_bitDbReadOnly.</span><span class="sxs-lookup"><span data-stu-id="b1e6c-176">JET_wrnFileOpenReadOnly indicates that the file was attached read-only, but <a href="gg269212(v=exchg.10).md">JetCreateDatabase</a> did not pass JET_bitDbReadOnly.</span></span> <span data-ttu-id="b1e6c-177">O banco de dados ainda está aberto com acesso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="b1e6c-177">The database is still opened with read-only access.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="b1e6c-178">Comentários</span><span class="sxs-lookup"><span data-stu-id="b1e6c-178">Remarks</span></span>

<span data-ttu-id="b1e6c-179">Se o banco de dados especificado em *szFilename* existir e JET_bitDbOverwriteExisting não tiver sido passado, a chamada à API falhará.</span><span class="sxs-lookup"><span data-stu-id="b1e6c-179">If the database specified in *szFilename* exists and JET_bitDbOverwriteExisting was not passed in, the API call will fail.</span></span> <span data-ttu-id="b1e6c-180">Se JET_bitDbOverwriteExisting foi passado, o arquivo de banco de dados antigo será excluído primeiro.</span><span class="sxs-lookup"><span data-stu-id="b1e6c-180">If JET_bitDbOverwriteExisting was passed in, the old database file will be deleted first.</span></span>

<span data-ttu-id="b1e6c-181">Se a API criar um arquivo de banco de dados e, em seguida, atingir outro erro, ele limpará e excluirá o arquivo.</span><span class="sxs-lookup"><span data-stu-id="b1e6c-181">If the API creates a database file and then hits another error, it will clean up and delete the file.</span></span>

<span data-ttu-id="b1e6c-182">**JetCreateDatabase2** irá abrir implicitamente o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="b1e6c-182">**JetCreateDatabase2** will implicitly open the database.</span></span> <span data-ttu-id="b1e6c-183">Não é necessário, subsequentemente, chamar [JetOpenDatabase](./jetopendatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="b1e6c-183">It is not necessary to subsequently call [JetOpenDatabase](./jetopendatabase-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="b1e6c-184">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1e6c-184">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b1e6c-185"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="b1e6c-185"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="b1e6c-186">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="b1e6c-186">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1e6c-187"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="b1e6c-187"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="b1e6c-188">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="b1e6c-188">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1e6c-189"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="b1e6c-189"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="b1e6c-190">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="b1e6c-190">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1e6c-191"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="b1e6c-191"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="b1e6c-192">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="b1e6c-192">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1e6c-193"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="b1e6c-193"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="b1e6c-194">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="b1e6c-194">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1e6c-195"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="b1e6c-195"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="b1e6c-196">Implementado como <strong>JetCreateDatabase2W</strong> (Unicode) e <strong>JetCreateDatabase2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="b1e6c-196">Implemented as <strong>JetCreateDatabase2W</strong> (Unicode) and <strong>JetCreateDatabase2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="b1e6c-197">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="b1e6c-197">See Also</span></span>

[<span data-ttu-id="b1e6c-198">Arquivos do mecanismo de armazenamento extensível</span><span class="sxs-lookup"><span data-stu-id="b1e6c-198">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="b1e6c-199">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="b1e6c-199">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="b1e6c-200">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="b1e6c-200">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="b1e6c-201">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="b1e6c-201">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="b1e6c-202">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="b1e6c-202">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="b1e6c-203">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="b1e6c-203">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="b1e6c-204">JetCloseDatabase</span><span class="sxs-lookup"><span data-stu-id="b1e6c-204">JetCloseDatabase</span></span>](./jetclosedatabase-function.md)  
[<span data-ttu-id="b1e6c-205">JetCreateDatabase</span><span class="sxs-lookup"><span data-stu-id="b1e6c-205">JetCreateDatabase</span></span>](./jetcreatedatabase-function.md)  
[<span data-ttu-id="b1e6c-206">JetOpenDatabase</span><span class="sxs-lookup"><span data-stu-id="b1e6c-206">JetOpenDatabase</span></span>](./jetopendatabase-function.md)  
[<span data-ttu-id="b1e6c-207">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="b1e6c-207">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="b1e6c-208">Parâmetros do sistema</span><span class="sxs-lookup"><span data-stu-id="b1e6c-208">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
