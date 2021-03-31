---
description: 'Saiba mais sobre: função JetOpenDatabase'
title: Função JetOpenDatabase
TOCTitle: JetOpenDatabase Function
ms:assetid: 7764f0c2-6795-4b93-be3d-f6830cdce369
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269299(v=EXCHG.10)
ms:contentKeyID: 32765591
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenDatabase
- JetOpenDatabaseW
- JetOpenDatabaseA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3492a037ac0c52a78bbe3265bd629969c301771c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663501"
---
# <a name="jetopendatabase-function"></a><span data-ttu-id="6ffe0-103">Função JetOpenDatabase</span><span class="sxs-lookup"><span data-stu-id="6ffe0-103">JetOpenDatabase Function</span></span>


<span data-ttu-id="6ffe0-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="6ffe0-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetopendatabase-function"></a><span data-ttu-id="6ffe0-105">Função JetOpenDatabase</span><span class="sxs-lookup"><span data-stu-id="6ffe0-105">JetOpenDatabase Function</span></span>

<span data-ttu-id="6ffe0-106">A função **JetOpenDatabase** abre um banco de dados anexado anteriormente, usando as funções [JetAttachDatabase](./jetattachdatabase-function.md) ou [JetAttachDatabase2](./jetattachdatabase2-function.md) , para uso com uma sessão de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6ffe0-106">The **JetOpenDatabase** function opens a previously attached database, using the [JetAttachDatabase](./jetattachdatabase-function.md) or [JetAttachDatabase2](./jetattachdatabase2-function.md) functions, for use with a database session.</span></span> <span data-ttu-id="6ffe0-107">Essa função pode ser chamada várias vezes para o mesmo banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6ffe0-107">This function can be called multiple times for the same database.</span></span>

```cpp
    JET_ERR JET_API JetOpenDatabase(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in_opt      const tchar* szConnect,
      __out         JET_DBID* pdbid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="6ffe0-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6ffe0-108">Parameters</span></span>

<span data-ttu-id="6ffe0-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="6ffe0-109">*sesid*</span></span>

<span data-ttu-id="6ffe0-110">O contexto da sessão de banco de dados a ser usado para a chamada à API.</span><span class="sxs-lookup"><span data-stu-id="6ffe0-110">The database session context to use for the API call.</span></span>

<span data-ttu-id="6ffe0-111">*szFilename*</span><span class="sxs-lookup"><span data-stu-id="6ffe0-111">*szFilename*</span></span>

<span data-ttu-id="6ffe0-112">O nome do banco de dados a ser aberto.</span><span class="sxs-lookup"><span data-stu-id="6ffe0-112">The name of the database to open.</span></span>

<span data-ttu-id="6ffe0-113">*szConnect*</span><span class="sxs-lookup"><span data-stu-id="6ffe0-113">*szConnect*</span></span>

<span data-ttu-id="6ffe0-114">Reservado.</span><span class="sxs-lookup"><span data-stu-id="6ffe0-114">Reserved.</span></span> <span data-ttu-id="6ffe0-115">Definido como NULL.</span><span class="sxs-lookup"><span data-stu-id="6ffe0-115">Set to NULL.</span></span>

<span data-ttu-id="6ffe0-116">*pdbid*</span><span class="sxs-lookup"><span data-stu-id="6ffe0-116">*pdbid*</span></span>

<span data-ttu-id="6ffe0-117">Ponteiro para um buffer que, em uma chamada bem-sucedida, contém o identificador do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6ffe0-117">Pointer to a buffer that, on a successful call, contains the identifier of the database.</span></span> <span data-ttu-id="6ffe0-118">Se a chamada falhar, o valor será indefinido.</span><span class="sxs-lookup"><span data-stu-id="6ffe0-118">If the call fails, the value is undefined.</span></span>

<span data-ttu-id="6ffe0-119">*grbit*</span><span class="sxs-lookup"><span data-stu-id="6ffe0-119">*grbit*</span></span>

<span data-ttu-id="6ffe0-120">Um grupo de bits que especifica zero ou mais das opções a seguir.</span><span class="sxs-lookup"><span data-stu-id="6ffe0-120">A group of bits that specify zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6ffe0-121">Valor</span><span class="sxs-lookup"><span data-stu-id="6ffe0-121">Value</span></span></p></th>
<th><p><span data-ttu-id="6ffe0-122">Significado</span><span class="sxs-lookup"><span data-stu-id="6ffe0-122">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6ffe0-123">JET_bitDbExclusive</span><span class="sxs-lookup"><span data-stu-id="6ffe0-123">JET_bitDbExclusive</span></span></p></td>
<td><p><span data-ttu-id="6ffe0-124">Permite que apenas uma única sessão anexe um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6ffe0-124">Allows only a single session to attach a database.</span></span> <span data-ttu-id="6ffe0-125">Normalmente, várias sessões podem abrir um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6ffe0-125">Normally, several sessions can open a database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ffe0-126">JET_bitDbReadOnly</span><span class="sxs-lookup"><span data-stu-id="6ffe0-126">JET_bitDbReadOnly</span></span></p></td>
<td><p><span data-ttu-id="6ffe0-127">Impede modificações no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6ffe0-127">Prevents modifications to the database.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="6ffe0-128">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="6ffe0-128">Return Value</span></span>

<span data-ttu-id="6ffe0-129">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="6ffe0-129">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="6ffe0-130">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="6ffe0-130">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6ffe0-131">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="6ffe0-131">Return code</span></span></p></th>
<th><p><span data-ttu-id="6ffe0-132">Descrição</span><span class="sxs-lookup"><span data-stu-id="6ffe0-132">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6ffe0-133">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="6ffe0-133">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="6ffe0-134">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="6ffe0-134">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ffe0-135">JET_errDatabaseInUse</span><span class="sxs-lookup"><span data-stu-id="6ffe0-135">JET_errDatabaseInUse</span></span></p></td>
<td><p><span data-ttu-id="6ffe0-136">O acesso exclusivo foi solicitado, mas não pôde ser concedido.</span><span class="sxs-lookup"><span data-stu-id="6ffe0-136">Exclusive access was requested, but could not be granted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ffe0-137">JET_errDatabaseInvalidPath</span><span class="sxs-lookup"><span data-stu-id="6ffe0-137">JET_errDatabaseInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="6ffe0-138">Um caminho inválido foi fornecido em <em>szFilename</em>.</span><span class="sxs-lookup"><span data-stu-id="6ffe0-138">An invalid path was given in <em>szFilename</em>.</span></span> <span data-ttu-id="6ffe0-139"><em>szFilename</em> deve ser não nulo e referir-se a um arquivo válido.</span><span class="sxs-lookup"><span data-stu-id="6ffe0-139"><em>szFilename</em> must be non-NULL and refer to a valid file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ffe0-140">JET_errDatabaseLocked</span><span class="sxs-lookup"><span data-stu-id="6ffe0-140">JET_errDatabaseLocked</span></span></p></td>
<td><p><span data-ttu-id="6ffe0-141">Outra sessão já abriu o banco de dados exclusivamente (usando JET_bitDbExclusive).</span><span class="sxs-lookup"><span data-stu-id="6ffe0-141">Another session has already opened the database exclusively (using JET_bitDbExclusive).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ffe0-142">JET_errDatabaseNotFound</span><span class="sxs-lookup"><span data-stu-id="6ffe0-142">JET_errDatabaseNotFound</span></span></p></td>
<td><p><span data-ttu-id="6ffe0-143">O banco de dados não foi anexado anteriormente (consulte <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a>).</span><span class="sxs-lookup"><span data-stu-id="6ffe0-143">The database was not previously attached (See <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ffe0-144">JET_errInvalidDatabase</span><span class="sxs-lookup"><span data-stu-id="6ffe0-144">JET_errInvalidDatabase</span></span></p></td>
<td><p><span data-ttu-id="6ffe0-145">Foi feita uma tentativa de abrir um arquivo que não é um arquivo de banco de dados válido.</span><span class="sxs-lookup"><span data-stu-id="6ffe0-145">An attempt was made to open a file that is not a valid database file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ffe0-146">JET_errOneDatabasePerSession</span><span class="sxs-lookup"><span data-stu-id="6ffe0-146">JET_errOneDatabasePerSession</span></span></p></td>
<td><p><span data-ttu-id="6ffe0-147">Foi feita uma tentativa de abrir mais de um banco de dados e <a href="gg269337(v=exchg.10).md">JET_paramOneDatabasePerSession</a> foi definido.</span><span class="sxs-lookup"><span data-stu-id="6ffe0-147">An attempt was made to open more than one database, and <a href="gg269337(v=exchg.10).md">JET_paramOneDatabasePerSession</a> was set.</span></span> <span data-ttu-id="6ffe0-148">Para obter mais informações, consulte <a href="gg294139(v=exchg.10).md">parâmetros do sistema</a>.</span><span class="sxs-lookup"><span data-stu-id="6ffe0-148">For more information, see <a href="gg294139(v=exchg.10).md">System Parameters</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ffe0-149">JET_wrnFileOpenReadOnly</span><span class="sxs-lookup"><span data-stu-id="6ffe0-149">JET_wrnFileOpenReadOnly</span></span></p></td>
<td><p><span data-ttu-id="6ffe0-150">O arquivo foi anexado como somente leitura, mas <strong>JetOpenDatabase</strong> não passou JET_bitDbReadOnly.</span><span class="sxs-lookup"><span data-stu-id="6ffe0-150">The file was attached as read-only, but <strong>JetOpenDatabase</strong> did not pass JET_bitDbReadOnly.</span></span> <span data-ttu-id="6ffe0-151">O banco de dados ainda está aberto com acesso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="6ffe0-151">The database is still opened with read-only access.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="requirements"></a><span data-ttu-id="6ffe0-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ffe0-152">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6ffe0-153"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="6ffe0-153"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="6ffe0-154">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="6ffe0-154">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ffe0-155"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="6ffe0-155"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="6ffe0-156">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="6ffe0-156">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ffe0-157"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="6ffe0-157"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="6ffe0-158">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="6ffe0-158">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ffe0-159"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="6ffe0-159"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="6ffe0-160">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="6ffe0-160">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ffe0-161"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="6ffe0-161"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="6ffe0-162">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="6ffe0-162">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ffe0-163"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="6ffe0-163"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="6ffe0-164">Implementado como <strong>JetOpenDatabaseW</strong> (Unicode) e <strong>JetOpenDatabaseA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="6ffe0-164">Implemented as <strong>JetOpenDatabaseW</strong> (Unicode) and <strong>JetOpenDatabaseA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="6ffe0-165">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="6ffe0-165">See Also</span></span>

[<span data-ttu-id="6ffe0-166">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="6ffe0-166">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="6ffe0-167">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="6ffe0-167">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="6ffe0-168">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="6ffe0-168">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="6ffe0-169">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="6ffe0-169">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="6ffe0-170">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="6ffe0-170">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="6ffe0-171">JetAttachDatabase2</span><span class="sxs-lookup"><span data-stu-id="6ffe0-171">JetAttachDatabase2</span></span>](./jetattachdatabase2-function.md)  
[<span data-ttu-id="6ffe0-172">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="6ffe0-172">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="6ffe0-173">Parâmetros do sistema</span><span class="sxs-lookup"><span data-stu-id="6ffe0-173">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
