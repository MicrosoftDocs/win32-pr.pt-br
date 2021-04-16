---
description: 'Saiba mais sobre: função JetGrowDatabase'
title: Função JetGrowDatabase
TOCTitle: JetGrowDatabase Function
ms:assetid: d9719991-6c80-4dcb-a1d6-f0c7de61f459
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294109(v=EXCHG.10)
ms:contentKeyID: 32765724
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGrowDatabase
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9ed8ee9888a2e4ab7908b72cc071f7b8143ca6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750532"
---
# <a name="jetgrowdatabase-function"></a><span data-ttu-id="d4ca9-103">Função JetGrowDatabase</span><span class="sxs-lookup"><span data-stu-id="d4ca9-103">JetGrowDatabase Function</span></span>


<span data-ttu-id="d4ca9-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d4ca9-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgrowdatabase-function"></a><span data-ttu-id="d4ca9-105">Função JetGrowDatabase</span><span class="sxs-lookup"><span data-stu-id="d4ca9-105">JetGrowDatabase Function</span></span>

<span data-ttu-id="d4ca9-106">A função **JetGrowDatabase** estende o tamanho de um banco de dados que está aberto no momento.</span><span class="sxs-lookup"><span data-stu-id="d4ca9-106">The **JetGrowDatabase** function extends the size of a database that is currently open.</span></span>

```cpp
    JET_ERR JET_API JetGrowDatabase(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          unsigned long cpg,
      __in          unsigned long* pcpgReal
    );
```

### <a name="parameters"></a><span data-ttu-id="d4ca9-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d4ca9-107">Parameters</span></span>

<span data-ttu-id="d4ca9-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="d4ca9-108">*sesid*</span></span>

<span data-ttu-id="d4ca9-109">O contexto da sessão de banco de dados a ser usado para a chamada à API.</span><span class="sxs-lookup"><span data-stu-id="d4ca9-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="d4ca9-110">*DBID*</span><span class="sxs-lookup"><span data-stu-id="d4ca9-110">*dbid*</span></span>

<span data-ttu-id="d4ca9-111">O banco de dados que será estendido.</span><span class="sxs-lookup"><span data-stu-id="d4ca9-111">The database that will be extended.</span></span>

<span data-ttu-id="d4ca9-112">*CPG*</span><span class="sxs-lookup"><span data-stu-id="d4ca9-112">*cpg*</span></span>

<span data-ttu-id="d4ca9-113">O tamanho desejado do banco de dados, em páginas.</span><span class="sxs-lookup"><span data-stu-id="d4ca9-113">The desired size of the database, in pages.</span></span>

<span data-ttu-id="d4ca9-114">*pcpgReal*</span><span class="sxs-lookup"><span data-stu-id="d4ca9-114">*pcpgReal*</span></span>

<span data-ttu-id="d4ca9-115">Ponteiro para um número que recebe o tamanho do banco de dados, em páginas, após a chamada à API.</span><span class="sxs-lookup"><span data-stu-id="d4ca9-115">Pointer to a number that receives the size of the database, in pages, after the API call.</span></span> <span data-ttu-id="d4ca9-116">Se a chamada à API falhar, o conteúdo de *pcpgReal* será indefinido.</span><span class="sxs-lookup"><span data-stu-id="d4ca9-116">If the API call fails, the contents of *pcpgReal* are undefined.</span></span>

### <a name="return-value"></a><span data-ttu-id="d4ca9-117">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="d4ca9-117">Return Value</span></span>

<span data-ttu-id="d4ca9-118">Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="d4ca9-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="d4ca9-119">Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="d4ca9-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d4ca9-120">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="d4ca9-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="d4ca9-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="d4ca9-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d4ca9-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="d4ca9-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="d4ca9-123">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="d4ca9-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4ca9-124">JET_errDiskFull</span><span class="sxs-lookup"><span data-stu-id="d4ca9-124">JET_errDiskFull</span></span></p></td>
<td><p><span data-ttu-id="d4ca9-125">Não há espaço livre suficiente no volume para executar a operação de crescimento.</span><span class="sxs-lookup"><span data-stu-id="d4ca9-125">There is insufficient free space on the volume to perform the grow operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4ca9-126">JET_errDiskIO</span><span class="sxs-lookup"><span data-stu-id="d4ca9-126">JET_errDiskIO</span></span></p></td>
<td><p><span data-ttu-id="d4ca9-127">Um erro relacionado a arquivo foi retornado por <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a>.</span><span class="sxs-lookup"><span data-stu-id="d4ca9-127">A file-related error was returned by <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a>.</span></span> <span data-ttu-id="d4ca9-128">Para obter mais informações sobre outros erros relacionados a arquivos que podem ser retornados, consulte <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a>.</span><span class="sxs-lookup"><span data-stu-id="d4ca9-128">For more information about other file-related errors that might be returned, see <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a>.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="d4ca9-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="d4ca9-129">Remarks</span></span>

<span data-ttu-id="d4ca9-130">Se **JetGrowDatabase** for chamado antes da inserção de grandes quantidades de dados, o arquivo de banco de dado será aumentado em uma única operação.</span><span class="sxs-lookup"><span data-stu-id="d4ca9-130">If **JetGrowDatabase** is called prior to inserting large amounts of data, the database file will be grown in one operation.</span></span> <span data-ttu-id="d4ca9-131">Isso reduzirá a probabilidade de o arquivo de banco de dados ficar fragmentado no nível do sistema de arquivos e também reduzir o número de vezes que o arquivo de banco de dados precisa ser aumentado.</span><span class="sxs-lookup"><span data-stu-id="d4ca9-131">This will reduce the likelihood of the database file becoming fragmented at the file system level, and also reduce the number of times the database file has to be grown.</span></span> <span data-ttu-id="d4ca9-132">Aumentar o arquivo de banco de dados uma vez pode ser mais rápido do que expandi-lo várias vezes.</span><span class="sxs-lookup"><span data-stu-id="d4ca9-132">Growing the database file once can be faster than growing it several times.</span></span>

<span data-ttu-id="d4ca9-133">No momento, há suporte para o aumento do arquivo.</span><span class="sxs-lookup"><span data-stu-id="d4ca9-133">Only growing the file is currently supported.</span></span> <span data-ttu-id="d4ca9-134">Para reduzir um arquivo, use o recurso de desfragmentação do programa utilitário de **esentutl.exe** .</span><span class="sxs-lookup"><span data-stu-id="d4ca9-134">To shrink a file, use the defragmentation feature of the **esentutl.exe** utility program.</span></span>

<span data-ttu-id="d4ca9-135">Para definir o tamanho de um banco de dados que não está aberto, consulte [JetSetDatabaseSize](./jetsetdatabasesize-function.md).</span><span class="sxs-lookup"><span data-stu-id="d4ca9-135">To set the size of a database that is not opened, see [JetSetDatabaseSize](./jetsetdatabasesize-function.md).</span></span>

<span data-ttu-id="d4ca9-136">O tamanho do arquivo pode não corresponder ao número de páginas retornadas em *pcpgReal*.</span><span class="sxs-lookup"><span data-stu-id="d4ca9-136">The file size might not match the number of pages that are returned in *pcpgReal*.</span></span> <span data-ttu-id="d4ca9-137">Há duas páginas reservadas adicionais que podem não ser contadas em *pcpgReal*.</span><span class="sxs-lookup"><span data-stu-id="d4ca9-137">There are two additional reserved pages that might not be counted in *pcpgReal*.</span></span>

#### <a name="requirements"></a><span data-ttu-id="d4ca9-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4ca9-138">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d4ca9-139"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="d4ca9-139"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d4ca9-140">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="d4ca9-140">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4ca9-141"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="d4ca9-141"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d4ca9-142">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="d4ca9-142">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4ca9-143"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="d4ca9-143"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d4ca9-144">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="d4ca9-144">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4ca9-145"><strong>Biblioteca</strong></span><span class="sxs-lookup"><span data-stu-id="d4ca9-145"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="d4ca9-146">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="d4ca9-146">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4ca9-147"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="d4ca9-147"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="d4ca9-148">Requer ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="d4ca9-148">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="d4ca9-149">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="d4ca9-149">See Also</span></span>

[<span data-ttu-id="d4ca9-150">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="d4ca9-150">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="d4ca9-151">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="d4ca9-151">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="d4ca9-152">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="d4ca9-152">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="d4ca9-153">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="d4ca9-153">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="d4ca9-154">JET_OBJECTINFO</span><span class="sxs-lookup"><span data-stu-id="d4ca9-154">JET_OBJECTINFO</span></span>](./jet-objectinfo-structure.md)  
[<span data-ttu-id="d4ca9-155">JET_OBJECTLIST</span><span class="sxs-lookup"><span data-stu-id="d4ca9-155">JET_OBJECTLIST</span></span>](./jet-objectlist-structure.md)  
[<span data-ttu-id="d4ca9-156">JetSetDatabaseSize</span><span class="sxs-lookup"><span data-stu-id="d4ca9-156">JetSetDatabaseSize</span></span>](./jetsetdatabasesize-function.md)
