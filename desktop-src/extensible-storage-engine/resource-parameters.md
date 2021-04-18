---
description: 'Saiba mais sobre: parâmetros de recurso'
title: Parâmetros do recurso
TOCTitle: Resource Parameters
ms:assetid: 1f61845a-ffa5-4894-9fe0-a58737b3b54e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269201(v=EXCHG.10)
ms:contentKeyID: 32765504
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
ms.openlocfilehash: 953488a273092413df78d4fe396899d284c7a01c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760189"
---
# <a name="resource-parameters"></a><span data-ttu-id="cd489-103">Parâmetros do recurso</span><span class="sxs-lookup"><span data-stu-id="cd489-103">Resource Parameters</span></span>


<span data-ttu-id="cd489-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="cd489-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="resource-parameters"></a><span data-ttu-id="cd489-105">Parâmetros do recurso</span><span class="sxs-lookup"><span data-stu-id="cd489-105">Resource Parameters</span></span>

<span data-ttu-id="cd489-106">Este tópico contém parâmetros que são usados para recursos.</span><span class="sxs-lookup"><span data-stu-id="cd489-106">This topic contains parameters that are used for resources.</span></span>

<span data-ttu-id="cd489-107">*JET_paramCachedClosedTables*</span><span class="sxs-lookup"><span data-stu-id="cd489-107">*JET_paramCachedClosedTables*</span></span>  
<span data-ttu-id="cd489-108">125</span><span class="sxs-lookup"><span data-stu-id="cd489-108">125</span></span>  

<span data-ttu-id="cd489-109">Esse parâmetro controla o número de recursos da árvore B + em cache pela instância depois que as tabelas que eles representam foram fechadas pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cd489-109">This parameter controls the number of B+ Tree resources cached by the instance after the tables they represent have been closed by the application.</span></span>

<span data-ttu-id="cd489-110">Valores grandes para esse parâmetro farão com que o mecanismo de banco de dados use mais memória, mas aumentará a velocidade com que um grande número de tabelas pode ser aberto aleatoriamente pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cd489-110">Large values for this parameter will cause the database engine to use more memory but will increase the speed with which a large number of tables can be opened randomly by the application.</span></span> <span data-ttu-id="cd489-111">Isso é útil para aplicativos que têm um esquema com um número muito grande de tabelas.</span><span class="sxs-lookup"><span data-stu-id="cd489-111">This is useful for applications that have a schema with a very large number of tables.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cd489-112">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="cd489-112">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="cd489-113">64</span><span class="sxs-lookup"><span data-stu-id="cd489-113">64</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-114">Tipo:</span><span class="sxs-lookup"><span data-stu-id="cd489-114">Type:</span></span></p></td>
<td><p><span data-ttu-id="cd489-115">Integer</span><span class="sxs-lookup"><span data-stu-id="cd489-115">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-116">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="cd489-116">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="cd489-117">1 a 2147483647</span><span class="sxs-lookup"><span data-stu-id="cd489-117">1 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-118">Escopo:</span><span class="sxs-lookup"><span data-stu-id="cd489-118">Scope:</span></span></p></td>
<td><p><span data-ttu-id="cd489-119">Instância</span><span class="sxs-lookup"><span data-stu-id="cd489-119">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-120">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="cd489-120">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="cd489-121">Yes</span><span class="sxs-lookup"><span data-stu-id="cd489-121">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-122">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="cd489-122">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="cd489-123">No</span><span class="sxs-lookup"><span data-stu-id="cd489-123">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-124">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="cd489-124">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="cd489-125">No</span><span class="sxs-lookup"><span data-stu-id="cd489-125">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-126">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="cd489-126">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="cd489-127">No</span><span class="sxs-lookup"><span data-stu-id="cd489-127">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-128">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="cd489-128">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="cd489-129">Yes</span><span class="sxs-lookup"><span data-stu-id="cd489-129">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-130">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="cd489-130">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="cd489-131">Yes</span><span class="sxs-lookup"><span data-stu-id="cd489-131">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-132">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="cd489-132">Availability:</span></span></p></td>
<td><p><span data-ttu-id="cd489-133">Windows Vista e versões posteriores</span><span class="sxs-lookup"><span data-stu-id="cd489-133">Windows Vista and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cd489-134">*JET_paramDisablePerfmon*</span><span class="sxs-lookup"><span data-stu-id="cd489-134">*JET_paramDisablePerfmon*</span></span>  
<span data-ttu-id="cd489-135">107</span><span class="sxs-lookup"><span data-stu-id="cd489-135">107</span></span>  

<span data-ttu-id="cd489-136">Esse parâmetro pode ser usado para impedir que o mecanismo de banco de dados publique em seu desempenho o Windows.</span><span class="sxs-lookup"><span data-stu-id="cd489-136">This parameter can be used to prevent the database engine from publishing data about its performance to Windows.</span></span> <span data-ttu-id="cd489-137">Isso pode ser feito para reduzir a atividade de thread de serviço do mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="cd489-137">This can be done to reduce the service thread activity of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cd489-138">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="cd489-138">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="cd489-139">Falso</span><span class="sxs-lookup"><span data-stu-id="cd489-139">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-140">Tipo:</span><span class="sxs-lookup"><span data-stu-id="cd489-140">Type:</span></span></p></td>
<td><p><span data-ttu-id="cd489-141">Boolean</span><span class="sxs-lookup"><span data-stu-id="cd489-141">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-142">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="cd489-142">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="cd489-143">Falso, verdadeiro</span><span class="sxs-lookup"><span data-stu-id="cd489-143">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-144">Escopo:</span><span class="sxs-lookup"><span data-stu-id="cd489-144">Scope:</span></span></p></td>
<td><p><span data-ttu-id="cd489-145">Global</span><span class="sxs-lookup"><span data-stu-id="cd489-145">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-146">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="cd489-146">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="cd489-147">No</span><span class="sxs-lookup"><span data-stu-id="cd489-147">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-148">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="cd489-148">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="cd489-149">No</span><span class="sxs-lookup"><span data-stu-id="cd489-149">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-150">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="cd489-150">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="cd489-151">No</span><span class="sxs-lookup"><span data-stu-id="cd489-151">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-152">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="cd489-152">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="cd489-153">No</span><span class="sxs-lookup"><span data-stu-id="cd489-153">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-154">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="cd489-154">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="cd489-155">No</span><span class="sxs-lookup"><span data-stu-id="cd489-155">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-156">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="cd489-156">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="cd489-157">Yes</span><span class="sxs-lookup"><span data-stu-id="cd489-157">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-158">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="cd489-158">Availability:</span></span></p></td>
<td><p><span data-ttu-id="cd489-159">Windows Vista e versões posteriores</span><span class="sxs-lookup"><span data-stu-id="cd489-159">Windows Vista and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cd489-160">*JET_paramGlobalMinVerPages*</span><span class="sxs-lookup"><span data-stu-id="cd489-160">*JET_paramGlobalMinVerPages*</span></span>  
<span data-ttu-id="cd489-161">81</span><span class="sxs-lookup"><span data-stu-id="cd489-161">81</span></span>  

<span data-ttu-id="cd489-162">Esse parâmetro permite que os aplicativos operem no modo de várias instâncias para alocar previamente a memória para páginas de versão em um pool global para emular o comportamento mais antigo.</span><span class="sxs-lookup"><span data-stu-id="cd489-162">This parameter allows applications that operate in multi-instance mode to pre-allocate memory for version pages in a global pool to emulate the older behavior.</span></span> <span data-ttu-id="cd489-163">Isso é útil no caso de o aplicativo desejar garantir que as transações de um determinado tamanho possam ter sucesso posteriormente, mesmo se a memória ficar escassa.</span><span class="sxs-lookup"><span data-stu-id="cd489-163">This is useful in case the application wishes to guarantee that transactions of a certain size can succeed later on even if memory becomes scarce.</span></span>

<span data-ttu-id="cd489-164">**Windows 2000:**  Memória suficiente para trás de todas as páginas de versão sempre é reservada no momento da [JetInit](./jetinit-function.md) .</span><span class="sxs-lookup"><span data-stu-id="cd489-164">**Windows 2000:**  Enough memory to back all version pages is always reserved at [JetInit](./jetinit-function.md) time.</span></span>

<span data-ttu-id="cd489-165">**Windows XP:**  A partir do Windows XP, isso ainda é verdadeiro quando estiver no modo de instância única.</span><span class="sxs-lookup"><span data-stu-id="cd489-165">**Windows XP:**  As of Windows XP, this is still true when in single instance mode.</span></span> <span data-ttu-id="cd489-166">No entanto, a memória da página de versão é alocada dinamicamente no modo de várias instâncias.</span><span class="sxs-lookup"><span data-stu-id="cd489-166">However, version page memory is dynamically allocated when in multi-instance mode.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cd489-167">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="cd489-167">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="cd489-168">64</span><span class="sxs-lookup"><span data-stu-id="cd489-168">64</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-169">Tipo:</span><span class="sxs-lookup"><span data-stu-id="cd489-169">Type:</span></span></p></td>
<td><p><span data-ttu-id="cd489-170">Integer</span><span class="sxs-lookup"><span data-stu-id="cd489-170">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-171">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="cd489-171">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="cd489-172">1 a 2147483647</span><span class="sxs-lookup"><span data-stu-id="cd489-172">1 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-173">Escopo:</span><span class="sxs-lookup"><span data-stu-id="cd489-173">Scope:</span></span></p></td>
<td><p><span data-ttu-id="cd489-174">Global</span><span class="sxs-lookup"><span data-stu-id="cd489-174">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-175">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="cd489-175">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="cd489-176">No</span><span class="sxs-lookup"><span data-stu-id="cd489-176">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-177">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="cd489-177">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="cd489-178">No</span><span class="sxs-lookup"><span data-stu-id="cd489-178">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-179">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="cd489-179">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="cd489-180">No</span><span class="sxs-lookup"><span data-stu-id="cd489-180">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-181">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="cd489-181">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="cd489-182">Yes</span><span class="sxs-lookup"><span data-stu-id="cd489-182">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-183">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="cd489-183">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="cd489-184">No</span><span class="sxs-lookup"><span data-stu-id="cd489-184">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-185">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="cd489-185">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="cd489-186">Yes</span><span class="sxs-lookup"><span data-stu-id="cd489-186">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-187">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="cd489-187">Availability:</span></span></p></td>
<td><p><span data-ttu-id="cd489-188">Windows XP e versões posteriores</span><span class="sxs-lookup"><span data-stu-id="cd489-188">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cd489-189">*JET_paramMaxCursors*</span><span class="sxs-lookup"><span data-stu-id="cd489-189">*JET_paramMaxCursors*</span></span>  
<span data-ttu-id="cd489-190">8</span><span class="sxs-lookup"><span data-stu-id="cd489-190">8</span></span>  

<span data-ttu-id="cd489-191">Esse parâmetro reserva o número solicitado de recursos de cursor para uso por uma instância.</span><span class="sxs-lookup"><span data-stu-id="cd489-191">This parameter reserves the requested number of cursor resources for use by an instance.</span></span> <span data-ttu-id="cd489-192">Um recurso de cursor corresponde diretamente a um tipo de dados [JET_TABLEID](./jet-tableid.md) .</span><span class="sxs-lookup"><span data-stu-id="cd489-192">A cursor resource directly corresponds to a [JET_TABLEID](./jet-tableid.md) data type.</span></span> <span data-ttu-id="cd489-193">Essa configuração afetará quantos cursores podem ser usados ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="cd489-193">This setting will affect how many cursors can be used at the same time.</span></span> <span data-ttu-id="cd489-194">Um recurso de cursor não pode ser compartilhado por sessões diferentes, portanto, esse parâmetro deve ser definido como um valor grande o suficiente para que cada sessão possa usar quantos cursores forem necessários.</span><span class="sxs-lookup"><span data-stu-id="cd489-194">A cursor resource cannot be shared by different sessions so this parameter must be set to a large enough value so that each session can use as many cursors as are required.</span></span>

<span data-ttu-id="cd489-195">**Windows 2000, Windows XP e Windows Server 2003:**  Valores grandes para esse parâmetro consumirão espaço de endereço e poderão aumentar o uso de memória.</span><span class="sxs-lookup"><span data-stu-id="cd489-195">**Windows 2000, Windows XP and Windows Server 2003:**  Large values for this parameter will consume address space and may increase memory usage.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cd489-196">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="cd489-196">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="cd489-197">1024</span><span class="sxs-lookup"><span data-stu-id="cd489-197">1024</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-198">Tipo:</span><span class="sxs-lookup"><span data-stu-id="cd489-198">Type:</span></span></p></td>
<td><p><span data-ttu-id="cd489-199">Integer</span><span class="sxs-lookup"><span data-stu-id="cd489-199">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-200">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="cd489-200">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="cd489-201">0 a 2147483647</span><span class="sxs-lookup"><span data-stu-id="cd489-201">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-202">Escopo:</span><span class="sxs-lookup"><span data-stu-id="cd489-202">Scope:</span></span></p></td>
<td><p><span data-ttu-id="cd489-203">Instância</span><span class="sxs-lookup"><span data-stu-id="cd489-203">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-204">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="cd489-204">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="cd489-205">Yes</span><span class="sxs-lookup"><span data-stu-id="cd489-205">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-206">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="cd489-206">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="cd489-207">No</span><span class="sxs-lookup"><span data-stu-id="cd489-207">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-208">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="cd489-208">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="cd489-209">No</span><span class="sxs-lookup"><span data-stu-id="cd489-209">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-210">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="cd489-210">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="cd489-211">No</span><span class="sxs-lookup"><span data-stu-id="cd489-211">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-212">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="cd489-212">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="cd489-213">No</span><span class="sxs-lookup"><span data-stu-id="cd489-213">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-214">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="cd489-214">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="cd489-215">Yes</span><span class="sxs-lookup"><span data-stu-id="cd489-215">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-216">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="cd489-216">Availability:</span></span></p></td>
<td><p><span data-ttu-id="cd489-217">Tudo</span><span class="sxs-lookup"><span data-stu-id="cd489-217">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cd489-218">*JET_paramMaxInstances*</span><span class="sxs-lookup"><span data-stu-id="cd489-218">*JET_paramMaxInstances*</span></span>  
<span data-ttu-id="cd489-219">104</span><span class="sxs-lookup"><span data-stu-id="cd489-219">104</span></span>  

<span data-ttu-id="cd489-220">Esse parâmetro controla o número máximo de instâncias que podem ser criadas em um único processo.</span><span class="sxs-lookup"><span data-stu-id="cd489-220">This parameter controls the maximum number of instances that can be created in a single process.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cd489-221">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="cd489-221">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="cd489-222">16</span><span class="sxs-lookup"><span data-stu-id="cd489-222">16</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-223">Tipo:</span><span class="sxs-lookup"><span data-stu-id="cd489-223">Type:</span></span></p></td>
<td><p><span data-ttu-id="cd489-224">Integer</span><span class="sxs-lookup"><span data-stu-id="cd489-224">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-225">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="cd489-225">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="cd489-226">1-1024</span><span class="sxs-lookup"><span data-stu-id="cd489-226">1-1024</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-227">Escopo:</span><span class="sxs-lookup"><span data-stu-id="cd489-227">Scope:</span></span></p></td>
<td><p><span data-ttu-id="cd489-228">Global</span><span class="sxs-lookup"><span data-stu-id="cd489-228">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-229">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="cd489-229">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="cd489-230">No</span><span class="sxs-lookup"><span data-stu-id="cd489-230">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-231">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="cd489-231">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="cd489-232">No</span><span class="sxs-lookup"><span data-stu-id="cd489-232">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-233">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="cd489-233">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="cd489-234">No</span><span class="sxs-lookup"><span data-stu-id="cd489-234">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-235">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="cd489-235">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="cd489-236">No</span><span class="sxs-lookup"><span data-stu-id="cd489-236">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-237">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="cd489-237">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="cd489-238">Yes</span><span class="sxs-lookup"><span data-stu-id="cd489-238">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-239">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="cd489-239">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="cd489-240">Yes</span><span class="sxs-lookup"><span data-stu-id="cd489-240">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-241">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="cd489-241">Availability:</span></span></p></td>
<td><p><span data-ttu-id="cd489-242">Windows XP e versões posteriores</span><span class="sxs-lookup"><span data-stu-id="cd489-242">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cd489-243">*JET_paramMaxOpenTables*</span><span class="sxs-lookup"><span data-stu-id="cd489-243">*JET_paramMaxOpenTables*</span></span>  
<span data-ttu-id="cd489-244">6</span><span class="sxs-lookup"><span data-stu-id="cd489-244">6</span></span>  

<span data-ttu-id="cd489-245">Esse parâmetro reserva o número solicitado de recursos da árvore B + para uso por uma instância.</span><span class="sxs-lookup"><span data-stu-id="cd489-245">This parameter reserves the requested number of B+ Tree resources for use by an instance.</span></span> <span data-ttu-id="cd489-246">Essa configuração afetará quantas tabelas podem ser usadas ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="cd489-246">This setting will affect how many tables can be used at the same time.</span></span> <span data-ttu-id="cd489-247">Esse parâmetro precisa ser definido em relação ao esquema físico dos bancos de dados em uso pelo mecanismo de banco de dados, portanto, essa configuração não é tão simples quanto poderia ser.</span><span class="sxs-lookup"><span data-stu-id="cd489-247">This parameter needs to be set relative to the physical schema of the databases in use by the database engine, so this setting is not as straightforward as it could be.</span></span>

<span data-ttu-id="cd489-248">Em geral, você precisará de dois recursos mais um recurso por índice secundário por tabela no uso simultâneo do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cd489-248">In general, you will need two resources plus one resource per secondary index per table in concurrent use by the application.</span></span>

<span data-ttu-id="cd489-249">**Windows 2000, Windows XP e Windows Server 2003:**  Valores grandes para esse parâmetro consumirão espaço de endereço e poderão aumentar o uso de memória.</span><span class="sxs-lookup"><span data-stu-id="cd489-249">**Windows 2000, Windows XP and Windows Server 2003:**  Large values for this parameter will consume address space and may increase memory usage.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cd489-250">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="cd489-250">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="cd489-251">300</span><span class="sxs-lookup"><span data-stu-id="cd489-251">300</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-252">Tipo:</span><span class="sxs-lookup"><span data-stu-id="cd489-252">Type:</span></span></p></td>
<td><p><span data-ttu-id="cd489-253">Integer</span><span class="sxs-lookup"><span data-stu-id="cd489-253">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-254">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="cd489-254">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="cd489-255">0 a 2147483647</span><span class="sxs-lookup"><span data-stu-id="cd489-255">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-256">Escopo:</span><span class="sxs-lookup"><span data-stu-id="cd489-256">Scope:</span></span></p></td>
<td><p><span data-ttu-id="cd489-257">Instância</span><span class="sxs-lookup"><span data-stu-id="cd489-257">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-258">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="cd489-258">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="cd489-259">Yes</span><span class="sxs-lookup"><span data-stu-id="cd489-259">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-260">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="cd489-260">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="cd489-261">No</span><span class="sxs-lookup"><span data-stu-id="cd489-261">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-262">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="cd489-262">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="cd489-263">No</span><span class="sxs-lookup"><span data-stu-id="cd489-263">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-264">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="cd489-264">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="cd489-265">No</span><span class="sxs-lookup"><span data-stu-id="cd489-265">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-266">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="cd489-266">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="cd489-267">No</span><span class="sxs-lookup"><span data-stu-id="cd489-267">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-268">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="cd489-268">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="cd489-269">Yes</span><span class="sxs-lookup"><span data-stu-id="cd489-269">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-270">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="cd489-270">Availability:</span></span></p></td>
<td><p><span data-ttu-id="cd489-271">Tudo</span><span class="sxs-lookup"><span data-stu-id="cd489-271">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cd489-272">*JET_paramMaxSessions*</span><span class="sxs-lookup"><span data-stu-id="cd489-272">*JET_paramMaxSessions*</span></span>  
<span data-ttu-id="cd489-273">5</span><span class="sxs-lookup"><span data-stu-id="cd489-273">5</span></span>  

<span data-ttu-id="cd489-274">Esse parâmetro reserva o número solicitado de recursos de sessão para uso por uma instância.</span><span class="sxs-lookup"><span data-stu-id="cd489-274">This parameter reserves the requested number of session resources for use by an instance.</span></span> <span data-ttu-id="cd489-275">Um recurso de sessão corresponde diretamente a um tipo de dados [JET_SESID](./jet-sesid.md) .</span><span class="sxs-lookup"><span data-stu-id="cd489-275">A session resource directly corresponds to a [JET_SESID](./jet-sesid.md) data type.</span></span> <span data-ttu-id="cd489-276">Essa configuração afetará quantas sessões podem ser usadas ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="cd489-276">This setting will affect how many sessions can be used at the same time.</span></span>

<span data-ttu-id="cd489-277">**Windows 2000, Windows XP e Windows Server 2003:**  Valores grandes para esse parâmetro consumirão espaço de endereço e poderão aumentar o uso de memória.</span><span class="sxs-lookup"><span data-stu-id="cd489-277">**Windows 2000, Windows XP and Windows Server 2003:**  Large values for this parameter will consume address space and may increase memory usage.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cd489-278">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="cd489-278">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="cd489-279">16</span><span class="sxs-lookup"><span data-stu-id="cd489-279">16</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-280">Tipo:</span><span class="sxs-lookup"><span data-stu-id="cd489-280">Type:</span></span></p></td>
<td><p><span data-ttu-id="cd489-281">Integer</span><span class="sxs-lookup"><span data-stu-id="cd489-281">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-282">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="cd489-282">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="cd489-283">0 a 30000</span><span class="sxs-lookup"><span data-stu-id="cd489-283">0 – 30000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-284">Escopo:</span><span class="sxs-lookup"><span data-stu-id="cd489-284">Scope:</span></span></p></td>
<td><p><span data-ttu-id="cd489-285">Instância</span><span class="sxs-lookup"><span data-stu-id="cd489-285">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-286">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="cd489-286">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="cd489-287">Yes</span><span class="sxs-lookup"><span data-stu-id="cd489-287">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-288">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="cd489-288">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="cd489-289">No</span><span class="sxs-lookup"><span data-stu-id="cd489-289">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-290">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="cd489-290">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="cd489-291">No</span><span class="sxs-lookup"><span data-stu-id="cd489-291">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-292">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="cd489-292">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="cd489-293">No</span><span class="sxs-lookup"><span data-stu-id="cd489-293">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-294">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="cd489-294">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="cd489-295">No</span><span class="sxs-lookup"><span data-stu-id="cd489-295">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-296">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="cd489-296">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="cd489-297">Yes</span><span class="sxs-lookup"><span data-stu-id="cd489-297">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-298">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="cd489-298">Availability:</span></span></p></td>
<td><p><span data-ttu-id="cd489-299">Tudo</span><span class="sxs-lookup"><span data-stu-id="cd489-299">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cd489-300">*JET_paramMaxTemporaryTables*</span><span class="sxs-lookup"><span data-stu-id="cd489-300">*JET_paramMaxTemporaryTables*</span></span>  
<span data-ttu-id="cd489-301">10</span><span class="sxs-lookup"><span data-stu-id="cd489-301">10</span></span>  

<span data-ttu-id="cd489-302">Esse parâmetro reserva o número solicitado de recursos de tabela temporária para uso por uma instância.</span><span class="sxs-lookup"><span data-stu-id="cd489-302">This parameter reserves the requested number of temporary table resources for use by an instance.</span></span> <span data-ttu-id="cd489-303">Essa configuração afetará quantas tabelas temporárias podem ser usadas ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="cd489-303">This setting will affect how many temporary tables can be used at the same time.</span></span>

<span data-ttu-id="cd489-304">**Windows 2000, Windows XP e Windows Server 2003:**  Valores grandes para esse parâmetro consumirão espaço de endereço e poderão aumentar o uso de memória.</span><span class="sxs-lookup"><span data-stu-id="cd489-304">**Windows 2000, Windows XP and Windows Server 2003:**  Large values for this parameter will consume address space and may increase memory usage.</span></span>

<span data-ttu-id="cd489-305">**Windows XP e posterior:**  Se esse parâmetro de sistema for definido como zero, nenhum banco de dados temporário será criado e qualquer atividade que exija o uso do banco de dados temporário falhará.</span><span class="sxs-lookup"><span data-stu-id="cd489-305">**Windows XP and later:**  If this system parameter is set to zero then no temporary database will be created and any activity that requires use of the temporary database will fail.</span></span> <span data-ttu-id="cd489-306">Essa configuração pode ser útil para evitar a e/s necessária para criar o banco de dados temporário se for conhecido que ele não será usado.</span><span class="sxs-lookup"><span data-stu-id="cd489-306">This setting can be useful to avoid the I/O required to create the temporary database if it is known that it will not be used.</span></span>

<span data-ttu-id="cd489-307">**Observação**  O uso de uma tabela temporária também requer um recurso de cursor.</span><span class="sxs-lookup"><span data-stu-id="cd489-307">**Note**  The use of a temporary table also requires a cursor resource.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cd489-308">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="cd489-308">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="cd489-309">20</span><span class="sxs-lookup"><span data-stu-id="cd489-309">20</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-310">Tipo:</span><span class="sxs-lookup"><span data-stu-id="cd489-310">Type:</span></span></p></td>
<td><p><span data-ttu-id="cd489-311">Integer</span><span class="sxs-lookup"><span data-stu-id="cd489-311">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-312">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="cd489-312">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="cd489-313">0 a 2147483647</span><span class="sxs-lookup"><span data-stu-id="cd489-313">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-314">Escopo:</span><span class="sxs-lookup"><span data-stu-id="cd489-314">Scope:</span></span></p></td>
<td><p><span data-ttu-id="cd489-315">Instância</span><span class="sxs-lookup"><span data-stu-id="cd489-315">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-316">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="cd489-316">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="cd489-317">Yes</span><span class="sxs-lookup"><span data-stu-id="cd489-317">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-318">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="cd489-318">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="cd489-319">No</span><span class="sxs-lookup"><span data-stu-id="cd489-319">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-320">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="cd489-320">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="cd489-321">Yes</span><span class="sxs-lookup"><span data-stu-id="cd489-321">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-322">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="cd489-322">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="cd489-323">No</span><span class="sxs-lookup"><span data-stu-id="cd489-323">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-324">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="cd489-324">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="cd489-325">No</span><span class="sxs-lookup"><span data-stu-id="cd489-325">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-326">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="cd489-326">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="cd489-327">Yes</span><span class="sxs-lookup"><span data-stu-id="cd489-327">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-328">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="cd489-328">Availability:</span></span></p></td>
<td><p><span data-ttu-id="cd489-329">Tudo</span><span class="sxs-lookup"><span data-stu-id="cd489-329">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cd489-330">*JET_paramMaxVerPages*</span><span class="sxs-lookup"><span data-stu-id="cd489-330">*JET_paramMaxVerPages*</span></span>  
<span data-ttu-id="cd489-331">9</span><span class="sxs-lookup"><span data-stu-id="cd489-331">9</span></span>  

<span data-ttu-id="cd489-332">Esse parâmetro reserva o número solicitado de páginas de repositório de versão para uso por uma instância.</span><span class="sxs-lookup"><span data-stu-id="cd489-332">This parameter reserves the requested number of version store pages for use by an instance.</span></span> <span data-ttu-id="cd489-333">O repositório de versão mantém um registro ao vivo de todas as diferentes versões de cada registro ou entrada de índice no banco de dados que pode ser visto por todas as transações ativas.</span><span class="sxs-lookup"><span data-stu-id="cd489-333">The version store holds a live record of all the different versions of each record or index entry in the database that can be seen by all active transactions.</span></span> <span data-ttu-id="cd489-334">Essas versões são usadas para dar suporte ao controle de simultaneidade de várias versões em uso pelo mecanismo de banco de dados para dar suporte a transações usando o isolamento de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="cd489-334">These versions are used to support the multi-versioned concurrency control in use by the database engine to support transactions using snapshot isolation.</span></span> <span data-ttu-id="cd489-335">Essa configuração afetará quantas atualizações podem ser mantidas na memória por vez.</span><span class="sxs-lookup"><span data-stu-id="cd489-335">This setting will affect how many updates can be held in memory at a time.</span></span> <span data-ttu-id="cd489-336">Isso, por sua vez, afetará o número máximo de atualizações que uma única transação pode executar, a duração máxima que uma transação pode ser mantida aberta, a carga simultânea máxima de transações de atualização no sistema ou uma combinação delas.</span><span class="sxs-lookup"><span data-stu-id="cd489-336">This in turn will affect either the maximum number of updates a single transaction can perform, the maximum duration a transaction can be held open, the maximum concurrent load of updating transactions on the system, or a combination of these.</span></span>

<span data-ttu-id="cd489-337">Cada página de repositório de versão conforme configurada por esse parâmetro é 16 KB em tamanho em computadores de 32 bits e 32 KB em computadores de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="cd489-337">Each version store page as configured by this parameter is 16KB in size on 32-bit machines, and 32KB on 64-bit machines.</span></span>

<span data-ttu-id="cd489-338">**Windows Vista e posterior:**  O tamanho da página de repositório de versão pode ser lido e alterado via JET_paramVerPageSize.</span><span class="sxs-lookup"><span data-stu-id="cd489-338">**Windows Vista and later:**  The version store page size can be read and changed via JET_paramVerPageSize.</span></span>

<span data-ttu-id="cd489-339">**Windows 2000, Windows XP e Windows Server 2003:**  Valores grandes para esse parâmetro consumirão espaço de endereço e poderão aumentar o uso de memória.</span><span class="sxs-lookup"><span data-stu-id="cd489-339">**Windows 2000, Windows XP and Windows Server 2003:**  Large values for this parameter will consume address space and may increase memory usage.</span></span>

<span data-ttu-id="cd489-340">**Observação**  Isso é, de longe, o recurso mais comum a ser esgotado pelo mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="cd489-340">**Note**  This is by far the most common resource to be exhausted by the database engine.</span></span> <span data-ttu-id="cd489-341">A atenção deve ser paga à configuração do parâmetro System e à carga transacional do aplicativo para evitar esgotar esse recurso em operação normal.</span><span class="sxs-lookup"><span data-stu-id="cd489-341">Careful attention must be paid to the setting of the system parameter and to the transactional load of the application to avoid exhausting this resource under normal operation.</span></span> <span data-ttu-id="cd489-342">Quando esse recurso estiver esgotado, as atualizações para o banco de dados serão rejeitadas com JET_errVersionStoreOutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="cd489-342">When this resource is exhausted, updates to the database will be rejected with JET_errVersionStoreOutOfMemory.</span></span> <span data-ttu-id="cd489-343">Para liberar alguns desses recursos, a transação pendente mais antiga deve ser anulada.</span><span class="sxs-lookup"><span data-stu-id="cd489-343">To release some of these resources, the oldest outstanding transaction must be aborted.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cd489-344">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="cd489-344">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="cd489-345">64</span><span class="sxs-lookup"><span data-stu-id="cd489-345">64</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-346">Tipo:</span><span class="sxs-lookup"><span data-stu-id="cd489-346">Type:</span></span></p></td>
<td><p><span data-ttu-id="cd489-347">Integer</span><span class="sxs-lookup"><span data-stu-id="cd489-347">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-348">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="cd489-348">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="cd489-349">1 a 2147483647</span><span class="sxs-lookup"><span data-stu-id="cd489-349">1 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-350">Escopo:</span><span class="sxs-lookup"><span data-stu-id="cd489-350">Scope:</span></span></p></td>
<td><p><span data-ttu-id="cd489-351">Instância</span><span class="sxs-lookup"><span data-stu-id="cd489-351">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-352">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="cd489-352">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="cd489-353">Yes</span><span class="sxs-lookup"><span data-stu-id="cd489-353">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-354">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="cd489-354">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="cd489-355">No</span><span class="sxs-lookup"><span data-stu-id="cd489-355">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-356">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="cd489-356">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="cd489-357">No</span><span class="sxs-lookup"><span data-stu-id="cd489-357">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-358">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="cd489-358">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="cd489-359">Yes</span><span class="sxs-lookup"><span data-stu-id="cd489-359">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-360">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="cd489-360">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="cd489-361">No</span><span class="sxs-lookup"><span data-stu-id="cd489-361">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-362">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="cd489-362">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="cd489-363">Yes</span><span class="sxs-lookup"><span data-stu-id="cd489-363">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-364">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="cd489-364">Availability:</span></span></p></td>
<td><p><span data-ttu-id="cd489-365">Tudo</span><span class="sxs-lookup"><span data-stu-id="cd489-365">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cd489-366">*JET_paramPageHintCacheSize*</span><span class="sxs-lookup"><span data-stu-id="cd489-366">*JET_paramPageHintCacheSize*</span></span>  
<span data-ttu-id="cd489-367">101</span><span class="sxs-lookup"><span data-stu-id="cd489-367">101</span></span>  

<span data-ttu-id="cd489-368">Esse parâmetro controla o tamanho de um cache especial usado para acelerar a pesquisa de ponteiros de página filho da árvore B + no cache de página do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="cd489-368">This parameter controls the size of a special cache used to accelerate the lookup of B+ Tree child page pointers in the database page cache.</span></span> <span data-ttu-id="cd489-369">O tamanho do cache está em bytes.</span><span class="sxs-lookup"><span data-stu-id="cd489-369">The size of the cache is in bytes.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cd489-370">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="cd489-370">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="cd489-371">262144</span><span class="sxs-lookup"><span data-stu-id="cd489-371">262144</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-372">Tipo:</span><span class="sxs-lookup"><span data-stu-id="cd489-372">Type:</span></span></p></td>
<td><p><span data-ttu-id="cd489-373">Integer</span><span class="sxs-lookup"><span data-stu-id="cd489-373">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-374">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="cd489-374">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="cd489-375">0 a 2147483647</span><span class="sxs-lookup"><span data-stu-id="cd489-375">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-376">Escopo:</span><span class="sxs-lookup"><span data-stu-id="cd489-376">Scope:</span></span></p></td>
<td><p><span data-ttu-id="cd489-377">Global</span><span class="sxs-lookup"><span data-stu-id="cd489-377">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-378">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="cd489-378">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="cd489-379">Yes</span><span class="sxs-lookup"><span data-stu-id="cd489-379">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-380">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="cd489-380">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="cd489-381">Yes</span><span class="sxs-lookup"><span data-stu-id="cd489-381">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-382">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="cd489-382">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="cd489-383">No</span><span class="sxs-lookup"><span data-stu-id="cd489-383">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-384">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="cd489-384">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="cd489-385">No</span><span class="sxs-lookup"><span data-stu-id="cd489-385">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-386">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="cd489-386">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="cd489-387">Yes</span><span class="sxs-lookup"><span data-stu-id="cd489-387">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-388">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="cd489-388">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="cd489-389">Yes</span><span class="sxs-lookup"><span data-stu-id="cd489-389">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-390">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="cd489-390">Availability:</span></span></p></td>
<td><p><span data-ttu-id="cd489-391">Windows XP e versões posteriores</span><span class="sxs-lookup"><span data-stu-id="cd489-391">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cd489-392">*JET_paramPreferredMaxOpenTables*</span><span class="sxs-lookup"><span data-stu-id="cd489-392">*JET_paramPreferredMaxOpenTables*</span></span>  
<span data-ttu-id="cd489-393">7</span><span class="sxs-lookup"><span data-stu-id="cd489-393">7</span></span>  

<span data-ttu-id="cd489-394">Esse parâmetro tenta manter o número de recursos da árvore B em uso abaixo do limite especificado.</span><span class="sxs-lookup"><span data-stu-id="cd489-394">This parameter attempts to keep the number of B+ Tree resources in use below the specified threshold.</span></span>

<span data-ttu-id="cd489-395">Se esse parâmetro for definido como zero, ele usará como padrão 100% de **JET_paramMaxOpenTables**.</span><span class="sxs-lookup"><span data-stu-id="cd489-395">If this parameter is set to zero then it will default to 100% of **JET_paramMaxOpenTables**.</span></span>

<span data-ttu-id="cd489-396">**Windows Vista e posterior:**  Esse parâmetro é obsoleto e não afeta a operação do mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="cd489-396">**Windows Vista and later:**  This parameter is obsolete and does not affect the operation of the database engine.</span></span> <span data-ttu-id="cd489-397">Os aplicativos devem usar JET_paramMaxCachedClosedTables em vez disso.</span><span class="sxs-lookup"><span data-stu-id="cd489-397">Applications should use JET_paramMaxCachedClosedTables instead.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cd489-398">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="cd489-398">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="cd489-399">0 (100% de <strong>JET_paramMaxOpenTables</strong>)</span><span class="sxs-lookup"><span data-stu-id="cd489-399">0 (100% of <strong>JET_paramMaxOpenTables</strong>)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-400">Tipo:</span><span class="sxs-lookup"><span data-stu-id="cd489-400">Type:</span></span></p></td>
<td><p><span data-ttu-id="cd489-401">Integer</span><span class="sxs-lookup"><span data-stu-id="cd489-401">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-402">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="cd489-402">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="cd489-403">0 a 2147483647</span><span class="sxs-lookup"><span data-stu-id="cd489-403">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-404">Escopo:</span><span class="sxs-lookup"><span data-stu-id="cd489-404">Scope:</span></span></p></td>
<td><p><span data-ttu-id="cd489-405">Instância</span><span class="sxs-lookup"><span data-stu-id="cd489-405">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-406">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="cd489-406">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="cd489-407">Yes</span><span class="sxs-lookup"><span data-stu-id="cd489-407">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-408">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="cd489-408">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="cd489-409">No</span><span class="sxs-lookup"><span data-stu-id="cd489-409">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-410">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="cd489-410">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="cd489-411">No</span><span class="sxs-lookup"><span data-stu-id="cd489-411">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-412">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="cd489-412">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="cd489-413">No</span><span class="sxs-lookup"><span data-stu-id="cd489-413">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-414">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="cd489-414">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="cd489-415">Yes</span><span class="sxs-lookup"><span data-stu-id="cd489-415">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-416">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="cd489-416">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="cd489-417">Yes</span><span class="sxs-lookup"><span data-stu-id="cd489-417">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-418">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="cd489-418">Availability:</span></span></p></td>
<td><p><span data-ttu-id="cd489-419">Tudo</span><span class="sxs-lookup"><span data-stu-id="cd489-419">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cd489-420">*JET_paramPreferredVerPages*</span><span class="sxs-lookup"><span data-stu-id="cd489-420">*JET_paramPreferredVerPages*</span></span>  
<span data-ttu-id="cd489-421">63</span><span class="sxs-lookup"><span data-stu-id="cd489-421">63</span></span>  

<span data-ttu-id="cd489-422">Esse parâmetro representa um limite relativo a **JET_paramMaxVerPages** que controla o uso discricionário de páginas de versão pelo mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="cd489-422">This parameter represents a threshold relative to **JET_paramMaxVerPages** that controls the discretionary use of version pages by the database engine.</span></span> <span data-ttu-id="cd489-423">Se o tamanho do repositório de versão exceder esse limite, todas as informações usadas apenas para tarefas em segundo plano opcionais, como a recuperação de espaço excluído no banco de dados, serão sacrificadas para preservar espaço para informações transacionais.</span><span class="sxs-lookup"><span data-stu-id="cd489-423">If the size of the version store exceeds this threshold then any information that is only used for optional background tasks, such as reclaiming deleted space in the database, is instead sacrificed to preserve room for transactional information.</span></span>

<span data-ttu-id="cd489-424">**Windows 2000, Windows XP e Windows Server 2003:**  Definir esse parâmetro como zero definiria o limite como 90% de **JET_paramMaxVerPages**.</span><span class="sxs-lookup"><span data-stu-id="cd489-424">**Windows 2000, Windows XP and Windows Server 2003:**  Setting this parameter to zero would set the threshold to be 90% of **JET_paramMaxVerPages**.</span></span>

<span data-ttu-id="cd489-425">**Windows Vista e posterior:**  Não há mais suporte para isso e o valor padrão desse parâmetro foi alterado para esclarecer seu comportamento.</span><span class="sxs-lookup"><span data-stu-id="cd489-425">**Windows Vista and later:**  This is no longer supported and the default value of this parameter was changed to clarify its behavior.</span></span>

<span data-ttu-id="cd489-426">Cada página de repositório de versão conforme configurada por esse parâmetro é 16 KB em tamanho em computadores de 32 bits e 32 KB em computadores de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="cd489-426">Each version store page as configured by this parameter is 16KB in size on 32-bit machines, and 32KB on 64-bit machines.</span></span>

<span data-ttu-id="cd489-427">**Windows Vista e posterior:**  O tamanho da página de repositório de versão pode ser lido e alterado via JET_paramVerPageSize.</span><span class="sxs-lookup"><span data-stu-id="cd489-427">**Windows Vista and later:**  The version store page size can be read and changed via JET_paramVerPageSize.</span></span>

<span data-ttu-id="cd489-428">**Observação**  Se o mecanismo de banco de dados operar acima desse limite com muita frequência, é possível que o banco de dados diminua no desempenho.</span><span class="sxs-lookup"><span data-stu-id="cd489-428">**Note**  If the database engine operates above this threshold too often then it is possible for the database to degrade in performance.</span></span> <span data-ttu-id="cd489-429">Isso acontece porque os processos em segundo plano que limpam o banco de dados não podem funcionar sem as informações opcionais que são geradas nesse cenário.</span><span class="sxs-lookup"><span data-stu-id="cd489-429">This happens because the background processes that clean up the database cannot function without the optional information that is thrown away in this scenario.</span></span> <span data-ttu-id="cd489-430">A desfragmentação online ou offline irá neutralizar esse efeito.</span><span class="sxs-lookup"><span data-stu-id="cd489-430">Online or offline defragmentation will counteract this effect.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cd489-431">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="cd489-431">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="cd489-432"><strong>Windows 2000, Windows XP e Windows Server 2003:</strong>  0 (90% do JET_paramMaxVerPages)</span><span class="sxs-lookup"><span data-stu-id="cd489-432"><strong>Windows 2000, Windows XP and Windows Server 2003:</strong>  0 (90% of JET_paramMaxVerPages)</span></span></p>
<p><span data-ttu-id="cd489-433"><strong>Windows Vista:</strong>  58</span><span class="sxs-lookup"><span data-stu-id="cd489-433"><strong>Windows Vista:</strong>  58</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-434">Tipo:</span><span class="sxs-lookup"><span data-stu-id="cd489-434">Type:</span></span></p></td>
<td><p><span data-ttu-id="cd489-435">Integer</span><span class="sxs-lookup"><span data-stu-id="cd489-435">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-436">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="cd489-436">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="cd489-437">1 a 2147483647</span><span class="sxs-lookup"><span data-stu-id="cd489-437">1 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-438">Escopo:</span><span class="sxs-lookup"><span data-stu-id="cd489-438">Scope:</span></span></p></td>
<td><p><span data-ttu-id="cd489-439">Instância</span><span class="sxs-lookup"><span data-stu-id="cd489-439">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-440">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="cd489-440">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="cd489-441">Yes</span><span class="sxs-lookup"><span data-stu-id="cd489-441">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-442">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="cd489-442">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="cd489-443">Yes</span><span class="sxs-lookup"><span data-stu-id="cd489-443">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-444">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="cd489-444">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="cd489-445">No</span><span class="sxs-lookup"><span data-stu-id="cd489-445">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-446">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="cd489-446">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="cd489-447">Yes</span><span class="sxs-lookup"><span data-stu-id="cd489-447">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-448">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="cd489-448">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="cd489-449">Yes</span><span class="sxs-lookup"><span data-stu-id="cd489-449">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-450">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="cd489-450">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="cd489-451">Yes</span><span class="sxs-lookup"><span data-stu-id="cd489-451">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-452">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="cd489-452">Availability:</span></span></p></td>
<td><p><span data-ttu-id="cd489-453">Tudo</span><span class="sxs-lookup"><span data-stu-id="cd489-453">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cd489-454">*JET_paramVerPageSize*</span><span class="sxs-lookup"><span data-stu-id="cd489-454">*JET_paramVerPageSize*</span></span>  
<span data-ttu-id="cd489-455">128</span><span class="sxs-lookup"><span data-stu-id="cd489-455">128</span></span>  

<span data-ttu-id="cd489-456">Esse parâmetro controla o tamanho das páginas de repositório de versão usadas pelo mecanismo de banco de dados para manter informações transacionais.</span><span class="sxs-lookup"><span data-stu-id="cd489-456">This parameter controls the size of the version store pages used by the database engine to hold transactional information.</span></span> <span data-ttu-id="cd489-457">O valor desse parâmetro é o tamanho da unidade para todos os outros parâmetros do sistema que estão em termos de páginas de versão (por exemplo, JET_paramMaxVerPages).</span><span class="sxs-lookup"><span data-stu-id="cd489-457">The value of this parameter is the unit size for all the other system parameters that are in terms of version pages (e.g. JET_paramMaxVerPages).</span></span>

<span data-ttu-id="cd489-458">O mecanismo de banco de dados pode optar por usar um tamanho de página de repositório de versão maior do que o solicitado.</span><span class="sxs-lookup"><span data-stu-id="cd489-458">The database engine may choose to use a larger version store page size than requested.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cd489-459">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="cd489-459">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="cd489-460">16384</span><span class="sxs-lookup"><span data-stu-id="cd489-460">16384</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-461">Tipo:</span><span class="sxs-lookup"><span data-stu-id="cd489-461">Type:</span></span></p></td>
<td><p><span data-ttu-id="cd489-462">Integer</span><span class="sxs-lookup"><span data-stu-id="cd489-462">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-463">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="cd489-463">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="cd489-464">1024, 2048, 4096, 8192, 16384, 32768, 65536</span><span class="sxs-lookup"><span data-stu-id="cd489-464">1024, 2048, 4096, 8192, 16384, 32768, 65536</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-465">Escopo:</span><span class="sxs-lookup"><span data-stu-id="cd489-465">Scope:</span></span></p></td>
<td><p><span data-ttu-id="cd489-466">Global</span><span class="sxs-lookup"><span data-stu-id="cd489-466">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-467">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="cd489-467">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="cd489-468">No</span><span class="sxs-lookup"><span data-stu-id="cd489-468">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-469">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="cd489-469">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="cd489-470">No</span><span class="sxs-lookup"><span data-stu-id="cd489-470">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-471">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="cd489-471">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="cd489-472">No</span><span class="sxs-lookup"><span data-stu-id="cd489-472">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-473">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="cd489-473">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="cd489-474">No</span><span class="sxs-lookup"><span data-stu-id="cd489-474">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-475">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="cd489-475">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="cd489-476">No</span><span class="sxs-lookup"><span data-stu-id="cd489-476">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-477">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="cd489-477">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="cd489-478">Yes</span><span class="sxs-lookup"><span data-stu-id="cd489-478">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-479">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="cd489-479">Availability:</span></span></p></td>
<td><p><span data-ttu-id="cd489-480">Windows Vista e posterior</span><span class="sxs-lookup"><span data-stu-id="cd489-480">Windows Vista and later</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cd489-481">*JET_paramVersionStoreTaskQueueMax*</span><span class="sxs-lookup"><span data-stu-id="cd489-481">*JET_paramVersionStoreTaskQueueMax*</span></span>  
<span data-ttu-id="cd489-482">105</span><span class="sxs-lookup"><span data-stu-id="cd489-482">105</span></span>  

<span data-ttu-id="cd489-483">Esse parâmetro controla o número de itens de trabalho de limpeza em segundo plano que podem ser enfileirados no pool de threads do mecanismo de banco de dados a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="cd489-483">This parameter controls the number of background cleanup work items that can be queued to the database engine thread pool at any one time.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cd489-484">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="cd489-484">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="cd489-485">32</span><span class="sxs-lookup"><span data-stu-id="cd489-485">32</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-486">Tipo:</span><span class="sxs-lookup"><span data-stu-id="cd489-486">Type:</span></span></p></td>
<td><p><span data-ttu-id="cd489-487">Integer</span><span class="sxs-lookup"><span data-stu-id="cd489-487">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-488">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="cd489-488">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="cd489-489"><strong>Windows XP e Windows Server 2003:  </strong>  1 a 63</span><span class="sxs-lookup"><span data-stu-id="cd489-489"><strong>Windows XP and Windows Server 2003:  </strong>  1 – 63</span></span></p>
<p><span data-ttu-id="cd489-490"><strong>Windows Vista:</strong>  1 a 127</span><span class="sxs-lookup"><span data-stu-id="cd489-490"><strong>Windows Vista:</strong>  1 – 127</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-491">Escopo:</span><span class="sxs-lookup"><span data-stu-id="cd489-491">Scope:</span></span></p></td>
<td><p><span data-ttu-id="cd489-492">Instância</span><span class="sxs-lookup"><span data-stu-id="cd489-492">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-493">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="cd489-493">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="cd489-494">Yes</span><span class="sxs-lookup"><span data-stu-id="cd489-494">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-495">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="cd489-495">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="cd489-496"><strong>Windows XP e Windows Server 2003:  </strong>  Não</span><span class="sxs-lookup"><span data-stu-id="cd489-496"><strong>Windows XP and Windows Server 2003:  </strong>  No</span></span></p>
<p><span data-ttu-id="cd489-497"><strong>Windows Vista:</strong>  Ok</span><span class="sxs-lookup"><span data-stu-id="cd489-497"><strong>Windows Vista:</strong>  Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-498">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="cd489-498">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="cd489-499">No</span><span class="sxs-lookup"><span data-stu-id="cd489-499">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-500">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="cd489-500">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="cd489-501">No</span><span class="sxs-lookup"><span data-stu-id="cd489-501">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-502">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="cd489-502">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="cd489-503">Yes</span><span class="sxs-lookup"><span data-stu-id="cd489-503">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-504">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="cd489-504">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="cd489-505">Yes</span><span class="sxs-lookup"><span data-stu-id="cd489-505">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-506">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="cd489-506">Availability:</span></span></p></td>
<td><p><span data-ttu-id="cd489-507">Windows XP e versões posteriores</span><span class="sxs-lookup"><span data-stu-id="cd489-507">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="cd489-508">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd489-508">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cd489-509"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="cd489-509"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="cd489-510">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="cd489-510">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd489-511"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="cd489-511"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="cd489-512">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="cd489-512">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd489-513"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="cd489-513"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="cd489-514">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="cd489-514">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="cd489-515">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="cd489-515">See Also</span></span>

[<span data-ttu-id="cd489-516">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="cd489-516">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="cd489-517">JetInit</span><span class="sxs-lookup"><span data-stu-id="cd489-517">JetInit</span></span>](./jetinit-function.md)
