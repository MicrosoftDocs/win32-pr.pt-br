---
description: 'Saiba mais sobre: parâmetros de cache de banco de dados'
title: Parâmetros de cache do banco de dados
TOCTitle: Database Cache Parameters
ms:assetid: 715e5495-0cd8-430f-bf21-509cf03bfbfd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269293(v=EXCHG.10)
ms:contentKeyID: 32765585
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 77d83ea8998da7c00fd294f81b94099d23d524e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765119"
---
# <a name="database-cache-parameters"></a><span data-ttu-id="d35de-103">Parâmetros de cache do banco de dados</span><span class="sxs-lookup"><span data-stu-id="d35de-103">Database Cache Parameters</span></span>


<span data-ttu-id="d35de-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d35de-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="database-cache-parameters"></a><span data-ttu-id="d35de-105">Parâmetros de cache do banco de dados</span><span class="sxs-lookup"><span data-stu-id="d35de-105">Database Cache Parameters</span></span>

<span data-ttu-id="d35de-106">Este tópico contém parâmetros que são usados para o cache de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d35de-106">This topic contains parameters that are used for the database cache.</span></span>

<span data-ttu-id="d35de-107">*JET_paramBatchIOBufferMax*</span><span class="sxs-lookup"><span data-stu-id="d35de-107">*JET_paramBatchIOBufferMax*</span></span>  
<span data-ttu-id="d35de-108">22</span><span class="sxs-lookup"><span data-stu-id="d35de-108">22</span></span>  

<span data-ttu-id="d35de-109">Esse parâmetro controla o tamanho de uma parte auxiliar do cache de página de banco de dados que é usado para simular e/s de dispersão, quando ele não está disponível.</span><span class="sxs-lookup"><span data-stu-id="d35de-109">This parameter controls the size of an auxiliary part of the database page cache that is used to simulate scatter gather I/O when it is otherwise not available.</span></span> <span data-ttu-id="d35de-110">O tamanho está em páginas de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d35de-110">The size is in database pages.</span></span>

<span data-ttu-id="d35de-111">**Windows XP e posterior:**  Esse parâmetro é obsoleto e não afeta a operação do mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d35de-111">**Windows XP and later:**  This parameter is obsolete and does not affect the operation of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d35de-112">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="d35de-112">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="d35de-113">256</span><span class="sxs-lookup"><span data-stu-id="d35de-113">256</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-114">Tipo:</span><span class="sxs-lookup"><span data-stu-id="d35de-114">Type:</span></span></p></td>
<td><p><span data-ttu-id="d35de-115">Integer</span><span class="sxs-lookup"><span data-stu-id="d35de-115">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-116">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="d35de-116">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="d35de-117">0, 2 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="d35de-117">0, 2 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-118">Escopo:</span><span class="sxs-lookup"><span data-stu-id="d35de-118">Scope:</span></span></p></td>
<td><p><span data-ttu-id="d35de-119">Global</span><span class="sxs-lookup"><span data-stu-id="d35de-119">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-120">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="d35de-120">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="d35de-121">No</span><span class="sxs-lookup"><span data-stu-id="d35de-121">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-122">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="d35de-122">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="d35de-123">No</span><span class="sxs-lookup"><span data-stu-id="d35de-123">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-124">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="d35de-124">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="d35de-125">No</span><span class="sxs-lookup"><span data-stu-id="d35de-125">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-126">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="d35de-126">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="d35de-127">No</span><span class="sxs-lookup"><span data-stu-id="d35de-127">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-128">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="d35de-128">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="d35de-129">Yes</span><span class="sxs-lookup"><span data-stu-id="d35de-129">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-130">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="d35de-130">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="d35de-131">Yes</span><span class="sxs-lookup"><span data-stu-id="d35de-131">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-132">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="d35de-132">Availability:</span></span></p></td>
<td><p><span data-ttu-id="d35de-133">Tudo</span><span class="sxs-lookup"><span data-stu-id="d35de-133">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d35de-134">*JET_paramCacheSize*</span><span class="sxs-lookup"><span data-stu-id="d35de-134">*JET_paramCacheSize*</span></span>  
<span data-ttu-id="d35de-135">41</span><span class="sxs-lookup"><span data-stu-id="d35de-135">41</span></span>  

<span data-ttu-id="d35de-136">Esse parâmetro pode ser usado para controlar o tamanho do cache de página do banco de dados em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="d35de-136">This parameter can be used to control the size of the database page cache at run time.</span></span> <span data-ttu-id="d35de-137">Normalmente, o cache ajustará automaticamente seu tamanho como uma função de níveis de atividade de banco de dados e máquina.</span><span class="sxs-lookup"><span data-stu-id="d35de-137">Ordinarily, the cache will automatically tune its size as a function of database and machine activity levels.</span></span> <span data-ttu-id="d35de-138">Se o aplicativo definir esse parâmetro como zero, o cache ajustará seu próprio tamanho dessa maneira.</span><span class="sxs-lookup"><span data-stu-id="d35de-138">If the application sets this parameter to zero, then the cache will tune its own size in this manner.</span></span> <span data-ttu-id="d35de-139">No entanto, se o aplicativo definir esse parâmetro como um valor diferente de zero, o cache se ajustará a esse tamanho de destino (em páginas de banco de dados).</span><span class="sxs-lookup"><span data-stu-id="d35de-139">However, if the application sets this parameter to a non-zero value then the cache will adjust itself to that target size (in database pages).</span></span> <span data-ttu-id="d35de-140">O cache manterá seu tamanho nesse limite até que um novo tamanho seja fornecido ou até que seja liberado para escolher seu próprio tamanho.</span><span class="sxs-lookup"><span data-stu-id="d35de-140">The cache will then hold its size at that threshold until given a new size or until it is released to choose its own size.</span></span>

<span data-ttu-id="d35de-141">**Observação**  O tamanho do cache ainda está sujeito aos limites impostos por **JET_paramCacheSizeMin** e **JET_paramCacheSizeMax**.</span><span class="sxs-lookup"><span data-stu-id="d35de-141">**Note**  The cache size is still subject to the limits imposed by **JET_paramCacheSizeMin** and **JET_paramCacheSizeMax**.</span></span>

<span data-ttu-id="d35de-142">Quando esse parâmetro é lido, o tamanho real do cache nas páginas do banco de dados é retornado.</span><span class="sxs-lookup"><span data-stu-id="d35de-142">When this parameter is read, the actual size of the cache in database pages is returned.</span></span> <span data-ttu-id="d35de-143">Esse tamanho pode ser usado pelo aplicativo como uma entrada para orientar seu ajuste manual do tamanho do cache.</span><span class="sxs-lookup"><span data-stu-id="d35de-143">This size can be used by the application as an input to drive its manual adjustment of the cache size.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d35de-144">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="d35de-144">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="d35de-145">Especial</span><span class="sxs-lookup"><span data-stu-id="d35de-145">Special</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-146">Tipo:</span><span class="sxs-lookup"><span data-stu-id="d35de-146">Type:</span></span></p></td>
<td><p><span data-ttu-id="d35de-147">Integer</span><span class="sxs-lookup"><span data-stu-id="d35de-147">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-148">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="d35de-148">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="d35de-149"><strong>Windows 2000:</strong>  1 a 1048575</span><span class="sxs-lookup"><span data-stu-id="d35de-149"><strong>Windows 2000:</strong>  1 – 1048575</span></span></p>
<p><span data-ttu-id="d35de-150"><strong>Windows XP:</strong>  1 a 4294967295</span><span class="sxs-lookup"><span data-stu-id="d35de-150"><strong>Windows XP:</strong>  1 – 4294967295</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-151">Escopo:</span><span class="sxs-lookup"><span data-stu-id="d35de-151">Scope:</span></span></p></td>
<td><p><span data-ttu-id="d35de-152">Global</span><span class="sxs-lookup"><span data-stu-id="d35de-152">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-153">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="d35de-153">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="d35de-154">Yes</span><span class="sxs-lookup"><span data-stu-id="d35de-154">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-155">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="d35de-155">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="d35de-156">Yes</span><span class="sxs-lookup"><span data-stu-id="d35de-156">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-157">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="d35de-157">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="d35de-158">No</span><span class="sxs-lookup"><span data-stu-id="d35de-158">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-159">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="d35de-159">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="d35de-160">No</span><span class="sxs-lookup"><span data-stu-id="d35de-160">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-161">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="d35de-161">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="d35de-162">Yes</span><span class="sxs-lookup"><span data-stu-id="d35de-162">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-163">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="d35de-163">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="d35de-164">Yes</span><span class="sxs-lookup"><span data-stu-id="d35de-164">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-165">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="d35de-165">Availability:</span></span></p></td>
<td><p><span data-ttu-id="d35de-166">Tudo</span><span class="sxs-lookup"><span data-stu-id="d35de-166">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d35de-167">*JET_paramCacheSizeMin*</span><span class="sxs-lookup"><span data-stu-id="d35de-167">*JET_paramCacheSizeMin*</span></span>  
<span data-ttu-id="d35de-168">60</span><span class="sxs-lookup"><span data-stu-id="d35de-168">60</span></span>  

<span data-ttu-id="d35de-169">Esse parâmetro configura o tamanho mínimo do cache de página do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d35de-169">This parameter configures the minimum size of the database page cache.</span></span> <span data-ttu-id="d35de-170">O tamanho está em páginas de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d35de-170">The size is in database pages.</span></span>

<span data-ttu-id="d35de-171">Por padrão, o cache de banco de dados ajustará automaticamente seu tamanho entre os limites definidos por **JET_paramCacheSizeMin** e **JET_paramCacheSizeMax**.</span><span class="sxs-lookup"><span data-stu-id="d35de-171">By default, the database cache will automatically adjust its size between the limits set by **JET_paramCacheSizeMin** and **JET_paramCacheSizeMax**.</span></span>

<span data-ttu-id="d35de-172">**Windows 2000:**  No Windows 2000, esse parâmetro deve ser definido como um valor aproximadamente igual a quatro vezes o número de threads que estarão dentro da API ESE ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="d35de-172">**Windows 2000:**  On Windows 2000, this parameter should be set to a value roughly equal to four times the number of threads that will be inside the ESE API at the same time.</span></span> <span data-ttu-id="d35de-173">Isso é necessário para evitar deadlocks causados por um número insuficiente de buffers de cache de página de banco de dados para executar operações complexas, como divisões de árvore B +.</span><span class="sxs-lookup"><span data-stu-id="d35de-173">This is required to avoid deadlocks caused by an insufficient number of database page cache buffers to perform complex operations like B+ Tree splits.</span></span>

<span data-ttu-id="d35de-174">**Windows XP e posterior:**  O Gerenciador de cache definirá automaticamente seu próprio tamanho mínimo de cache para evitar deadlocks.</span><span class="sxs-lookup"><span data-stu-id="d35de-174">**Windows XP and later:**  The cache manager will automatically set its own minimum cache size to avoid deadlocks.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d35de-175">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="d35de-175">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="d35de-176"><strong>Windows 2000:</strong>  64</span><span class="sxs-lookup"><span data-stu-id="d35de-176"><strong>Windows 2000:</strong>  64</span></span></p>
<p><span data-ttu-id="d35de-177"><strong>Windows XP:</strong>  1</span><span class="sxs-lookup"><span data-stu-id="d35de-177"><strong>Windows XP:</strong>  1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-178">Tipo:</span><span class="sxs-lookup"><span data-stu-id="d35de-178">Type:</span></span></p></td>
<td><p><span data-ttu-id="d35de-179">Integer</span><span class="sxs-lookup"><span data-stu-id="d35de-179">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-180">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="d35de-180">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="d35de-181"><strong>Windows 2000:</strong>  1 a 1048575</span><span class="sxs-lookup"><span data-stu-id="d35de-181"><strong>Windows 2000:</strong>  1 – 1048575</span></span></p>
<p><span data-ttu-id="d35de-182"><strong>Windows XP:</strong>  1 a 4294967295</span><span class="sxs-lookup"><span data-stu-id="d35de-182"><strong>Windows XP:</strong>  1 – 4294967295</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-183">Escopo:</span><span class="sxs-lookup"><span data-stu-id="d35de-183">Scope:</span></span></p></td>
<td><p><span data-ttu-id="d35de-184">Global</span><span class="sxs-lookup"><span data-stu-id="d35de-184">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-185">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="d35de-185">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="d35de-186"><strong>Windows 2000:</strong>  Não</span><span class="sxs-lookup"><span data-stu-id="d35de-186"><strong>Windows 2000:</strong>  No</span></span></p>
<p><span data-ttu-id="d35de-187"><strong>Windows XP:</strong>  Ok</span><span class="sxs-lookup"><span data-stu-id="d35de-187"><strong>Windows XP:</strong>  Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-188">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="d35de-188">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="d35de-189"><strong>Windows 2000:</strong>  Não</span><span class="sxs-lookup"><span data-stu-id="d35de-189"><strong>Windows 2000:</strong>  No</span></span></p>
<p><span data-ttu-id="d35de-190"><strong>Windows XP:</strong>  Ok</span><span class="sxs-lookup"><span data-stu-id="d35de-190"><strong>Windows XP:</strong>  Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-191">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="d35de-191">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="d35de-192">No</span><span class="sxs-lookup"><span data-stu-id="d35de-192">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-193">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="d35de-193">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="d35de-194">No</span><span class="sxs-lookup"><span data-stu-id="d35de-194">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-195">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="d35de-195">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="d35de-196">Yes</span><span class="sxs-lookup"><span data-stu-id="d35de-196">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-197">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="d35de-197">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="d35de-198">Yes</span><span class="sxs-lookup"><span data-stu-id="d35de-198">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-199">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="d35de-199">Availability:</span></span></p></td>
<td><p><span data-ttu-id="d35de-200">Tudo</span><span class="sxs-lookup"><span data-stu-id="d35de-200">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d35de-201">*JET_paramCacheSizeMax*</span><span class="sxs-lookup"><span data-stu-id="d35de-201">*JET_paramCacheSizeMax*</span></span>  
<span data-ttu-id="d35de-202">23</span><span class="sxs-lookup"><span data-stu-id="d35de-202">23</span></span>  

<span data-ttu-id="d35de-203">Esse parâmetro configura o tamanho máximo do cache de página do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d35de-203">This parameter configures the maximum size of the database page cache.</span></span> <span data-ttu-id="d35de-204">O tamanho está em páginas de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d35de-204">The size is in database pages.</span></span>

<span data-ttu-id="d35de-205">Por padrão, o cache de banco de dados ajustará automaticamente seu tamanho entre os limites definidos por **JET_paramCacheSizeMin** e **JET_paramCacheSizeMax**.</span><span class="sxs-lookup"><span data-stu-id="d35de-205">By default, the database cache will automatically adjust its size between the limits set by **JET_paramCacheSizeMin** and **JET_paramCacheSizeMax**.</span></span>

<span data-ttu-id="d35de-206">**Observação**   Se esse parâmetro for deixado para seu valor padrão, o tamanho máximo do cache será definido como o tamanho da memória física quando [JetInit](./jetinit-function.md) for chamado.</span><span class="sxs-lookup"><span data-stu-id="d35de-206">**Note**   If this parameter is left to its default value, then the maximum size of the cache will be set to the size of physical memory when [JetInit](./jetinit-function.md) is called.</span></span>

<span data-ttu-id="d35de-207">**Windows Vista:**  A partir do Windows Vista, o valor padrão desse parâmetro foi alterado para esclarecer esse comportamento.</span><span class="sxs-lookup"><span data-stu-id="d35de-207">**Windows Vista:**  As of Windows Vista, the default value of this parameter was changed to clarify this behavior.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d35de-208">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="d35de-208">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="d35de-209"><strong>Windows 2000, Windows XP e Windows Server 2003:</strong>  512</span><span class="sxs-lookup"><span data-stu-id="d35de-209"><strong>Windows 2000, Windows XP and Windows Server 2003:</strong>  512</span></span></p>
<p><span data-ttu-id="d35de-210"><strong>Windows Vista:</strong>  2000000000</span><span class="sxs-lookup"><span data-stu-id="d35de-210"><strong>Windows Vista:</strong>  2000000000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-211">Tipo:</span><span class="sxs-lookup"><span data-stu-id="d35de-211">Type:</span></span></p></td>
<td><p><span data-ttu-id="d35de-212">Integer</span><span class="sxs-lookup"><span data-stu-id="d35de-212">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-213">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="d35de-213">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="d35de-214"><strong>Windows 2000:</strong>  1 a 1048575</span><span class="sxs-lookup"><span data-stu-id="d35de-214"><strong>Windows 2000:</strong>  1 – 1048575</span></span></p>
<p><span data-ttu-id="d35de-215"><strong>Windows XP:</strong>  1 a 4294967295</span><span class="sxs-lookup"><span data-stu-id="d35de-215"><strong>Windows XP:</strong>  1 – 4294967295</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-216">Escopo:</span><span class="sxs-lookup"><span data-stu-id="d35de-216">Scope:</span></span></p></td>
<td><p><span data-ttu-id="d35de-217">Global</span><span class="sxs-lookup"><span data-stu-id="d35de-217">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-218">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="d35de-218">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="d35de-219"><strong>Windows 2000:</strong>  Não</span><span class="sxs-lookup"><span data-stu-id="d35de-219"><strong>Windows 2000:</strong>  No</span></span></p>
<p><span data-ttu-id="d35de-220"><strong>Windows XP:</strong>  Ok</span><span class="sxs-lookup"><span data-stu-id="d35de-220"><strong>Windows XP:</strong>  Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-221">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="d35de-221">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="d35de-222"><strong>Windows XP e windows 2000:</strong>  Não</span><span class="sxs-lookup"><span data-stu-id="d35de-222"><strong>Windows XP and Windows 2000:</strong>  No</span></span></p>
<p><span data-ttu-id="d35de-223"><strong>Windows Vista e Windows Server 2003:</strong>  Ok</span><span class="sxs-lookup"><span data-stu-id="d35de-223"><strong>Windows Vista and Windows Server 2003:</strong>  Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-224">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="d35de-224">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="d35de-225">No</span><span class="sxs-lookup"><span data-stu-id="d35de-225">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-226">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="d35de-226">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="d35de-227">No</span><span class="sxs-lookup"><span data-stu-id="d35de-227">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-228">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="d35de-228">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="d35de-229">Yes</span><span class="sxs-lookup"><span data-stu-id="d35de-229">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-230">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="d35de-230">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="d35de-231">Yes</span><span class="sxs-lookup"><span data-stu-id="d35de-231">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-232">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="d35de-232">Availability:</span></span></p></td>
<td><p><span data-ttu-id="d35de-233">Tudo</span><span class="sxs-lookup"><span data-stu-id="d35de-233">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d35de-234">*JET_paramCheckpointDepthMax*</span><span class="sxs-lookup"><span data-stu-id="d35de-234">*JET_paramCheckpointDepthMax*</span></span>  
<span data-ttu-id="d35de-235">24</span><span class="sxs-lookup"><span data-stu-id="d35de-235">24</span></span> 

<span data-ttu-id="d35de-236">Esse parâmetro controla o quão agressivamente as páginas do banco de dados são liberadas do cache de página do banco de dados para minimizar a quantidade de tempo que levará para se recuperar de uma falha.</span><span class="sxs-lookup"><span data-stu-id="d35de-236">This parameter controls how aggressively database pages are flushed from the database page cache to minimize the amount of time it will take to recover from a crash.</span></span> <span data-ttu-id="d35de-237">O parâmetro é um limite em bytes para saber quantos arquivos de log de transações deverão ser reproduzidos após uma falha.</span><span class="sxs-lookup"><span data-stu-id="d35de-237">The parameter is a threshold in bytes for about how many transaction log files will need to be replayed after a crash.</span></span>

<span data-ttu-id="d35de-238">Se o log circular estiver habilitado usando [JET_paramCircularLog](./transaction-log-parameters.md) , esse parâmetro também controlará a quantidade aproximada de arquivos de log de transações que serão retidos no disco.</span><span class="sxs-lookup"><span data-stu-id="d35de-238">If circular logging is enabled using [JET_paramCircularLog](./transaction-log-parameters.md) then this parameter will also control the approximate amount of transaction log files that will be retained on disk.</span></span>

<span data-ttu-id="d35de-239">É importante que esse parâmetro não seja definido como muito baixo.</span><span class="sxs-lookup"><span data-stu-id="d35de-239">It is important that this parameter not be set too low.</span></span> <span data-ttu-id="d35de-240">Como o valor desse parâmetro se aproxima de zero, o cache se tornará cada vez mais agressivo ao liberar páginas de banco de dados para o disco.</span><span class="sxs-lookup"><span data-stu-id="d35de-240">As the value of this parameter approaches zero, the cache will become more and more aggressive when flushing database pages to disk.</span></span> <span data-ttu-id="d35de-241">Isso não apenas resulta em um número maior de gravações nos arquivos de banco de dados, mas também causa indiretamente um número maior de leituras nesses arquivos.</span><span class="sxs-lookup"><span data-stu-id="d35de-241">This not only results in an increased number of writes to the database files but it also indirectly causes an increased number of reads to those files as well.</span></span> <span data-ttu-id="d35de-242">Isso pode causar problemas de desempenho muito significativos em alguns casos.</span><span class="sxs-lookup"><span data-stu-id="d35de-242">This can cause very significant performance problems in some cases.</span></span> <span data-ttu-id="d35de-243">Infelizmente, definir o menor valor ideal para esse parâmetro só pode ser feito usando experimentação com o aplicativo de destino.</span><span class="sxs-lookup"><span data-stu-id="d35de-243">Unfortunately, setting the smallest optimal value for this parameter can only be done using experimentation with the target application.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d35de-244">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="d35de-244">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="d35de-245">20971520</span><span class="sxs-lookup"><span data-stu-id="d35de-245">20971520</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-246">Tipo:</span><span class="sxs-lookup"><span data-stu-id="d35de-246">Type:</span></span></p></td>
<td><p><span data-ttu-id="d35de-247">Integer</span><span class="sxs-lookup"><span data-stu-id="d35de-247">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-248">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="d35de-248">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="d35de-249"><strong>Windows 2000, Windows XP e Windows Server 2003:</strong>  0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="d35de-249"><strong>Windows 2000, Windows XP and Windows Server 2003:</strong>  0 – 2147483647</span></span></p>
<p><span data-ttu-id="d35de-250"><strong>Windows Vista:</strong>  Todos os valores</span><span class="sxs-lookup"><span data-stu-id="d35de-250"><strong>Windows Vista:</strong>  All Values</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-251">Escopo:</span><span class="sxs-lookup"><span data-stu-id="d35de-251">Scope:</span></span></p></td>
<td><p><span data-ttu-id="d35de-252"><strong>Windows 2000, Windows XP e Windows Server 2003:</strong> Esse parâmetro é global.</span><span class="sxs-lookup"><span data-stu-id="d35de-252"><strong>Windows 2000, Windows XP and Windows Server 2003:</strong> This parameter is global.</span></span></p>
<p><span data-ttu-id="d35de-253"><strong>Windows Vista:</strong>  Esse parâmetro é por instância.</span><span class="sxs-lookup"><span data-stu-id="d35de-253"><strong>Windows Vista:</strong>  This parameter is per instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-254">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="d35de-254">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="d35de-255">Yes</span><span class="sxs-lookup"><span data-stu-id="d35de-255">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-256">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="d35de-256">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="d35de-257">Yes</span><span class="sxs-lookup"><span data-stu-id="d35de-257">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-258">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="d35de-258">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="d35de-259">No</span><span class="sxs-lookup"><span data-stu-id="d35de-259">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-260">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="d35de-260">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="d35de-261">Yes</span><span class="sxs-lookup"><span data-stu-id="d35de-261">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-262">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="d35de-262">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="d35de-263">Yes</span><span class="sxs-lookup"><span data-stu-id="d35de-263">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-264">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="d35de-264">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="d35de-265">Yes</span><span class="sxs-lookup"><span data-stu-id="d35de-265">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-266">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="d35de-266">Availability:</span></span></p></td>
<td><p><span data-ttu-id="d35de-267">Tudo</span><span class="sxs-lookup"><span data-stu-id="d35de-267">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d35de-268">*JET_paramCheckpointIOMax*</span><span class="sxs-lookup"><span data-stu-id="d35de-268">*JET_paramCheckpointIOMax*</span></span>  
<span data-ttu-id="d35de-269">135</span><span class="sxs-lookup"><span data-stu-id="d35de-269">135</span></span>  

<span data-ttu-id="d35de-270">Esse parâmetro controla o número máximo de gravações simultâneas que o mecanismo de banco de dados usará para liberar páginas de banco de dados modificadas com a finalidade de avançar o ponto de verificação.</span><span class="sxs-lookup"><span data-stu-id="d35de-270">This parameter controls the maximum number of concurrent writes that the database engine will use to flush modified database pages for the purpose of advancing the checkpoint.</span></span> <span data-ttu-id="d35de-271">O valor desse parâmetro pode ser usado para balancear a velocidade com a qual o ponto de verificação pode ser avançado versus o impacto negativo que esse processo terá no tempo de resposta para outras operações de e/s nos discos que contêm o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d35de-271">The value of this parameter can be used to balance the speed with which the checkpoint can be advanced versus the negative impact this process will have on the response time for other I/O operations to the disks holding the database.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d35de-272">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="d35de-272">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="d35de-273">96</span><span class="sxs-lookup"><span data-stu-id="d35de-273">96</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-274">Tipo:</span><span class="sxs-lookup"><span data-stu-id="d35de-274">Type:</span></span></p></td>
<td><p><span data-ttu-id="d35de-275">Integer</span><span class="sxs-lookup"><span data-stu-id="d35de-275">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-276">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="d35de-276">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="d35de-277">8 a 1024</span><span class="sxs-lookup"><span data-stu-id="d35de-277">8 – 1024</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-278">Escopo:</span><span class="sxs-lookup"><span data-stu-id="d35de-278">Scope:</span></span></p></td>
<td><p><span data-ttu-id="d35de-279">Global</span><span class="sxs-lookup"><span data-stu-id="d35de-279">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-280">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="d35de-280">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="d35de-281">Yes</span><span class="sxs-lookup"><span data-stu-id="d35de-281">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-282">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="d35de-282">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="d35de-283">Yes</span><span class="sxs-lookup"><span data-stu-id="d35de-283">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-284">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="d35de-284">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="d35de-285">No</span><span class="sxs-lookup"><span data-stu-id="d35de-285">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-286">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="d35de-286">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="d35de-287">No</span><span class="sxs-lookup"><span data-stu-id="d35de-287">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-288">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="d35de-288">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="d35de-289">Yes</span><span class="sxs-lookup"><span data-stu-id="d35de-289">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-290">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="d35de-290">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="d35de-291">No</span><span class="sxs-lookup"><span data-stu-id="d35de-291">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-292">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="d35de-292">Availability:</span></span></p></td>
<td><p><span data-ttu-id="d35de-293">Windows Vista e posterior</span><span class="sxs-lookup"><span data-stu-id="d35de-293">Windows Vista and later</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d35de-294">*JET_paramEnableViewCache*</span><span class="sxs-lookup"><span data-stu-id="d35de-294">*JET_paramEnableViewCache*</span></span>  
<span data-ttu-id="d35de-295">127</span><span class="sxs-lookup"><span data-stu-id="d35de-295">127</span></span>  

<span data-ttu-id="d35de-296">Quando esse parâmetro for **true**, o mecanismo de banco de dados usará os bancos de dado diretamente do cache de arquivos do Windows em vez de copiar os dados armazenados em cache em sua própria memória privada.</span><span class="sxs-lookup"><span data-stu-id="d35de-296">When this parameter is **True**, the database engine will use database data directly from the Windows file cache rather than copying the cached data into its own private memory.</span></span> <span data-ttu-id="d35de-297">Qualquer dado de banco de dados modificado ainda será armazenado em cache na memória privada.</span><span class="sxs-lookup"><span data-stu-id="d35de-297">Any database data that is modified will still be cached in private memory.</span></span>

<span data-ttu-id="d35de-298">A intenção desse modo é reduzir ainda mais a quantidade de memória privada usada pelo mecanismo de banco de dados do para armazenar em cache as</span><span class="sxs-lookup"><span data-stu-id="d35de-298">The intent of this mode is to further reduce the amount of private memory used by the database engine to cache database data.</span></span>

<span data-ttu-id="d35de-299">O cache de exibição só poderá ser usado se o uso do cache de arquivos do Windows estiver habilitado por meio da configuração de JET_paramEnableFileCache como **true**.</span><span class="sxs-lookup"><span data-stu-id="d35de-299">The view cache may only be used if the use of the Windows file cache is enabled by setting JET_paramEnableFileCache to **True**.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d35de-300">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="d35de-300">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="d35de-301">Falso</span><span class="sxs-lookup"><span data-stu-id="d35de-301">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-302">Tipo:</span><span class="sxs-lookup"><span data-stu-id="d35de-302">Type:</span></span></p></td>
<td><p><span data-ttu-id="d35de-303">Boolean</span><span class="sxs-lookup"><span data-stu-id="d35de-303">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-304">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="d35de-304">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="d35de-305">Falso, verdadeiro</span><span class="sxs-lookup"><span data-stu-id="d35de-305">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-306">Escopo:</span><span class="sxs-lookup"><span data-stu-id="d35de-306">Scope:</span></span></p></td>
<td><p><span data-ttu-id="d35de-307">Global</span><span class="sxs-lookup"><span data-stu-id="d35de-307">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-308">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="d35de-308">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="d35de-309">No</span><span class="sxs-lookup"><span data-stu-id="d35de-309">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-310">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="d35de-310">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="d35de-311">No</span><span class="sxs-lookup"><span data-stu-id="d35de-311">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-312">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="d35de-312">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="d35de-313">No</span><span class="sxs-lookup"><span data-stu-id="d35de-313">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-314">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="d35de-314">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="d35de-315">No</span><span class="sxs-lookup"><span data-stu-id="d35de-315">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-316">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="d35de-316">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="d35de-317">Yes</span><span class="sxs-lookup"><span data-stu-id="d35de-317">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-318">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="d35de-318">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="d35de-319">Yes</span><span class="sxs-lookup"><span data-stu-id="d35de-319">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-320">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="d35de-320">Availability:</span></span></p></td>
<td><p><span data-ttu-id="d35de-321">Windows Vista e posterior</span><span class="sxs-lookup"><span data-stu-id="d35de-321">Windows Vista and later</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d35de-322">*JET_paramLRUKCorrInterval*</span><span class="sxs-lookup"><span data-stu-id="d35de-322">*JET_paramLRUKCorrInterval*</span></span>  
<span data-ttu-id="d35de-323">25</span><span class="sxs-lookup"><span data-stu-id="d35de-323">25</span></span>  

<span data-ttu-id="d35de-324">Esse parâmetro define o intervalo de tempo em microssegundos sobre o qual dois acessos de página de banco de dados são considerados correlacionados.</span><span class="sxs-lookup"><span data-stu-id="d35de-324">This parameter sets the time interval in microseconds over which two database page accesses are considered to be correlated.</span></span> <span data-ttu-id="d35de-325">Esse intervalo de correlação controla a sensibilidade do algoritmo de substituição de página do cache (LRU-K) aos acessos de página sucessivos.</span><span class="sxs-lookup"><span data-stu-id="d35de-325">This correlation interval controls the sensitivity of the cache's page replacement algorithm (LRU-K) to successive page accesses.</span></span> <span data-ttu-id="d35de-326">Isso, por sua vez, afetará as páginas que ele escolhe manter em cache.</span><span class="sxs-lookup"><span data-stu-id="d35de-326">This in turn will affect which pages it chooses to keep cached.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d35de-327">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="d35de-327">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="d35de-328">128000</span><span class="sxs-lookup"><span data-stu-id="d35de-328">128000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-329">Tipo:</span><span class="sxs-lookup"><span data-stu-id="d35de-329">Type:</span></span></p></td>
<td><p><span data-ttu-id="d35de-330">Integer</span><span class="sxs-lookup"><span data-stu-id="d35de-330">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-331">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="d35de-331">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="d35de-332"><strong>Windows 2000, Windows XP e Windows Server 2003: </strong>    0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="d35de-332"><strong>Windows 2000, Windows XP and Windows Server 2003: </strong>    0 – 2147483647</span></span></p>
<p><span data-ttu-id="d35de-333"><strong>Windows Vista:</strong>  Todos os valores</span><span class="sxs-lookup"><span data-stu-id="d35de-333"><strong>Windows Vista:</strong>  All Values</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-334">Escopo:</span><span class="sxs-lookup"><span data-stu-id="d35de-334">Scope:</span></span></p></td>
<td><p><span data-ttu-id="d35de-335">Global</span><span class="sxs-lookup"><span data-stu-id="d35de-335">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-336">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="d35de-336">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="d35de-337">No</span><span class="sxs-lookup"><span data-stu-id="d35de-337">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-338">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="d35de-338">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="d35de-339">No</span><span class="sxs-lookup"><span data-stu-id="d35de-339">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-340">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="d35de-340">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="d35de-341">No</span><span class="sxs-lookup"><span data-stu-id="d35de-341">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-342">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="d35de-342">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="d35de-343">No</span><span class="sxs-lookup"><span data-stu-id="d35de-343">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-344">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="d35de-344">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="d35de-345">Yes</span><span class="sxs-lookup"><span data-stu-id="d35de-345">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-346">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="d35de-346">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="d35de-347">No</span><span class="sxs-lookup"><span data-stu-id="d35de-347">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-348">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="d35de-348">Availability:</span></span></p></td>
<td><p><span data-ttu-id="d35de-349">Tudo</span><span class="sxs-lookup"><span data-stu-id="d35de-349">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d35de-350">*JET_paramLRUKHistoryMax*</span><span class="sxs-lookup"><span data-stu-id="d35de-350">*JET_paramLRUKHistoryMax*</span></span>  
<span data-ttu-id="d35de-351">26</span><span class="sxs-lookup"><span data-stu-id="d35de-351">26</span></span>  

<span data-ttu-id="d35de-352">Esse parâmetro define o número máximo de páginas de banco de dados não armazenadas em cache para as quais os tempos de acesso da página do banco de dados serão retidos.</span><span class="sxs-lookup"><span data-stu-id="d35de-352">This parameter sets the maximum number of non cached database pages for which database page access times will be retained.</span></span> <span data-ttu-id="d35de-353">Esses registros de histórico permitem que o algoritmo de substituição de página do cache (LRU-K) detecte com mais precisão as páginas populares que foram removidas erroneamente do cache da página do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d35de-353">These history records allow the cache's page replacement algorithm (LRU-K) to more accurately detect popular pages that were wrongly evicted from the database page cache.</span></span>

<span data-ttu-id="d35de-354">**Windows XP e Windows Server 2003:**  Esse parâmetro é ignorado no Windows XP e no Windows Server 2003 e não afeta a operação do mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d35de-354">**Windows XP and Windows Server 2003:**  This parameter is ignored on Windows XP and Windows Server 2003 and does not affect the operation of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d35de-355">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="d35de-355">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="d35de-356"><strong>Windows 2000:</strong>  1024</span><span class="sxs-lookup"><span data-stu-id="d35de-356"><strong>Windows 2000:</strong>  1024</span></span></p>
<p><span data-ttu-id="d35de-357"><strong>Windows Vista:</strong>  100000</span><span class="sxs-lookup"><span data-stu-id="d35de-357"><strong>Windows Vista:</strong>  100000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-358">Tipo:</span><span class="sxs-lookup"><span data-stu-id="d35de-358">Type:</span></span></p></td>
<td><p><span data-ttu-id="d35de-359">Integer</span><span class="sxs-lookup"><span data-stu-id="d35de-359">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-360">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="d35de-360">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="d35de-361"><strong>Windows 2000:</strong>  0 a 4194303</span><span class="sxs-lookup"><span data-stu-id="d35de-361"><strong>Windows 2000:</strong>  0 – 4194303</span></span></p>
<p><span data-ttu-id="d35de-362"><strong>Windows Vista:</strong>  Todos os valores</span><span class="sxs-lookup"><span data-stu-id="d35de-362"><strong>Windows Vista:</strong>  All Values</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-363">Escopo:</span><span class="sxs-lookup"><span data-stu-id="d35de-363">Scope:</span></span></p></td>
<td><p><span data-ttu-id="d35de-364">Global</span><span class="sxs-lookup"><span data-stu-id="d35de-364">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-365">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="d35de-365">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="d35de-366">No</span><span class="sxs-lookup"><span data-stu-id="d35de-366">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-367">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="d35de-367">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="d35de-368">No</span><span class="sxs-lookup"><span data-stu-id="d35de-368">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-369">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="d35de-369">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="d35de-370">No</span><span class="sxs-lookup"><span data-stu-id="d35de-370">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-371">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="d35de-371">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="d35de-372">No</span><span class="sxs-lookup"><span data-stu-id="d35de-372">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-373">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="d35de-373">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="d35de-374">Yes</span><span class="sxs-lookup"><span data-stu-id="d35de-374">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-375">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="d35de-375">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="d35de-376">Yes</span><span class="sxs-lookup"><span data-stu-id="d35de-376">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-377">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="d35de-377">Availability:</span></span></p></td>
<td><p><span data-ttu-id="d35de-378">Tudo</span><span class="sxs-lookup"><span data-stu-id="d35de-378">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d35de-379">*JET_paramLRUKPolicy*</span><span class="sxs-lookup"><span data-stu-id="d35de-379">*JET_paramLRUKPolicy*</span></span>  
<span data-ttu-id="d35de-380">27</span><span class="sxs-lookup"><span data-stu-id="d35de-380">27</span></span>  

<span data-ttu-id="d35de-381">Esse parâmetro configura o número de acessos de página do banco de dados que são considerados para determinar a utilidade da página.</span><span class="sxs-lookup"><span data-stu-id="d35de-381">This parameter configures the number of database page accesses that are considered for determining the usefulness of the page.</span></span> <span data-ttu-id="d35de-382">Esse parâmetro é essencialmente o K no LRU-K, o algoritmo de substituição de página do cache de página do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d35de-382">This parameter is essentially the K in LRU-K, the database page cache's page replacement algorithm.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d35de-383">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="d35de-383">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="d35de-384">2</span><span class="sxs-lookup"><span data-stu-id="d35de-384">2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-385">Tipo:</span><span class="sxs-lookup"><span data-stu-id="d35de-385">Type:</span></span></p></td>
<td><p><span data-ttu-id="d35de-386">Integer</span><span class="sxs-lookup"><span data-stu-id="d35de-386">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-387">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="d35de-387">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="d35de-388">1-2</span><span class="sxs-lookup"><span data-stu-id="d35de-388">1-2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-389">Escopo:</span><span class="sxs-lookup"><span data-stu-id="d35de-389">Scope:</span></span></p></td>
<td><p><span data-ttu-id="d35de-390">Global</span><span class="sxs-lookup"><span data-stu-id="d35de-390">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-391">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="d35de-391">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="d35de-392">No</span><span class="sxs-lookup"><span data-stu-id="d35de-392">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-393">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="d35de-393">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="d35de-394">No</span><span class="sxs-lookup"><span data-stu-id="d35de-394">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-395">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="d35de-395">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="d35de-396">No</span><span class="sxs-lookup"><span data-stu-id="d35de-396">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-397">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="d35de-397">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="d35de-398">No</span><span class="sxs-lookup"><span data-stu-id="d35de-398">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-399">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="d35de-399">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="d35de-400">Yes</span><span class="sxs-lookup"><span data-stu-id="d35de-400">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-401">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="d35de-401">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="d35de-402">No</span><span class="sxs-lookup"><span data-stu-id="d35de-402">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-403">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="d35de-403">Availability:</span></span></p></td>
<td><p><span data-ttu-id="d35de-404">Tudo</span><span class="sxs-lookup"><span data-stu-id="d35de-404">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d35de-405">*JET_paramLRUKTimeout*</span><span class="sxs-lookup"><span data-stu-id="d35de-405">*JET_paramLRUKTimeout*</span></span>  
<span data-ttu-id="d35de-406">28</span><span class="sxs-lookup"><span data-stu-id="d35de-406">28</span></span>

<span data-ttu-id="d35de-407">Esse parâmetro indica o período de tempo em segundos após o qual uma página no cache de página do banco de dados é considerada perdida um acesso à página com a finalidade de considerar a utilidade da página.</span><span class="sxs-lookup"><span data-stu-id="d35de-407">This parameter indicates the period of time in seconds after which a page in the database page cache is considered to have lost a page access for the purpose of considering the usefulness of the page.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d35de-408">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="d35de-408">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="d35de-409">100</span><span class="sxs-lookup"><span data-stu-id="d35de-409">100</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-410">Tipo:</span><span class="sxs-lookup"><span data-stu-id="d35de-410">Type:</span></span></p></td>
<td><p><span data-ttu-id="d35de-411">Integer</span><span class="sxs-lookup"><span data-stu-id="d35de-411">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-412">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="d35de-412">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="d35de-413"><strong>Windows 2000, Windows XP e Windows Server 2003:</strong>  1 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="d35de-413"><strong>Windows 2000, Windows XP and Windows Server 2003:</strong>  1 – 2147483647</span></span></p>
<p><span data-ttu-id="d35de-414"><strong>Windows Vista:</strong>   1 a 4294967295</span><span class="sxs-lookup"><span data-stu-id="d35de-414"><strong>Windows Vista:</strong>   1 – 4294967295</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-415">Escopo:</span><span class="sxs-lookup"><span data-stu-id="d35de-415">Scope:</span></span></p></td>
<td><p><span data-ttu-id="d35de-416">Global</span><span class="sxs-lookup"><span data-stu-id="d35de-416">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-417">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="d35de-417">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="d35de-418">No</span><span class="sxs-lookup"><span data-stu-id="d35de-418">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-419">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="d35de-419">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="d35de-420">No</span><span class="sxs-lookup"><span data-stu-id="d35de-420">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-421">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="d35de-421">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="d35de-422">No</span><span class="sxs-lookup"><span data-stu-id="d35de-422">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-423">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="d35de-423">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="d35de-424">No</span><span class="sxs-lookup"><span data-stu-id="d35de-424">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-425">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="d35de-425">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="d35de-426">Yes</span><span class="sxs-lookup"><span data-stu-id="d35de-426">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-427">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="d35de-427">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="d35de-428">No</span><span class="sxs-lookup"><span data-stu-id="d35de-428">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-429">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="d35de-429">Availability:</span></span></p></td>
<td><p><span data-ttu-id="d35de-430">Tudo</span><span class="sxs-lookup"><span data-stu-id="d35de-430">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d35de-431">*JET_paramLRUKTrxCorrInterval*</span><span class="sxs-lookup"><span data-stu-id="d35de-431">*JET_paramLRUKTrxCorrInterval*</span></span>  
<span data-ttu-id="d35de-432">29</span><span class="sxs-lookup"><span data-stu-id="d35de-432">29</span></span>  

<span data-ttu-id="d35de-433">Esse parâmetro é obsoleto e não afeta a operação do mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d35de-433">This parameter is obsolete and does not affect the operation of the database engine.</span></span>

<span data-ttu-id="d35de-434">*JET_paramStartFlushThreshold*</span><span class="sxs-lookup"><span data-stu-id="d35de-434">*JET_paramStartFlushThreshold*</span></span>  
<span data-ttu-id="d35de-435">31</span><span class="sxs-lookup"><span data-stu-id="d35de-435">31</span></span>  

<span data-ttu-id="d35de-436">Esse parâmetro controla quando o cache de página do banco de dados começa a remover páginas do cache para liberar espaço para páginas que não são armazenadas em cache.</span><span class="sxs-lookup"><span data-stu-id="d35de-436">This parameter controls when the database page cache begins evicting pages from the cache to make room for pages that are not cached.</span></span> <span data-ttu-id="d35de-437">Quando o número de buffers de página no cache cair abaixo desse limite, um processo em segundo plano será iniciado para reabastecer o pool de buffers disponíveis.</span><span class="sxs-lookup"><span data-stu-id="d35de-437">When the number of page buffers in the cache drops below this threshold then a background process will be started to replenish that pool of available buffers.</span></span> <span data-ttu-id="d35de-438">Esse limite é sempre relativo ao tamanho máximo do cache, conforme definido por **JET_paramCacheSizeMax**.</span><span class="sxs-lookup"><span data-stu-id="d35de-438">This threshold is always relative to the maximum cache size as set by **JET_paramCacheSizeMax**.</span></span> <span data-ttu-id="d35de-439">Esse limite também deve ser menor que o limite de parada definido por **JET_paramStopFlushThreshold**.</span><span class="sxs-lookup"><span data-stu-id="d35de-439">This threshold must also always be less than the stop threshold as set by **JET_paramStopFlushThreshold**.</span></span>

<span data-ttu-id="d35de-440">A altura da distância do limite inicial determinará o tempo de resposta que o cache da página do banco de dados deve ter para produzir os buffers disponíveis antes que o aplicativo precise deles.</span><span class="sxs-lookup"><span data-stu-id="d35de-440">The distance height of the start threshold will determine the response time that the database page cache must have to produce available buffers before the application needs them.</span></span> <span data-ttu-id="d35de-441">Um limite de início alto dará ao processo em segundo plano mais tempo para reagir.</span><span class="sxs-lookup"><span data-stu-id="d35de-441">A high start threshold will give the background process more time to react.</span></span> <span data-ttu-id="d35de-442">No entanto, um limite de início alto implica um limite de parada maior e reduzirá o tamanho efetivo do cache de página de banco de dados para páginas modificadas (Windows 2000) ou para todas as páginas (Windows XP e posterior).</span><span class="sxs-lookup"><span data-stu-id="d35de-442">However, a high start threshold implies a higher stop threshold and that will reduce the effective size of the database page cache for modified pages (Windows 2000) or for all pages (Windows XP and later).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d35de-443">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="d35de-443">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="d35de-444"><strong>Windows 2000, Windows XP e Windows Server 2003:</strong>  5 (1%)</span><span class="sxs-lookup"><span data-stu-id="d35de-444"><strong>Windows 2000, Windows XP and Windows Server 2003:</strong>  5 (1%)</span></span></p>
<p><span data-ttu-id="d35de-445"><strong>Windows Vista:</strong>  20 milhões (1%)</span><span class="sxs-lookup"><span data-stu-id="d35de-445"><strong>Windows Vista:</strong>  20000000 (1%)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-446">Tipo:</span><span class="sxs-lookup"><span data-stu-id="d35de-446">Type:</span></span></p></td>
<td><p><span data-ttu-id="d35de-447">Integer</span><span class="sxs-lookup"><span data-stu-id="d35de-447">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-448">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="d35de-448">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="d35de-449"><strong>Windows 2000:</strong>  1 a 1048575</span><span class="sxs-lookup"><span data-stu-id="d35de-449"><strong>Windows 2000:</strong>  1 – 1048575</span></span></p>
<p><span data-ttu-id="d35de-450"><strong>Windows XP:</strong>  1 a 4294967295</span><span class="sxs-lookup"><span data-stu-id="d35de-450"><strong>Windows XP:</strong>  1 – 4294967295</span></span></p>
<p><span data-ttu-id="d35de-451"><strong>Windows Vista:</strong>  Todos os valores</span><span class="sxs-lookup"><span data-stu-id="d35de-451"><strong>Windows Vista:</strong>  All Values</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-452">Escopo:</span><span class="sxs-lookup"><span data-stu-id="d35de-452">Scope:</span></span></p></td>
<td><p><span data-ttu-id="d35de-453">Global</span><span class="sxs-lookup"><span data-stu-id="d35de-453">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-454">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="d35de-454">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="d35de-455">Yes</span><span class="sxs-lookup"><span data-stu-id="d35de-455">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-456">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="d35de-456">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="d35de-457">Yes</span><span class="sxs-lookup"><span data-stu-id="d35de-457">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-458">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="d35de-458">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="d35de-459">No</span><span class="sxs-lookup"><span data-stu-id="d35de-459">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-460">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="d35de-460">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="d35de-461">No</span><span class="sxs-lookup"><span data-stu-id="d35de-461">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-462">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="d35de-462">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="d35de-463">Yes</span><span class="sxs-lookup"><span data-stu-id="d35de-463">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-464">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="d35de-464">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="d35de-465">Yes</span><span class="sxs-lookup"><span data-stu-id="d35de-465">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-466">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="d35de-466">Availability:</span></span></p></td>
<td><p><span data-ttu-id="d35de-467">Tudo</span><span class="sxs-lookup"><span data-stu-id="d35de-467">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d35de-468">*JET_paramStopFlushThreshold*</span><span class="sxs-lookup"><span data-stu-id="d35de-468">*JET_paramStopFlushThreshold*</span></span>  
<span data-ttu-id="d35de-469">32</span><span class="sxs-lookup"><span data-stu-id="d35de-469">32</span></span>  

<span data-ttu-id="d35de-470">Esse parâmetro controla quando o cache da página do banco de dados encerra a remoção de páginas do cache para liberar espaço para páginas que não são armazenadas em cache.</span><span class="sxs-lookup"><span data-stu-id="d35de-470">This parameter controls when the database page cache ends evicting pages from the cache to make room for pages that are not cached.</span></span> <span data-ttu-id="d35de-471">Quando o número de buffers de página no cache ultrapassar esse limite, o processo em segundo plano que foi iniciado para reabastecer o pool de buffers disponíveis será interrompido.</span><span class="sxs-lookup"><span data-stu-id="d35de-471">When the number of page buffers in the cache rises above this threshold then the background process that was started to replenish that pool of available buffers is stopped.</span></span> <span data-ttu-id="d35de-472">Esse limite é sempre relativo ao tamanho máximo do cache, conforme definido por **JET_paramCacheSizeMax**.</span><span class="sxs-lookup"><span data-stu-id="d35de-472">This threshold is always relative to the maximum cache size as set by **JET_paramCacheSizeMax**.</span></span> <span data-ttu-id="d35de-473">Esse limite também deve ser maior que o limite de início definido por **JET_paramStartFlushThreshold**.</span><span class="sxs-lookup"><span data-stu-id="d35de-473">This threshold must also always be greater than the start threshold as set by **JET_paramStartFlushThreshold**.</span></span>

<span data-ttu-id="d35de-474">A distância entre o limite inicial e o limite de interrupção afeta a eficiência com a qual as páginas de banco de dados são liberadas pelo processo em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="d35de-474">The distance between the start threshold and the stop threshold affects the efficiency with which database pages are flushed by the background process.</span></span> <span data-ttu-id="d35de-475">Um intervalo maior fará com que seja mais provável que as gravações nas páginas vizinhas possam ser combinadas.</span><span class="sxs-lookup"><span data-stu-id="d35de-475">A larger gap will make it more likely that writes to neighboring pages may be combined.</span></span> <span data-ttu-id="d35de-476">No entanto, um limite de parada alta reduzirá o tamanho efetivo do cache de página de banco de dados para páginas modificadas (Windows 2000) ou para todas as páginas (Windows XP e posterior).</span><span class="sxs-lookup"><span data-stu-id="d35de-476">However, a high stop threshold will reduce the effective size of the database page cache for modified pages (Windows 2000) or for all pages (Windows XP and later).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d35de-477">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="d35de-477">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="d35de-478"><strong>Windows 2000, Windows XP e Windows Server 2003:</strong>  10 (2%)</span><span class="sxs-lookup"><span data-stu-id="d35de-478"><strong>Windows 2000, Windows XP and Windows Server 2003:</strong>  10 (2%)</span></span></p>
<p><span data-ttu-id="d35de-479"><strong>Windows Vista:</strong>  40 milhões (2%)</span><span class="sxs-lookup"><span data-stu-id="d35de-479"><strong>Windows Vista:</strong>  40000000 (2%)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-480">Tipo:</span><span class="sxs-lookup"><span data-stu-id="d35de-480">Type:</span></span></p></td>
<td><p><span data-ttu-id="d35de-481">Integer</span><span class="sxs-lookup"><span data-stu-id="d35de-481">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-482">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="d35de-482">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="d35de-483"><strong>Windows 2000:</strong>  1 a 1048575</span><span class="sxs-lookup"><span data-stu-id="d35de-483"><strong>Windows 2000:</strong>  1 – 1048575</span></span></p>
<p><span data-ttu-id="d35de-484"><strong>Windows XP:</strong>  1 a 4294967295</span><span class="sxs-lookup"><span data-stu-id="d35de-484"><strong>Windows XP:</strong>  1 – 4294967295</span></span></p>
<p><span data-ttu-id="d35de-485"><strong>Windows Vista:</strong>  Todos os valores</span><span class="sxs-lookup"><span data-stu-id="d35de-485"><strong>Windows Vista:</strong>  All Values</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-486">Escopo:</span><span class="sxs-lookup"><span data-stu-id="d35de-486">Scope:</span></span></p></td>
<td><p><span data-ttu-id="d35de-487">Global</span><span class="sxs-lookup"><span data-stu-id="d35de-487">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-488">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="d35de-488">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="d35de-489">Yes</span><span class="sxs-lookup"><span data-stu-id="d35de-489">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-490">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="d35de-490">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="d35de-491">Yes</span><span class="sxs-lookup"><span data-stu-id="d35de-491">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-492">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="d35de-492">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="d35de-493">No</span><span class="sxs-lookup"><span data-stu-id="d35de-493">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-494">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="d35de-494">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="d35de-495">No</span><span class="sxs-lookup"><span data-stu-id="d35de-495">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-496">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="d35de-496">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="d35de-497">Yes</span><span class="sxs-lookup"><span data-stu-id="d35de-497">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-498">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="d35de-498">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="d35de-499">Yes</span><span class="sxs-lookup"><span data-stu-id="d35de-499">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-500">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="d35de-500">Availability:</span></span></p></td>
<td><p><span data-ttu-id="d35de-501">Tudo</span><span class="sxs-lookup"><span data-stu-id="d35de-501">All</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="d35de-502">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d35de-502">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d35de-503"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="d35de-503"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d35de-504">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="d35de-504">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d35de-505"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="d35de-505"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d35de-506">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="d35de-506">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d35de-507"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="d35de-507"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d35de-508">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="d35de-508">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="d35de-509">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="d35de-509">See Also</span></span>

[<span data-ttu-id="d35de-510">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="d35de-510">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="d35de-511">JetInit</span><span class="sxs-lookup"><span data-stu-id="d35de-511">JetInit</span></span>](./jetinit-function.md)
