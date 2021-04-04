---
description: 'Saiba mais sobre: parâmetros informativos'
title: Parâmetros informativos
TOCTitle: Informational Parameters
ms:assetid: 48500fc9-6d89-45b8-92ad-afb997b729f3
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269241(v=EXCHG.10)
ms:contentKeyID: 32765543
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
ms.openlocfilehash: a8923b544726e474775684f54fed47d8b4ba281e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647604"
---
# <a name="informational-parameters"></a><span data-ttu-id="6c105-103">Parâmetros informativos</span><span class="sxs-lookup"><span data-stu-id="6c105-103">Informational Parameters</span></span>


<span data-ttu-id="6c105-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="6c105-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="informational-parameters"></a><span data-ttu-id="6c105-105">Parâmetros informativos</span><span class="sxs-lookup"><span data-stu-id="6c105-105">Informational Parameters</span></span>

<span data-ttu-id="6c105-106">Este tópico contém parâmetros que são usados para expor informações sobre o mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6c105-106">This topic contains parameters that are used to expose information about the database engine.</span></span>

<span data-ttu-id="6c105-107">*JET_paramKeyMost*</span><span class="sxs-lookup"><span data-stu-id="6c105-107">*JET_paramKeyMost*</span></span>  
<span data-ttu-id="6c105-108">134</span><span class="sxs-lookup"><span data-stu-id="6c105-108">134</span></span>  

<span data-ttu-id="6c105-109">Esse parâmetro somente leitura indica o comprimento máximo de chave de índice permitido que pode ser selecionado para o tamanho da página do banco de dados atual (conforme configurado por JET_paramDatabasePageSize).</span><span class="sxs-lookup"><span data-stu-id="6c105-109">This read-only parameter indicates the maximum allowable index key length that can be selected for the current database page size (as configured by JET_paramDatabasePageSize).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c105-110">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="6c105-110">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="6c105-111">JET_cbKeyMost4KBytePage</span><span class="sxs-lookup"><span data-stu-id="6c105-111">JET_cbKeyMost4KBytePage</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c105-112">Tipo:</span><span class="sxs-lookup"><span data-stu-id="6c105-112">Type:</span></span></p></td>
<td><p><span data-ttu-id="6c105-113">Integer</span><span class="sxs-lookup"><span data-stu-id="6c105-113">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c105-114">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="6c105-114">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="6c105-115">255 – 65535</span><span class="sxs-lookup"><span data-stu-id="6c105-115">255 – 65535</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c105-116">Escopo:</span><span class="sxs-lookup"><span data-stu-id="6c105-116">Scope:</span></span></p></td>
<td><p><span data-ttu-id="6c105-117">Global</span><span class="sxs-lookup"><span data-stu-id="6c105-117">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c105-118">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="6c105-118">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="6c105-119">N/D</span><span class="sxs-lookup"><span data-stu-id="6c105-119">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c105-120">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="6c105-120">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="6c105-121">N/D</span><span class="sxs-lookup"><span data-stu-id="6c105-121">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c105-122">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="6c105-122">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="6c105-123">Não</span><span class="sxs-lookup"><span data-stu-id="6c105-123">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c105-124">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="6c105-124">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="6c105-125">Não</span><span class="sxs-lookup"><span data-stu-id="6c105-125">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c105-126">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="6c105-126">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="6c105-127">Não</span><span class="sxs-lookup"><span data-stu-id="6c105-127">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c105-128">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="6c105-128">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="6c105-129">Não</span><span class="sxs-lookup"><span data-stu-id="6c105-129">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c105-130">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="6c105-130">Availability:</span></span></p></td>
<td><p><span data-ttu-id="6c105-131">Começando com o Windows Server 2008 e o Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6c105-131">Starting with Windows Server 2008 and Windows Vista</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6c105-132">*JET_paramMaxColtyp*</span><span class="sxs-lookup"><span data-stu-id="6c105-132">*JET_paramMaxColtyp*</span></span>  
<span data-ttu-id="6c105-133">131</span><span class="sxs-lookup"><span data-stu-id="6c105-133">131</span></span>  

<span data-ttu-id="6c105-134">Esse parâmetro somente leitura retorna o [JET_COLTYP](./jet-coltyp.md) máximo (JET_coltypMax) para essa versão do mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6c105-134">This read only parameter returns the maximum [JET_COLTYP](./jet-coltyp.md) (JET_coltypMax) for that version of the database engine.</span></span> <span data-ttu-id="6c105-135">Esse valor pode ser usado para testar o suporte de um [JET_COLTYP](./jet-coltyp.md)específico.</span><span class="sxs-lookup"><span data-stu-id="6c105-135">This value can be used to test for support of a specific [JET_COLTYP](./jet-coltyp.md).</span></span> <span data-ttu-id="6c105-136">Se um determinado [JET_COLTYP](./jet-coltyp.md) for menor que o valor desse parâmetro, ele será suportado pelo mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6c105-136">If a given [JET_COLTYP](./jet-coltyp.md) is less than the value of this parameter then it is supported by the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c105-137">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="6c105-137">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="6c105-138">JET_coltypUnsignedShort + 1</span><span class="sxs-lookup"><span data-stu-id="6c105-138">JET_coltypUnsignedShort + 1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c105-139">Tipo:</span><span class="sxs-lookup"><span data-stu-id="6c105-139">Type:</span></span></p></td>
<td><p><span data-ttu-id="6c105-140">Integer</span><span class="sxs-lookup"><span data-stu-id="6c105-140">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c105-141">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="6c105-141">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="6c105-142">0 a 255</span><span class="sxs-lookup"><span data-stu-id="6c105-142">0 – 255</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c105-143">Escopo:</span><span class="sxs-lookup"><span data-stu-id="6c105-143">Scope:</span></span></p></td>
<td><p><span data-ttu-id="6c105-144">Global</span><span class="sxs-lookup"><span data-stu-id="6c105-144">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c105-145">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="6c105-145">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="6c105-146">N/D</span><span class="sxs-lookup"><span data-stu-id="6c105-146">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c105-147">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="6c105-147">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="6c105-148">N/D</span><span class="sxs-lookup"><span data-stu-id="6c105-148">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c105-149">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="6c105-149">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="6c105-150">Não</span><span class="sxs-lookup"><span data-stu-id="6c105-150">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c105-151">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="6c105-151">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="6c105-152">Não</span><span class="sxs-lookup"><span data-stu-id="6c105-152">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c105-153">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="6c105-153">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="6c105-154">Não</span><span class="sxs-lookup"><span data-stu-id="6c105-154">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c105-155">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="6c105-155">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="6c105-156">Não</span><span class="sxs-lookup"><span data-stu-id="6c105-156">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c105-157">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="6c105-157">Availability:</span></span></p></td>
<td><p><span data-ttu-id="6c105-158">Começando com o Windows Server 2008 e o Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6c105-158">Starting with Windows Server 2008 and Windows Vista</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6c105-159">*JET_paramLVChunkSizeMost*</span><span class="sxs-lookup"><span data-stu-id="6c105-159">*JET_paramLVChunkSizeMost*</span></span>  
<span data-ttu-id="6c105-160">163</span><span class="sxs-lookup"><span data-stu-id="6c105-160">163</span></span>  

<span data-ttu-id="6c105-161">Parâmetro somente leitura que retorna o tamanho da parte de valor longo com base no tamanho da página configurada.</span><span class="sxs-lookup"><span data-stu-id="6c105-161">Read only parameter that returns the long-value chunk size based on configured page size.</span></span> <span data-ttu-id="6c105-162">Se um valor longo for para ser lido ou gravado com várias chamadas de coluna Jet {Set, Retrieve}, o uso de um buffer cujo tamanho é um múltiplo do tamanho da parte é mais eficiente.</span><span class="sxs-lookup"><span data-stu-id="6c105-162">If a long-value is to be read or written with multiple Jet{Set,Retrieve}Column calls then using a buffer whose size is a multiple of the chunk size is more efficient.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c105-163">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="6c105-163">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="6c105-164">2 KB página = 1966 bytes</span><span class="sxs-lookup"><span data-stu-id="6c105-164">2kb page = 1966 bytes</span></span><br />
<span data-ttu-id="6c105-165">página de 4 KB = 4014 bytes</span><span class="sxs-lookup"><span data-stu-id="6c105-165">4kb page = 4014 bytes</span></span><br />
<span data-ttu-id="6c105-166">8 KB página = 8110 bytes</span><span class="sxs-lookup"><span data-stu-id="6c105-166">8kb page = 8110 bytes</span></span><br />
<span data-ttu-id="6c105-167">16 KB página = 4050 bytes</span><span class="sxs-lookup"><span data-stu-id="6c105-167">16kb page = 4050 bytes</span></span><br />
<span data-ttu-id="6c105-168">32 KB página = 8150 bytes</span><span class="sxs-lookup"><span data-stu-id="6c105-168">32kb page = 8150 bytes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c105-169">Tipo:</span><span class="sxs-lookup"><span data-stu-id="6c105-169">Type:</span></span></p></td>
<td><p><span data-ttu-id="6c105-170">Integer</span><span class="sxs-lookup"><span data-stu-id="6c105-170">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c105-171">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="6c105-171">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="6c105-172">0-10000</span><span class="sxs-lookup"><span data-stu-id="6c105-172">0-10000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c105-173">Escopo:</span><span class="sxs-lookup"><span data-stu-id="6c105-173">Scope:</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c105-174">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="6c105-174">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c105-175">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="6c105-175">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c105-176">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="6c105-176">Affects Physical Layout:</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c105-177">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="6c105-177">Affects Reliability:</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c105-178">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="6c105-178">Affects Performance:</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c105-179">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="6c105-179">Affects Resources:</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c105-180">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="6c105-180">Availability:</span></span></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="6c105-181">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c105-181">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c105-182"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="6c105-182"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="6c105-183">Requer o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6c105-183">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c105-184"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="6c105-184"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="6c105-185">Requer o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="6c105-185">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c105-186"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="6c105-186"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="6c105-187">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="6c105-187">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="6c105-188">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="6c105-188">See Also</span></span>

[<span data-ttu-id="6c105-189">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="6c105-189">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="6c105-190">JetInit</span><span class="sxs-lookup"><span data-stu-id="6c105-190">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="6c105-191">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="6c105-191">JET_COLTYP</span></span>](./jet-coltyp.md)
