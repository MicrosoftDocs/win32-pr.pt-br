---
description: 'Saiba mais sobre: códigos de erro do mecanismo de armazenamento extensível'
title: Códigos de erro do mecanismo de armazenamento extensível
TOCTitle: Extensible Storage Engine Error Codes
ms:assetid: 7534370d-aed6-4980-b1ca-c3d063507e31
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269297(v=EXCHG.10)
ms:contentKeyID: 32765589
ms.date: 09/22/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9de4bd8157e0b7210315352ba0760293a892f087
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105798522"
---
# <a name="extensible-storage-engine-error-codes"></a><span data-ttu-id="a6ec4-103">Códigos de erro do mecanismo de armazenamento extensível</span><span class="sxs-lookup"><span data-stu-id="a6ec4-103">Extensible Storage Engine Error Codes</span></span>


<span data-ttu-id="a6ec4-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a6ec4-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="extensible-storage-engine-error-codes"></a><span data-ttu-id="a6ec4-105">Códigos de erro do mecanismo de armazenamento extensível</span><span class="sxs-lookup"><span data-stu-id="a6ec4-105">Extensible Storage Engine Error Codes</span></span>

<span data-ttu-id="a6ec4-106">Os códigos de erro (sinalizadores) a seguir são usados por funções na API do mecanismo de armazenamento extensível.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-106">The following error codes (flags) are used by functions in the Extensible Storage Engine API.</span></span>

<span data-ttu-id="a6ec4-107">Um valor de [JET_ERR](./jet-err.md) de zero deve ser interpretado como êxito.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-107">A [JET_ERR](./jet-err.md) value of zero should be interpreted as success.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a6ec4-108">Êxito</span><span class="sxs-lookup"><span data-stu-id="a6ec4-108">Success</span></span></p></th>
<th><p><span data-ttu-id="a6ec4-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="a6ec4-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-110">JET_errSuccess 0</span><span class="sxs-lookup"><span data-stu-id="a6ec4-110">JET_errSuccess 0</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-111">A função foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-111">The function succeeded.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a6ec4-112">Um valor [JET_ERR](./jet-err.md) maior que zero deve ser interpretado como um aviso.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-112">A [JET_ERR](./jet-err.md) value that is greater than zero should be interpreted as a warning.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a6ec4-113">Warnings</span><span class="sxs-lookup"><span data-stu-id="a6ec4-113">Warnings</span></span></p></th>
<th><p><span data-ttu-id="a6ec4-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="a6ec4-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-115">JET_wrnRemainingVersions</span><span class="sxs-lookup"><span data-stu-id="a6ec4-115">JET_wrnRemainingVersions</span></span><br />
<span data-ttu-id="a6ec4-116">321</span><span class="sxs-lookup"><span data-stu-id="a6ec4-116">321</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-117">O repositório de versão ainda está ativo.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-117">The version store is still active.</span></span> <span data-ttu-id="a6ec4-118">Esse erro é retornado pelo Gerenciador de diretórios.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-118">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-119">JET_wrnUniqueKey</span><span class="sxs-lookup"><span data-stu-id="a6ec4-119">JET_wrnUniqueKey</span></span><br />
<span data-ttu-id="a6ec4-120">345</span><span class="sxs-lookup"><span data-stu-id="a6ec4-120">345</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-121">Uma busca em um índice não exclusivo gerou uma chave exclusiva.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-121">A seek on a non-unique index yielded a unique key.</span></span> <span data-ttu-id="a6ec4-122">Esse erro é retornado pelo Gerenciador de diretórios.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-122">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-123">JET_wrnSeparateLongValue</span><span class="sxs-lookup"><span data-stu-id="a6ec4-123">JET_wrnSeparateLongValue</span></span><br />
<span data-ttu-id="a6ec4-124">406</span><span class="sxs-lookup"><span data-stu-id="a6ec4-124">406</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-125">Uma coluna de banco de dados é um valor longo separado.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-125">A database column is a separated long value.</span></span> <span data-ttu-id="a6ec4-126">Esse erro é retornado pelo Gerenciador de registros.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-126">This error is returned by the record manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-127">JET_wrnExistingLogFileHasBadSignature</span><span class="sxs-lookup"><span data-stu-id="a6ec4-127">JET_wrnExistingLogFileHasBadSignature</span></span><br />
<span data-ttu-id="a6ec4-128">558</span><span class="sxs-lookup"><span data-stu-id="a6ec4-128">558</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-129">O arquivo de log existente tem uma assinatura inadequada.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-129">The existing log file has a bad signature.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-130">JET_wrnExistingLogFileIsNotContiguous</span><span class="sxs-lookup"><span data-stu-id="a6ec4-130">JET_wrnExistingLogFileIsNotContiguous</span></span><br />
<span data-ttu-id="a6ec4-131">559</span><span class="sxs-lookup"><span data-stu-id="a6ec4-131">559</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-132">O arquivo de log existente não é contíguo.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-132">The existing log file is not contiguous.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-133">JET_wrnSkipThisRecord</span><span class="sxs-lookup"><span data-stu-id="a6ec4-133">JET_wrnSkipThisRecord</span></span><br />
<span data-ttu-id="a6ec4-134">564</span><span class="sxs-lookup"><span data-stu-id="a6ec4-134">564</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-135">Esse erro é somente para uso interno.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-135">This error is for internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-136">JET_wrnTargetInstanceRunning</span><span class="sxs-lookup"><span data-stu-id="a6ec4-136">JET_wrnTargetInstanceRunning</span></span><br />
<span data-ttu-id="a6ec4-137">578</span><span class="sxs-lookup"><span data-stu-id="a6ec4-137">578</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-138">O TargetInstance especificado para a restauração está em execução.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-138">The TargetInstance specified for the restore is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-139">JET_wrnDatabaseRepaired</span><span class="sxs-lookup"><span data-stu-id="a6ec4-139">JET_wrnDatabaseRepaired</span></span><br />
<span data-ttu-id="a6ec4-140">595</span><span class="sxs-lookup"><span data-stu-id="a6ec4-140">595</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-141">A corrupção do banco de dados foi reparada.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-141">The database corruption has been repaired.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-142">JET_wrnColumnNull</span><span class="sxs-lookup"><span data-stu-id="a6ec4-142">JET_wrnColumnNull</span></span><br />
<span data-ttu-id="a6ec4-143">1004</span><span class="sxs-lookup"><span data-stu-id="a6ec4-143">1004</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-144">A coluna tem um valor <strong>nulo</strong> .</span><span class="sxs-lookup"><span data-stu-id="a6ec4-144">The column has a <strong>NULL</strong> value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-145">JET_wrnBufferTruncated</span><span class="sxs-lookup"><span data-stu-id="a6ec4-145">JET_wrnBufferTruncated</span></span><br />
<span data-ttu-id="a6ec4-146">1006</span><span class="sxs-lookup"><span data-stu-id="a6ec4-146">1006</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-147">O buffer é muito pequeno para os dados.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-147">The buffer is too small for the data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-148">JET_wrnDatabaseAttached</span><span class="sxs-lookup"><span data-stu-id="a6ec4-148">JET_wrnDatabaseAttached</span></span><br />
<span data-ttu-id="a6ec4-149">1007</span><span class="sxs-lookup"><span data-stu-id="a6ec4-149">1007</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-150">O banco de dados já está anexado.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-150">The database is already attached.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-151">JET_wrnSortOverflow</span><span class="sxs-lookup"><span data-stu-id="a6ec4-151">JET_wrnSortOverflow</span></span><br />
<span data-ttu-id="a6ec4-152">1009</span><span class="sxs-lookup"><span data-stu-id="a6ec4-152">1009</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-153">A classificação que está sendo tentada não tem memória suficiente para ser concluída.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-153">The sort that is being attempted does not have enough memory to complete.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-154">JET_wrnSeekNotEqual</span><span class="sxs-lookup"><span data-stu-id="a6ec4-154">JET_wrnSeekNotEqual</span></span><br />
<span data-ttu-id="a6ec4-155">1039</span><span class="sxs-lookup"><span data-stu-id="a6ec4-155">1039</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-156">Uma correspondência exata não foi encontrada durante uma busca.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-156">An exact match was not found during a seek.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-157">JET_wrnRecordFoundGreater</span><span class="sxs-lookup"><span data-stu-id="a6ec4-157">JET_wrnRecordFoundGreater</span></span><br />
<span data-ttu-id="a6ec4-158">JET_wrnSeekNotEqual</span><span class="sxs-lookup"><span data-stu-id="a6ec4-158">JET_wrnSeekNotEqual</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-159">Uma correspondência exata não foi encontrada durante uma busca.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-159">An exact match was not found during a seek.</span></span> <span data-ttu-id="a6ec4-160">Esse erro é retornado pelo Gerenciador de registros.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-160">This error is returned by the record manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-161">JET_wrnRecordFoundLess</span><span class="sxs-lookup"><span data-stu-id="a6ec4-161">JET_wrnRecordFoundLess</span></span><br />
<span data-ttu-id="a6ec4-162">JET_wrnSeekNotEqual</span><span class="sxs-lookup"><span data-stu-id="a6ec4-162">JET_wrnSeekNotEqual</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-163">Uma correspondência exata não foi encontrada durante uma busca.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-163">An exact match was not found during a seek.</span></span> <span data-ttu-id="a6ec4-164">Esse erro é retornado pelo Gerenciador de registros.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-164">This error is returned by the record manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-165">JET_wrnNoErrorInfo</span><span class="sxs-lookup"><span data-stu-id="a6ec4-165">JET_wrnNoErrorInfo</span></span><br />
<span data-ttu-id="a6ec4-166">1055</span><span class="sxs-lookup"><span data-stu-id="a6ec4-166">1055</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-167">Não há informações de erro estendidas.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-167">There is no extended error information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-168">JET_wrnNoIdleActivity</span><span class="sxs-lookup"><span data-stu-id="a6ec4-168">JET_wrnNoIdleActivity</span></span><br />
<span data-ttu-id="a6ec4-169">1058</span><span class="sxs-lookup"><span data-stu-id="a6ec4-169">1058</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-170">Não ocorreu nenhuma atividade ociosa.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-170">No idle activity occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-171">JET_wrnNoWriteLock</span><span class="sxs-lookup"><span data-stu-id="a6ec4-171">JET_wrnNoWriteLock</span></span><br />
<span data-ttu-id="a6ec4-172">1067</span><span class="sxs-lookup"><span data-stu-id="a6ec4-172">1067</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-173">Não há um bloqueio de gravação no nível de transação 0.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-173">There is a no write lock at transaction level 0.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-174">JET_wrnColumnSetNull</span><span class="sxs-lookup"><span data-stu-id="a6ec4-174">JET_wrnColumnSetNull</span></span><br />
<span data-ttu-id="a6ec4-175">1068</span><span class="sxs-lookup"><span data-stu-id="a6ec4-175">1068</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-176">A coluna está definida como um valor <strong>nulo</strong> .</span><span class="sxs-lookup"><span data-stu-id="a6ec4-176">The column is set to a <strong>NULL</strong> value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-177">JET_wrnTableEmpty</span><span class="sxs-lookup"><span data-stu-id="a6ec4-177">JET_wrnTableEmpty</span></span><br />
<span data-ttu-id="a6ec4-178">1301</span><span class="sxs-lookup"><span data-stu-id="a6ec4-178">1301</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-179">Uma tabela vazia foi aberta.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-179">An empty table was opened.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-180">JET_wrnTableInUseBySystem</span><span class="sxs-lookup"><span data-stu-id="a6ec4-180">JET_wrnTableInUseBySystem</span></span><br />
<span data-ttu-id="a6ec4-181">1327</span><span class="sxs-lookup"><span data-stu-id="a6ec4-181">1327</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-182">A limpeza do sistema tem um cursor aberto na tabela.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-182">The system cleanup has a cursor open on the table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-183">JET_wrnCorruptIndexDeleted</span><span class="sxs-lookup"><span data-stu-id="a6ec4-183">JET_wrnCorruptIndexDeleted</span></span><br />
<span data-ttu-id="a6ec4-184">1415</span><span class="sxs-lookup"><span data-stu-id="a6ec4-184">1415</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-185">O índice desatualizado deve ser removido.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-185">The out-of-date index must be removed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-186">JET_wrnColumnMaxTruncated</span><span class="sxs-lookup"><span data-stu-id="a6ec4-186">JET_wrnColumnMaxTruncated</span></span><br />
<span data-ttu-id="a6ec4-187">1512</span><span class="sxs-lookup"><span data-stu-id="a6ec4-187">1512</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-188">O comprimento máximo é muito grande e foi truncado.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-188">The Max length is too large and has been truncated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-189">JET_wrnCopyLongValue</span><span class="sxs-lookup"><span data-stu-id="a6ec4-189">JET_wrnCopyLongValue</span></span><br />
<span data-ttu-id="a6ec4-190">1520</span><span class="sxs-lookup"><span data-stu-id="a6ec4-190">1520</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-191">Um valor de BLOB foi movido do registro para um armazenamento separado de BLOBs grandes.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-191">A BLOB value has been moved from the record into a separate storage of large BLOBs.</span></span></p>
<p><span data-ttu-id="a6ec4-192"><strong>Observação</strong> Esse erro é somente para uso interno.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-192"><strong>Note</strong> This error is for internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-193">JET_wrnColumnSkipped</span><span class="sxs-lookup"><span data-stu-id="a6ec4-193">JET_wrnColumnSkipped</span></span><br />
<span data-ttu-id="a6ec4-194">1531</span><span class="sxs-lookup"><span data-stu-id="a6ec4-194">1531</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-195">Os valores da coluna não foram retornados porque a ID da coluna correspondente ou o membro <em>itagSequence</em> da estrutura de <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a> solicitada para enumeração era nulo.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-195">The column values were not returned because the corresponding column ID or <em>itagSequence</em> member from the <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a> structure that was requested for enumeration was null.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-196">JET_wrnColumnNotLocal</span><span class="sxs-lookup"><span data-stu-id="a6ec4-196">JET_wrnColumnNotLocal</span></span><br />
<span data-ttu-id="a6ec4-197">1532</span><span class="sxs-lookup"><span data-stu-id="a6ec4-197">1532</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-198">Os valores de coluna não foram retornados porque não puderam ser reconstruídos a partir dos dados existentes.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-198">The column values were not returned because they could not be reconstructed from the existing data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-199">JET_wrnColumnMoreTags</span><span class="sxs-lookup"><span data-stu-id="a6ec4-199">JET_wrnColumnMoreTags</span></span><br />
<span data-ttu-id="a6ec4-200">1533</span><span class="sxs-lookup"><span data-stu-id="a6ec4-200">1533</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-201">Os valores de coluna existentes não foram solicitados para enumeração.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-201">The existing column values were not requested for enumeration.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-202">JET_wrnColumnTruncated</span><span class="sxs-lookup"><span data-stu-id="a6ec4-202">JET_wrnColumnTruncated</span></span><br />
<span data-ttu-id="a6ec4-203">1534</span><span class="sxs-lookup"><span data-stu-id="a6ec4-203">1534</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-204">O valor da coluna foi truncado no limite de tamanho solicitado durante a enumeração.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-204">The column value was truncated at the requested size limit during enumeration.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-205">JET_wrnColumnPresent</span><span class="sxs-lookup"><span data-stu-id="a6ec4-205">JET_wrnColumnPresent</span></span><br />
<span data-ttu-id="a6ec4-206">1535</span><span class="sxs-lookup"><span data-stu-id="a6ec4-206">1535</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-207">Os valores de coluna existem, mas não foram retornados pela solicitação.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-207">The column values exist but were not returned by the request.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-208">JET_wrnColumnSingleValue</span><span class="sxs-lookup"><span data-stu-id="a6ec4-208">JET_wrnColumnSingleValue</span></span><br />
<span data-ttu-id="a6ec4-209">1536</span><span class="sxs-lookup"><span data-stu-id="a6ec4-209">1536</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-210">O valor da coluna foi retornado em JET_COLUMNENUM como resultado da JET_bitEnumerateCompressOutput que está sendo definida.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-210">The column value was returned in JET_COLUMNENUM as a result of the JET_bitEnumerateCompressOutput being set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-211">JET_wrnColumnDefault</span><span class="sxs-lookup"><span data-stu-id="a6ec4-211">JET_wrnColumnDefault</span></span><br />
<span data-ttu-id="a6ec4-212">1537</span><span class="sxs-lookup"><span data-stu-id="a6ec4-212">1537</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-213">O valor da coluna é definido como o valor padrão da coluna.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-213">The column value is set to the default value of the column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-214">JET_wrnDataHasChanged</span><span class="sxs-lookup"><span data-stu-id="a6ec4-214">JET_wrnDataHasChanged</span></span><br />
<span data-ttu-id="a6ec4-215">1610</span><span class="sxs-lookup"><span data-stu-id="a6ec4-215">1610</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-216">Os dados foram alterados.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-216">The data has changed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-217">JET_wrnKeyChanged</span><span class="sxs-lookup"><span data-stu-id="a6ec4-217">JET_wrnKeyChanged</span></span><br />
<span data-ttu-id="a6ec4-218">1618</span><span class="sxs-lookup"><span data-stu-id="a6ec4-218">1618</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-219">Uma nova chave está sendo usada.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-219">A new key is being used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-220">JET_wrnFileOpenReadOnly</span><span class="sxs-lookup"><span data-stu-id="a6ec4-220">JET_wrnFileOpenReadOnly</span></span><br />
<span data-ttu-id="a6ec4-221">1813</span><span class="sxs-lookup"><span data-stu-id="a6ec4-221">1813</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-222">O arquivo de banco de dados é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-222">The database file is read only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-223">JET_wrnIdleFull</span><span class="sxs-lookup"><span data-stu-id="a6ec4-223">JET_wrnIdleFull</span></span><br />
<span data-ttu-id="a6ec4-224">1908</span><span class="sxs-lookup"><span data-stu-id="a6ec4-224">1908</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-225">O registro ocioso está cheio.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-225">The idle registry is full.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-226">JET_wrnDefragAlreadyRunning</span><span class="sxs-lookup"><span data-stu-id="a6ec4-226">JET_wrnDefragAlreadyRunning</span></span><br />
<span data-ttu-id="a6ec4-227">2000</span><span class="sxs-lookup"><span data-stu-id="a6ec4-227">2000</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-228">Já havia uma desfragmentação online em execução no banco de dados especificado.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-228">There was an online defragmentation already running on the specified database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-229">JET_wrnDefragNotRunning</span><span class="sxs-lookup"><span data-stu-id="a6ec4-229">JET_wrnDefragNotRunning</span></span><br />
<span data-ttu-id="a6ec4-230">2001</span><span class="sxs-lookup"><span data-stu-id="a6ec4-230">2001</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-231">Uma desfragmentação online não está em execução no banco de dados especificado.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-231">An online defragmentation is not running on the specified database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-232">JET_wrnCallbackNotRegistered</span><span class="sxs-lookup"><span data-stu-id="a6ec4-232">JET_wrnCallbackNotRegistered</span></span><br />
<span data-ttu-id="a6ec4-233">2.100</span><span class="sxs-lookup"><span data-stu-id="a6ec4-233">2100</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-234">Uma função de retorno de chamada não existente teve o registro cancelado.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-234">A non-existent callback function was unregistered.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a6ec4-235">Um valor [JET_ERR](./jet-err.md) menor que zero deve ser interpretado como um erro.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-235">A [JET_ERR](./jet-err.md) value that is less than zero should be interpreted as an error.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a6ec4-236">Errors</span><span class="sxs-lookup"><span data-stu-id="a6ec4-236">Errors</span></span></p></th>
<th><p><span data-ttu-id="a6ec4-237">Descrição</span><span class="sxs-lookup"><span data-stu-id="a6ec4-237">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-238">JET_wrnNyi</span><span class="sxs-lookup"><span data-stu-id="a6ec4-238">JET_wrnNyi</span></span><br />
<span data-ttu-id="a6ec4-239">-1</span><span class="sxs-lookup"><span data-stu-id="a6ec4-239">-1</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-240">A função ainda não foi implementada.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-240">The function is not yet implemented.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-241">JET_errRfsFailure</span><span class="sxs-lookup"><span data-stu-id="a6ec4-241">JET_errRfsFailure</span></span><br />
<span data-ttu-id="a6ec4-242">-100</span><span class="sxs-lookup"><span data-stu-id="a6ec4-242">-100</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-243">Falha no simulador de falha de recurso.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-243">The Resource Failure Simulator failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-244">JET_errRfsNotArmed</span><span class="sxs-lookup"><span data-stu-id="a6ec4-244">JET_errRfsNotArmed</span></span><br />
<span data-ttu-id="a6ec4-245">-101</span><span class="sxs-lookup"><span data-stu-id="a6ec4-245">-101</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-246">O simulador de falha de recurso não foi inicializado.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-246">The Resource Failure Simulator has not been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-247">JET_errFileClose</span><span class="sxs-lookup"><span data-stu-id="a6ec4-247">JET_errFileClose</span></span><br />
<span data-ttu-id="a6ec4-248">-102</span><span class="sxs-lookup"><span data-stu-id="a6ec4-248">-102</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-249">Não foi possível fechar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-249">The file could not be closed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-250">JET_errOutOfThreads</span><span class="sxs-lookup"><span data-stu-id="a6ec4-250">JET_errOutOfThreads</span></span><br />
<span data-ttu-id="a6ec4-251">-103</span><span class="sxs-lookup"><span data-stu-id="a6ec4-251">-103</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-252">Não foi possível iniciar o thread.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-252">The thread could not be started.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-253">JET_errTooManyIO</span><span class="sxs-lookup"><span data-stu-id="a6ec4-253">JET_errTooManyIO</span></span><br />
<span data-ttu-id="a6ec4-254">-105</span><span class="sxs-lookup"><span data-stu-id="a6ec4-254">-105</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-255">O sistema está ocupado devido a muitos IOs.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-255">The system is busy due to too many IOs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-256">JET_errTaskDropped</span><span class="sxs-lookup"><span data-stu-id="a6ec4-256">JET_errTaskDropped</span></span><br />
<span data-ttu-id="a6ec4-257">-106</span><span class="sxs-lookup"><span data-stu-id="a6ec4-257">-106</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-258">Não foi possível executar a tarefa assíncrona solicitada.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-258">The requested asynchronous task could not be executed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-259">JET_errInternalError</span><span class="sxs-lookup"><span data-stu-id="a6ec4-259">JET_errInternalError</span></span><br />
<span data-ttu-id="a6ec4-260">-107</span><span class="sxs-lookup"><span data-stu-id="a6ec4-260">-107</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-261">Ocorreu um erro interno fatal.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-261">There was a fatal internal error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-262">JET_errDatabaseBufferDependenciesCorrupted</span><span class="sxs-lookup"><span data-stu-id="a6ec4-262">JET_errDatabaseBufferDependenciesCorrupted</span></span><br />
<span data-ttu-id="a6ec4-263">-255</span><span class="sxs-lookup"><span data-stu-id="a6ec4-263">-255</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-264">As dependências de buffer foram definidas incorretamente e houve uma falha na recuperação.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-264">The buffer dependencies were set improperly and there was a recovery failure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-265">JET_errPreviousVersion</span><span class="sxs-lookup"><span data-stu-id="a6ec4-265">JET_errPreviousVersion</span></span><br />
<span data-ttu-id="a6ec4-266">-322</span><span class="sxs-lookup"><span data-stu-id="a6ec4-266">-322</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-267">A versão já existia e houve uma falha na recuperação.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-267">The version already existed and there was a recovery failure.</span></span> <span data-ttu-id="a6ec4-268">Esse erro é retornado pelo Gerenciador de diretórios.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-268">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-269">JET_errPageBoundary</span><span class="sxs-lookup"><span data-stu-id="a6ec4-269">JET_errPageBoundary</span></span><br />
<span data-ttu-id="a6ec4-270">-323</span><span class="sxs-lookup"><span data-stu-id="a6ec4-270">-323</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-271">O limite da página foi atingido.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-271">The page boundary has been reached.</span></span> <span data-ttu-id="a6ec4-272">Esse erro é retornado pelo Gerenciador de diretórios.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-272">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-273">JET_errKeyBoundary</span><span class="sxs-lookup"><span data-stu-id="a6ec4-273">JET_errKeyBoundary</span></span><br />
<span data-ttu-id="a6ec4-274">-324</span><span class="sxs-lookup"><span data-stu-id="a6ec4-274">-324</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-275">O limite de chave foi atingido.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-275">The key boundary has been reached.</span></span> <span data-ttu-id="a6ec4-276">Esse erro é retornado pelo Gerenciador de diretórios.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-276">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-277">JET_errBadPageLink</span><span class="sxs-lookup"><span data-stu-id="a6ec4-277">JET_errBadPageLink</span></span><br />
<span data-ttu-id="a6ec4-278">-327</span><span class="sxs-lookup"><span data-stu-id="a6ec4-278">-327</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-279">O banco de dados está corrompido.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-279">The database is corrupt.</span></span> <span data-ttu-id="a6ec4-280">Esse erro é retornado pelo Gerenciador de diretórios.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-280">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-281">JET_errBadBookmark</span><span class="sxs-lookup"><span data-stu-id="a6ec4-281">JET_errBadBookmark</span></span><br />
<span data-ttu-id="a6ec4-282">-328</span><span class="sxs-lookup"><span data-stu-id="a6ec4-282">-328</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-283">O indicador não tem nenhum endereço correspondente no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-283">The bookmark has no corresponding address in the database.</span></span> <span data-ttu-id="a6ec4-284">Esse erro é retornado pelo Gerenciador de diretórios.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-284">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-285">JET_errNTSystemCallFailed</span><span class="sxs-lookup"><span data-stu-id="a6ec4-285">JET_errNTSystemCallFailed</span></span><br />
<span data-ttu-id="a6ec4-286">-334</span><span class="sxs-lookup"><span data-stu-id="a6ec4-286">-334</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-287">Falha na chamada para o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-287">The call to the operating system failed.</span></span> <span data-ttu-id="a6ec4-288">Esse erro é retornado pelo Gerenciador de diretórios.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-288">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-289">JET_errBadParentPageLink</span><span class="sxs-lookup"><span data-stu-id="a6ec4-289">JET_errBadParentPageLink</span></span><br />
<span data-ttu-id="a6ec4-290">-338</span><span class="sxs-lookup"><span data-stu-id="a6ec4-290">-338</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-291">Um banco de dados pai está corrompido.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-291">A parent database is corrupt.</span></span> <span data-ttu-id="a6ec4-292">Esse erro é retornado pelo Gerenciador de diretórios.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-292">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-293">JET_errSPAvailExtCacheOutOfSync</span><span class="sxs-lookup"><span data-stu-id="a6ec4-293">JET_errSPAvailExtCacheOutOfSync</span></span><br />
<span data-ttu-id="a6ec4-294">-340</span><span class="sxs-lookup"><span data-stu-id="a6ec4-294">-340</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-295">O cache AvailExt não corresponde à árvore B +.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-295">The AvailExt cache does not match the B+ tree.</span></span> <span data-ttu-id="a6ec4-296">Esse erro é retornado pelo Gerenciador de diretórios.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-296">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-297">JET_errSPAvailExtCorrupted</span><span class="sxs-lookup"><span data-stu-id="a6ec4-297">JET_errSPAvailExtCorrupted</span></span><br />
<span data-ttu-id="a6ec4-298">-341</span><span class="sxs-lookup"><span data-stu-id="a6ec4-298">-341</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-299">A árvore de espaço AllAvailExt está corrompida.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-299">The AllAvailExt space tree is corrupt.</span></span> <span data-ttu-id="a6ec4-300">Esse erro é retornado pelo Gerenciador de diretórios.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-300">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-301">JET_errSPAvailExtCacheOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="a6ec4-301">JET_errSPAvailExtCacheOutOfMemory</span></span><br />
<span data-ttu-id="a6ec4-302">-342</span><span class="sxs-lookup"><span data-stu-id="a6ec4-302">-342</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-303">Ocorreu um erro de memória insuficiente ao alocar um nó de cache AvailExt.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-303">An out of memory error occurred while allocating an AvailExt cache node.</span></span> <span data-ttu-id="a6ec4-304">Esse erro é retornado pelo Gerenciador de diretórios.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-304">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-305">JET_errSPOwnExtCorrupted</span><span class="sxs-lookup"><span data-stu-id="a6ec4-305">JET_errSPOwnExtCorrupted</span></span><br />
<span data-ttu-id="a6ec4-306">-343</span><span class="sxs-lookup"><span data-stu-id="a6ec4-306">-343</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-307">A árvore de espaço OwnExt está corrompida.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-307">The OwnExt space tree is corrupt.</span></span> <span data-ttu-id="a6ec4-308">Esse erro é retornado pelo Gerenciador de diretórios.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-308">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-309">JET_errDbTimeCorrupted</span><span class="sxs-lookup"><span data-stu-id="a6ec4-309">JET_errDbTimeCorrupted</span></span><br />
<span data-ttu-id="a6ec4-310">-344</span><span class="sxs-lookup"><span data-stu-id="a6ec4-310">-344</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-311">O dbtime na página atual é maior que o banco de dados global dbtime.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-311">The Dbtime on the current page is greater than the global database dbtime.</span></span> <span data-ttu-id="a6ec4-312">Esse erro é retornado pelo Gerenciador de diretórios.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-312">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-313">JET_errKeyTruncated</span><span class="sxs-lookup"><span data-stu-id="a6ec4-313">JET_errKeyTruncated</span></span><br />
<span data-ttu-id="a6ec4-314">-346</span><span class="sxs-lookup"><span data-stu-id="a6ec4-314">-346</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-315">Falha ao tentar criar uma chave para uma entrada de índice porque a chave teria sido truncada e a definição de índice não permite truncamento de chave.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-315">An attempt to create a key for an index entry failed because the key would have been truncated and the index definition disallows key truncation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-316">JET_errKeyTooBig</span><span class="sxs-lookup"><span data-stu-id="a6ec4-316">JET_errKeyTooBig</span></span><br />
<span data-ttu-id="a6ec4-317">-408</span><span class="sxs-lookup"><span data-stu-id="a6ec4-317">-408</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-318">A chave é muito grande.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-318">The key is too large.</span></span> <span data-ttu-id="a6ec4-319">Esse erro é retornado pelo Gerenciador de registros.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-319">This error is returned by the record manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-320">JET_errInvalidLoggedOperation</span><span class="sxs-lookup"><span data-stu-id="a6ec4-320">JET_errInvalidLoggedOperation</span></span><br />
<span data-ttu-id="a6ec4-321">-500</span><span class="sxs-lookup"><span data-stu-id="a6ec4-321">-500</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-322">A operação registrada em log não pode ser refeita.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-322">The logged operation cannot be redone.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-323">JET_errLogFileCorrupt</span><span class="sxs-lookup"><span data-stu-id="a6ec4-323">JET_errLogFileCorrupt</span></span><br />
<span data-ttu-id="a6ec4-324">-501</span><span class="sxs-lookup"><span data-stu-id="a6ec4-324">-501</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-325">O arquivo de log está corrompido.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-325">The log file is corrupt.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-326">JET_errNoBackupDirectory</span><span class="sxs-lookup"><span data-stu-id="a6ec4-326">JET_errNoBackupDirectory</span></span><br />
<span data-ttu-id="a6ec4-327">-503</span><span class="sxs-lookup"><span data-stu-id="a6ec4-327">-503</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-328">Um diretório de backup não foi fornecido.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-328">A backup directory was not given.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-329">JET_errBackupDirectoryNotEmpty</span><span class="sxs-lookup"><span data-stu-id="a6ec4-329">JET_errBackupDirectoryNotEmpty</span></span><br />
<span data-ttu-id="a6ec4-330">-504</span><span class="sxs-lookup"><span data-stu-id="a6ec4-330">-504</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-331">O diretório de backup não está vazio.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-331">The backup directory is not empty.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-332">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="a6ec4-332">JET_errBackupInProgress</span></span><br />
<span data-ttu-id="a6ec4-333">-505</span><span class="sxs-lookup"><span data-stu-id="a6ec4-333">-505</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-334">O backup já está ativo.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-334">The backup is active already.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-335">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="a6ec4-335">JET_errRestoreInProgress</span></span><br />
<span data-ttu-id="a6ec4-336">-506</span><span class="sxs-lookup"><span data-stu-id="a6ec4-336">-506</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-337">Uma restauração está em andamento.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-337">A restore is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-338">JET_errMissingPreviousLogFile</span><span class="sxs-lookup"><span data-stu-id="a6ec4-338">JET_errMissingPreviousLogFile</span></span><br />
<span data-ttu-id="a6ec4-339">-509</span><span class="sxs-lookup"><span data-stu-id="a6ec4-339">-509</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-340">O arquivo de log está ausente para o ponto de verificação.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-340">The log file is missing for the check point.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-341">JET_errLogWriteFail</span><span class="sxs-lookup"><span data-stu-id="a6ec4-341">JET_errLogWriteFail</span></span><br />
<span data-ttu-id="a6ec4-342">-510</span><span class="sxs-lookup"><span data-stu-id="a6ec4-342">-510</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-343">Houve uma falha ao gravar no arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-343">There was a failure writing to the log file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-344">JET_errLogDisabledDueToRecoveryFailure</span><span class="sxs-lookup"><span data-stu-id="a6ec4-344">JET_errLogDisabledDueToRecoveryFailure</span></span><br />
<span data-ttu-id="a6ec4-345">-511</span><span class="sxs-lookup"><span data-stu-id="a6ec4-345">-511</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-346">Falha na tentativa de gravar no log após a recuperação.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-346">The attempt to write to the log after recovery failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-347">JET_errCannotLogDuringRecoveryRedo</span><span class="sxs-lookup"><span data-stu-id="a6ec4-347">JET_errCannotLogDuringRecoveryRedo</span></span><br />
<span data-ttu-id="a6ec4-348">-512</span><span class="sxs-lookup"><span data-stu-id="a6ec4-348">-512</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-349">Falha na tentativa de gravar no log durante a refazer recuperação.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-349">The attempt to write to the log during the recovery redo failed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-350">JET_errLogGenerationMismatch</span><span class="sxs-lookup"><span data-stu-id="a6ec4-350">JET_errLogGenerationMismatch</span></span><br />
<span data-ttu-id="a6ec4-351">-513</span><span class="sxs-lookup"><span data-stu-id="a6ec4-351">-513</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-352">O nome do arquivo de log não corresponde ao número de geração interno.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-352">The name of of the log file does not match the internal generation number.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-353">JET_errBadLogVersion</span><span class="sxs-lookup"><span data-stu-id="a6ec4-353">JET_errBadLogVersion</span></span><br />
<span data-ttu-id="a6ec4-354">-514</span><span class="sxs-lookup"><span data-stu-id="a6ec4-354">-514</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-355">A versão do arquivo de log não é compatível com a versão do ESE.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-355">The version of the log file is not compatible with the ESE version.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-356">JET_errInvalidLogSequence</span><span class="sxs-lookup"><span data-stu-id="a6ec4-356">JET_errInvalidLogSequence</span></span><br />
<span data-ttu-id="a6ec4-357">-515</span><span class="sxs-lookup"><span data-stu-id="a6ec4-357">-515</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-358">O carimbo de data/hora no próximo log não corresponde ao carimbo de data/hora esperado.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-358">The timestamp in the next log does not match the expected timestamp.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-359">JET_errLoggingDisabled</span><span class="sxs-lookup"><span data-stu-id="a6ec4-359">JET_errLoggingDisabled</span></span><br />
<span data-ttu-id="a6ec4-360">-516</span><span class="sxs-lookup"><span data-stu-id="a6ec4-360">-516</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-361">O log não está ativo.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-361">The log is not active.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-362">JET_errLogBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="a6ec4-362">JET_errLogBufferTooSmall</span></span><br />
<span data-ttu-id="a6ec4-363">-517</span><span class="sxs-lookup"><span data-stu-id="a6ec4-363">-517</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-364">O buffer de log é muito pequeno para recuperação.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-364">The log buffer is too small for recovery.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-365">JET_errLogSequenceEnd</span><span class="sxs-lookup"><span data-stu-id="a6ec4-365">JET_errLogSequenceEnd</span></span><br />
<span data-ttu-id="a6ec4-366">-519</span><span class="sxs-lookup"><span data-stu-id="a6ec4-366">-519</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-367">O número máximo do arquivo de log foi excedido.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-367">The maximum log file number has been exceeded.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-368">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="a6ec4-368">JET_errNoBackup</span></span><br />
<span data-ttu-id="a6ec4-369">-520</span><span class="sxs-lookup"><span data-stu-id="a6ec4-369">-520</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-370">Não há backup em andamento.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-370">There is no backup in progress.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-371">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="a6ec4-371">JET_errInvalidBackupSequence</span></span><br />
<span data-ttu-id="a6ec4-372">-521</span><span class="sxs-lookup"><span data-stu-id="a6ec4-372">-521</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-373">A chamada de backup está fora de sequência.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-373">The backup call is out of sequence.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-374">JET_errBackupNotAllowedYet</span><span class="sxs-lookup"><span data-stu-id="a6ec4-374">JET_errBackupNotAllowedYet</span></span><br />
<span data-ttu-id="a6ec4-375">-523</span><span class="sxs-lookup"><span data-stu-id="a6ec4-375">-523</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-376">Não é possível fazer um backup no momento.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-376">A backup cannot be done at this time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-377">JET_errDeleteBackupFileFail</span><span class="sxs-lookup"><span data-stu-id="a6ec4-377">JET_errDeleteBackupFileFail</span></span><br />
<span data-ttu-id="a6ec4-378">-524</span><span class="sxs-lookup"><span data-stu-id="a6ec4-378">-524</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-379">Não foi possível excluir um arquivo de backup.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-379">A backup file could not be deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-380">JET_errMakeBackupDirectoryFail</span><span class="sxs-lookup"><span data-stu-id="a6ec4-380">JET_errMakeBackupDirectoryFail</span></span><br />
<span data-ttu-id="a6ec4-381">-525</span><span class="sxs-lookup"><span data-stu-id="a6ec4-381">-525</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-382">Não foi possível criar o diretório temporário de backup.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-382">The backup temporary directory could not be created.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-383">JET_errInvalidBackup</span><span class="sxs-lookup"><span data-stu-id="a6ec4-383">JET_errInvalidBackup</span></span><br />
<span data-ttu-id="a6ec4-384">-526</span><span class="sxs-lookup"><span data-stu-id="a6ec4-384">-526</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-385">O log circular está habilitado; Não é possível executar um backup incremental.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-385">Circular logging is enabled; an incremental backup cannot be performed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-386">JET_errRecoveredWithErrors</span><span class="sxs-lookup"><span data-stu-id="a6ec4-386">JET_errRecoveredWithErrors</span></span><br />
<span data-ttu-id="a6ec4-387">-527</span><span class="sxs-lookup"><span data-stu-id="a6ec4-387">-527</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-388">Os dados foram restaurados com erros.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-388">The data was restored with errors.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-389">JET_errMissingLogFile</span><span class="sxs-lookup"><span data-stu-id="a6ec4-389">JET_errMissingLogFile</span></span><br />
<span data-ttu-id="a6ec4-390">-528</span><span class="sxs-lookup"><span data-stu-id="a6ec4-390">-528</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-391">O arquivo de log atual está faltando.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-391">The current log file is missing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-392">JET_errLogDiskFull</span><span class="sxs-lookup"><span data-stu-id="a6ec4-392">JET_errLogDiskFull</span></span><br />
<span data-ttu-id="a6ec4-393">-529</span><span class="sxs-lookup"><span data-stu-id="a6ec4-393">-529</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-394">O disco de log está cheio.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-394">The log disk is full.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-395">JET_errBadLogSignature</span><span class="sxs-lookup"><span data-stu-id="a6ec4-395">JET_errBadLogSignature</span></span><br />
<span data-ttu-id="a6ec4-396">-530</span><span class="sxs-lookup"><span data-stu-id="a6ec4-396">-530</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-397">Há uma assinatura inadequada para um arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-397">There is a bad signature for a log file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-398">JET_errBadDbSignature</span><span class="sxs-lookup"><span data-stu-id="a6ec4-398">JET_errBadDbSignature</span></span><br />
<span data-ttu-id="a6ec4-399">-531</span><span class="sxs-lookup"><span data-stu-id="a6ec4-399">-531</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-400">Há uma assinatura inadequada para um arquivo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-400">There is a bad signature for a database file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-401">JET_errBadCheckpointSignature</span><span class="sxs-lookup"><span data-stu-id="a6ec4-401">JET_errBadCheckpointSignature</span></span><br />
<span data-ttu-id="a6ec4-402">-532</span><span class="sxs-lookup"><span data-stu-id="a6ec4-402">-532</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-403">Há uma assinatura inadequada para um arquivo de ponto de verificação.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-403">There is a bad signature for a checkpoint file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-404">JET_errCheckpointCorrupt</span><span class="sxs-lookup"><span data-stu-id="a6ec4-404">JET_errCheckpointCorrupt</span></span><br />
<span data-ttu-id="a6ec4-405">-533</span><span class="sxs-lookup"><span data-stu-id="a6ec4-405">-533</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-406">O arquivo de ponto de verificação não foi encontrado ou estava corrompido.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-406">The checkpoint file was not found or was corrupt.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-407">JET_errMissingPatchPage</span><span class="sxs-lookup"><span data-stu-id="a6ec4-407">JET_errMissingPatchPage</span></span><br />
<span data-ttu-id="a6ec4-408">-534</span><span class="sxs-lookup"><span data-stu-id="a6ec4-408">-534</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-409">A página do arquivo de patch do banco de dados não foi encontrada durante a recuperação.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-409">The database patch file page was not found during recovery.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-410">JET_errBadPatchPage</span><span class="sxs-lookup"><span data-stu-id="a6ec4-410">JET_errBadPatchPage</span></span><br />
<span data-ttu-id="a6ec4-411">-535</span><span class="sxs-lookup"><span data-stu-id="a6ec4-411">-535</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-412">A página do arquivo de patch do banco de dados não é válida.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-412">The database patch file page is not valid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-413">JET_errRedoAbruptEnded</span><span class="sxs-lookup"><span data-stu-id="a6ec4-413">JET_errRedoAbruptEnded</span></span><br />
<span data-ttu-id="a6ec4-414">-536</span><span class="sxs-lookup"><span data-stu-id="a6ec4-414">-536</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-415">A refazer abruptamente terminou devido a uma falha repentina durante a leitura de logs do arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-415">The redo abruptly ended due to a sudden failure while reading logs from the log file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-416">JET_errBadSLVSignature</span><span class="sxs-lookup"><span data-stu-id="a6ec4-416">JET_errBadSLVSignature</span></span><br />
<span data-ttu-id="a6ec4-417">-537</span><span class="sxs-lookup"><span data-stu-id="a6ec4-417">-537</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-418">Esse sinalizador é reservado.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-418">This flag is reserved.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-419">JET_errPatchFileMissing</span><span class="sxs-lookup"><span data-stu-id="a6ec4-419">JET_errPatchFileMissing</span></span><br />
<span data-ttu-id="a6ec4-420">-538</span><span class="sxs-lookup"><span data-stu-id="a6ec4-420">-538</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-421">A restauração complexa detectou que um arquivo de patch de banco de dados está ausente do conjunto de backup.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-421">The hard restore detected that a database patch file is missing from the backup set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-422">JET_errDatabaseLogSetMismatch</span><span class="sxs-lookup"><span data-stu-id="a6ec4-422">JET_errDatabaseLogSetMismatch</span></span><br />
<span data-ttu-id="a6ec4-423">-539</span><span class="sxs-lookup"><span data-stu-id="a6ec4-423">-539</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-424">O banco de dados não pertence ao conjunto atual de arquivos de log.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-424">The database does not belong with the current set of log files.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-425">JET_errDatabaseStreamingFileMismatch</span><span class="sxs-lookup"><span data-stu-id="a6ec4-425">JET_errDatabaseStreamingFileMismatch</span></span><br />
<span data-ttu-id="a6ec4-426">-540</span><span class="sxs-lookup"><span data-stu-id="a6ec4-426">-540</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-427">Esse sinalizador é reservado.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-427">This flag is reserved.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-428">JET_errLogFileSizeMismatch</span><span class="sxs-lookup"><span data-stu-id="a6ec4-428">JET_errLogFileSizeMismatch</span></span><br />
<span data-ttu-id="a6ec4-429">-541</span><span class="sxs-lookup"><span data-stu-id="a6ec4-429">-541</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-430">O tamanho real do arquivo de log não corresponde ao <a href="gg269235(v=exchg.10).md">JET_paramLogFileSize</a>.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-430">The actual log file size does not match <a href="gg269235(v=exchg.10).md">JET_paramLogFileSize</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-431">JET_errCheckpointFileNotFound</span><span class="sxs-lookup"><span data-stu-id="a6ec4-431">JET_errCheckpointFileNotFound</span></span><br />
<span data-ttu-id="a6ec4-432">-542</span><span class="sxs-lookup"><span data-stu-id="a6ec4-432">-542</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-433">Não foi possível localizar o arquivo de ponto de verificação.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-433">The checkpoint file could not be located.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-434">JET_errRequiredLogFilesMissing</span><span class="sxs-lookup"><span data-stu-id="a6ec4-434">JET_errRequiredLogFilesMissing</span></span><br />
<span data-ttu-id="a6ec4-435">-543</span><span class="sxs-lookup"><span data-stu-id="a6ec4-435">-543</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-436">Os arquivos de log necessários para recuperação estão ausentes.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-436">The required log files for recovery are missing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-437">JET_errSoftRecoveryOnBackupDatabase</span><span class="sxs-lookup"><span data-stu-id="a6ec4-437">JET_errSoftRecoveryOnBackupDatabase</span></span><br />
<span data-ttu-id="a6ec4-438">-544</span><span class="sxs-lookup"><span data-stu-id="a6ec4-438">-544</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-439">Uma recuperação simples está prestes a ser usada em um banco de dados de backup quando uma restauração deve ser usada em vez disso.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-439">A soft recovery is about to be used on a backup database when a restore should be used instead.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-440">JET_errLogFileSizeMismatchDatabasesConsistent</span><span class="sxs-lookup"><span data-stu-id="a6ec4-440">JET_errLogFileSizeMismatchDatabasesConsistent</span></span><br />
<span data-ttu-id="a6ec4-441">-545</span><span class="sxs-lookup"><span data-stu-id="a6ec4-441">-545</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-442">Os bancos de dados foram recuperados, mas o tamanho do arquivo de log usado durante a recuperação não corresponde ao <a href="gg269235(v=exchg.10).md">JET_paramLogFileSize</a>.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-442">The databases have been recovered, but the log file size used during recovery does not match <a href="gg269235(v=exchg.10).md">JET_paramLogFileSize</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-443">JET_errLogSectorSizeMismatch</span><span class="sxs-lookup"><span data-stu-id="a6ec4-443">JET_errLogSectorSizeMismatch</span></span><br />
<span data-ttu-id="a6ec4-444">-546</span><span class="sxs-lookup"><span data-stu-id="a6ec4-444">-546</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-445">O tamanho do setor do arquivo de log não corresponde ao tamanho do setor do volume atual.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-445">The log file sector size does not match the sector size of the current volume.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-446">JET_errLogSectorSizeMismatchDatabasesConsistent</span><span class="sxs-lookup"><span data-stu-id="a6ec4-446">JET_errLogSectorSizeMismatchDatabasesConsistent</span></span><br />
<span data-ttu-id="a6ec4-447">-547</span><span class="sxs-lookup"><span data-stu-id="a6ec4-447">-547</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-448">Os bancos de dados foram recuperados, mas o tamanho do setor do arquivo de log (usado durante a recuperação) não corresponde ao tamanho do setor do volume atual.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-448">The databases have been recovered, but the log file sector size (used during recovery) does not match the sector size of the current volume.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-449">JET_errLogSequenceEndDatabasesConsistent</span><span class="sxs-lookup"><span data-stu-id="a6ec4-449">JET_errLogSequenceEndDatabasesConsistent</span></span><br />
<span data-ttu-id="a6ec4-450">-548</span><span class="sxs-lookup"><span data-stu-id="a6ec4-450">-548</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-451">Os bancos de dados foram recuperados, mas todas as gerações de log possíveis na sequência atual foram usadas.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-451">The databases have been recovered, but all possible log generations in the current sequence have been used.</span></span> <span data-ttu-id="a6ec4-452">Todos os arquivos de log e o arquivo de ponto de verificação devem ser excluídos e o backup dos bancos de dados deve ser feito antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-452">All log files and the checkpoint file must be deleted and databases must be backed up before continuing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-453">JET_errStreamingDataNotLogged</span><span class="sxs-lookup"><span data-stu-id="a6ec4-453">JET_errStreamingDataNotLogged</span></span><br />
<span data-ttu-id="a6ec4-454">-549</span><span class="sxs-lookup"><span data-stu-id="a6ec4-454">-549</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-455">Houve uma tentativa ilegal de reproduzir uma operação de arquivo de streaming em que os dados não foram registrados.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-455">There was an illegal attempt to replay a streaming file operation where the data was not logged.</span></span> <span data-ttu-id="a6ec4-456">Isso provavelmente é causado por uma tentativa de avanço com o log circular habilitado.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-456">This is probably caused by an attempt to rollforward with circular logging enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-457">JET_errDatabaseDirtyShutdown</span><span class="sxs-lookup"><span data-stu-id="a6ec4-457">JET_errDatabaseDirtyShutdown</span></span><br />
<span data-ttu-id="a6ec4-458">-550</span><span class="sxs-lookup"><span data-stu-id="a6ec4-458">-550</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-459">O banco de dados não foi desligado corretamente.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-459">The database was not shutdown cleanly.</span></span> <span data-ttu-id="a6ec4-460">Uma recuperação deve primeiro ser executada para concluir corretamente as operações de banco de dados para o desligamento anterior.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-460">A recovery must first be run to properly complete database operations for the previous shutdown.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-461">JET_errDatabaseInconsistent</span><span class="sxs-lookup"><span data-stu-id="a6ec4-461">JET_errDatabaseInconsistent</span></span><br />
<span data-ttu-id="a6ec4-462">JET_errDatabaseDirtyShutdown</span><span class="sxs-lookup"><span data-stu-id="a6ec4-462">JET_errDatabaseDirtyShutdown</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-463">Este erro está obsoleto e foi substituído por JET_errDatabaseDirtyShutdown.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-463">This error is obsolete and has been replaced by JET_errDatabaseDirtyShutdown.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-464">JET_errConsistentTimeMismatch</span><span class="sxs-lookup"><span data-stu-id="a6ec4-464">JET_errConsistentTimeMismatch</span></span><br />
<span data-ttu-id="a6ec4-465">-551</span><span class="sxs-lookup"><span data-stu-id="a6ec4-465">-551</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-466">A hora da última consistência do banco de dados não foi correspondida.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-466">The last consistent time for the database has not been matched.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-467">JET_errDatabasePatchFileMismatch</span><span class="sxs-lookup"><span data-stu-id="a6ec4-467">JET_errDatabasePatchFileMismatch</span></span><br />
<span data-ttu-id="a6ec4-468">-552</span><span class="sxs-lookup"><span data-stu-id="a6ec4-468">-552</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-469">O arquivo de patch do banco de dados não é gerado deste backup.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-469">The database patch file is not generated from this backup.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-470">JET_errEndingRestoreLogTooLow</span><span class="sxs-lookup"><span data-stu-id="a6ec4-470">JET_errEndingRestoreLogTooLow</span></span><br />
<span data-ttu-id="a6ec4-471">-553</span><span class="sxs-lookup"><span data-stu-id="a6ec4-471">-553</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-472">O número de log inicial é muito baixo para a restauração.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-472">The starting log number is too low for the restore.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-473">JET_errStartingRestoreLogTooHigh</span><span class="sxs-lookup"><span data-stu-id="a6ec4-473">JET_errStartingRestoreLogTooHigh</span></span><br />
<span data-ttu-id="a6ec4-474">-554</span><span class="sxs-lookup"><span data-stu-id="a6ec4-474">-554</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-475">O número de log inicial é muito alto para a restauração.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-475">The starting log number is too high for the restore.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-476">JET_errGivenLogFileHasBadSignature</span><span class="sxs-lookup"><span data-stu-id="a6ec4-476">JET_errGivenLogFileHasBadSignature</span></span><br />
<span data-ttu-id="a6ec4-477">-555</span><span class="sxs-lookup"><span data-stu-id="a6ec4-477">-555</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-478">O arquivo de log de restauração tem uma assinatura inadequada.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-478">The restore log file has a bad signature.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-479">JET_errGivenLogFileIsNotContiguous</span><span class="sxs-lookup"><span data-stu-id="a6ec4-479">JET_errGivenLogFileIsNotContiguous</span></span><br />
<span data-ttu-id="a6ec4-480">-556</span><span class="sxs-lookup"><span data-stu-id="a6ec4-480">-556</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-481">O arquivo de log de restauração não é contíguo.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-481">The restore log file is not contiguous.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-482">JET_errMissingRestoreLogFiles</span><span class="sxs-lookup"><span data-stu-id="a6ec4-482">JET_errMissingRestoreLogFiles</span></span><br />
<span data-ttu-id="a6ec4-483">-557</span><span class="sxs-lookup"><span data-stu-id="a6ec4-483">-557</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-484">Alguns arquivos de log de restauração estão ausentes.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-484">Some restore log files are missing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-485">JET_errMissingFullBackup</span><span class="sxs-lookup"><span data-stu-id="a6ec4-485">JET_errMissingFullBackup</span></span><br />
<span data-ttu-id="a6ec4-486">-560</span><span class="sxs-lookup"><span data-stu-id="a6ec4-486">-560</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-487">O banco de dados perdeu um backup completo anterior antes de tentar executar um backup incremental.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-487">The database missed a previous full backup before attempting to perform an incremental backup.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-488">JET_errBadBackupDatabaseSize</span><span class="sxs-lookup"><span data-stu-id="a6ec4-488">JET_errBadBackupDatabaseSize</span></span><br />
<span data-ttu-id="a6ec4-489">-561</span><span class="sxs-lookup"><span data-stu-id="a6ec4-489">-561</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-490">O tamanho do banco de dados de backup não é um múltiplo do tamanho da página do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-490">The backup database size is not a multiple of the database page size.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-491">JET_errDatabaseAlreadyUpgraded</span><span class="sxs-lookup"><span data-stu-id="a6ec4-491">JET_errDatabaseAlreadyUpgraded</span></span><br />
<span data-ttu-id="a6ec4-492">-562</span><span class="sxs-lookup"><span data-stu-id="a6ec4-492">-562</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-493">A tentativa atual de atualizar um banco de dados foi interrompida porque o banco de dados já está atualizado.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-493">The current attempt to upgrade a database has been stopped because the database is already current.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-494">JET_errDatabaseIncompleteUpgrade</span><span class="sxs-lookup"><span data-stu-id="a6ec4-494">JET_errDatabaseIncompleteUpgrade</span></span><br />
<span data-ttu-id="a6ec4-495">-563</span><span class="sxs-lookup"><span data-stu-id="a6ec4-495">-563</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-496">O banco de dados foi parcialmente convertido no formato atual.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-496">The database was only partially converted to the current format.</span></span> <span data-ttu-id="a6ec4-497">O banco de dados deve ser restaurado do backup.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-497">The database must be restored from backup.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-498">JET_errMissingCurrentLogFiles</span><span class="sxs-lookup"><span data-stu-id="a6ec4-498">JET_errMissingCurrentLogFiles</span></span><br />
<span data-ttu-id="a6ec4-499">-565</span><span class="sxs-lookup"><span data-stu-id="a6ec4-499">-565</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-500">Alguns arquivos de log atuais estão ausentes para restauração contínua.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-500">Some current log files are missing for continuous restore.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-501">JET_errDbTimeTooOld</span><span class="sxs-lookup"><span data-stu-id="a6ec4-501">JET_errDbTimeTooOld</span></span><br />
<span data-ttu-id="a6ec4-502">-566</span><span class="sxs-lookup"><span data-stu-id="a6ec4-502">-566</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-503">O dbtime em uma página é menor do que o dbtimeBefore que está no registro.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-503">The dbtime on a page is smaller than the dbtimeBefore that is in the record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-504">JET_errDbTimeTooNew</span><span class="sxs-lookup"><span data-stu-id="a6ec4-504">JET_errDbTimeTooNew</span></span><br />
<span data-ttu-id="a6ec4-505">-567</span><span class="sxs-lookup"><span data-stu-id="a6ec4-505">-567</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-506">O dbtime em uma página está antes do dbtimeBefore que está no registro.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-506">The dbtime on a page is in advance of the dbtimeBefore that is in the record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-507">JET_errMissingFileToBackup</span><span class="sxs-lookup"><span data-stu-id="a6ec4-507">JET_errMissingFileToBackup</span></span><br />
<span data-ttu-id="a6ec4-508">-569</span><span class="sxs-lookup"><span data-stu-id="a6ec4-508">-569</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-509">Alguns arquivos de patch de log ou banco de dados estavam ausentes durante o backup.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-509">Some log or database patch files were missing during the backup.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-510">JET_errLogTornWriteDuringHardRestore</span><span class="sxs-lookup"><span data-stu-id="a6ec4-510">JET_errLogTornWriteDuringHardRestore</span></span><br />
<span data-ttu-id="a6ec4-511">-570</span><span class="sxs-lookup"><span data-stu-id="a6ec4-511">-570</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-512">Foi detectada uma gravação interrompida em um backup definido durante uma restauração complexa.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-512">A torn write was detected in a backup that was set during a hard restore.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-513">JET_errLogTornWriteDuringHardRecovery</span><span class="sxs-lookup"><span data-stu-id="a6ec4-513">JET_errLogTornWriteDuringHardRecovery</span></span><br />
<span data-ttu-id="a6ec4-514">-571</span><span class="sxs-lookup"><span data-stu-id="a6ec4-514">-571</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-515">Foi detectada uma gravação interrompida durante uma recuperação complexa (o log não era parte de um conjunto de backup).</span><span class="sxs-lookup"><span data-stu-id="a6ec4-515">A torn write was detected during a hard recovery (the log was not part of a backup set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-516">JET_errLogCorruptDuringHardRestore</span><span class="sxs-lookup"><span data-stu-id="a6ec4-516">JET_errLogCorruptDuringHardRestore</span></span><br />
<span data-ttu-id="a6ec4-517">-573</span><span class="sxs-lookup"><span data-stu-id="a6ec4-517">-573</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-518">Corrupção detectada em um conjunto de backup durante uma restauração complexa.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-518">Corruption was detected in a backup set during a hard restore.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-519">JET_errLogCorruptDuringHardRecovery</span><span class="sxs-lookup"><span data-stu-id="a6ec4-519">JET_errLogCorruptDuringHardRecovery</span></span><br />
<span data-ttu-id="a6ec4-520">-574</span><span class="sxs-lookup"><span data-stu-id="a6ec4-520">-574</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-521">Foi detectada corrupção durante a recuperação complexa (o log não era parte de um conjunto de backup).</span><span class="sxs-lookup"><span data-stu-id="a6ec4-521">Corruption was detected during hard recovery (the log was not part of a backup set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-522">JET_errMustDisableLoggingForDbUpgrade</span><span class="sxs-lookup"><span data-stu-id="a6ec4-522">JET_errMustDisableLoggingForDbUpgrade</span></span><br />
<span data-ttu-id="a6ec4-523">-575</span><span class="sxs-lookup"><span data-stu-id="a6ec4-523">-575</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-524">O registro em log não pode ser habilitado durante a tentativa de atualizar um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-524">Logging cannot be enabled while attempting to upgrade a database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-525">JET_errBadRestoreTargetInstance</span><span class="sxs-lookup"><span data-stu-id="a6ec4-525">JET_errBadRestoreTargetInstance</span></span><br />
<span data-ttu-id="a6ec4-526">-577</span><span class="sxs-lookup"><span data-stu-id="a6ec4-526">-577</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-527">O TargetInstance que foi especificado para restauração não foi encontrado ou os arquivos de log não coincidem.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-527">Either the TargetInstance that was specified for restore has not been found or the log files do not match.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-528">JET_errRecoveredWithoutUndo</span><span class="sxs-lookup"><span data-stu-id="a6ec4-528">JET_errRecoveredWithoutUndo</span></span><br />
<span data-ttu-id="a6ec4-529">-579</span><span class="sxs-lookup"><span data-stu-id="a6ec4-529">-579</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-530">O mecanismo de banco de dados reproduziu com êxito todas as operações no log de transações para executar uma recuperação de falha, mas o chamador optou por interromper a recuperação sem reverter atualizações não confirmadas.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-530">The database engine successfully replayed all operations in the transaction log to perform a crash recovery but the caller elected to stop recovery without rolling back uncommitted updates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-531">JET_errDatabasesNotFromSameSnapshot</span><span class="sxs-lookup"><span data-stu-id="a6ec4-531">JET_errDatabasesNotFromSameSnapshot</span></span><br />
<span data-ttu-id="a6ec4-532">-580</span><span class="sxs-lookup"><span data-stu-id="a6ec4-532">-580</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-533">Os bancos de dados a serem restaurados não são do mesmo backup de cópia de sombra.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-533">The databases to be restored are not from the same shadow copy backup.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-534">JET_errSoftRecoveryOnSnapshot</span><span class="sxs-lookup"><span data-stu-id="a6ec4-534">JET_errSoftRecoveryOnSnapshot</span></span><br />
<span data-ttu-id="a6ec4-535">-581</span><span class="sxs-lookup"><span data-stu-id="a6ec4-535">-581</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-536">Há uma recuperação suave em um banco de dados de um conjunto de backup de cópia de sombra.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-536">There is a soft recovery on a database from a shadow copy backup set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-537">JET_errUnicodeTranslationBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="a6ec4-537">JET_errUnicodeTranslationBufferTooSmall</span></span><br />
<span data-ttu-id="a6ec4-538">-601</span><span class="sxs-lookup"><span data-stu-id="a6ec4-538">-601</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-539">O buffer de conversão Unicode é muito pequeno.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-539">The Unicode translation buffer is too small.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-540">JET_errUnicodeTranslationFail</span><span class="sxs-lookup"><span data-stu-id="a6ec4-540">JET_errUnicodeTranslationFail</span></span><br />
<span data-ttu-id="a6ec4-541">-602</span><span class="sxs-lookup"><span data-stu-id="a6ec4-541">-602</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-542">Falha na normalização Unicode.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-542">The Unicode normalization failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-543">JET_errUnicodeNormalizationNotSupported</span><span class="sxs-lookup"><span data-stu-id="a6ec4-543">JET_errUnicodeNormalizationNotSupported</span></span><br />
<span data-ttu-id="a6ec4-544">-603</span><span class="sxs-lookup"><span data-stu-id="a6ec4-544">-603</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-545">O sistema operacional não fornece suporte para normalização Unicode e um retorno de chamada de normalização não foi especificado.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-545">The operating system does not provide support for Unicode normalization and a normalization callback was not specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-546">JET_errExistingLogFileHasBadSignature</span><span class="sxs-lookup"><span data-stu-id="a6ec4-546">JET_errExistingLogFileHasBadSignature</span></span><br />
<span data-ttu-id="a6ec4-547">-610</span><span class="sxs-lookup"><span data-stu-id="a6ec4-547">-610</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-548">O arquivo de log existente tem uma assinatura inadequada.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-548">The existing log file has a bad signature.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-549">JET_errExistingLogFileIsNotContiguous</span><span class="sxs-lookup"><span data-stu-id="a6ec4-549">JET_errExistingLogFileIsNotContiguous</span></span><br />
<span data-ttu-id="a6ec4-550">-611</span><span class="sxs-lookup"><span data-stu-id="a6ec4-550">-611</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-551">Um arquivo de log existente não é contíguo.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-551">An existing log file is not contiguous.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-552">JET_errLogReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="a6ec4-552">JET_errLogReadVerifyFailure</span></span><br />
<span data-ttu-id="a6ec4-553">-612</span><span class="sxs-lookup"><span data-stu-id="a6ec4-553">-612</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-554">Um erro de soma de verificação foi encontrado no arquivo de log durante o backup.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-554">A checksum error was found in the log file during backup.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-555">JET_errSLVReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="a6ec4-555">JET_errSLVReadVerifyFailure</span></span><br />
<span data-ttu-id="a6ec4-556">-613</span><span class="sxs-lookup"><span data-stu-id="a6ec4-556">-613</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-557">Esse sinalizador é reservado.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-557">This flag is reserved.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-558">JET_errCheckpointDepthTooDeep</span><span class="sxs-lookup"><span data-stu-id="a6ec4-558">JET_errCheckpointDepthTooDeep</span></span><br />
<span data-ttu-id="a6ec4-559">-614</span><span class="sxs-lookup"><span data-stu-id="a6ec4-559">-614</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-560">Há muitas gerações pendentes entre o ponto de verificação e a geração atual.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-560">There are too many outstanding generations between the checkpoint and the current generation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-561">JET_errRestoreOfNonBackupDatabase</span><span class="sxs-lookup"><span data-stu-id="a6ec4-561">JET_errRestoreOfNonBackupDatabase</span></span><br />
<span data-ttu-id="a6ec4-562">-615</span><span class="sxs-lookup"><span data-stu-id="a6ec4-562">-615</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-563">Uma recuperação complexa foi tentada em um banco de dados que não era um banco de dados de backup.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-563">A hard recovery was attempted on a database that was not a backup database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-564">JET_errInvalidGrbit</span><span class="sxs-lookup"><span data-stu-id="a6ec4-564">JET_errInvalidGrbit</span></span><br />
<span data-ttu-id="a6ec4-565">-900</span><span class="sxs-lookup"><span data-stu-id="a6ec4-565">-900</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-566">Há um parâmetro grbit inválido.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-566">There is an invalid grbit parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-567">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="a6ec4-567">JET_errTermInProgress</span></span><br />
<span data-ttu-id="a6ec4-568">-1000</span><span class="sxs-lookup"><span data-stu-id="a6ec4-568">-1000</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-569">O encerramento está em andamento.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-569">Termination is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-570">JET_errFeatureNotAvailable</span><span class="sxs-lookup"><span data-stu-id="a6ec4-570">JET_errFeatureNotAvailable</span></span><br />
<span data-ttu-id="a6ec4-571">-1001</span><span class="sxs-lookup"><span data-stu-id="a6ec4-571">-1001</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-572">Não há suporte para este elemento de API.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-572">This API element is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-573">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="a6ec4-573">JET_errInvalidName</span></span><br />
<span data-ttu-id="a6ec4-574">-1002</span><span class="sxs-lookup"><span data-stu-id="a6ec4-574">-1002</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-575">Um nome inválido está sendo usado.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-575">An invalid name is being used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-576">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="a6ec4-576">JET_errInvalidParameter</span></span><br />
<span data-ttu-id="a6ec4-577">-1003</span><span class="sxs-lookup"><span data-stu-id="a6ec4-577">-1003</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-578">Um parâmetro de API inválido está sendo usado.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-578">An invalid API parameter is being used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-579">JET_errDatabaseFileReadOnly</span><span class="sxs-lookup"><span data-stu-id="a6ec4-579">JET_errDatabaseFileReadOnly</span></span><br />
<span data-ttu-id="a6ec4-580">-1008</span><span class="sxs-lookup"><span data-stu-id="a6ec4-580">-1008</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-581">Houve uma tentativa de anexar a um arquivo de banco de dados somente leitura para operações de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-581">There was an attempt to attach to a read-only database file for read/write operations.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-582">JET_errInvalidDatabaseId</span><span class="sxs-lookup"><span data-stu-id="a6ec4-582">JET_errInvalidDatabaseId</span></span><br />
<span data-ttu-id="a6ec4-583">-1010</span><span class="sxs-lookup"><span data-stu-id="a6ec4-583">-1010</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-584">Há uma ID de banco de dados inválida.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-584">There is an invalid database ID.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-585">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="a6ec4-585">JET_errOutOfMemory</span></span><br />
<span data-ttu-id="a6ec4-586">-1011</span><span class="sxs-lookup"><span data-stu-id="a6ec4-586">-1011</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-587">O sistema está sem memória.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-587">The system is out of memory.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-588">JET_errOutOfDatabaseSpace</span><span class="sxs-lookup"><span data-stu-id="a6ec4-588">JET_errOutOfDatabaseSpace</span></span><br />
<span data-ttu-id="a6ec4-589">-1012</span><span class="sxs-lookup"><span data-stu-id="a6ec4-589">-1012</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-590">O tamanho máximo do banco de dados foi atingido.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-590">The maximum database size has been reached.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-591">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="a6ec4-591">JET_errOutOfCursors</span></span><br />
<span data-ttu-id="a6ec4-592">-1013</span><span class="sxs-lookup"><span data-stu-id="a6ec4-592">-1013</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-593">A tabela está sem cursores.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-593">The table is out of cursors.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-594">JET_errOutOfBuffers</span><span class="sxs-lookup"><span data-stu-id="a6ec4-594">JET_errOutOfBuffers</span></span><br />
<span data-ttu-id="a6ec4-595">-1014</span><span class="sxs-lookup"><span data-stu-id="a6ec4-595">-1014</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-596">O banco de dados está sem buffers de página.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-596">The database is out of page buffers.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-597">JET_errTooManyIndexes</span><span class="sxs-lookup"><span data-stu-id="a6ec4-597">JET_errTooManyIndexes</span></span><br />
<span data-ttu-id="a6ec4-598">-1015</span><span class="sxs-lookup"><span data-stu-id="a6ec4-598">-1015</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-599">Há muitos índices.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-599">There are too many indexes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-600">JET_errTooManyKeys</span><span class="sxs-lookup"><span data-stu-id="a6ec4-600">JET_errTooManyKeys</span></span><br />
<span data-ttu-id="a6ec4-601">-1016</span><span class="sxs-lookup"><span data-stu-id="a6ec4-601">-1016</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-602">Há muitas colunas em um índice.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-602">There are too many columns in an index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-603">JET_errRecordDeleted</span><span class="sxs-lookup"><span data-stu-id="a6ec4-603">JET_errRecordDeleted</span></span><br />
<span data-ttu-id="a6ec4-604">-1017</span><span class="sxs-lookup"><span data-stu-id="a6ec4-604">-1017</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-605">O registro foi excluído.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-605">The record has been deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-606">JET_errReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="a6ec4-606">JET_errReadVerifyFailure</span></span><br />
<span data-ttu-id="a6ec4-607">-1018</span><span class="sxs-lookup"><span data-stu-id="a6ec4-607">-1018</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-608">Há um erro de soma de verificação em uma página de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-608">There is a checksum error on a database page.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-609">JET_errPageNotInitialized</span><span class="sxs-lookup"><span data-stu-id="a6ec4-609">JET_errPageNotInitialized</span></span><br />
<span data-ttu-id="a6ec4-610">-1019</span><span class="sxs-lookup"><span data-stu-id="a6ec4-610">-1019</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-611">Há uma página de banco de dados em branco.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-611">There is a blank database page.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-612">JET_errOutOfFileHandles</span><span class="sxs-lookup"><span data-stu-id="a6ec4-612">JET_errOutOfFileHandles</span></span><br />
<span data-ttu-id="a6ec4-613">-1020</span><span class="sxs-lookup"><span data-stu-id="a6ec4-613">-1020</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-614">Não há identificadores de arquivo.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-614">There are no file handles.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-615">JET_errDiskIO</span><span class="sxs-lookup"><span data-stu-id="a6ec4-615">JET_errDiskIO</span></span><br />
<span data-ttu-id="a6ec4-616">-1022</span><span class="sxs-lookup"><span data-stu-id="a6ec4-616">-1022</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-617">Há um erro de e/s de disco.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-617">There is a disk IO error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-618">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="a6ec4-618">JET_errInvalidPath</span></span><br />
<span data-ttu-id="a6ec4-619">-1023</span><span class="sxs-lookup"><span data-stu-id="a6ec4-619">-1023</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-620">Há um caminho de arquivo inválido.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-620">There is an invalid file path.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-621">JET_errInvalidSystemPath</span><span class="sxs-lookup"><span data-stu-id="a6ec4-621">JET_errInvalidSystemPath</span></span><br />
<span data-ttu-id="a6ec4-622">-1024</span><span class="sxs-lookup"><span data-stu-id="a6ec4-622">-1024</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-623">Há um caminho de sistema inválido.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-623">There is an invalid system path.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-624">JET_errInvalidLogDirectory</span><span class="sxs-lookup"><span data-stu-id="a6ec4-624">JET_errInvalidLogDirectory</span></span><br />
<span data-ttu-id="a6ec4-625">-1025</span><span class="sxs-lookup"><span data-stu-id="a6ec4-625">-1025</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-626">Há um diretório de log inválido.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-626">There is an invalid log directory.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-627">JET_errRecordTooBig</span><span class="sxs-lookup"><span data-stu-id="a6ec4-627">JET_errRecordTooBig</span></span><br />
<span data-ttu-id="a6ec4-628">-1026</span><span class="sxs-lookup"><span data-stu-id="a6ec4-628">-1026</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-629">O registro é maior que o tamanho máximo.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-629">The record is larger than maximum size.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-630">JET_errTooManyOpenDatabases</span><span class="sxs-lookup"><span data-stu-id="a6ec4-630">JET_errTooManyOpenDatabases</span></span><br />
<span data-ttu-id="a6ec4-631">-1027</span><span class="sxs-lookup"><span data-stu-id="a6ec4-631">-1027</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-632">Há muitos bancos de dados abertos.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-632">There are too many open databases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-633">JET_errInvalidDatabase</span><span class="sxs-lookup"><span data-stu-id="a6ec4-633">JET_errInvalidDatabase</span></span><br />
<span data-ttu-id="a6ec4-634">-1028</span><span class="sxs-lookup"><span data-stu-id="a6ec4-634">-1028</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-635">Este não é um arquivo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-635">This is not a database file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-636">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="a6ec4-636">JET_errNotInitialized</span></span><br />
<span data-ttu-id="a6ec4-637">-1029</span><span class="sxs-lookup"><span data-stu-id="a6ec4-637">-1029</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-638">O mecanismo de banco de dados não foi inicializado.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-638">The database engine has not been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-639">JET_errAlreadyInitialized</span><span class="sxs-lookup"><span data-stu-id="a6ec4-639">JET_errAlreadyInitialized</span></span><br />
<span data-ttu-id="a6ec4-640">-1030</span><span class="sxs-lookup"><span data-stu-id="a6ec4-640">-1030</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-641">O mecanismo de banco de dados já foi inicializado.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-641">The database engine is already initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-642">JET_errInitInProgress</span><span class="sxs-lookup"><span data-stu-id="a6ec4-642">JET_errInitInProgress</span></span><br />
<span data-ttu-id="a6ec4-643">-1031</span><span class="sxs-lookup"><span data-stu-id="a6ec4-643">-1031</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-644">O mecanismo de banco de dados está sendo inicializado.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-644">The database engine is being initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-645">JET_errFileAccessDenied</span><span class="sxs-lookup"><span data-stu-id="a6ec4-645">JET_errFileAccessDenied</span></span><br />
<span data-ttu-id="a6ec4-646">-1032</span><span class="sxs-lookup"><span data-stu-id="a6ec4-646">-1032</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-647">O arquivo não pode ser acessado porque o arquivo está bloqueado ou em uso.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-647">The file cannot be accessed because the file is locked or in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-648">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="a6ec4-648">JET_errBufferTooSmall</span></span><br />
<span data-ttu-id="a6ec4-649">-1038</span><span class="sxs-lookup"><span data-stu-id="a6ec4-649">-1038</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-650">O buffer é muito pequeno.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-650">The buffer is too small.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-651">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="a6ec4-651">JET_errTooManyColumns</span></span><br />
<span data-ttu-id="a6ec4-652">-1040</span><span class="sxs-lookup"><span data-stu-id="a6ec4-652">-1040</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-653">Há muitas colunas definidas.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-653">Too many columns are defined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-654">JET_errContainerNotEmpty</span><span class="sxs-lookup"><span data-stu-id="a6ec4-654">JET_errContainerNotEmpty</span></span><br />
<span data-ttu-id="a6ec4-655">-1043</span><span class="sxs-lookup"><span data-stu-id="a6ec4-655">-1043</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-656">O contêiner não está vazio.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-656">The container is not empty.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-657">JET_errInvalidFilename</span><span class="sxs-lookup"><span data-stu-id="a6ec4-657">JET_errInvalidFilename</span></span><br />
<span data-ttu-id="a6ec4-658">-1044</span><span class="sxs-lookup"><span data-stu-id="a6ec4-658">-1044</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-659">O nome do arquivo é inválido.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-659">The filename is invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-660">JET_errInvalidBookmark</span><span class="sxs-lookup"><span data-stu-id="a6ec4-660">JET_errInvalidBookmark</span></span><br />
<span data-ttu-id="a6ec4-661">-1045</span><span class="sxs-lookup"><span data-stu-id="a6ec4-661">-1045</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-662">Há um indicador inválido.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-662">There is an invalid bookmark.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-663">JET_errColumnInUse</span><span class="sxs-lookup"><span data-stu-id="a6ec4-663">JET_errColumnInUse</span></span><br />
<span data-ttu-id="a6ec4-664">-1046</span><span class="sxs-lookup"><span data-stu-id="a6ec4-664">-1046</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-665">A coluna usada está em um índice.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-665">The column used is in an index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-666">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="a6ec4-666">JET_errInvalidBufferSize</span></span><br />
<span data-ttu-id="a6ec4-667">-1047</span><span class="sxs-lookup"><span data-stu-id="a6ec4-667">-1047</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-668">O buffer de dados não corresponde ao tamanho da coluna.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-668">The data buffer does not match the column size.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-669">JET_errColumnNotUpdatable</span><span class="sxs-lookup"><span data-stu-id="a6ec4-669">JET_errColumnNotUpdatable</span></span><br />
<span data-ttu-id="a6ec4-670">-1048</span><span class="sxs-lookup"><span data-stu-id="a6ec4-670">-1048</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-671">O valor da coluna não pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-671">The column value cannot be set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-672">JET_errIndexInUse</span><span class="sxs-lookup"><span data-stu-id="a6ec4-672">JET_errIndexInUse</span></span><br />
<span data-ttu-id="a6ec4-673">-1051</span><span class="sxs-lookup"><span data-stu-id="a6ec4-673">-1051</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-674">O índice está em uso.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-674">The index is in use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-675">JET_errLinkNotSupported</span><span class="sxs-lookup"><span data-stu-id="a6ec4-675">JET_errLinkNotSupported</span></span><br />
<span data-ttu-id="a6ec4-676">-1052</span><span class="sxs-lookup"><span data-stu-id="a6ec4-676">-1052</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-677">O suporte ao link não está disponível.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-677">The link support is unavailable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-678">JET_errNullKeyDisallowed</span><span class="sxs-lookup"><span data-stu-id="a6ec4-678">JET_errNullKeyDisallowed</span></span><br />
<span data-ttu-id="a6ec4-679">-1053</span><span class="sxs-lookup"><span data-stu-id="a6ec4-679">-1053</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-680">Chaves nulas não são permitidas em um índice.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-680">Null keys are not allowed on an index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-681">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="a6ec4-681">JET_errNotInTransaction</span></span><br />
<span data-ttu-id="a6ec4-682">-1054</span><span class="sxs-lookup"><span data-stu-id="a6ec4-682">-1054</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-683">A operação deve ocorrer em uma transação.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-683">The operation must occur within a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-684">JET_errTooManyActiveUsers</span><span class="sxs-lookup"><span data-stu-id="a6ec4-684">JET_errTooManyActiveUsers</span></span><br />
<span data-ttu-id="a6ec4-685">-1059</span><span class="sxs-lookup"><span data-stu-id="a6ec4-685">-1059</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-686">Há muitos usuários de banco de dados ativos</span><span class="sxs-lookup"><span data-stu-id="a6ec4-686">There are too many active database users</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-687">JET_errInvalidCountry</span><span class="sxs-lookup"><span data-stu-id="a6ec4-687">JET_errInvalidCountry</span></span><br />
<span data-ttu-id="a6ec4-688">-1061</span><span class="sxs-lookup"><span data-stu-id="a6ec4-688">-1061</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-689">Há um código de país inválido ou desconhecido.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-689">There is an invalid or unknown country code.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-690">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="a6ec4-690">JET_errInvalidLanguageId</span></span><br />
<span data-ttu-id="a6ec4-691">-1062</span><span class="sxs-lookup"><span data-stu-id="a6ec4-691">-1062</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-692">Há uma ID de idioma inválida ou desconhecida.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-692">There is an invalid or unknown language ID.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-693">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="a6ec4-693">JET_errInvalidCodePage</span></span><br />
<span data-ttu-id="a6ec4-694">-1063</span><span class="sxs-lookup"><span data-stu-id="a6ec4-694">-1063</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-695">Há uma página de código inválida ou desconhecida.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-695">There is an invalid or unknown code page.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-696">JET_errInvalidLCMapStringFlags</span><span class="sxs-lookup"><span data-stu-id="a6ec4-696">JET_errInvalidLCMapStringFlags</span></span><br />
<span data-ttu-id="a6ec4-697">-1064</span><span class="sxs-lookup"><span data-stu-id="a6ec4-697">-1064</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-698">Há Sinalizadores inválidos sendo usados para <a href="/windows/win32/api/winnls/nf-winnls-lcmapstringa">LCMapString</a>.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-698">There are invalid flags being used for <a href="/windows/win32/api/winnls/nf-winnls-lcmapstringa">LCMapString</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-699">JET_errVersionStoreEntryTooBig</span><span class="sxs-lookup"><span data-stu-id="a6ec4-699">JET_errVersionStoreEntryTooBig</span></span><br />
<span data-ttu-id="a6ec4-700">-1065</span><span class="sxs-lookup"><span data-stu-id="a6ec4-700">-1065</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-701">Houve uma tentativa de criar uma entrada de repositório de versão (RCE) que era maior que um Bucket de versão.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-701">There was an attempt to create a version store entry (RCE) that was larger than a version bucket.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-702">JET_errVersionStoreOutOfMemoryAndCleanupTimedOut</span><span class="sxs-lookup"><span data-stu-id="a6ec4-702">JET_errVersionStoreOutOfMemoryAndCleanupTimedOut</span></span><br />
<span data-ttu-id="a6ec4-703">-1066</span><span class="sxs-lookup"><span data-stu-id="a6ec4-703">-1066</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-704">O repositório de versão está sem memória e a tentativa de limpeza não foi concluída.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-704">The version store is out of memory and the cleanup attempt failed to complete.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-705">JET_errVersionStoreOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="a6ec4-705">JET_errVersionStoreOutOfMemory</span></span><br />
<span data-ttu-id="a6ec4-706">-1069</span><span class="sxs-lookup"><span data-stu-id="a6ec4-706">-1069</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-707">O repositório de versão está sem memória e uma limpeza já foi tentada).</span><span class="sxs-lookup"><span data-stu-id="a6ec4-707">The version store is out of memory and a cleanup was already attempted).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-708">JET_errCannotIndex</span><span class="sxs-lookup"><span data-stu-id="a6ec4-708">JET_errCannotIndex</span></span><br />
<span data-ttu-id="a6ec4-709">-1071</span><span class="sxs-lookup"><span data-stu-id="a6ec4-709">-1071</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-710">As colunas caução e SLV não podem ser indexadas.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-710">The escrow and SLV columns cannot be indexed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-711">JET_errRecordNotDeleted</span><span class="sxs-lookup"><span data-stu-id="a6ec4-711">JET_errRecordNotDeleted</span></span><br />
<span data-ttu-id="a6ec4-712">-1072</span><span class="sxs-lookup"><span data-stu-id="a6ec4-712">-1072</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-713">O registro não foi excluído.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-713">The record has not been deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-714">JET_errTooManyMempoolEntries</span><span class="sxs-lookup"><span data-stu-id="a6ec4-714">JET_errTooManyMempoolEntries</span></span><br />
<span data-ttu-id="a6ec4-715">-1073</span><span class="sxs-lookup"><span data-stu-id="a6ec4-715">-1073</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-716">Foram solicitadas muitas entradas mempool.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-716">Too many mempool entries have been requested.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-717">JET_errOutOfObjectIDs</span><span class="sxs-lookup"><span data-stu-id="a6ec4-717">JET_errOutOfObjectIDs</span></span><br />
<span data-ttu-id="a6ec4-718">-1074</span><span class="sxs-lookup"><span data-stu-id="a6ec4-718">-1074</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-719">O banco de dados está fora dos ObjectIDs da árvore B + e, portanto, uma desfragmentação offline deve ser executada para recuperar ObjectIds liberadas ou não utilizadas.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-719">The database is out of B+ tree ObjectIDs so an offline defragmentation must be performed to reclaim freed or unused ObjectIds.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-720">JET_errOutOfLongValueIDs</span><span class="sxs-lookup"><span data-stu-id="a6ec4-720">JET_errOutOfLongValueIDs</span></span><br />
<span data-ttu-id="a6ec4-721">-1075</span><span class="sxs-lookup"><span data-stu-id="a6ec4-721">-1075</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-722">O contador de ID de valor longo atingiu o valor máximo.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-722">The Long-value ID counter has reached the maximum value.</span></span> <span data-ttu-id="a6ec4-723">Uma desfragmentação offline deve ser executada para recuperar LongValueIDs livres ou não utilizados.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-723">An offline defragmentation must be performed to reclaim free or unused LongValueIDs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-724">JET_errOutOfAutoincrementValues</span><span class="sxs-lookup"><span data-stu-id="a6ec4-724">JET_errOutOfAutoincrementValues</span></span><br />
<span data-ttu-id="a6ec4-725">-1076</span><span class="sxs-lookup"><span data-stu-id="a6ec4-725">-1076</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-726">O contador de incremento automático atingiu o valor máximo.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-726">The auto-increment counter has reached the maximum value.</span></span> <span data-ttu-id="a6ec4-727">Uma desfragmentação offline não será capaz de recuperar valores de incremento automáticos gratuitos ou não utilizados).</span><span class="sxs-lookup"><span data-stu-id="a6ec4-727">An offline defragmentation will not be able to reclaim free or unused auto-increment values).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-728">JET_errOutOfDbtimeValues</span><span class="sxs-lookup"><span data-stu-id="a6ec4-728">JET_errOutOfDbtimeValues</span></span><br />
<span data-ttu-id="a6ec4-729">-1077</span><span class="sxs-lookup"><span data-stu-id="a6ec4-729">-1077</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-730">O contador dbtime atingiu o valor máximo.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-730">The Dbtime counter has reached the maximum value.</span></span> <span data-ttu-id="a6ec4-731">Uma desfragmentação offline deve ser executada para recuperar valores de dbtime livres ou não utilizados.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-731">An offline defragmentation must be performed to reclaim free or unused Dbtime values.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-732">JET_errOutOfSequentialIndexValues</span><span class="sxs-lookup"><span data-stu-id="a6ec4-732">JET_errOutOfSequentialIndexValues</span></span><br />
<span data-ttu-id="a6ec4-733">-1078</span><span class="sxs-lookup"><span data-stu-id="a6ec4-733">-1078</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-734">Um contador de índice sequencial atingiu o valor máximo.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-734">A sequential index counter has reached the maximum value.</span></span> <span data-ttu-id="a6ec4-735">Uma desfragmentação offline deve ser executada para recuperar valores de SequentialIndex livres ou não utilizados.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-735">An offline defragmentation must be performed to reclaim free or unused SequentialIndex values.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-736">JET_errRunningInOneInstanceMode</span><span class="sxs-lookup"><span data-stu-id="a6ec4-736">JET_errRunningInOneInstanceMode</span></span><br />
<span data-ttu-id="a6ec4-737">-1080</span><span class="sxs-lookup"><span data-stu-id="a6ec4-737">-1080</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-738">Esta chamada de várias instâncias tem o modo de instância única habilitado.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-738">This multi-instance call has the single-instance mode enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-739">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="a6ec4-739">JET_errRunningInMultiInstanceMode</span></span><br />
<span data-ttu-id="a6ec4-740">-1081</span><span class="sxs-lookup"><span data-stu-id="a6ec4-740">-1081</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-741">Esta chamada de instância única tem o modo de várias instâncias habilitado.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-741">This single-instance call has the multi-instance mode enabled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-742">JET_errSystemParamsAlreadySet</span><span class="sxs-lookup"><span data-stu-id="a6ec4-742">JET_errSystemParamsAlreadySet</span></span><br />
<span data-ttu-id="a6ec4-743">-1082</span><span class="sxs-lookup"><span data-stu-id="a6ec4-743">-1082</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-744">Os parâmetros do sistema global já foram definidos.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-744">The global system parameters have already been set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-745">JET_errSystemPathInUse</span><span class="sxs-lookup"><span data-stu-id="a6ec4-745">JET_errSystemPathInUse</span></span><br />
<span data-ttu-id="a6ec4-746">-1083</span><span class="sxs-lookup"><span data-stu-id="a6ec4-746">-1083</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-747">O caminho do sistema já está sendo usado por outra instância de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-747">The system path is already being used by another database instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-748">JET_errLogFilePathInUse</span><span class="sxs-lookup"><span data-stu-id="a6ec4-748">JET_errLogFilePathInUse</span></span><br />
<span data-ttu-id="a6ec4-749">-1084</span><span class="sxs-lookup"><span data-stu-id="a6ec4-749">-1084</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-750">O caminho do arquivo de log já está sendo usado por outra instância de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-750">The log file path is already being used by another database instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-751">JET_errTempPathInUse</span><span class="sxs-lookup"><span data-stu-id="a6ec4-751">JET_errTempPathInUse</span></span><br />
<span data-ttu-id="a6ec4-752">-1085</span><span class="sxs-lookup"><span data-stu-id="a6ec4-752">-1085</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-753">O caminho para o banco de dados temporário já está sendo usado por outra instância de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-753">The path to the temporary database is already being used by another database instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-754">JET_errInstanceNameInUse</span><span class="sxs-lookup"><span data-stu-id="a6ec4-754">JET_errInstanceNameInUse</span></span><br />
<span data-ttu-id="a6ec4-755">-1086</span><span class="sxs-lookup"><span data-stu-id="a6ec4-755">-1086</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-756">O nome da instância já está em uso.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-756">The instance name is already in use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-757">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="a6ec4-757">JET_errInstanceUnavailable</span></span><br />
<span data-ttu-id="a6ec4-758">-1090</span><span class="sxs-lookup"><span data-stu-id="a6ec4-758">-1090</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-759">Esta instância não pode ser usada porque encontrou um erro fatal.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-759">This instance cannot be used because it encountered a fatal error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-760">JET_errDatabaseUnavailable</span><span class="sxs-lookup"><span data-stu-id="a6ec4-760">JET_errDatabaseUnavailable</span></span><br />
<span data-ttu-id="a6ec4-761">-1091</span><span class="sxs-lookup"><span data-stu-id="a6ec4-761">-1091</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-762">Este banco de dados não pode ser usado porque encontrou um erro fatal.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-762">This database cannot be used because it encountered a fatal error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-763">JET_errInstanceUnavailableDueToFatalLogDiskFull</span><span class="sxs-lookup"><span data-stu-id="a6ec4-763">JET_errInstanceUnavailableDueToFatalLogDiskFull</span></span><br />
<span data-ttu-id="a6ec4-764">-1092</span><span class="sxs-lookup"><span data-stu-id="a6ec4-764">-1092</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-765">Esta instância não pode ser usada porque encontrou um erro de disco cheio durante a execução de uma operação (como uma reversão de transação) que não pôde tolerar a falha.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-765">This instance cannot be used because it encountered a log-disk-full error while performing an operation (such as a transaction rollback) that could not tolerate failure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-766">JET_errOutOfSessions</span><span class="sxs-lookup"><span data-stu-id="a6ec4-766">JET_errOutOfSessions</span></span><br />
<span data-ttu-id="a6ec4-767">-1101</span><span class="sxs-lookup"><span data-stu-id="a6ec4-767">-1101</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-768">O banco de dados está fora de sessões.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-768">The database is out of sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-769">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="a6ec4-769">JET_errWriteConflict</span></span><br />
<span data-ttu-id="a6ec4-770">-1102</span><span class="sxs-lookup"><span data-stu-id="a6ec4-770">-1102</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-771">Falha no bloqueio de gravação devido à existência de um bloqueio de gravação pendente.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-771">The write lock failed due to the existence of an outstanding write lock.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-772">JET_errTransTooDeep</span><span class="sxs-lookup"><span data-stu-id="a6ec4-772">JET_errTransTooDeep</span></span><br />
<span data-ttu-id="a6ec4-773">-1103</span><span class="sxs-lookup"><span data-stu-id="a6ec4-773">-1103</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-774">As transações estão aninhadas muito profundamente.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-774">The transactions are nested too deeply.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-775">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="a6ec4-775">JET_errInvalidSesid</span></span><br />
<span data-ttu-id="a6ec4-776">-1104</span><span class="sxs-lookup"><span data-stu-id="a6ec4-776">-1104</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-777">Identificador de sessão inválido.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-777">There is an invalid session handle.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-778">JET_errWriteConflictPrimaryIndex</span><span class="sxs-lookup"><span data-stu-id="a6ec4-778">JET_errWriteConflictPrimaryIndex</span></span><br />
<span data-ttu-id="a6ec4-779">-1105</span><span class="sxs-lookup"><span data-stu-id="a6ec4-779">-1105</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-780">Houve uma tentativa de atualização em um índice primário não confirmado.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-780">An update was attempted on an uncommitted primary index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-781">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="a6ec4-781">JET_errInTransaction</span></span><br />
<span data-ttu-id="a6ec4-782">-1108</span><span class="sxs-lookup"><span data-stu-id="a6ec4-782">-1108</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-783">A operação não é permitida em uma transação.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-783">The operation is not allowed within a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-784">JET_errRollbackRequired</span><span class="sxs-lookup"><span data-stu-id="a6ec4-784">JET_errRollbackRequired</span></span><br />
<span data-ttu-id="a6ec4-785">-1109</span><span class="sxs-lookup"><span data-stu-id="a6ec4-785">-1109</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-786">A transação atual deve ser revertida.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-786">The current transaction must be rolled back.</span></span> <span data-ttu-id="a6ec4-787">Ele não pode ser confirmado e um novo não pode ser iniciado.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-787">It cannot be committed and a new one cannot be started.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-788">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="a6ec4-788">JET_errTransReadOnly</span></span><br />
<span data-ttu-id="a6ec4-789">-1110</span><span class="sxs-lookup"><span data-stu-id="a6ec4-789">-1110</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-790">Uma transação somente leitura tentou modificar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-790">A read-only transaction tried to modify the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-791">JET_errSessionWriteConflict</span><span class="sxs-lookup"><span data-stu-id="a6ec4-791">JET_errSessionWriteConflict</span></span><br />
<span data-ttu-id="a6ec4-792">-1111</span><span class="sxs-lookup"><span data-stu-id="a6ec4-792">-1111</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-793">Houve uma tentativa de substituir o mesmo registro por dois cursores diferentes na mesma sessão.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-793">There was an attempt to replace the same record by two different cursors in the same session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-794">JET_errRecordTooBigForBackwardCompatibility</span><span class="sxs-lookup"><span data-stu-id="a6ec4-794">JET_errRecordTooBigForBackwardCompatibility</span></span><br />
<span data-ttu-id="a6ec4-795">-1112</span><span class="sxs-lookup"><span data-stu-id="a6ec4-795">-1112</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-796">O registro será muito grande se for representado em um formato de banco de dados de uma versão anterior do Jet.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-796">The record would be too big if represented in a database format from a previous version of Jet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-797">JET_errCannotMaterializeForwardOnlySort</span><span class="sxs-lookup"><span data-stu-id="a6ec4-797">JET_errCannotMaterializeForwardOnlySort</span></span><br />
<span data-ttu-id="a6ec4-798">-1113</span><span class="sxs-lookup"><span data-stu-id="a6ec4-798">-1113</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-799">Não foi possível criar a tabela temporária devido a parâmetros que entram em conflito com JET_bitTTForwardOnly.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-799">The temporary table could not be created due to parameters that conflict with JET_bitTTForwardOnly.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-800">JET_errSesidTableIdMismatch</span><span class="sxs-lookup"><span data-stu-id="a6ec4-800">JET_errSesidTableIdMismatch</span></span><br />
<span data-ttu-id="a6ec4-801">-1114</span><span class="sxs-lookup"><span data-stu-id="a6ec4-801">-1114</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-802">O identificador de sessão não pode ser usado com a ID de tabela porque não foi usado para criá-lo.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-802">The session handle cannot be used with the table id because it was not used to create it.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-803">JET_errInvalidInstance</span><span class="sxs-lookup"><span data-stu-id="a6ec4-803">JET_errInvalidInstance</span></span><br />
<span data-ttu-id="a6ec4-804">-1115</span><span class="sxs-lookup"><span data-stu-id="a6ec4-804">-1115</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-805">O identificador de instância é inválido ou se refere a uma instância que foi desligada.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-805">The instance handle is invalid or refers to an instance that has been shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-806">JET_errReadLostFlushVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="a6ec4-806">JET_errReadLostFlushVerifyFailure</span></span><br />
<span data-ttu-id="a6ec4-807">-1119</span><span class="sxs-lookup"><span data-stu-id="a6ec4-807">-1119</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-808">A página do banco de dados lida no disco tinha uma gravação anterior não representada na página.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-808">The database page read from disk had a previous write not represented on the page.</span></span> <span data-ttu-id="a6ec4-809">Disponível no Windows 8 e posterior para o cliente e o Windows Server 2012 e posterior para o servidor.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-809">Available on Windows 8 and later for client, and Windows Server 2012 and later for server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-810">JET_errDatabaseDuplicate</span><span class="sxs-lookup"><span data-stu-id="a6ec4-810">JET_errDatabaseDuplicate</span></span><br />
<span data-ttu-id="a6ec4-811">-1201</span><span class="sxs-lookup"><span data-stu-id="a6ec4-811">-1201</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-812">O banco de dados já existe.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-812">The database already exists.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-813">JET_errDatabaseInUse</span><span class="sxs-lookup"><span data-stu-id="a6ec4-813">JET_errDatabaseInUse</span></span><br />
<span data-ttu-id="a6ec4-814">-1202</span><span class="sxs-lookup"><span data-stu-id="a6ec4-814">-1202</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-815">O banco de dados em uso.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-815">The database in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-816">JET_errDatabaseNotFound</span><span class="sxs-lookup"><span data-stu-id="a6ec4-816">JET_errDatabaseNotFound</span></span><br />
<span data-ttu-id="a6ec4-817">-1203</span><span class="sxs-lookup"><span data-stu-id="a6ec4-817">-1203</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-818">Não há nenhum banco de dados desse tipo.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-818">There is no such database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-819">JET_errDatabaseInvalidName</span><span class="sxs-lookup"><span data-stu-id="a6ec4-819">JET_errDatabaseInvalidName</span></span><br />
<span data-ttu-id="a6ec4-820">-1204</span><span class="sxs-lookup"><span data-stu-id="a6ec4-820">-1204</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-821">O nome do banco de dados é inválido.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-821">The database name is invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-822">JET_errDatabaseInvalidPages</span><span class="sxs-lookup"><span data-stu-id="a6ec4-822">JET_errDatabaseInvalidPages</span></span><br />
<span data-ttu-id="a6ec4-823">-1205</span><span class="sxs-lookup"><span data-stu-id="a6ec4-823">-1205</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-824">Há um número inválido de páginas.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-824">There are an invalid number of pages.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-825">JET_errDatabaseCorrupted</span><span class="sxs-lookup"><span data-stu-id="a6ec4-825">JET_errDatabaseCorrupted</span></span><br />
<span data-ttu-id="a6ec4-826">-1206</span><span class="sxs-lookup"><span data-stu-id="a6ec4-826">-1206</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-827">Há um arquivo que não é de banco de dados ou um banco de dados corrompido.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-827">There is a non-database file or corrupt database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-828">JET_errDatabaseLocked</span><span class="sxs-lookup"><span data-stu-id="a6ec4-828">JET_errDatabaseLocked</span></span><br />
<span data-ttu-id="a6ec4-829">-1207</span><span class="sxs-lookup"><span data-stu-id="a6ec4-829">-1207</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-830">O banco de dados está bloqueado exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-830">The database is exclusively locked.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-831">JET_errCannotDisableVersioning</span><span class="sxs-lookup"><span data-stu-id="a6ec4-831">JET_errCannotDisableVersioning</span></span><br />
<span data-ttu-id="a6ec4-832">-1208</span><span class="sxs-lookup"><span data-stu-id="a6ec4-832">-1208</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-833">O controle de versão deste banco de dados não pode ser desabilitado.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-833">The versioning for this database cannot be disabled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-834">JET_errInvalidDatabaseVersion</span><span class="sxs-lookup"><span data-stu-id="a6ec4-834">JET_errInvalidDatabaseVersion</span></span><br />
<span data-ttu-id="a6ec4-835">-1209</span><span class="sxs-lookup"><span data-stu-id="a6ec4-835">-1209</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-836">O mecanismo de banco de dados é incompatível com o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-836">The database engine is incompatible with the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-837">JET_errDatabase200Format</span><span class="sxs-lookup"><span data-stu-id="a6ec4-837">JET_errDatabase200Format</span></span><br />
<span data-ttu-id="a6ec4-838">-1210</span><span class="sxs-lookup"><span data-stu-id="a6ec4-838">-1210</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-839">O banco de dados está em um formato mais antigo (200).</span><span class="sxs-lookup"><span data-stu-id="a6ec4-839">The database is in an older (200) format.</span></span> <span data-ttu-id="a6ec4-840">Esse erro será retornado por <a href="gg294068(v=exchg.10).md">JetInit</a> se <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> estiver definido.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-840">This error is returned by <a href="gg294068(v=exchg.10).md">JetInit</a> if <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> is set.</span></span> <span data-ttu-id="a6ec4-841">Somente Windows NT Client.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-841">Windows NT client only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-842">JET_errDatabase400Format</span><span class="sxs-lookup"><span data-stu-id="a6ec4-842">JET_errDatabase400Format</span></span><br />
<span data-ttu-id="a6ec4-843">-1211</span><span class="sxs-lookup"><span data-stu-id="a6ec4-843">-1211</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-844">O banco de dados está em um formato mais antigo (400).</span><span class="sxs-lookup"><span data-stu-id="a6ec4-844">The database is in an older (400) format.</span></span> <span data-ttu-id="a6ec4-845">Esse erro será retornado por <a href="gg294068(v=exchg.10).md">JetInit</a> se <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> estiver definido.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-845">This error is returned by <a href="gg294068(v=exchg.10).md">JetInit</a> if <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> is set.</span></span> <span data-ttu-id="a6ec4-846">Somente Windows NT Client.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-846">Windows NT client only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-847">JET_errDatabase500Format</span><span class="sxs-lookup"><span data-stu-id="a6ec4-847">JET_errDatabase500Format</span></span><br />
<span data-ttu-id="a6ec4-848">-1212</span><span class="sxs-lookup"><span data-stu-id="a6ec4-848">-1212</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-849">O banco de dados está em um formato mais antigo (500).</span><span class="sxs-lookup"><span data-stu-id="a6ec4-849">The database is in an older (500) format.</span></span> <span data-ttu-id="a6ec4-850">Esse erro será retornado por <a href="gg294068(v=exchg.10).md">JetInit</a> se <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> estiver definido.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-850">This error is returned by <a href="gg294068(v=exchg.10).md">JetInit</a> if <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> is set.</span></span> <span data-ttu-id="a6ec4-851">Somente Windows NT Client.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-851">Windows NT client only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-852">JET_errPageSizeMismatch</span><span class="sxs-lookup"><span data-stu-id="a6ec4-852">JET_errPageSizeMismatch</span></span><br />
<span data-ttu-id="a6ec4-853">-1213</span><span class="sxs-lookup"><span data-stu-id="a6ec4-853">-1213</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-854">O tamanho da página do banco de dados não corresponde ao mecanismo.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-854">The database page size does not match the engine.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-855">JET_errTooManyInstances</span><span class="sxs-lookup"><span data-stu-id="a6ec4-855">JET_errTooManyInstances</span></span><br />
<span data-ttu-id="a6ec4-856">-1214</span><span class="sxs-lookup"><span data-stu-id="a6ec4-856">-1214</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-857">Não é possível iniciar mais instâncias de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-857">No more database instances can be started.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-858">JET_errDatabaseSharingViolation</span><span class="sxs-lookup"><span data-stu-id="a6ec4-858">JET_errDatabaseSharingViolation</span></span><br />
<span data-ttu-id="a6ec4-859">-1215</span><span class="sxs-lookup"><span data-stu-id="a6ec4-859">-1215</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-860">Uma instância de banco de dados diferente está usando este banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-860">A different database instance is using this database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-861">JET_errAttachedDatabaseMismatch</span><span class="sxs-lookup"><span data-stu-id="a6ec4-861">JET_errAttachedDatabaseMismatch</span></span><br />
<span data-ttu-id="a6ec4-862">-1216</span><span class="sxs-lookup"><span data-stu-id="a6ec4-862">-1216</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-863">Um anexo de banco de dados pendente foi detectado no início ou no fim da recuperação, mas o banco de dados está ausente ou não corresponde às informações de anexo.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-863">An outstanding database attachment has been detected at the start or end of the recovery, but the database is missing or does not match attachment info.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-864">JET_errDatabaseInvalidPath</span><span class="sxs-lookup"><span data-stu-id="a6ec4-864">JET_errDatabaseInvalidPath</span></span><br />
<span data-ttu-id="a6ec4-865">-1217</span><span class="sxs-lookup"><span data-stu-id="a6ec4-865">-1217</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-866">O caminho especificado para o arquivo de banco de dados é inválido.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-866">The specified path to the database file is illegal.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-867">JET_errDatabaseIdInUse</span><span class="sxs-lookup"><span data-stu-id="a6ec4-867">JET_errDatabaseIdInUse</span></span><br />
<span data-ttu-id="a6ec4-868">-1218</span><span class="sxs-lookup"><span data-stu-id="a6ec4-868">-1218</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-869">Um banco de dados está sendo atribuído a uma ID que já está em uso.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-869">A database is being assigned an ID that is already in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-870">JET_errForceDetachNotAllowed</span><span class="sxs-lookup"><span data-stu-id="a6ec4-870">JET_errForceDetachNotAllowed</span></span><br />
<span data-ttu-id="a6ec4-871">-1219</span><span class="sxs-lookup"><span data-stu-id="a6ec4-871">-1219</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-872">A desanexação forçada só é permitida depois que a desanexação normal foi interrompida devido a um erro.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-872">The force detach is allowed only after the normal detach was stopped due to an error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-873">JET_errCatalogCorrupted</span><span class="sxs-lookup"><span data-stu-id="a6ec4-873">JET_errCatalogCorrupted</span></span><br />
<span data-ttu-id="a6ec4-874">-1220</span><span class="sxs-lookup"><span data-stu-id="a6ec4-874">-1220</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-875">Corrupção detectada no catálogo.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-875">Corruption was detected in the catalog.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-876">JET_errPartiallyAttachedDB</span><span class="sxs-lookup"><span data-stu-id="a6ec4-876">JET_errPartiallyAttachedDB</span></span><br />
<span data-ttu-id="a6ec4-877">-1221</span><span class="sxs-lookup"><span data-stu-id="a6ec4-877">-1221</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-878">O banco de dados está parcialmente anexado e a operação de anexação não pode ser concluída.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-878">The database is only partially attached and the attach operation cannot be completed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-879">JET_errDatabaseSignInUse</span><span class="sxs-lookup"><span data-stu-id="a6ec4-879">JET_errDatabaseSignInUse</span></span><br />
<span data-ttu-id="a6ec4-880">-1222</span><span class="sxs-lookup"><span data-stu-id="a6ec4-880">-1222</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-881">O banco de dados com a mesma assinatura já está em uso.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-881">The database with the same signature is already in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-882">JET_errDatabaseCorruptedNoRepair</span><span class="sxs-lookup"><span data-stu-id="a6ec4-882">JET_errDatabaseCorruptedNoRepair</span></span><br />
<span data-ttu-id="a6ec4-883">-1224</span><span class="sxs-lookup"><span data-stu-id="a6ec4-883">-1224</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-884">O banco de dados está corrompido, mas não é permitido um reparo.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-884">The database is corrupted but a repair is not allowed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-885">JET_errInvalidCreateDbVersion</span><span class="sxs-lookup"><span data-stu-id="a6ec4-885">JET_errInvalidCreateDbVersion</span></span><br />
<span data-ttu-id="a6ec4-886">-1225</span><span class="sxs-lookup"><span data-stu-id="a6ec4-886">-1225</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-887">O mecanismo de banco de dados tentou reproduzir uma operação criar banco de dados do log de transações, mas falhou devido a uma versão incompatível da operação.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-887">The database engine attempted to replay a Create Database operation from the transaction log but failed due to an incompatible version of that operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-888">JET_errTableLocked</span><span class="sxs-lookup"><span data-stu-id="a6ec4-888">JET_errTableLocked</span></span><br />
<span data-ttu-id="a6ec4-889">-1302</span><span class="sxs-lookup"><span data-stu-id="a6ec4-889">-1302</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-890">A tabela está bloqueada exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-890">The table is exclusively locked.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-891">JET_errTableDuplicate</span><span class="sxs-lookup"><span data-stu-id="a6ec4-891">JET_errTableDuplicate</span></span><br />
<span data-ttu-id="a6ec4-892">-1303</span><span class="sxs-lookup"><span data-stu-id="a6ec4-892">-1303</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-893">A tabela já existe.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-893">The table already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-894">JET_errTableInUse</span><span class="sxs-lookup"><span data-stu-id="a6ec4-894">JET_errTableInUse</span></span><br />
<span data-ttu-id="a6ec4-895">-1304</span><span class="sxs-lookup"><span data-stu-id="a6ec4-895">-1304</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-896">A tabela está em uso e não pode ser bloqueada.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-896">The table is in use and cannot be locked.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-897">JET_errObjectNotFound</span><span class="sxs-lookup"><span data-stu-id="a6ec4-897">JET_errObjectNotFound</span></span><br />
<span data-ttu-id="a6ec4-898">-1305</span><span class="sxs-lookup"><span data-stu-id="a6ec4-898">-1305</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-899">Não há essa tabela ou objeto.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-899">There is no such table or object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-900">JET_errDensityInvalid</span><span class="sxs-lookup"><span data-stu-id="a6ec4-900">JET_errDensityInvalid</span></span><br />
<span data-ttu-id="a6ec4-901">-1307</span><span class="sxs-lookup"><span data-stu-id="a6ec4-901">-1307</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-902">Há um arquivo ou uma densidade de índice inválidos.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-902">There is a bad file or index density.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-903">JET_errTableNotEmpty</span><span class="sxs-lookup"><span data-stu-id="a6ec4-903">JET_errTableNotEmpty</span></span><br />
<span data-ttu-id="a6ec4-904">-1308</span><span class="sxs-lookup"><span data-stu-id="a6ec4-904">-1308</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-905">A tabela não está vazia.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-905">The table is not empty.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-906">JET_errInvalidTableId</span><span class="sxs-lookup"><span data-stu-id="a6ec4-906">JET_errInvalidTableId</span></span><br />
<span data-ttu-id="a6ec4-907">-1310</span><span class="sxs-lookup"><span data-stu-id="a6ec4-907">-1310</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-908">A ID da tabela é inválida.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-908">The table ID is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-909">JET_errTooManyOpenTables</span><span class="sxs-lookup"><span data-stu-id="a6ec4-909">JET_errTooManyOpenTables</span></span><br />
<span data-ttu-id="a6ec4-910">-1311</span><span class="sxs-lookup"><span data-stu-id="a6ec4-910">-1311</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-911">Não é possível abrir mais tabelas, mesmo após a execução da tarefa de limpeza interna.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-911">No more tables can be opened, even after the internal cleanup task has run.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-912">JET_errIllegalOperation</span><span class="sxs-lookup"><span data-stu-id="a6ec4-912">JET_errIllegalOperation</span></span><br />
<span data-ttu-id="a6ec4-913">-1312</span><span class="sxs-lookup"><span data-stu-id="a6ec4-913">-1312</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-914">Não há suporte para a operação na tabela.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-914">The operation is not supported on the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-915">JET_errTooManyOpenTablesAndCleanupTimedOut</span><span class="sxs-lookup"><span data-stu-id="a6ec4-915">JET_errTooManyOpenTablesAndCleanupTimedOut</span></span><br />
<span data-ttu-id="a6ec4-916">-1313</span><span class="sxs-lookup"><span data-stu-id="a6ec4-916">-1313</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-917">Não é possível abrir mais tabelas porque a tentativa de limpeza não foi concluída.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-917">No more tables can be opened because the cleanup attempt failed to complete.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-918">JET_errObjectDuplicate</span><span class="sxs-lookup"><span data-stu-id="a6ec4-918">JET_errObjectDuplicate</span></span><br />
<span data-ttu-id="a6ec4-919">-1314</span><span class="sxs-lookup"><span data-stu-id="a6ec4-919">-1314</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-920">O nome da tabela ou do objeto está em uso.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-920">The table or object name is in use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-921">JET_errInvalidObject</span><span class="sxs-lookup"><span data-stu-id="a6ec4-921">JET_errInvalidObject</span></span><br />
<span data-ttu-id="a6ec4-922">-1316</span><span class="sxs-lookup"><span data-stu-id="a6ec4-922">-1316</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-923">O objeto é inválido para a operação.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-923">The object is invalid for operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-924">JET_errCannotDeleteTempTable</span><span class="sxs-lookup"><span data-stu-id="a6ec4-924">JET_errCannotDeleteTempTable</span></span><br />
<span data-ttu-id="a6ec4-925">-1317</span><span class="sxs-lookup"><span data-stu-id="a6ec4-925">-1317</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-926"><a href="gg294087(v=exchg.10).md">JetCloseTable</a> deve ser usado em vez de <a href="gg294128(v=exchg.10).md">JetDeleteTable</a> para excluir uma tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-926"><a href="gg294087(v=exchg.10).md">JetCloseTable</a> must be used instead of <a href="gg294128(v=exchg.10).md">JetDeleteTable</a> to delete a temporary table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-927">JET_errCannotDeleteSystemTable</span><span class="sxs-lookup"><span data-stu-id="a6ec4-927">JET_errCannotDeleteSystemTable</span></span><br />
<span data-ttu-id="a6ec4-928">-1318</span><span class="sxs-lookup"><span data-stu-id="a6ec4-928">-1318</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-929">Houve uma tentativa inválida de excluir uma tabela do sistema.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-929">There was an illegal attempt to delete a system table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-930">JET_errCannotDeleteTemplateTable</span><span class="sxs-lookup"><span data-stu-id="a6ec4-930">JET_errCannotDeleteTemplateTable</span></span><br />
<span data-ttu-id="a6ec4-931">-1319</span><span class="sxs-lookup"><span data-stu-id="a6ec4-931">-1319</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-932">Houve uma tentativa inválida de excluir uma tabela de modelo.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-932">There was an illegal attempt to delete a template table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-933">JET_errExclusiveTableLockRequired</span><span class="sxs-lookup"><span data-stu-id="a6ec4-933">JET_errExclusiveTableLockRequired</span></span><br />
<span data-ttu-id="a6ec4-934">-1322</span><span class="sxs-lookup"><span data-stu-id="a6ec4-934">-1322</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-935">Deve haver um bloqueio exclusivo na tabela.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-935">There must be an exclusive lock on the table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-936">JET_errFixedDDL</span><span class="sxs-lookup"><span data-stu-id="a6ec4-936">JET_errFixedDDL</span></span><br />
<span data-ttu-id="a6ec4-937">-1323</span><span class="sxs-lookup"><span data-stu-id="a6ec4-937">-1323</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-938">As operações DDL são proibidas nesta tabela.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-938">DDL operations are prohibited on this table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-939">JET_errFixedInheritedDDL</span><span class="sxs-lookup"><span data-stu-id="a6ec4-939">JET_errFixedInheritedDDL</span></span><br />
<span data-ttu-id="a6ec4-940">-1324</span><span class="sxs-lookup"><span data-stu-id="a6ec4-940">-1324</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-941">Em uma tabela derivada, as operações DDL são proibidas na parte herdada do DDL.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-941">On a derived table, DDL operations are prohibited on the inherited portion of the DDL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-942">JET_errCannotNestDDL</span><span class="sxs-lookup"><span data-stu-id="a6ec4-942">JET_errCannotNestDDL</span></span><br />
<span data-ttu-id="a6ec4-943">-1325</span><span class="sxs-lookup"><span data-stu-id="a6ec4-943">-1325</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-944">O aninhamento da DDL hierárquica não tem suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-944">Nesting the hierarchical DDL is not currently supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-945">JET_errDDLNotInheritable</span><span class="sxs-lookup"><span data-stu-id="a6ec4-945">JET_errDDLNotInheritable</span></span><br />
<span data-ttu-id="a6ec4-946">-1326</span><span class="sxs-lookup"><span data-stu-id="a6ec4-946">-1326</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-947">Houve uma tentativa de herdar um DDL de uma tabela que não está marcada como uma tabela de modelo.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-947">There was an attempt to inherit a DDL from a table that is not marked as a template table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-948">JET_errInvalidSettings</span><span class="sxs-lookup"><span data-stu-id="a6ec4-948">JET_errInvalidSettings</span></span><br />
<span data-ttu-id="a6ec4-949">-1328</span><span class="sxs-lookup"><span data-stu-id="a6ec4-949">-1328</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-950">Os parâmetros do sistema foram definidos incorretamente.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-950">The system parameters were set improperly.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-951">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="a6ec4-951">JET_errClientRequestToStopJetService</span></span><br />
<span data-ttu-id="a6ec4-952">-1329</span><span class="sxs-lookup"><span data-stu-id="a6ec4-952">-1329</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-953">O cliente solicitou que o serviço seja interrompido.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-953">The client has requested that the service be stopped.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-954">JET_errCannotAddFixedVarColumnToDerivedTable</span><span class="sxs-lookup"><span data-stu-id="a6ec4-954">JET_errCannotAddFixedVarColumnToDerivedTable</span></span><br />
<span data-ttu-id="a6ec4-955">-1330</span><span class="sxs-lookup"><span data-stu-id="a6ec4-955">-1330</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-956">A tabela de modelo foi criada com o sinalizador NoFixedVarColumnsInDerivedTables definido.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-956">The Template table was created with the NoFixedVarColumnsInDerivedTables flag set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-957">JET_errIndexCantBuild</span><span class="sxs-lookup"><span data-stu-id="a6ec4-957">JET_errIndexCantBuild</span></span><br />
<span data-ttu-id="a6ec4-958">-1401</span><span class="sxs-lookup"><span data-stu-id="a6ec4-958">-1401</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-959">Falha na compilação do índice.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-959">The index build failed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-960">JET_errIndexHasPrimary</span><span class="sxs-lookup"><span data-stu-id="a6ec4-960">JET_errIndexHasPrimary</span></span><br />
<span data-ttu-id="a6ec4-961">-1402</span><span class="sxs-lookup"><span data-stu-id="a6ec4-961">-1402</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-962">O índice primário já está definido.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-962">The primary index is already defined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-963">JET_errIndexDuplicate</span><span class="sxs-lookup"><span data-stu-id="a6ec4-963">JET_errIndexDuplicate</span></span><br />
<span data-ttu-id="a6ec4-964">-1403</span><span class="sxs-lookup"><span data-stu-id="a6ec4-964">-1403</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-965">O índice já está definido.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-965">The index is already defined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-966">JET_errIndexNotFound</span><span class="sxs-lookup"><span data-stu-id="a6ec4-966">JET_errIndexNotFound</span></span><br />
<span data-ttu-id="a6ec4-967">-1404</span><span class="sxs-lookup"><span data-stu-id="a6ec4-967">-1404</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-968">Não há esse índice.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-968">There is no such index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-969">JET_errIndexMustStay</span><span class="sxs-lookup"><span data-stu-id="a6ec4-969">JET_errIndexMustStay</span></span><br />
<span data-ttu-id="a6ec4-970">-1405</span><span class="sxs-lookup"><span data-stu-id="a6ec4-970">-1405</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-971">O índice clusterizado não pode ser excluído.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-971">The clustered index cannot be deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-972">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="a6ec4-972">JET_errIndexInvalidDef</span></span><br />
<span data-ttu-id="a6ec4-973">-1406</span><span class="sxs-lookup"><span data-stu-id="a6ec4-973">-1406</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-974">A definição do índice é inválida.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-974">The index definition is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-975">JET_errInvalidCreateIndex</span><span class="sxs-lookup"><span data-stu-id="a6ec4-975">JET_errInvalidCreateIndex</span></span><br />
<span data-ttu-id="a6ec4-976">-1409</span><span class="sxs-lookup"><span data-stu-id="a6ec4-976">-1409</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-977">A criação da descrição do índice era inválida.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-977">The creation of the index description was invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-978">JET_errTooManyOpenIndexes</span><span class="sxs-lookup"><span data-stu-id="a6ec4-978">JET_errTooManyOpenIndexes</span></span><br />
<span data-ttu-id="a6ec4-979">-1410</span><span class="sxs-lookup"><span data-stu-id="a6ec4-979">-1410</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-980">O banco de dados está sem blocos de descrição de índice.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-980">The database is out of index description blocks.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-981">JET_errMultiValuedIndexViolation</span><span class="sxs-lookup"><span data-stu-id="a6ec4-981">JET_errMultiValuedIndexViolation</span></span><br />
<span data-ttu-id="a6ec4-982">-1411</span><span class="sxs-lookup"><span data-stu-id="a6ec4-982">-1411</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-983">Chaves de índice entre registros não exclusivas foram geradas para um índice de valores múltiplos.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-983">Non-unique inter-record index keys have been generated for a multi-valued index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-984">JET_errIndexBuildCorrupted</span><span class="sxs-lookup"><span data-stu-id="a6ec4-984">JET_errIndexBuildCorrupted</span></span><br />
<span data-ttu-id="a6ec4-985">-1412</span><span class="sxs-lookup"><span data-stu-id="a6ec4-985">-1412</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-986">Um índice secundário que reflete corretamente o índice primário falhou ao compilar.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-986">A secondary index that properly reflects the primary index failed to build.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-987">JET_errPrimaryIndexCorrupted</span><span class="sxs-lookup"><span data-stu-id="a6ec4-987">JET_errPrimaryIndexCorrupted</span></span><br />
<span data-ttu-id="a6ec4-988">-1413</span><span class="sxs-lookup"><span data-stu-id="a6ec4-988">-1413</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-989">O índice primário está corrompido e o banco de dados deve ser desfragmentado.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-989">The primary index is corrupt and the database must be defragmented.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-990">JET_errSecondaryIndexCorrupted</span><span class="sxs-lookup"><span data-stu-id="a6ec4-990">JET_errSecondaryIndexCorrupted</span></span><br />
<span data-ttu-id="a6ec4-991">-1414</span><span class="sxs-lookup"><span data-stu-id="a6ec4-991">-1414</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-992">O índice secundário está corrompido e o banco de dados deve ser desfragmentado.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-992">The secondary index is corrupt and the database must be defragmented.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-993">JET_errInvalidIndexId</span><span class="sxs-lookup"><span data-stu-id="a6ec4-993">JET_errInvalidIndexId</span></span><br />
<span data-ttu-id="a6ec4-994">-1416</span><span class="sxs-lookup"><span data-stu-id="a6ec4-994">-1416</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-995">A ID do índice é inválida.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-995">The index ID is invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-996">JET_errIndexTuplesSecondaryIndexOnly</span><span class="sxs-lookup"><span data-stu-id="a6ec4-996">JET_errIndexTuplesSecondaryIndexOnly</span></span><br />
<span data-ttu-id="a6ec4-997">-1430</span><span class="sxs-lookup"><span data-stu-id="a6ec4-997">-1430</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-998">O índice de tupla só pode ser definido em um índice secundário.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-998">The tuple index can only be set on a secondary index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-999">JET_errIndexTuplesTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="a6ec4-999">JET_errIndexTuplesTooManyColumns</span></span><br />
<span data-ttu-id="a6ec4-1000">-1431</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1000">-1431</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1001">A definição de índice para o índice de tupla contém mais colunas de chave às quais o mecanismo de banco de dados pode dar suporte.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1001">The index definition for the tuple index contains more key columns that the database engine can support.</span></span></p>
<p><span data-ttu-id="a6ec4-1002"><strong>Observação  </strong> O erro de JET_errIndexTuplesOneColumnOnly é obsoleto e foi substituído por JET_errIndexTuplesTooManyColumns.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1002"><strong>Note  </strong>The JET_errIndexTuplesOneColumnOnly error is obsolete and has been replaced by JET_errIndexTuplesTooManyColumns.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-1003">JET_errIndexTuplesNonUniqueOnly</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1003">JET_errIndexTuplesNonUniqueOnly</span></span><br />
<span data-ttu-id="a6ec4-1004">-1432</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1004">-1432</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1005">O índice de tupla deve ser um índice não exclusivo.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1005">The tuple index must be a non-unique index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-1006">JET_errIndexTuplesTextBinaryColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1006">JET_errIndexTuplesTextBinaryColumnsOnly</span></span><br />
<span data-ttu-id="a6ec4-1007">-1433</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1007">-1433</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1008">Uma definição de índice de tupla só pode conter colunas de chave que têm tipos de texto ou de coluna binária.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1008">A tuple index definition can only contain key columns that have text or binary column types.</span></span></p>
<p><span data-ttu-id="a6ec4-1009"><strong>Observação  </strong> O erro de JET_errIndexTuplesTextColumnsOnly é obsoleto e foi substituído por JET_errIndexTuplesTextBinaryColumnsOnly.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1009"><strong>Note  </strong>The JET_errIndexTuplesTextColumnsOnly error is obsolete and has been replaced by JET_errIndexTuplesTextBinaryColumnsOnly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-1010">JET_errIndexTuplesVarSegMacNotAllowed</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1010">JET_errIndexTuplesVarSegMacNotAllowed</span></span><br />
<span data-ttu-id="a6ec4-1011">-1434</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1011">-1434</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1012">O índice de tupla não permite a configuração de cbVarSegMac.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1012">The tuple index does not allow setting cbVarSegMac.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-1013">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1013">JET_errIndexTuplesInvalidLimits</span></span><br />
<span data-ttu-id="a6ec4-1014">-1435</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1014">-1435</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1015">O comprimento mínimo/máximo da tupla ou o número máximo de caracteres especificado para um índice são inválidos.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1015">The minimum/maximum tuple length or the maximum number of characters that are specified for an index are invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-1016">JET_errIndexTuplesCannotRetrieveFromIndex</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1016">JET_errIndexTuplesCannotRetrieveFromIndex</span></span><br />
<span data-ttu-id="a6ec4-1017">-1436</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1017">-1436</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1018"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> não pode ser chamado com o sinalizador JET_bitRetrieveFromIndex definido ao recuperar uma coluna em um índice de tupla.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1018"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> cannot be called with the JET_bitRetrieveFromIndex flag set while retrieving a column on a tuple index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-1019">JET_errIndexTuplesKeyTooSmall</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1019">JET_errIndexTuplesKeyTooSmall</span></span><br />
<span data-ttu-id="a6ec4-1020">-1437</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1020">-1437</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1021">A chave especificada não atende ao comprimento mínimo da tupla.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1021">The specified key does not meet the minimum tuple length.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-1022">JET_errColumnLong</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1022">JET_errColumnLong</span></span><br />
<span data-ttu-id="a6ec4-1023">-1501</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1023">-1501</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1024">O valor da coluna é longo.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1024">The column value is long.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-1025">JET_errColumnNoChunk</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1025">JET_errColumnNoChunk</span></span><br />
<span data-ttu-id="a6ec4-1026">-1502</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1026">-1502</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1027">Não há nenhuma parte desse tipo em um valor longo.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1027">There is no such chunk in a long value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-1028">JET_errColumnDoesNotFit</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1028">JET_errColumnDoesNotFit</span></span><br />
<span data-ttu-id="a6ec4-1029">-1503</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1029">-1503</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1030">O campo não será ajustado no registro.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1030">The field will not fit in the record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-1031">JET_errNullInvalid</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1031">JET_errNullInvalid</span></span><br />
<span data-ttu-id="a6ec4-1032">-1504</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1032">-1504</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1033">NULL não é válido.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1033">Null is not valid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-1034">JET_errColumnIllegalNull</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1034">JET_errColumnIllegalNull</span></span><br />
<span data-ttu-id="a6ec4-1035">JET_errNullInvalid</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1035">JET_errNullInvalid</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1036">NULL não é válido.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1036">Null is not valid.</span></span> <span data-ttu-id="a6ec4-1037">Esse erro é retornado pelo Gerenciador de registros.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1037">This error is returned by the record manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-1038">JET_errColumnIndexed-1505</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1038">JET_errColumnIndexed -1505</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1039">A coluna está indexada e não pode ser excluída.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1039">The column is indexed and cannot be deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-1040">JET_errColumnTooBig-1506</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1040">JET_errColumnTooBig -1506</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1041">O tamanho do campo é maior que o comprimento máximo permitido.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1041">The field length is greater than maximum allowed length.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-1042">JET_errColumnNotFound-1507</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1042">JET_errColumnNotFound -1507</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1043">Não há nenhuma coluna.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1043">There is no such column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-1044">JET_errColumnDuplicate-1508</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1044">JET_errColumnDuplicate -1508</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1045">Este campo já está definido.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1045">This field is already defined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-1046">JET_errMultiValuedColumnMustBeTagged-1509</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1046">JET_errMultiValuedColumnMustBeTagged -1509</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1047">Foi feita uma tentativa de criar uma coluna com vários valores, mas a coluna não estava marcada.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1047">An attempt was made to create a multi-valued column, but the column was not tagged.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-1048">JET_errColumnRedundant-1510</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1048">JET_errColumnRedundant -1510</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1049">Houve uma segunda coluna de versão ou incremento automático.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1049">There was a second auto-increment or version column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-1050">JET_errInvalidColumnType-1511</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1050">JET_errInvalidColumnType -1511</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1051">O tipo de dados da coluna é inválido.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1051">The column data type is invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-1052">JET_errTaggedNotNULL-1514</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1052">JET_errTaggedNotNULL -1514</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1053">Não há colunas marcadas não nulas.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1053">There are no non-NULL tagged columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-1054">JET_errNoCurrentIndex-1515</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1054">JET_errNoCurrentIndex -1515</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1055">O banco de dados é inválido porque não contém um índice atual.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1055">The database is invalid because it does not contain a current index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-1056">JET_errKeyIsMade-1516</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1056">JET_errKeyIsMade -1516</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1057">A chave é completamente feita.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1057">The key is completely made.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-1058">JET_errBadColumnId-1517</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1058">JET_errBadColumnId -1517</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1059">A ID da coluna está incorreta.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1059">The column ID is incorrect.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-1060">JET_errBadItagSequence-1518</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1060">JET_errBadItagSequence -1518</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1061">Há um itagSequence inadequado para a coluna marcada.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1061">There is a bad itagSequence for the tagged column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-1062">JET_errColumnInRelationship-1519</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1062">JET_errColumnInRelationship -1519</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1063">Não é possível excluir uma coluna porque ela faz parte de uma relação.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1063">A column cannot be deleted because it is part of a relationship.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-1064">JET_errCannotBeTagged-1521</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1064">JET_errCannotBeTagged -1521</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1065">O incremento automático e a versão não podem ser marcados.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1065">The auto increment and version cannot be tagged.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-1066">JET_errDefaultValueTooBig-1524</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1066">JET_errDefaultValueTooBig -1524</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1067">O valor padrão excede o tamanho máximo.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1067">The default value exceeds the maximum size.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-1068">JET_errMultiValuedDuplicate-1525</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1068">JET_errMultiValuedDuplicate -1525</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1069">Um valor duplicado foi detectado em uma coluna de valores múltiplos exclusiva.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1069">A duplicate value was detected on a unique multi-valued column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-1070">JET_errLVCorrupted-1526</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1070">JET_errLVCorrupted -1526</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1071">Corrupção encontrada em uma árvore de valor longo.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1071">Corruption was encountered in a long-value tree.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-1072">JET_errMultiValuedDuplicateAfterTruncation-1528</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1072">JET_errMultiValuedDuplicateAfterTruncation -1528</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1073">Um valor duplicado foi detectado em uma coluna com vários valores exclusivos depois que os dados foram normalizados e está normalizando truncamento dos dados antes da comparação.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1073">A duplicate value was detected on a unique multi-valued column after the data was normalized, and it is normalizing truncated the data before comparison.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-1074">JET_errDerivedColumnCorruption-1529</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1074">JET_errDerivedColumnCorruption -1529</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1075">Há uma coluna inválida na tabela derivada.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1075">There is an invalid column in derived table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-1076">JET_errInvalidPlaceholderColumn-1530</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1076">JET_errInvalidPlaceholderColumn -1530</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1077">Foi feita uma tentativa de converter uma coluna em um espaço reservado de índice primário, mas a coluna não atende aos critérios necessários.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1077">An attempt was made to convert a column to a primary index placeholder, but the column does not meet the necessary criteria.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-1078">JET_errRecordNotFound-1601</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1078">JET_errRecordNotFound -1601</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1079">A chave não foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1079">The key was not found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-1080">JET_errRecordNoCopy-1602</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1080">JET_errRecordNoCopy -1602</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1081">Não há um buffer de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1081">There is no working buffer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-1082">JET_errNoCurrentRecord-1603</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1082">JET_errNoCurrentRecord -1603</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1083">Não há nenhum registro atual.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1083">There is no current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-1084">JET_errRecordPrimaryChanged-1604</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1084">JET_errRecordPrimaryChanged -1604</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1085">A chave primária pode não ser alterada.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1085">The primary key might not change.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-1086">JET_errKeyDuplicate-1605</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1086">JET_errKeyDuplicate -1605</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1087">Há uma chave duplicada ilegal.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1087">There is an illegal duplicate key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-1088">JET_errAlreadyPrepared-1607</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1088">JET_errAlreadyPrepared -1607</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1089">Foi feita uma tentativa de atualizar um registro enquanto uma atualização de registro já estava em andamento.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1089">An attempt was made to update a record while a record update was already in progress.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-1090">JET_errKeyNotMade-1608</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1090">JET_errKeyNotMade -1608</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1091">Não foi feita uma chamada para <a href="gg269329(v=exchg.10).md">JetMakeKey</a>.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1091">A call was not made to <a href="gg269329(v=exchg.10).md">JetMakeKey</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-1092">JET_errUpdateNotPrepared-1609</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1092">JET_errUpdateNotPrepared -1609</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1093">Não foi feita uma chamada para <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1093">A call was not made to <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-1094">JET_errDataHasChanged-1611</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1094">JET_errDataHasChanged -1611</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1095">Os dados foram alterados e a operação foi anulada.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1095">The data has changed and the operation was aborted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-1096">JET_errLanguageNotSupported-1619</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1096">JET_errLanguageNotSupported -1619</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1097">Esta instalação do Windows não oferece suporte ao idioma selecionado.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1097">This Windows installation does not support the selected language.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-1098">JET_errTooManySorts-1701</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1098">JET_errTooManySorts -1701</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1099">Há muitos processos de classificação.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1099">There are too many sort processes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-1100">JET_errInvalidOnSort-1702</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1100">JET_errInvalidOnSort -1702</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1101">Ocorreu uma operação inválida durante uma classificação.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1101">An invalid operation occurred during a sort.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-1102">JET_errTempFileOpenError-1803</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1102">JET_errTempFileOpenError -1803</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1103">Não foi possível abrir o arquivo temporário.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1103">The temporary file could not be opened.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-1104">JET_errTooManyAttachedDatabases-1805</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1104">JET_errTooManyAttachedDatabases -1805</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1105">Um número excessivo de bancos de dados está aberto.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1105">Too many databases are open.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-1106">JET_errDiskFull-1808</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1106">JET_errDiskFull -1808</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1107">Não há espaço restante no disco.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1107">There is no space left on disk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-1108">JET_errPermissionDenied-1809</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1108">JET_errPermissionDenied -1809</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1109">Permissão negada.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1109">Permission is denied.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-1110">JET_errFileNotFound-1811</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1110">JET_errFileNotFound -1811</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1111">O arquivo não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1111">The file was not found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-1112">JET_errFileInvalidType-1812</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1112">JET_errFileInvalidType -1812</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1113">O tipo de arquivo é inválido.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1113">The file type is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-1114">JET_errAfterInitialization-1850</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1114">JET_errAfterInitialization -1850</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1115">Uma restauração não pode ser iniciada após a inicialização.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1115">A restore cannot be started after initialization.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-1116">JET_errLogCorrupted-1852</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1116">JET_errLogCorrupted -1852</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1117">Não foi possível interpretar os logs.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1117">The logs could not be interpreted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-1118">JET_errInvalidOperation-1906</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1118">JET_errInvalidOperation -1906</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1119">A operação é inválida.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1119">The operation is invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-1120">JET_errAccessDenied-1907</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1120">JET_errAccessDenied -1907</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1121">O acesso foi negado.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1121">Access is denied.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-1122">JET_errTooManySplits-1909</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1122">JET_errTooManySplits -1909</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1123">Uma divisão infinita.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1123">An infinite split.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-1124">JET_errSessionSharingViolation-1910</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1124">JET_errSessionSharingViolation -1910</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1125">Vários threads estão usando a mesma sessão.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1125">Multiple threads are using the same session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-1126">JET_errEntryPointNotFound-1911</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1126">JET_errEntryPointNotFound -1911</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1127">Não foi possível encontrar um ponto de entrada em uma DLL necessária.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1127">An entry point in a required DLL could not be found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-1128">JET_errSessionContextAlreadySet-1912</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1128">JET_errSessionContextAlreadySet -1912</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1129">A sessão especificada já tem um contexto de sessão definido.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1129">The specified session already has a session context set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-1130">JET_errSessionContextNotSetByThisThread-1913</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1130">JET_errSessionContextNotSetByThisThread -1913</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1131">Foi feita uma tentativa de redefinir o contexto da sessão, mas o thread atual não era o original que definiu o contexto da sessão.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1131">An attempt was made to reset the session context, but the current thread was not the original one that set the session context.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-1132">JET_errSessionInUse-1914</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1132">JET_errSessionInUse -1914</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1133">Foi feita uma tentativa de encerrar a sessão em uso no momento.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1133">An attempt was made to terminate the session currently in use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-1134">JET_errRecordFormatConversionFailed-1915</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1134">JET_errRecordFormatConversionFailed -1915</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1135">Ocorreu um erro interno durante uma conversão de formato de registro dinâmico.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1135">An internal error occurred during a dynamic record format conversion.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-1136">JET_errOneDatabasePerSession-1916</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1136">JET_errOneDatabasePerSession -1916</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1137">Somente um banco de dados de usuário aberto por sessão é permitido (conforme indicado pela configuração do sinalizador de <a href="gg269337(v=exchg.10).md">JET_paramOneDatabasePerSession</a> durante a criação do banco de dados).</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1137">Only one open user database per session is allowed (as indicated by setting the <a href="gg269337(v=exchg.10).md">JET_paramOneDatabasePerSession</a> flag during database creation).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-1138">JET_errRollbackError-1917</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1138">JET_errRollbackError -1917</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1139">Ocorreu um erro durante a reversão.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1139">There was an error during rollback.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-1140">JET_errCallbackFailed-2101</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1140">JET_errCallbackFailed -2101</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1141">Falha em uma chamada de função de retorno.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1141">A callback function call failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-1142">JET_errCallbackNotResolved-2102</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1142">JET_errCallbackNotResolved -2102</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1143">Não foi possível encontrar uma função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1143">A callback function could not be found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-1144">JET_errOSSnapshotInvalidSequence-2401</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1144">JET_errOSSnapshotInvalidSequence -2401</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1145">A API de cópia de sombra do sistema operacional foi usada em uma sequência inválida.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1145">The operating system shadow copy API was used in an invalid sequence.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-1146">JET_errOSSnapshotTimeOut-2402</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1146">JET_errOSSnapshotTimeOut -2402</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1147">A cópia de sombra do sistema operacional terminou com um tempo limite.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1147">The operating system shadow copy ended with a time-out.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-1148">JET_errOSSnapshotNotAllowed-2403</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1148">JET_errOSSnapshotNotAllowed -2403</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1149">A cópia de sombra do sistema operacional não é permitida porque um backup ou uma recuperação em andamento.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1149">The operating system shadow copy is not allowed because a backup or recovery in is progress.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-1150">JET_errOSSnapshotInvalidSnapId-2404</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1150">JET_errOSSnapshotInvalidSnapId -2404</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1151">A operação falhou porque o identificador de cópia de sombra do sistema operacional especificado era inválido.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1151">The operation failed because the specified operating system shadow copy handle was invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-1152">JET_errLSCallbackNotSpecified-3000</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1152">JET_errLSCallbackNotSpecified -3000</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1153">Foi feita uma tentativa de usar o armazenamento local sem a especificação de uma função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1153">An attempt was made to use local storage without a callback function being specified.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-1154">JET_errLSAlreadySet-3001</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1154">JET_errLSAlreadySet -3001</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1155">Foi feita uma tentativa de definir o armazenamento local para um objeto que já tinha sido definido.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1155">An attempt was made to set the local storage for an object which already had it set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-1156">JET_errLSNotSet-3002</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1156">JET_errLSNotSet -3002</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1157">Foi feita uma tentativa de recuperar o armazenamento local de um objeto que não tinha sido definido.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1157">An attempt was made to retrieve local storage from an object which did not have it set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-1158">JET_errFileIOSparse-4000</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1158">JET_errFileIOSparse -4000</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1159">Uma operação de e/s falhou porque foi tentada em relação a uma região não alocada de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1159">An I/O operation failed because it was attempted against an unallocated region of a file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-1160">JET_errFileIOBeyondEOF-4001</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1160">JET_errFileIOBeyondEOF -4001</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1161">Uma leitura foi emitida para um local além do EOF (as gravações expandirão o arquivo).</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1161">A read was issued to a location beyond the EOF (writes will expand the file).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-1162">JET_errFileIOAbort-4002</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1162">JET_errFileIOAbort -4002</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1163">Esse sinalizador instrui o chamador JET_ABORTRETRYFAILCALLBACK a anular a e/s especificada.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1163">This flag instructs the JET_ABORTRETRYFAILCALLBACK caller to abort the specified I/O.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-1164">JET_errFileIORetry-4003</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1164">JET_errFileIORetry -4003</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1165">Esse sinalizador instrui o chamador JET_ABORTRETRYFAILCALLBACK a repetir a e/s especificada.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1165">This flag instructs the JET_ABORTRETRYFAILCALLBACK caller to retry the specified I/O.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-1166">JET_errFileIOFail-4004</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1166">JET_errFileIOFail -4004</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1167">Esse sinalizador instrui o chamador JET_ABORTRETRYFAILCALLBACK a falhar na e/s especificada.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1167">This flag instructs the JET_ABORTRETRYFAILCALLBACK caller to fail the specified I/O.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-1168">JET_errFileCompressed-4005</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1168">JET_errFileCompressed -4005</span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1169">Não há suporte para acesso de leitura/gravação em arquivos compactados.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1169">Read/write access is not supported on compressed files.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="remarks"></a><span data-ttu-id="a6ec4-1170">Comentários</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1170">Remarks</span></span>

<span data-ttu-id="a6ec4-1171">Em geral, um valor maior que zero deve ser interpretado como um aviso, um valor de zero deve ser interpretado como êxito e um valor menor que zero deve ser interpretado como um erro.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1171">In general, a value that is greater than zero should be interpreted as a warning, a value of zero should be interpreted as success, and a value that is less than zero should be interpreted as an error.</span></span> <span data-ttu-id="a6ec4-1172">Nenhum outro padrão nesses valores, como intervalos de valores, deve ser confiado por um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1172">No other patterns in these values, such as ranges of values, should be relied upon by an application.</span></span>

### <a name="requirements"></a><span data-ttu-id="a6ec4-1173">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1173">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-1174"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="a6ec4-1174"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1175">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1175">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6ec4-1176"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="a6ec4-1176"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1177">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1177">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6ec4-1178"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="a6ec4-1178"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a6ec4-1179">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1179">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="a6ec4-1180">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1180">See Also</span></span>

[<span data-ttu-id="a6ec4-1181">Parâmetros de tratamento de erros</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1181">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="a6ec4-1182">Erros do mecanismo de armazenamento extensível</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1182">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="a6ec4-1183">Arquivos do mecanismo de armazenamento extensível</span><span class="sxs-lookup"><span data-stu-id="a6ec4-1183">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)
