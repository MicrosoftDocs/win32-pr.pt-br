---
description: 'Saiba mais sobre: função JetResizeDatabase'
title: Função JetResizeDatabase
TOCTitle: JetResizeDatabase Function
ms:assetid: b6420de7-acff-480e-838b-f0e5acc29c65
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835047(v=EXCHG.10)
ms:contentKeyID: 49894669
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetResizeDatabase
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dadaa7eaa310c5b3a6a2730d316218bc2607d100
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764385"
---
# <a name="jetresizedatabase-function"></a><span data-ttu-id="da51d-103">Função JetResizeDatabase</span><span class="sxs-lookup"><span data-stu-id="da51d-103">JetResizeDatabase Function</span></span>


<span data-ttu-id="da51d-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="da51d-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="da51d-105">A função **JetResizeDatabase** estende ou reduz o tamanho de um banco de dados que está aberto no momento.</span><span class="sxs-lookup"><span data-stu-id="da51d-105">The **JetResizeDatabase** function extends or shrinks the size of a database that is currently open.</span></span>

<span data-ttu-id="da51d-106">A função **JetResizeDatabase** foi introduzida no sistema operacional Windows 8.</span><span class="sxs-lookup"><span data-stu-id="da51d-106">The **JetResizeDatabase** function was introduced in the Windows 8 operating system.</span></span>

``` c++
JET_ERR JET_API JetResizeDatabase(
  __in          JET_SESID sesid,
  __in          JET_DBID dbid,
  __in          unsigned long cpg,
  __out         unsigned long* pcpgActual,
  __in          const JET_GRBIT grbit
);
```

### <a name="parameters"></a><span data-ttu-id="da51d-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="da51d-107">Parameters</span></span>

<span data-ttu-id="da51d-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="da51d-108">*sesid*</span></span>

<span data-ttu-id="da51d-109">O contexto da sessão de banco de dados a ser usado para a chamada à API.</span><span class="sxs-lookup"><span data-stu-id="da51d-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="da51d-110">*DBID*</span><span class="sxs-lookup"><span data-stu-id="da51d-110">*dbid*</span></span>

<span data-ttu-id="da51d-111">O banco de dados que será estendido.</span><span class="sxs-lookup"><span data-stu-id="da51d-111">The database that will be extended.</span></span>

<span data-ttu-id="da51d-112">*CPG*</span><span class="sxs-lookup"><span data-stu-id="da51d-112">*cpg*</span></span>

<span data-ttu-id="da51d-113">O tamanho solicitado do banco de dados, em páginas.</span><span class="sxs-lookup"><span data-stu-id="da51d-113">The requested size of the database, in pages.</span></span>

<span data-ttu-id="da51d-114">*pcpgActual*</span><span class="sxs-lookup"><span data-stu-id="da51d-114">*pcpgActual*</span></span>

<span data-ttu-id="da51d-115">Um ponteiro para um número que recebe o tamanho do banco de dados, em páginas, após a chamada à API.</span><span class="sxs-lookup"><span data-stu-id="da51d-115">A pointer to a number that receives the size of the database, in pages, after the API call.</span></span> <span data-ttu-id="da51d-116">Se a chamada à API falhar, o conteúdo do parâmetro *pcpgActual* será indefinido.</span><span class="sxs-lookup"><span data-stu-id="da51d-116">If the API call fails, the contents of *pcpgActual* parameter are undefined.</span></span>

<span data-ttu-id="da51d-117">*grbit*</span><span class="sxs-lookup"><span data-stu-id="da51d-117">*grbit*</span></span>

<span data-ttu-id="da51d-118">Um grupo de bits que especifica zero ou mais valores listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="da51d-118">A group of bits that specifies zero or more of the values listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="da51d-119">Valor</span><span class="sxs-lookup"><span data-stu-id="da51d-119">Value</span></span></p></th>
<th><p><span data-ttu-id="da51d-120">Significado</span><span class="sxs-lookup"><span data-stu-id="da51d-120">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="da51d-121">JET_bitResizeDatabaseOnlyGrow</span><span class="sxs-lookup"><span data-stu-id="da51d-121">JET_bitResizeDatabaseOnlyGrow</span></span></p></td>
<td><p><span data-ttu-id="da51d-122">Aumentar apenas o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="da51d-122">Only grow the database.</span></span> <span data-ttu-id="da51d-123">Se a chamada de redimensionamento reduzir o banco de dados, não faça nada.</span><span class="sxs-lookup"><span data-stu-id="da51d-123">If the resize call would shrink the database, do nothing.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="da51d-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="da51d-124">Return value</span></span>

<span data-ttu-id="da51d-125">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="da51d-125">This function returns the [JET_ERR](./jet-err.md) datatype with one of the return codes listed in the following table.</span></span> <span data-ttu-id="da51d-126">Para obter mais informações sobre os possíveis erros do ESE (mecanismo de armazenamento extensível), consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="da51d-126">For more information about the possible Extensible Storage Engine (ESE) errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="da51d-127">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="da51d-127">Return code</span></span></p></th>
<th><p><span data-ttu-id="da51d-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="da51d-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="da51d-129">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="da51d-129">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="da51d-130">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="da51d-130">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da51d-131">JET_errDiskFull</span><span class="sxs-lookup"><span data-stu-id="da51d-131">JET_errDiskFull</span></span></p></td>
<td><p><span data-ttu-id="da51d-132">Não há espaço livre suficiente no volume para executar a operação de crescimento.</span><span class="sxs-lookup"><span data-stu-id="da51d-132">There is insufficient free space on the volume to perform the grow operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da51d-133">JET_errDiskIO</span><span class="sxs-lookup"><span data-stu-id="da51d-133">JET_errDiskIO</span></span></p></td>
<td><p><span data-ttu-id="da51d-134">Um erro relacionado a arquivo foi retornado pela função <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a> .</span><span class="sxs-lookup"><span data-stu-id="da51d-134">A file-related error was returned by the <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a> function.</span></span> <span data-ttu-id="da51d-135">Para obter mais informações sobre outros erros relacionados a arquivos que podem ser retornados, consulte <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a>.</span><span class="sxs-lookup"><span data-stu-id="da51d-135">For more information about other file-related errors that might be returned, see <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a>.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="da51d-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="da51d-136">Remarks</span></span>

<span data-ttu-id="da51d-137">Se a função **JetResizeDatabase** for chamada antes da inserção de grandes quantidades de dados, o arquivo de banco de dado será aumentado em uma única operação.</span><span class="sxs-lookup"><span data-stu-id="da51d-137">If the **JetResizeDatabase** function is called prior to inserting large amounts of data, the database file will be grown in one operation.</span></span> <span data-ttu-id="da51d-138">Isso reduzirá a probabilidade de o arquivo de banco de dados ficar fragmentado no nível do sistema de arquivos e também reduzir o número de vezes que o arquivo de banco de dados precisa ser aumentado.</span><span class="sxs-lookup"><span data-stu-id="da51d-138">This will reduce the likelihood of the database file becoming fragmented at the file system level, and also reduce the number of times the database file has to be grown.</span></span> <span data-ttu-id="da51d-139">Aumentar o arquivo de banco de dados uma vez pode ser mais rápido do que expandi-lo várias vezes.</span><span class="sxs-lookup"><span data-stu-id="da51d-139">Growing the database file once can be faster than growing it several times.</span></span>

<span data-ttu-id="da51d-140">Para definir o tamanho de um banco de dados que não está aberto, consulte [JetSetDatabaseSize](./jetsetdatabasesize-function.md).</span><span class="sxs-lookup"><span data-stu-id="da51d-140">To set the size of a database that is not opened, see [JetSetDatabaseSize](./jetsetdatabasesize-function.md).</span></span>

<span data-ttu-id="da51d-141">O tamanho do arquivo pode não corresponder ao número de páginas retornadas no parâmetro *pcpgReal* .</span><span class="sxs-lookup"><span data-stu-id="da51d-141">The file size might not match the number of pages that are returned in the *pcpgReal* parameter.</span></span> <span data-ttu-id="da51d-142">Duas páginas reservadas adicionais podem não ser contadas no parâmetro *pcpgReal* .</span><span class="sxs-lookup"><span data-stu-id="da51d-142">Two additional reserved pages might not be counted in the *pcpgReal* parameter.</span></span>

#### <a name="requirements"></a><span data-ttu-id="da51d-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da51d-143">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="da51d-144"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="da51d-144"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="da51d-145">Requer o Windows 8.</span><span class="sxs-lookup"><span data-stu-id="da51d-145">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da51d-146"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="da51d-146"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="da51d-147">Requer o Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="da51d-147">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da51d-148"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="da51d-148"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="da51d-149">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="da51d-149">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da51d-150"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="da51d-150"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="da51d-151">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="da51d-151">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da51d-152"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="da51d-152"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="da51d-153">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="da51d-153">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="da51d-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="da51d-154">See also</span></span>

[<span data-ttu-id="da51d-155">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="da51d-155">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="da51d-156">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="da51d-156">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="da51d-157">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="da51d-157">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="da51d-158">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="da51d-158">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="da51d-159">JET_OBJECTINFO</span><span class="sxs-lookup"><span data-stu-id="da51d-159">JET_OBJECTINFO</span></span>](./jet-objectinfo-structure.md)  
[<span data-ttu-id="da51d-160">JET_OBJECTLIST</span><span class="sxs-lookup"><span data-stu-id="da51d-160">JET_OBJECTLIST</span></span>](./jet-objectlist-structure.md)  
[<span data-ttu-id="da51d-161">JetSetDatabaseSize</span><span class="sxs-lookup"><span data-stu-id="da51d-161">JetSetDatabaseSize</span></span>](./jetsetdatabasesize-function.md)
