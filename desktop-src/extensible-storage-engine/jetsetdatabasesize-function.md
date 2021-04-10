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
# <a name="jetsetdatabasesize-function"></a><span data-ttu-id="40a89-103">Função JetSetDatabaseSize</span><span class="sxs-lookup"><span data-stu-id="40a89-103">JetSetDatabaseSize Function</span></span>


<span data-ttu-id="40a89-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="40a89-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetdatabasesize-function"></a><span data-ttu-id="40a89-105">Função JetSetDatabaseSize</span><span class="sxs-lookup"><span data-stu-id="40a89-105">JetSetDatabaseSize Function</span></span>

<span data-ttu-id="40a89-106">A função **JetSetDatabaseSize** define o tamanho de um arquivo de banco de dados não aberto.</span><span class="sxs-lookup"><span data-stu-id="40a89-106">The **JetSetDatabaseSize** function sets the size of an unopened database file.</span></span>

```cpp
    JET_ERR JET_API JetSetDatabaseSize(
      __in          JET_SESID sesid,
      __in          JET_PCSTR szDatabaseName,
      __in          unsigned long cpg,
      __out         unsigned long* pcpgReal
    );
```

### <a name="parameters"></a><span data-ttu-id="40a89-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="40a89-107">Parameters</span></span>

<span data-ttu-id="40a89-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="40a89-108">*sesid*</span></span>

<span data-ttu-id="40a89-109">Identifica o contexto de sessão de banco de dados a ser usado para a chamada à API.</span><span class="sxs-lookup"><span data-stu-id="40a89-109">Identifies the database session context to use for the API call.</span></span>

<span data-ttu-id="40a89-110">*szDatabaseName*</span><span class="sxs-lookup"><span data-stu-id="40a89-110">*szDatabaseName*</span></span>

<span data-ttu-id="40a89-111">Identifica o nome do arquivo de banco de dados cujo tamanho deve ser alterado.</span><span class="sxs-lookup"><span data-stu-id="40a89-111">Identifies the name of the database file whose size is to be altered.</span></span>

<span data-ttu-id="40a89-112">*CPG*</span><span class="sxs-lookup"><span data-stu-id="40a89-112">*cpg*</span></span>

<span data-ttu-id="40a89-113">Especifica o tamanho desejado do banco de dados, em páginas.</span><span class="sxs-lookup"><span data-stu-id="40a89-113">Specifies the desired size of the database, in pages.</span></span>

<span data-ttu-id="40a89-114">*pcpgReal*</span><span class="sxs-lookup"><span data-stu-id="40a89-114">*pcpgReal*</span></span>

<span data-ttu-id="40a89-115">Ponteiro para um número que recebe o tamanho do banco de dados, em páginas, após a chamada à API.</span><span class="sxs-lookup"><span data-stu-id="40a89-115">Pointer to a number that receives the size of the database, in pages, after the API call.</span></span> <span data-ttu-id="40a89-116">Se a chamada à API não tiver sido bem-sucedida, o conteúdo de *pcpgReal* será indefinido.</span><span class="sxs-lookup"><span data-stu-id="40a89-116">If the API call was unsuccessful, the contents of *pcpgReal* are undefined.</span></span>

### <a name="return-value"></a><span data-ttu-id="40a89-117">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="40a89-117">Return Value</span></span>

<span data-ttu-id="40a89-118">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="40a89-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="40a89-119">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="40a89-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="40a89-120">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="40a89-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="40a89-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="40a89-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="40a89-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="40a89-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="40a89-123">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="40a89-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40a89-124">JET_errDatabaseInconsistent</span><span class="sxs-lookup"><span data-stu-id="40a89-124">JET_errDatabaseInconsistent</span></span><br />
<span data-ttu-id="40a89-125">JET_errDatabaseDirtyShutdown</span><span class="sxs-lookup"><span data-stu-id="40a89-125">JET_errDatabaseDirtyShutdown</span></span></p></td>
<td><p><span data-ttu-id="40a89-126">JET_errDatabaseInconsistent e JET_errDatabaseDirtyShutdown são do mesmo valor numérico.</span><span class="sxs-lookup"><span data-stu-id="40a89-126">JET_errDatabaseInconsistent and JET_errDatabaseDirtyShutdown are the same numeric value.</span></span> <span data-ttu-id="40a89-127">O banco de dados cujo tamanho será ajustado deve estar em um desligamento normal, conhecido como um estado consistente.</span><span class="sxs-lookup"><span data-stu-id="40a89-127">The database whose size is to be adjusted must be in a clean shutdown, known as a consistent state.</span></span> <span data-ttu-id="40a89-128">Um banco de dados inconsistente não está corrompido, mas requer que os arquivos de log sejam reproduzidos.</span><span class="sxs-lookup"><span data-stu-id="40a89-128">An inconsistent database is not corrupted, but it requires log files to be replayed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40a89-129">JET_errDatabaseInvalidPath</span><span class="sxs-lookup"><span data-stu-id="40a89-129">JET_errDatabaseInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="40a89-130"><em>szDatabaseName</em> não deve ser uma cadeia de caracteres vazia e não nula.</span><span class="sxs-lookup"><span data-stu-id="40a89-130"><em>szDatabaseName</em> must not be an empty, non-NULL string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40a89-131">JET_errDiskFull</span><span class="sxs-lookup"><span data-stu-id="40a89-131">JET_errDiskFull</span></span></p></td>
<td><p><span data-ttu-id="40a89-132">Não há espaço livre suficiente no volume para executar a operação de crescimento.</span><span class="sxs-lookup"><span data-stu-id="40a89-132">There is insufficient free space on the volume to perform the grow operation.</span></span> <span data-ttu-id="40a89-133">O <strong>JetSetDatabaseSize</strong> também pode retornar muitos erros relacionados a arquivos, incluindo, mas não se limitando a:</span><span class="sxs-lookup"><span data-stu-id="40a89-133"><strong>JetSetDatabaseSize</strong> may also return many file-related errors, including, but not limited to:</span></span></p>
<ul>
<li><p><span data-ttu-id="40a89-134">JET_errDiskIO</span><span class="sxs-lookup"><span data-stu-id="40a89-134">JET_errDiskIO</span></span></p></li>
<li><p><span data-ttu-id="40a89-135">JET_errFileNotFound</span><span class="sxs-lookup"><span data-stu-id="40a89-135">JET_errFileNotFound</span></span></p></li>
<li><p><span data-ttu-id="40a89-136">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="40a89-136">JET_errInvalidPath</span></span></p></li>
<li><p><span data-ttu-id="40a89-137">JET_errFileAccessDenied</span><span class="sxs-lookup"><span data-stu-id="40a89-137">JET_errFileAccessDenied</span></span></p></li>
<li><p><span data-ttu-id="40a89-138">JET_errOutOfFileHandles</span><span class="sxs-lookup"><span data-stu-id="40a89-138">JET_errOutOfFileHandles</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40a89-139">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="40a89-139">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="40a89-140">Um dos motivos pelos quais esse erro pode ser retornado é se o <em>CPG</em> atender ao tamanho mínimo do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="40a89-140">One of the reasons this error may be returned is if <em>cpg</em> does meet the minimum database size.</span></span> <span data-ttu-id="40a89-141">O tamanho mínimo atual do banco de dados é de 256 páginas.</span><span class="sxs-lookup"><span data-stu-id="40a89-141">The current minimum database size is 256 pages.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40a89-142">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="40a89-142">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="40a89-143">O sistema está com poucos recursos de memória.</span><span class="sxs-lookup"><span data-stu-id="40a89-143">The system is low on memory resources.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="40a89-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="40a89-144">Remarks</span></span>

<span data-ttu-id="40a89-145">Se **JetSetDatabaseSize** for chamado antes da inserção de grandes quantidades de dados, o arquivo de banco de dado será aumentado em uma única operação.</span><span class="sxs-lookup"><span data-stu-id="40a89-145">If **JetSetDatabaseSize** is called prior to inserting large amounts of data, the database file will be grown in one operation.</span></span> <span data-ttu-id="40a89-146">Isso reduzirá a probabilidade de o arquivo de banco de dados ficar fragmentado no nível do sistema de arquivos e também reduzir o número de vezes que o arquivo de banco de dados precisa ser aumentado.</span><span class="sxs-lookup"><span data-stu-id="40a89-146">This will reduce the likelihood of the database file becoming fragmented at the file system level, and also reduce the number of times the database file has to be grown.</span></span> <span data-ttu-id="40a89-147">Aumentar o arquivo de banco de dados uma vez pode ser mais rápido do que expandi-lo várias vezes.</span><span class="sxs-lookup"><span data-stu-id="40a89-147">Growing the database file once can be faster than growing it several times.</span></span>

<span data-ttu-id="40a89-148">No momento, há suporte para o aumento do arquivo.</span><span class="sxs-lookup"><span data-stu-id="40a89-148">Only growing the file is currently supported.</span></span> <span data-ttu-id="40a89-149">Para reduzir um arquivo, use o recurso de desfragmentação do programa utilitário de esentutl.exe.</span><span class="sxs-lookup"><span data-stu-id="40a89-149">To shrink a file, use the defragmentation feature of the esentutl.exe utility program.</span></span>

<span data-ttu-id="40a89-150">Se *CPG* for menor do que o tamanho atual do banco de dados, a operação será ignorada.</span><span class="sxs-lookup"><span data-stu-id="40a89-150">If *cpg* is smaller than the current size of the database, the operation will be ignored.</span></span> <span data-ttu-id="40a89-151">Se *CPG* for menor que o tamanho mínimo do banco de dados (atualmente 256 páginas), ele retornará JET_errInvalidParameter.</span><span class="sxs-lookup"><span data-stu-id="40a89-151">If *cpg* is less than the minimum database size (currently 256 pages), it will return JET_errInvalidParameter.</span></span>

<span data-ttu-id="40a89-152">Para definir o tamanho de um banco de dados que está aberto, consulte [JetGrowDatabase](./jetgrowdatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="40a89-152">To set the size of a database that is opened, see [JetGrowDatabase](./jetgrowdatabase-function.md).</span></span>

<span data-ttu-id="40a89-153">O tamanho do arquivo pode não corresponder ao número de páginas retornadas em *pcpgReal*.</span><span class="sxs-lookup"><span data-stu-id="40a89-153">The file size may not match the number of pages returned in *pcpgReal*.</span></span> <span data-ttu-id="40a89-154">Há duas páginas reservadas adicionais que podem não ser contadas em *pcpgReal*.</span><span class="sxs-lookup"><span data-stu-id="40a89-154">There are two additional reserved pages that may not be counted in *pcpgReal*.</span></span>

#### <a name="requirements"></a><span data-ttu-id="40a89-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40a89-155">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="40a89-156"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="40a89-156"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="40a89-157">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="40a89-157">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40a89-158"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="40a89-158"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="40a89-159">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="40a89-159">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40a89-160"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="40a89-160"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="40a89-161">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="40a89-161">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40a89-162"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="40a89-162"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="40a89-163">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="40a89-163">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40a89-164"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="40a89-164"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="40a89-165">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="40a89-165">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40a89-166"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="40a89-166"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="40a89-167">Implementado como <strong>JetSetDatabaseSizeW</strong> (Unicode) e <strong>JetSetDatabaseSizeA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="40a89-167">Implemented as <strong>JetSetDatabaseSizeW</strong> (Unicode) and <strong>JetSetDatabaseSizeA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="40a89-168">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="40a89-168">See Also</span></span>

[<span data-ttu-id="40a89-169">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="40a89-169">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="40a89-170">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="40a89-170">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="40a89-171">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="40a89-171">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="40a89-172">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="40a89-172">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="40a89-173">JET_OBJECTINFO</span><span class="sxs-lookup"><span data-stu-id="40a89-173">JET_OBJECTINFO</span></span>](./jet-objectinfo-structure.md)  
[<span data-ttu-id="40a89-174">JET_OBJECTLIST</span><span class="sxs-lookup"><span data-stu-id="40a89-174">JET_OBJECTLIST</span></span>](./jet-objectlist-structure.md)  
[<span data-ttu-id="40a89-175">JetGrowDatabase</span><span class="sxs-lookup"><span data-stu-id="40a89-175">JetGrowDatabase</span></span>](./jetgrowdatabase-function.md)
