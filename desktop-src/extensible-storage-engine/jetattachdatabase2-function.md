---
description: 'Saiba mais sobre: função JetAttachDatabase2'
title: Função JetAttachDatabase2
TOCTitle: JetAttachDatabase2 Function
ms:assetid: 8667f3fc-d178-49f1-9474-f09352614f92
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269322(v=EXCHG.10)
ms:contentKeyID: 32765612
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetAttachDatabase2A
- JetAttachDatabase2
- JetAttachDatabase2W
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a5839559751fe45ec18a55de14c565116a0f9a4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785255"
---
# <a name="jetattachdatabase2-function"></a><span data-ttu-id="b5a88-103">Função JetAttachDatabase2</span><span class="sxs-lookup"><span data-stu-id="b5a88-103">JetAttachDatabase2 Function</span></span>


<span data-ttu-id="b5a88-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="b5a88-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetattachdatabase2-function"></a><span data-ttu-id="b5a88-105">Função JetAttachDatabase2</span><span class="sxs-lookup"><span data-stu-id="b5a88-105">JetAttachDatabase2 Function</span></span>

<span data-ttu-id="b5a88-106">A função **JetAttachDatabase2** anexa um arquivo de banco de dados para uso com uma instância de banco de dados e especifica um tamanho máximo para esse banco de dados.</span><span class="sxs-lookup"><span data-stu-id="b5a88-106">The **JetAttachDatabase2** function attaches a database file for use with a database instance and specifies a maximum size for that database.</span></span> <span data-ttu-id="b5a88-107">Para usar o banco de dados, será necessário abri-lo posteriormente com [JetOpenDatabase](./jetopendatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="b5a88-107">In order to use the database, it will need to be subsequently opened with [JetOpenDatabase](./jetopendatabase-function.md).</span></span>

```cpp
    JET_ERR JET_API JetAttachDatabase2(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          const unsigned long cpgDatabaseSizeMax,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="b5a88-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b5a88-108">Parameters</span></span>

<span data-ttu-id="b5a88-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="b5a88-109">*sesid*</span></span>

<span data-ttu-id="b5a88-110">O contexto de sessão de banco de dados que será usado para a chamada à API.</span><span class="sxs-lookup"><span data-stu-id="b5a88-110">The database session context that will be used for the API call.</span></span>

<span data-ttu-id="b5a88-111">*szFilename*</span><span class="sxs-lookup"><span data-stu-id="b5a88-111">*szFilename*</span></span>

<span data-ttu-id="b5a88-112">O nome do banco de dados a ser anexado.</span><span class="sxs-lookup"><span data-stu-id="b5a88-112">The name of the database to attach.</span></span>

<span data-ttu-id="b5a88-113">*cpgDatabaseSizeMax*</span><span class="sxs-lookup"><span data-stu-id="b5a88-113">*cpgDatabaseSizeMax*</span></span>

<span data-ttu-id="b5a88-114">O tamanho máximo, em páginas de banco de dados, para o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="b5a88-114">The maximum size, in database pages, for database.</span></span> <span data-ttu-id="b5a88-115">O tamanho da página do banco de dados padrão é 4 quilobytes, que pode ser alterado usando a função [JetSetSystemParameter](./jetsetsystemparameter-function.md) antes de criar um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="b5a88-115">The default database page size is 4 kilobytes, which can be changed using the [JetSetSystemParameter](./jetsetsystemparameter-function.md) function prior to creating a database.</span></span>

<span data-ttu-id="b5a88-116">Passar zero significa que não há nenhum máximo imposto pelo mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="b5a88-116">Passing zero means that there is no maximum enforced by the database engine.</span></span>

<span data-ttu-id="b5a88-117">*grbit*</span><span class="sxs-lookup"><span data-stu-id="b5a88-117">*grbit*</span></span>

<span data-ttu-id="b5a88-118">Um grupo de bits que contém as opções a serem usadas para esta chamada, que incluem zero ou mais dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="b5a88-118">A group of bits that contain the options to be used for this call, which include zero or more of the following:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b5a88-119">Valor</span><span class="sxs-lookup"><span data-stu-id="b5a88-119">Value</span></span></p></th>
<th><p><span data-ttu-id="b5a88-120">Significado</span><span class="sxs-lookup"><span data-stu-id="b5a88-120">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b5a88-121">JET_bitDbDeleteCorruptIndexes</span><span class="sxs-lookup"><span data-stu-id="b5a88-121">JET_bitDbDeleteCorruptIndexes</span></span></p></td>
<td><p><span data-ttu-id="b5a88-122">Se <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a> tiver sido definido, todos os índices sobre dados Unicode serão excluídos.</span><span class="sxs-lookup"><span data-stu-id="b5a88-122">If <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a> has been set, all indexes over Unicode data will be deleted.</span></span> <span data-ttu-id="b5a88-123">Para obter mais detalhes, consulte a seção Comentários.</span><span class="sxs-lookup"><span data-stu-id="b5a88-123">See the Remarks section for more details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5a88-124">JET_bitDbDeleteUnicodeIndexes</span><span class="sxs-lookup"><span data-stu-id="b5a88-124">JET_bitDbDeleteUnicodeIndexes</span></span></p></td>
<td><p><span data-ttu-id="b5a88-125">Todos os índices sobre dados Unicode serão excluídos, independentemente da configuração de <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a>.</span><span class="sxs-lookup"><span data-stu-id="b5a88-125">All indexes over Unicode data will be deleted, regardless of the setting of <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a>.</span></span> <span data-ttu-id="b5a88-126">Para obter mais detalhes, consulte a seção Comentários.</span><span class="sxs-lookup"><span data-stu-id="b5a88-126">See the Remarks section for more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5a88-127">JET_bitDbReadOnly</span><span class="sxs-lookup"><span data-stu-id="b5a88-127">JET_bitDbReadOnly</span></span></p></td>
<td><p><span data-ttu-id="b5a88-128">Impede modificações no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="b5a88-128">Prevents modifications to the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5a88-129">JET_bitDbUpgrade</span><span class="sxs-lookup"><span data-stu-id="b5a88-129">JET_bitDbUpgrade</span></span></p></td>
<td><p><span data-ttu-id="b5a88-130">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="b5a88-130">Reserved for future use.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="b5a88-131">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="b5a88-131">Return Value</span></span>

<span data-ttu-id="b5a88-132">A função retorna um dos [JET_ERR](./jet-err.md) códigos de erro.</span><span class="sxs-lookup"><span data-stu-id="b5a88-132">The function returns one of the [JET_ERR](./jet-err.md) error codes.</span></span> <span data-ttu-id="b5a88-133">Veja a seguir as mais comumente retornadas.</span><span class="sxs-lookup"><span data-stu-id="b5a88-133">The following are the most commonly returned.</span></span> <span data-ttu-id="b5a88-134">(Para obter uma lista completa de erros para essa API, consulte [códigos de erro do mecanismo de armazenamento extensível](./extensible-storage-engine-error-codes.md).)</span><span class="sxs-lookup"><span data-stu-id="b5a88-134">(For a complete list of errors for this API, see [Extensible Storage Engine Error Codes](./extensible-storage-engine-error-codes.md).)</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b5a88-135">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="b5a88-135">Return code</span></span></p></th>
<th><p><span data-ttu-id="b5a88-136">Descrição</span><span class="sxs-lookup"><span data-stu-id="b5a88-136">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b5a88-137">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="b5a88-137">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="b5a88-138">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="b5a88-138">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5a88-139">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="b5a88-139">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="b5a88-140">Não é permitido anexar um banco de dados durante um backup.</span><span class="sxs-lookup"><span data-stu-id="b5a88-140">Attaching a database is not allowed during a backup.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5a88-141">JET_errDatabaseFileReadOnly</span><span class="sxs-lookup"><span data-stu-id="b5a88-141">JET_errDatabaseFileReadOnly</span></span></p></td>
<td><p><span data-ttu-id="b5a88-142">O arquivo de banco de dados especificado por <em>szFilename</em> deve ser gravável.</span><span class="sxs-lookup"><span data-stu-id="b5a88-142">The database file specified by <em>szFilename</em> must be writable.</span></span> <span data-ttu-id="b5a88-143">O atributo Read-Only não deve ser definido e o processo em execução deve ter privilégios suficientes para gravar no arquivo.</span><span class="sxs-lookup"><span data-stu-id="b5a88-143">The Read-Only attribute must not be set, and the running process must have sufficient privileges to write to the file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5a88-144">JET_errDatabaseInUse</span><span class="sxs-lookup"><span data-stu-id="b5a88-144">JET_errDatabaseInUse</span></span></p></td>
<td><p><span data-ttu-id="b5a88-145">O arquivo de banco de dados já está aberto por outro processo.</span><span class="sxs-lookup"><span data-stu-id="b5a88-145">The database file is already opened by another process.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5a88-146">JET_errDatabaseInvalidPath</span><span class="sxs-lookup"><span data-stu-id="b5a88-146">JET_errDatabaseInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="b5a88-147">Um caminho inválido foi fornecido em <em>szFilename</em>.</span><span class="sxs-lookup"><span data-stu-id="b5a88-147">An invalid path was given in <em>szFilename</em>.</span></span> <span data-ttu-id="b5a88-148"><em>szFilename</em> deve ser não nulo e referir-se a um caminho válido.</span><span class="sxs-lookup"><span data-stu-id="b5a88-148"><em>szFilename</em> must be non-NULL and refer to a valid path.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5a88-149">JET_errDatabaseSharingViolation</span><span class="sxs-lookup"><span data-stu-id="b5a88-149">JET_errDatabaseSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="b5a88-150">O arquivo de banco de dados já foi anexado por uma sessão diferente.</span><span class="sxs-lookup"><span data-stu-id="b5a88-150">The database file has already been attached by a different session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5a88-151">JET_errFileNotFound</span><span class="sxs-lookup"><span data-stu-id="b5a88-151">JET_errFileNotFound</span></span></p></td>
<td><p><span data-ttu-id="b5a88-152">O arquivo fornecido em <em>szFilename</em> não existe.</span><span class="sxs-lookup"><span data-stu-id="b5a88-152">The file given in <em>szFilename</em> does not exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5a88-153">JET_errPrimaryIndexCorrupted</span><span class="sxs-lookup"><span data-stu-id="b5a88-153">JET_errPrimaryIndexCorrupted</span></span></p></td>
<td><p><span data-ttu-id="b5a88-154">Há um erro com o índice primário.</span><span class="sxs-lookup"><span data-stu-id="b5a88-154">There is an error with the primary index.</span></span> <span data-ttu-id="b5a88-155">Isso pode ser de corrupção física (como corrupção de disco ou memória).</span><span class="sxs-lookup"><span data-stu-id="b5a88-155">This may be from physical corruption (such as disk or memory corruption).</span></span> <span data-ttu-id="b5a88-156">Ele também pode ser retornado ao anexar um banco de dados que foi modificado pela última vez em um sistema operacional mais antigo e o índice primário está sobre uma coluna com dado Unicode.</span><span class="sxs-lookup"><span data-stu-id="b5a88-156">It may also be returned when attaching a database last modified on an older operating system and the primary index is over a column with Unicode data.</span></span> <span data-ttu-id="b5a88-157">Consulte os comentários para obter mais informações sobre índices sobre dados Unicode.</span><span class="sxs-lookup"><span data-stu-id="b5a88-157">See the remarks for more information on indexes over Unicode data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5a88-158">JET_errSecondaryIndexCorrupted</span><span class="sxs-lookup"><span data-stu-id="b5a88-158">JET_errSecondaryIndexCorrupted</span></span></p></td>
<td><p><span data-ttu-id="b5a88-159">Há um erro com um índice secundário.</span><span class="sxs-lookup"><span data-stu-id="b5a88-159">There is an error with a secondary index.</span></span> <span data-ttu-id="b5a88-160">Isso pode ser de corrupção física (como corrupção de disco ou memória).</span><span class="sxs-lookup"><span data-stu-id="b5a88-160">This may be from physical corruption (such as disk or memory corruption).</span></span> <span data-ttu-id="b5a88-161">Ele também pode ser retornado ao anexar um banco de dados modificado pela última vez em um sistema operacional mais antigo, e um índice secundário está sobre uma coluna com dado Unicode.</span><span class="sxs-lookup"><span data-stu-id="b5a88-161">It may also be returned when attaching a database last modified on an older operating system and a secondary index is over a column with Unicode data.</span></span> <span data-ttu-id="b5a88-162">Consulte os comentários para obter mais informações sobre índices sobre dados Unicode.</span><span class="sxs-lookup"><span data-stu-id="b5a88-162">See the remarks for more information on indexes over Unicode data.</span></span> <span data-ttu-id="b5a88-163">Os índices secundários são completamente recriados quando um banco de dados é desfragmentado com um utilitário offline usando o seguinte comando: <strong>esentutl-d</strong>.</span><span class="sxs-lookup"><span data-stu-id="b5a88-163">Secondary indexes are completely rebuilt when a database is defragmented with an offline utility using the following command: <strong>esentutl -d</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5a88-164">JET_errTooManyAttachedDatabases</span><span class="sxs-lookup"><span data-stu-id="b5a88-164">JET_errTooManyAttachedDatabases</span></span></p></td>
<td><p><span data-ttu-id="b5a88-165">Somente um número finito de bancos de dados pode ser anexado por instância.</span><span class="sxs-lookup"><span data-stu-id="b5a88-165">Only a finite number of databases can be attached per instance.</span></span> <span data-ttu-id="b5a88-166">Atualmente, o limite é de sete bancos de dados por instância.</span><span class="sxs-lookup"><span data-stu-id="b5a88-166">The limit is currently seven databases per instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5a88-167">JET_wrnDatabaseAttached</span><span class="sxs-lookup"><span data-stu-id="b5a88-167">JET_wrnDatabaseAttached</span></span></p></td>
<td><p><span data-ttu-id="b5a88-168">Um aviso não fatal que indica que o arquivo de banco de dados já foi anexado por esta sessão.</span><span class="sxs-lookup"><span data-stu-id="b5a88-168">A nonfatal warning indicating that the database file has already been attached by this session.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="b5a88-169">Comentários</span><span class="sxs-lookup"><span data-stu-id="b5a88-169">Remarks</span></span>

<span data-ttu-id="b5a88-170">O arquivo de banco de dados é desanexado usando [JetDetachDatabase](./jetdetachdatabase-function.md) ou [JetDetachDatabase2](./jetdetachdatabase2-function.md).</span><span class="sxs-lookup"><span data-stu-id="b5a88-170">The database file is detached using [JetDetachDatabase](./jetdetachdatabase-function.md) or [JetDetachDatabase2](./jetdetachdatabase2-function.md).</span></span>

<span data-ttu-id="b5a88-171">Consulte [JetAttachDatabase](./jetattachdatabase-function.md) para ver comentários.</span><span class="sxs-lookup"><span data-stu-id="b5a88-171">See [JetAttachDatabase](./jetattachdatabase-function.md) for remarks.</span></span>

#### <a name="requirements"></a><span data-ttu-id="b5a88-172">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5a88-172">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b5a88-173"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="b5a88-173"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="b5a88-174">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="b5a88-174">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5a88-175"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="b5a88-175"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="b5a88-176">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="b5a88-176">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5a88-177"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="b5a88-177"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="b5a88-178">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="b5a88-178">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5a88-179"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="b5a88-179"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="b5a88-180">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="b5a88-180">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5a88-181"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="b5a88-181"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="b5a88-182">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="b5a88-182">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5a88-183"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="b5a88-183"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="b5a88-184">Implementado como <strong>JetAttachDatabase2W</strong> (Unicode) e <strong>JetAttachDatabase2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="b5a88-184">Implemented as <strong>JetAttachDatabase2W</strong> (Unicode) and <strong>JetAttachDatabase2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="b5a88-185">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="b5a88-185">See Also</span></span>

[<span data-ttu-id="b5a88-186">Arquivos do mecanismo de armazenamento extensível</span><span class="sxs-lookup"><span data-stu-id="b5a88-186">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="b5a88-187">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="b5a88-187">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="b5a88-188">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="b5a88-188">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="b5a88-189">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="b5a88-189">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="b5a88-190">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="b5a88-190">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="b5a88-191">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="b5a88-191">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="b5a88-192">JetCreateDatabase</span><span class="sxs-lookup"><span data-stu-id="b5a88-192">JetCreateDatabase</span></span>](./jetcreatedatabase-function.md)  
[<span data-ttu-id="b5a88-193">JetOpenDatabase</span><span class="sxs-lookup"><span data-stu-id="b5a88-193">JetOpenDatabase</span></span>](./jetopendatabase-function.md)  
[<span data-ttu-id="b5a88-194">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="b5a88-194">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
