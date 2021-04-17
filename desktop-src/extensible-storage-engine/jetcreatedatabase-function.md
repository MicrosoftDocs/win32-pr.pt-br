---
description: 'Saiba mais sobre: função JetCreateDatabase'
title: Função JetCreateDatabase
TOCTitle: JetCreateDatabase Function
ms:assetid: 2b13b038-1694-46d8-b903-9be64384cb06
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269212(v=EXCHG.10)
ms:contentKeyID: 32765515
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateDatabase
- JetCreateDatabaseA
- JetCreateDatabaseW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b8fbec76e3b38f9b42c36156b2312a8e77a6b43a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105798497"
---
# <a name="jetcreatedatabase-function"></a><span data-ttu-id="de65b-103">Função JetCreateDatabase</span><span class="sxs-lookup"><span data-stu-id="de65b-103">JetCreateDatabase Function</span></span>


<span data-ttu-id="de65b-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="de65b-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreatedatabase-function"></a><span data-ttu-id="de65b-105">Função JetCreateDatabase</span><span class="sxs-lookup"><span data-stu-id="de65b-105">JetCreateDatabase Function</span></span>

<span data-ttu-id="de65b-106">A função **JetCreateDatabase** cria e anexa um arquivo de banco de dados a ser usado com o mecanismo de banco de dados ESE.</span><span class="sxs-lookup"><span data-stu-id="de65b-106">The **JetCreateDatabase** function creates and attaches a database file to be used with the ESE database engine.</span></span> <span data-ttu-id="de65b-107">Chamar [JetCreateDatabase2](./jetcreatedatabase2-function.md) com *cpgDatabaseSizeMax* definido como zero é idêntico a chamar **JETCREATEDATABASE** com *szConnect* definido como nulo.</span><span class="sxs-lookup"><span data-stu-id="de65b-107">Calling [JetCreateDatabase2](./jetcreatedatabase2-function.md) with *cpgDatabaseSizeMax* set to zero is identical to calling **JetCreateDatabase** with *szConnect* set to NULL.</span></span> <span data-ttu-id="de65b-108">Atualmente, até sete bancos de dados podem ser criados por instância.</span><span class="sxs-lookup"><span data-stu-id="de65b-108">Currently, up to seven databases can be created per instance.</span></span>

```cpp
    JET_ERR JET_API JetCreateDatabase(
      __in          JET_SESID sesid,
      __in          JET_PCSTR szFilename,
      __in_opt      JET_PCSTR szConnect,
      __out         JET_DBID* pdbid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="de65b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="de65b-109">Parameters</span></span>

<span data-ttu-id="de65b-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="de65b-110">*sesid*</span></span>

<span data-ttu-id="de65b-111">O contexto da sessão de banco de dados a ser usado para a chamada à API.</span><span class="sxs-lookup"><span data-stu-id="de65b-111">The database session context to use for the API call.</span></span>

<span data-ttu-id="de65b-112">*szFilename*</span><span class="sxs-lookup"><span data-stu-id="de65b-112">*szFilename*</span></span>

<span data-ttu-id="de65b-113">O nome do banco de dados a ser criado.</span><span class="sxs-lookup"><span data-stu-id="de65b-113">The name of the database to be created.</span></span>

<span data-ttu-id="de65b-114">*szConnect*</span><span class="sxs-lookup"><span data-stu-id="de65b-114">*szConnect*</span></span>

<span data-ttu-id="de65b-115">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="de65b-115">Reserved for future use.</span></span> <span data-ttu-id="de65b-116">Definido como NULL.</span><span class="sxs-lookup"><span data-stu-id="de65b-116">Set to NULL.</span></span>

<span data-ttu-id="de65b-117">*pdbid*</span><span class="sxs-lookup"><span data-stu-id="de65b-117">*pdbid*</span></span>

<span data-ttu-id="de65b-118">Ponteiro para um buffer que, em uma chamada bem-sucedida, contém o identificador do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="de65b-118">Pointer to a buffer that, on a successful call, contains the identifier of the database.</span></span> <span data-ttu-id="de65b-119">Em caso de falha, o valor é indefinido.</span><span class="sxs-lookup"><span data-stu-id="de65b-119">On failure, the value is undefined.</span></span>

<span data-ttu-id="de65b-120">*grbit*</span><span class="sxs-lookup"><span data-stu-id="de65b-120">*grbit*</span></span>

<span data-ttu-id="de65b-121">Um grupo de bits que especifica zero ou mais das opções a seguir.</span><span class="sxs-lookup"><span data-stu-id="de65b-121">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="de65b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="de65b-122">Value</span></span></p></th>
<th><p><span data-ttu-id="de65b-123">Significado</span><span class="sxs-lookup"><span data-stu-id="de65b-123">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="de65b-124">JET_bitDbOverwriteExisting</span><span class="sxs-lookup"><span data-stu-id="de65b-124">JET_bitDbOverwriteExisting</span></span></p></td>
<td><p><span data-ttu-id="de65b-125">Por padrão, se <strong>JetCreateDatabase</strong> for chamado e o banco de dados já existir, a chamada à API falhará e o banco de dados original não será substituído.</span><span class="sxs-lookup"><span data-stu-id="de65b-125">By default, if <strong>JetCreateDatabase</strong> is called and the database already exists, the API call will fail and the original database will not be overwritten.</span></span> <span data-ttu-id="de65b-126">JET_bitDbOverwriteExisting altera esse comportamento e o banco de dados antigo será substituído por um novo.</span><span class="sxs-lookup"><span data-stu-id="de65b-126">JET_bitDbOverwriteExisting changes this behavior, and the old database will be overwritten with a new one.</span></span> <span data-ttu-id="de65b-127">Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="de65b-127">Windows XP and later.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de65b-128">JET_bitDbRecoveryOff</span><span class="sxs-lookup"><span data-stu-id="de65b-128">JET_bitDbRecoveryOff</span></span></p></td>
<td><p><span data-ttu-id="de65b-129">JET_bitDbRecoveryOff desativa o registro em log.</span><span class="sxs-lookup"><span data-stu-id="de65b-129">JET_bitDbRecoveryOff turns off logging.</span></span> <span data-ttu-id="de65b-130">A definição desse bit perde a capacidade de reproduzir arquivos de log e recuperar o banco de dados para um estado utilizável consistente após um evento catastrófico.</span><span class="sxs-lookup"><span data-stu-id="de65b-130">Setting this bit loses the ability to replay log files and recover the database to a consistent usable state after a catastrophic event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de65b-131">JET_bitDbShadowingOff</span><span class="sxs-lookup"><span data-stu-id="de65b-131">JET_bitDbShadowingOff</span></span></p></td>
<td><p><span data-ttu-id="de65b-132">A configuração JET_bitDbShadowingOff desabilitará a duplicação de algumas estruturas de banco de dados internas (sombreamento).</span><span class="sxs-lookup"><span data-stu-id="de65b-132">Setting JET_bitDbShadowingOff will disable the duplication of some internal database structures (shadowing).</span></span> <span data-ttu-id="de65b-133">A duplicação dessas estruturas é feita para manter a resiliência. portanto, a configuração JET_bitDbShadowingOff removerá essa resiliência.</span><span class="sxs-lookup"><span data-stu-id="de65b-133">The duplication of these structures is done for resiliency, so setting JET_bitDbShadowingOff will remove that resiliency.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="de65b-134">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="de65b-134">Return Value</span></span>

<span data-ttu-id="de65b-135">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="de65b-135">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="de65b-136">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="de65b-136">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="de65b-137">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="de65b-137">Return code</span></span></p></th>
<th><p><span data-ttu-id="de65b-138">Descrição</span><span class="sxs-lookup"><span data-stu-id="de65b-138">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="de65b-139">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="de65b-139">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="de65b-140">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="de65b-140">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de65b-141">JET_errDatabaseDuplicate</span><span class="sxs-lookup"><span data-stu-id="de65b-141">JET_errDatabaseDuplicate</span></span></p></td>
<td><p><span data-ttu-id="de65b-142">O banco de dados nomeado em <em>szFilename</em> já existe.</span><span class="sxs-lookup"><span data-stu-id="de65b-142">The database named in <em>szFilename</em> already exists.</span></span> <span data-ttu-id="de65b-143">Quando esse erro é retornado, o banco de dados não é anexado.</span><span class="sxs-lookup"><span data-stu-id="de65b-143">When this error is returned, the database does not get attached.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de65b-144">JET_errDatabaseInUse</span><span class="sxs-lookup"><span data-stu-id="de65b-144">JET_errDatabaseInUse</span></span></p></td>
<td><p><span data-ttu-id="de65b-145">Pode ser retornado se o acesso exclusivo tiver sido solicitado, mas não puder ser concedido ou se outra sessão já tiver aberto o banco de dados exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="de65b-145">Can be returned if exclusive access was requested, but could not be granted, or if another session has already opened the database exclusively.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de65b-146">JET_errDatabaseInvalidPages</span><span class="sxs-lookup"><span data-stu-id="de65b-146">JET_errDatabaseInvalidPages</span></span></p></td>
<td><p><span data-ttu-id="de65b-147">Retornado quando <em>cpgDatabaseSizeMax</em> é maior do que o número máximo de páginas permitido em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="de65b-147">Returned when <em>cpgDatabaseSizeMax</em> is larger than the maximum number of pages allowed in a database.</span></span> <span data-ttu-id="de65b-148">O máximo atual é 2147483646 (0x7FFFFFFE).</span><span class="sxs-lookup"><span data-stu-id="de65b-148">The current maximum is 2147483646 (0x7ffffffe).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de65b-149">JET_errDatabaseInvalidPath</span><span class="sxs-lookup"><span data-stu-id="de65b-149">JET_errDatabaseInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="de65b-150">Um caminho inválido foi fornecido em <em>szFilename</em>.</span><span class="sxs-lookup"><span data-stu-id="de65b-150">An invalid path was given in <em>szFilename</em>.</span></span> <span data-ttu-id="de65b-151"><em>szFilename</em> deve ser não nulo.</span><span class="sxs-lookup"><span data-stu-id="de65b-151"><em>szFilename</em> must be non-NULL.</span></span> <span data-ttu-id="de65b-152">Por padrão, <em>szFilename</em> deve apontar para um diretório existente.</span><span class="sxs-lookup"><span data-stu-id="de65b-152">By default, <em>szFilename</em> must point to a directory that exists.</span></span> <span data-ttu-id="de65b-153">O caminho será criado se <em>JET_paramCreatePathIfNotExist</em> estiver definido (consulte <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a>).</span><span class="sxs-lookup"><span data-stu-id="de65b-153">The path will be created if <em>JET_paramCreatePathIfNotExist</em> is set (See <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de65b-154">JET_errDatabaseLocked</span><span class="sxs-lookup"><span data-stu-id="de65b-154">JET_errDatabaseLocked</span></span></p></td>
<td><p><span data-ttu-id="de65b-155">Indica que outra sessão já abriu o banco de dados exclusivamente (usando JET_bitDbExclusive).</span><span class="sxs-lookup"><span data-stu-id="de65b-155">Indicates that another session has already opened the database exclusively (using JET_bitDbExclusive).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de65b-156">JET_errDatabaseNotFound</span><span class="sxs-lookup"><span data-stu-id="de65b-156">JET_errDatabaseNotFound</span></span></p></td>
<td><p><span data-ttu-id="de65b-157">O banco de dados não foi anexado anteriormente (consulte <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a>).</span><span class="sxs-lookup"><span data-stu-id="de65b-157">The database was not previously attached (See <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de65b-158">JET_errDatabaseSharingViolation</span><span class="sxs-lookup"><span data-stu-id="de65b-158">JET_errDatabaseSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="de65b-159">O arquivo de banco de dados já foi anexado por uma sessão diferente.</span><span class="sxs-lookup"><span data-stu-id="de65b-159">The database file has already been attached by a different session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de65b-160">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="de65b-160">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="de65b-161">Foi feita uma tentativa de criar um banco de dados em uma transação.</span><span class="sxs-lookup"><span data-stu-id="de65b-161">An attempt was made to create a database while in a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de65b-162">JET_errInvalidDatabase</span><span class="sxs-lookup"><span data-stu-id="de65b-162">JET_errInvalidDatabase</span></span></p></td>
<td><p><span data-ttu-id="de65b-163">Foi feita uma tentativa de abrir um arquivo que não é um arquivo de banco de dados válido.</span><span class="sxs-lookup"><span data-stu-id="de65b-163">An attempt was made to open a file that is not a valid database file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de65b-164">JET_errOneDatabasePerSession</span><span class="sxs-lookup"><span data-stu-id="de65b-164">JET_errOneDatabasePerSession</span></span></p></td>
<td><p><span data-ttu-id="de65b-165">Foi feita uma tentativa de abrir mais de um banco de dados e JET_paramOneDatabasePerSession foi definido.</span><span class="sxs-lookup"><span data-stu-id="de65b-165">An attempt was made to open more than one database, and JET_paramOneDatabasePerSession was set.</span></span> <span data-ttu-id="de65b-166">Consulte <a href="gg269337(v=exchg.10).md">parâmetros de banco de dados</a>.</span><span class="sxs-lookup"><span data-stu-id="de65b-166">See <a href="gg269337(v=exchg.10).md">Database Parameters</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de65b-167">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="de65b-167">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="de65b-168">A operação falhou porque não foi possível alocar memória.</span><span class="sxs-lookup"><span data-stu-id="de65b-168">The operation failed because memory could not be allocated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de65b-169">JET_errTooManyAttachedDatabases</span><span class="sxs-lookup"><span data-stu-id="de65b-169">JET_errTooManyAttachedDatabases</span></span></p></td>
<td><p><span data-ttu-id="de65b-170">Somente um número finito de banco de dados pode ser anexado por instância.</span><span class="sxs-lookup"><span data-stu-id="de65b-170">Only a finite number of database can be attached per instance.</span></span> <span data-ttu-id="de65b-171">Atualmente, o limite é de sete bancos de dados por instância.</span><span class="sxs-lookup"><span data-stu-id="de65b-171">The limit is currently seven databases per instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de65b-172">JET_wrnDatabaseAttached</span><span class="sxs-lookup"><span data-stu-id="de65b-172">JET_wrnDatabaseAttached</span></span></p></td>
<td><p><span data-ttu-id="de65b-173">Um aviso não fatal que indica que o arquivo de banco de dados já foi anexado por esta sessão.</span><span class="sxs-lookup"><span data-stu-id="de65b-173">A nonfatal warning indicating that the database file has already been attached by this session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de65b-174">JET_wrnFileOpenReadOnly</span><span class="sxs-lookup"><span data-stu-id="de65b-174">JET_wrnFileOpenReadOnly</span></span></p></td>
<td><p><span data-ttu-id="de65b-175">JET_wrnFileOpenReadOnly indica que o arquivo foi anexado somente leitura, mas <strong>JetCreateDatabase</strong> não passou JET_bitDbReadOnly.</span><span class="sxs-lookup"><span data-stu-id="de65b-175">JET_wrnFileOpenReadOnly indicates that the file was attached read-only, but <strong>JetCreateDatabase</strong> did not pass JET_bitDbReadOnly.</span></span> <span data-ttu-id="de65b-176">O banco de dados ainda está aberto com acesso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="de65b-176">The database is still opened with read-only access.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="de65b-177">Comentários</span><span class="sxs-lookup"><span data-stu-id="de65b-177">Remarks</span></span>

<span data-ttu-id="de65b-178">Se o banco de dados especificado em *szFilename* existir e JET_bitDbOverwriteExisting não tiver sido passado, a chamada à API falhará.</span><span class="sxs-lookup"><span data-stu-id="de65b-178">If the database specified in *szFilename* exists and JET_bitDbOverwriteExisting was not passed in, the API call will fail.</span></span> <span data-ttu-id="de65b-179">Se JET_bitDbOverwriteExisting foi passado, o arquivo de banco de dados antigo será excluído primeiro.</span><span class="sxs-lookup"><span data-stu-id="de65b-179">If JET_bitDbOverwriteExisting was passed in, the old database file will be deleted first.</span></span>

<span data-ttu-id="de65b-180">Se a API criar um arquivo de banco de dados e, em seguida, atingir outro erro, ele limpará e excluirá o arquivo.</span><span class="sxs-lookup"><span data-stu-id="de65b-180">If the API creates a database file and then hits another error, it will clean up and delete the file.</span></span>

<span data-ttu-id="de65b-181">**JetCreateDatabase** irá abrir implicitamente o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="de65b-181">**JetCreateDatabase** will implicitly open the database.</span></span> <span data-ttu-id="de65b-182">Não é necessariamente chamar [JetOpenDatabase](./jetopendatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="de65b-182">It is not necessarily to subsequently call [JetOpenDatabase](./jetopendatabase-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="de65b-183">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de65b-183">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="de65b-184"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="de65b-184"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="de65b-185">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="de65b-185">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de65b-186"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="de65b-186"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="de65b-187">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="de65b-187">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de65b-188"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="de65b-188"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="de65b-189">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="de65b-189">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de65b-190"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="de65b-190"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="de65b-191">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="de65b-191">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de65b-192"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="de65b-192"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="de65b-193">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="de65b-193">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de65b-194"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="de65b-194"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="de65b-195">Implementado como <strong>JetCreateDatabaseW</strong> (Unicode) e <strong>JetCreateDatabaseA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="de65b-195">Implemented as <strong>JetCreateDatabaseW</strong> (Unicode) and <strong>JetCreateDatabaseA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="de65b-196">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="de65b-196">See Also</span></span>

[<span data-ttu-id="de65b-197">Arquivos do mecanismo de armazenamento extensível</span><span class="sxs-lookup"><span data-stu-id="de65b-197">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="de65b-198">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="de65b-198">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="de65b-199">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="de65b-199">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="de65b-200">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="de65b-200">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="de65b-201">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="de65b-201">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="de65b-202">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="de65b-202">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="de65b-203">JetCloseDatabase</span><span class="sxs-lookup"><span data-stu-id="de65b-203">JetCloseDatabase</span></span>](./jetclosedatabase-function.md)  
[<span data-ttu-id="de65b-204">JetCreateDatabase2</span><span class="sxs-lookup"><span data-stu-id="de65b-204">JetCreateDatabase2</span></span>](./jetcreatedatabase2-function.md)  
[<span data-ttu-id="de65b-205">JetOpenDatabase</span><span class="sxs-lookup"><span data-stu-id="de65b-205">JetOpenDatabase</span></span>](./jetopendatabase-function.md)  
[<span data-ttu-id="de65b-206">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="de65b-206">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="de65b-207">Parâmetros do sistema</span><span class="sxs-lookup"><span data-stu-id="de65b-207">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
