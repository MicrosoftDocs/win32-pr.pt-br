---
description: 'Saiba mais sobre: parâmetros de índice'
title: Parâmetros de Índice
TOCTitle: Index Parameters
ms:assetid: df3dfbc7-71fb-4ae2-a94a-b00eaa1572ec
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294119(v=EXCHG.10)
ms:contentKeyID: 32765733
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
ms.openlocfilehash: 2901887233ff8b25114334c97e6a731072a69ce1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011780"
---
# <a name="index-parameters"></a><span data-ttu-id="c8798-103">Parâmetros de Índice</span><span class="sxs-lookup"><span data-stu-id="c8798-103">Index Parameters</span></span>


<span data-ttu-id="c8798-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c8798-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="index-parameters"></a><span data-ttu-id="c8798-105">Parâmetros de Índice</span><span class="sxs-lookup"><span data-stu-id="c8798-105">Index Parameters</span></span>

<span data-ttu-id="c8798-106">Este tópico contém parâmetros que são usados para o índice.</span><span class="sxs-lookup"><span data-stu-id="c8798-106">This topic contains parameters that are used for the index.</span></span>

<span data-ttu-id="c8798-107">*JET_paramIndexTupleIncrement*</span><span class="sxs-lookup"><span data-stu-id="c8798-107">*JET_paramIndexTupleIncrement*</span></span>  
<span data-ttu-id="c8798-108">132</span><span class="sxs-lookup"><span data-stu-id="c8798-108">132</span></span>  

<span data-ttu-id="c8798-109">Esse parâmetro especifica o padrão para o incremento de deslocamento usado para percorrer o valor da coluna de origem ao gerar cada tupla.</span><span class="sxs-lookup"><span data-stu-id="c8798-109">This parameter specifies the default for the offset increment used to step through the source column value while generating each tuple.</span></span> <span data-ttu-id="c8798-110">Para obter mais informações, consulte a estrutura de [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="c8798-110">For more information, see the [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) structure.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c8798-111">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="c8798-111">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="c8798-112">1</span><span class="sxs-lookup"><span data-stu-id="c8798-112">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8798-113">Tipo:</span><span class="sxs-lookup"><span data-stu-id="c8798-113">Type:</span></span></p></td>
<td><p><span data-ttu-id="c8798-114">Integer</span><span class="sxs-lookup"><span data-stu-id="c8798-114">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8798-115">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="c8798-115">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="c8798-116">0 - 32767</span><span class="sxs-lookup"><span data-stu-id="c8798-116">0 - 32767</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8798-117">Escopo:</span><span class="sxs-lookup"><span data-stu-id="c8798-117">Scope:</span></span></p></td>
<td><p><span data-ttu-id="c8798-118">Instância</span><span class="sxs-lookup"><span data-stu-id="c8798-118">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8798-119">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="c8798-119">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="c8798-120">Yes</span><span class="sxs-lookup"><span data-stu-id="c8798-120">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8798-121">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="c8798-121">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="c8798-122">No</span><span class="sxs-lookup"><span data-stu-id="c8798-122">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8798-123">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="c8798-123">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="c8798-124">No</span><span class="sxs-lookup"><span data-stu-id="c8798-124">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8798-125">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="c8798-125">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="c8798-126">No</span><span class="sxs-lookup"><span data-stu-id="c8798-126">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8798-127">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="c8798-127">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="c8798-128">No</span><span class="sxs-lookup"><span data-stu-id="c8798-128">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8798-129">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="c8798-129">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="c8798-130">No</span><span class="sxs-lookup"><span data-stu-id="c8798-130">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8798-131">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="c8798-131">Availability:</span></span></p></td>
<td><p><span data-ttu-id="c8798-132">Windows Vista e versões posteriores</span><span class="sxs-lookup"><span data-stu-id="c8798-132">Windows Vista and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c8798-133">*JET_paramIndexTupleStart*</span><span class="sxs-lookup"><span data-stu-id="c8798-133">*JET_paramIndexTupleStart*</span></span>  
<span data-ttu-id="c8798-134">133</span><span class="sxs-lookup"><span data-stu-id="c8798-134">133</span></span>  

<span data-ttu-id="c8798-135">Esse parâmetro especifica o padrão para o deslocamento no valor da coluna de origem no qual a geração de tupla será iniciada.</span><span class="sxs-lookup"><span data-stu-id="c8798-135">This parameter specifies the default for the offset in the source column value at which tuple generation will start.</span></span> <span data-ttu-id="c8798-136">Para obter mais informações, consulte a estrutura de [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="c8798-136">For more information, see the [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) structure.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c8798-137">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="c8798-137">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="c8798-138">0</span><span class="sxs-lookup"><span data-stu-id="c8798-138">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8798-139">Tipo:</span><span class="sxs-lookup"><span data-stu-id="c8798-139">Type:</span></span></p></td>
<td><p><span data-ttu-id="c8798-140">Integer</span><span class="sxs-lookup"><span data-stu-id="c8798-140">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8798-141">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="c8798-141">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="c8798-142">0 - 32767</span><span class="sxs-lookup"><span data-stu-id="c8798-142">0 - 32767</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8798-143">Escopo:</span><span class="sxs-lookup"><span data-stu-id="c8798-143">Scope:</span></span></p></td>
<td><p><span data-ttu-id="c8798-144">Instância</span><span class="sxs-lookup"><span data-stu-id="c8798-144">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8798-145">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="c8798-145">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="c8798-146">Yes</span><span class="sxs-lookup"><span data-stu-id="c8798-146">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8798-147">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="c8798-147">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="c8798-148">No</span><span class="sxs-lookup"><span data-stu-id="c8798-148">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8798-149">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="c8798-149">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="c8798-150">No</span><span class="sxs-lookup"><span data-stu-id="c8798-150">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8798-151">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="c8798-151">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="c8798-152">No</span><span class="sxs-lookup"><span data-stu-id="c8798-152">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8798-153">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="c8798-153">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="c8798-154">No</span><span class="sxs-lookup"><span data-stu-id="c8798-154">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8798-155">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="c8798-155">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="c8798-156">No</span><span class="sxs-lookup"><span data-stu-id="c8798-156">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8798-157">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="c8798-157">Availability:</span></span></p></td>
<td><p><span data-ttu-id="c8798-158">Windows Vista e versões posteriores</span><span class="sxs-lookup"><span data-stu-id="c8798-158">Windows Vista and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c8798-159">*JET_paramIndexTuplesLengthMax*</span><span class="sxs-lookup"><span data-stu-id="c8798-159">*JET_paramIndexTuplesLengthMax*</span></span>  
<span data-ttu-id="c8798-160">111</span><span class="sxs-lookup"><span data-stu-id="c8798-160">111</span></span>  

<span data-ttu-id="c8798-161">Esse parâmetro especifica o padrão para o comprimento máximo de tupla em um índice de tupla.</span><span class="sxs-lookup"><span data-stu-id="c8798-161">This parameter specifies the default for the maximum tuple length in a tuple index.</span></span> <span data-ttu-id="c8798-162">Para obter mais informações, consulte a estrutura de [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="c8798-162">For more information, see the [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) structure.</span></span>

<span data-ttu-id="c8798-163">**Windows Vista:**  Antes do Windows Vista, definir esse parâmetro como zero o definiria de volta para seu valor padrão.</span><span class="sxs-lookup"><span data-stu-id="c8798-163">**Windows Vista:**  Prior to Windows Vista, setting this parameter to zero would set it back to its default value.</span></span> <span data-ttu-id="c8798-164">Para o Windows Vista, não há mais suporte para isso.</span><span class="sxs-lookup"><span data-stu-id="c8798-164">For Windows Vista, this is no longer supported.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c8798-165">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="c8798-165">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="c8798-166">10</span><span class="sxs-lookup"><span data-stu-id="c8798-166">10</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8798-167">Tipo:</span><span class="sxs-lookup"><span data-stu-id="c8798-167">Type:</span></span></p></td>
<td><p><span data-ttu-id="c8798-168">Integer</span><span class="sxs-lookup"><span data-stu-id="c8798-168">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8798-169">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="c8798-169">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="c8798-170"><strong>Windows 2000, Windows XP e Windows Server 2003: </strong>  0, 2-255</span><span class="sxs-lookup"><span data-stu-id="c8798-170"><strong>Windows 2000, Windows XP and Windows Server 2003: </strong>  0, 2-255</span></span></p>
<p><span data-ttu-id="c8798-171"><strong>Windows Vista:</strong>  2-255</span><span class="sxs-lookup"><span data-stu-id="c8798-171"><strong>Windows Vista:</strong>  2-255</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8798-172">Escopo:</span><span class="sxs-lookup"><span data-stu-id="c8798-172">Scope:</span></span></p></td>
<td><p><span data-ttu-id="c8798-173">Instância</span><span class="sxs-lookup"><span data-stu-id="c8798-173">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8798-174">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="c8798-174">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="c8798-175">Yes</span><span class="sxs-lookup"><span data-stu-id="c8798-175">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8798-176">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="c8798-176">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="c8798-177">No</span><span class="sxs-lookup"><span data-stu-id="c8798-177">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8798-178">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="c8798-178">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="c8798-179">No</span><span class="sxs-lookup"><span data-stu-id="c8798-179">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8798-180">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="c8798-180">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="c8798-181">No</span><span class="sxs-lookup"><span data-stu-id="c8798-181">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8798-182">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="c8798-182">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="c8798-183">No</span><span class="sxs-lookup"><span data-stu-id="c8798-183">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8798-184">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="c8798-184">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="c8798-185">No</span><span class="sxs-lookup"><span data-stu-id="c8798-185">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8798-186">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="c8798-186">Availability:</span></span></p></td>
<td><p><span data-ttu-id="c8798-187">Windows XP e versões posteriores</span><span class="sxs-lookup"><span data-stu-id="c8798-187">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c8798-188">*JET_paramIndexTuplesLengthMin*</span><span class="sxs-lookup"><span data-stu-id="c8798-188">*JET_paramIndexTuplesLengthMin*</span></span>  
<span data-ttu-id="c8798-189">110</span><span class="sxs-lookup"><span data-stu-id="c8798-189">110</span></span>  

<span data-ttu-id="c8798-190">Esse parâmetro especifica o padrão para o comprimento mínimo de tupla em um índice de tupla.</span><span class="sxs-lookup"><span data-stu-id="c8798-190">This parameter specifies the default for the minimum tuple length in a tuple index.</span></span> <span data-ttu-id="c8798-191">Consulte [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="c8798-191">See [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) for more information.</span></span>

<span data-ttu-id="c8798-192">**Windows Vista:**  Antes do Windows Vista, definir esse parâmetro como zero o definiria de volta para seu valor padrão.</span><span class="sxs-lookup"><span data-stu-id="c8798-192">**Windows Vista:**  Prior to Windows Vista, setting this parameter to zero would set it back to its default value.</span></span> <span data-ttu-id="c8798-193">Para o Windows Vista, não há mais suporte para isso.</span><span class="sxs-lookup"><span data-stu-id="c8798-193">For Windows Vista, this is no longer supported.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c8798-194">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="c8798-194">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="c8798-195">3</span><span class="sxs-lookup"><span data-stu-id="c8798-195">3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8798-196">Tipo:</span><span class="sxs-lookup"><span data-stu-id="c8798-196">Type:</span></span></p></td>
<td><p><span data-ttu-id="c8798-197">Integer</span><span class="sxs-lookup"><span data-stu-id="c8798-197">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8798-198">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="c8798-198">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="c8798-199"><strong>Windows 2000, Windows XP e Windows Server 2003: </strong>  0, 2-255</span><span class="sxs-lookup"><span data-stu-id="c8798-199"><strong>Windows 2000, Windows XP and Windows Server 2003: </strong>  0, 2-255</span></span></p>
<p><span data-ttu-id="c8798-200"><strong>Windows Vista:</strong>  2-255</span><span class="sxs-lookup"><span data-stu-id="c8798-200"><strong>Windows Vista:</strong>  2-255</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8798-201">Escopo:</span><span class="sxs-lookup"><span data-stu-id="c8798-201">Scope:</span></span></p></td>
<td><p><span data-ttu-id="c8798-202">Instância</span><span class="sxs-lookup"><span data-stu-id="c8798-202">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8798-203">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="c8798-203">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="c8798-204">Yes</span><span class="sxs-lookup"><span data-stu-id="c8798-204">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8798-205">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="c8798-205">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="c8798-206">No</span><span class="sxs-lookup"><span data-stu-id="c8798-206">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8798-207">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="c8798-207">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="c8798-208">No</span><span class="sxs-lookup"><span data-stu-id="c8798-208">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8798-209">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="c8798-209">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="c8798-210">No</span><span class="sxs-lookup"><span data-stu-id="c8798-210">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8798-211">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="c8798-211">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="c8798-212">No</span><span class="sxs-lookup"><span data-stu-id="c8798-212">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8798-213">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="c8798-213">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="c8798-214">No</span><span class="sxs-lookup"><span data-stu-id="c8798-214">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8798-215">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="c8798-215">Availability:</span></span></p></td>
<td><p><span data-ttu-id="c8798-216">Windows XP e versões posteriores</span><span class="sxs-lookup"><span data-stu-id="c8798-216">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c8798-217">*JET_paramIndexTuplesToIndexMax*</span><span class="sxs-lookup"><span data-stu-id="c8798-217">*JET_paramIndexTuplesToIndexMax*</span></span>  
<span data-ttu-id="c8798-218">112</span><span class="sxs-lookup"><span data-stu-id="c8798-218">112</span></span>  

<span data-ttu-id="c8798-219">Esse parâmetro especifica o padrão para o comprimento máximo de uma cadeia de caracteres de origem a ser dividida em tuplas para um índice de tupla.</span><span class="sxs-lookup"><span data-stu-id="c8798-219">This parameter specifies the default for the maximum length of a source string to break into tuples for a tuple index.</span></span> <span data-ttu-id="c8798-220">Consulte [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="c8798-220">See [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) for more information.</span></span>

<span data-ttu-id="c8798-221">**Windows Vista:**  Antes do Windows Vista, definir esse parâmetro como zero o definiria de volta para seu valor padrão.</span><span class="sxs-lookup"><span data-stu-id="c8798-221">**Windows Vista:**  Prior to Windows Vista, setting this parameter to zero would set it back to its default value.</span></span> <span data-ttu-id="c8798-222">Para o Windows Vista, não há mais suporte para isso.</span><span class="sxs-lookup"><span data-stu-id="c8798-222">For Windows Vista, this is no longer supported.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c8798-223">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="c8798-223">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="c8798-224">32767</span><span class="sxs-lookup"><span data-stu-id="c8798-224">32767</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8798-225">Tipo:</span><span class="sxs-lookup"><span data-stu-id="c8798-225">Type:</span></span></p></td>
<td><p><span data-ttu-id="c8798-226">Integer</span><span class="sxs-lookup"><span data-stu-id="c8798-226">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8798-227">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="c8798-227">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="c8798-228"><strong>Windows 2000, Windows XP e Windows Server 2003:</strong>  0 – 32767</span><span class="sxs-lookup"><span data-stu-id="c8798-228"><strong>Windows 2000, Windows XP and Windows Server 2003:</strong>  0 – 32767</span></span></p>
<p><span data-ttu-id="c8798-229"><strong>Windows Vista:</strong>  1 a 32767</span><span class="sxs-lookup"><span data-stu-id="c8798-229"><strong>Windows Vista:</strong>  1 – 32767</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8798-230">Escopo:</span><span class="sxs-lookup"><span data-stu-id="c8798-230">Scope:</span></span></p></td>
<td><p><span data-ttu-id="c8798-231">Instância</span><span class="sxs-lookup"><span data-stu-id="c8798-231">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8798-232">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="c8798-232">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="c8798-233">Yes</span><span class="sxs-lookup"><span data-stu-id="c8798-233">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8798-234">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="c8798-234">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="c8798-235">No</span><span class="sxs-lookup"><span data-stu-id="c8798-235">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8798-236">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="c8798-236">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="c8798-237">No</span><span class="sxs-lookup"><span data-stu-id="c8798-237">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8798-238">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="c8798-238">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="c8798-239">No</span><span class="sxs-lookup"><span data-stu-id="c8798-239">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8798-240">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="c8798-240">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="c8798-241">No</span><span class="sxs-lookup"><span data-stu-id="c8798-241">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8798-242">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="c8798-242">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="c8798-243">No</span><span class="sxs-lookup"><span data-stu-id="c8798-243">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8798-244">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="c8798-244">Availability:</span></span></p></td>
<td><p><span data-ttu-id="c8798-245">Windows XP e versões posteriores</span><span class="sxs-lookup"><span data-stu-id="c8798-245">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c8798-246">*JET_paramUnicodeIndexDefault*</span><span class="sxs-lookup"><span data-stu-id="c8798-246">*JET_paramUnicodeIndexDefault*</span></span>  
<span data-ttu-id="c8798-247">72</span><span class="sxs-lookup"><span data-stu-id="c8798-247">72</span></span>  

<span data-ttu-id="c8798-248">Esse parâmetro controla os parâmetros Unicode padrão usados por qualquer índice em uma coluna de chave Unicode.</span><span class="sxs-lookup"><span data-stu-id="c8798-248">This parameter controls the default Unicode parameters used by any index over a Unicode key column.</span></span> <span data-ttu-id="c8798-249">O tipo desse parâmetro é [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) e, na verdade, é passado usando um ponteiro de buffer armazenado no parâmetro Integer de [JetGetSystemParameter](./jetgetsystemparameter-function.md) e [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="c8798-249">The type of this parameter is [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) and is actually passed using a buffer pointer stored in the integer parameter of [JetGetSystemParameter](./jetgetsystemparameter-function.md) and [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span> <span data-ttu-id="c8798-250">O tamanho do buffer deve ser igual ao tamanho de [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) e deve ser passado para [JetGetSystemParameter](./jetgetsystemparameter-function.md) usando o parâmetro de tamanho do buffer de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="c8798-250">The size of the buffer must equal the size of [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) and must be passed to [JetGetSystemParameter](./jetgetsystemparameter-function.md) using the string buffer size parameter.</span></span> <span data-ttu-id="c8798-251">Isso é claramente inconsistente, mas esse é o comportamento desse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="c8798-251">This is clearly inconsistent but that is the behavior of this parameter.</span></span>

<span data-ttu-id="c8798-252">O valor padrão desse parâmetro contém um LCID para a localidade inglês dos EUA e os seguintes sinalizadores [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa): LCMAP_SORTKEY, NORM_IGNORECASE, NORM_IGNOREKANATYPE e NORM_IGNOREWIDTH.</span><span class="sxs-lookup"><span data-stu-id="c8798-252">The default value of this parameter contains an LCID for the U.S. English locale and the following [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa)flags: LCMAP_SORTKEY, NORM_IGNORECASE, NORM_IGNOREKANATYPE, and NORM_IGNOREWIDTH.</span></span>

<span data-ttu-id="c8798-253">**Windows 2000:**  A SORTid no LCID é ignorada.</span><span class="sxs-lookup"><span data-stu-id="c8798-253">**Windows 2000:**  The SORTID in the LCID is ignored.</span></span> <span data-ttu-id="c8798-254">Uma SORTid de SORT_DEFAULT sempre é usada.</span><span class="sxs-lookup"><span data-stu-id="c8798-254">A SORTID of SORT_DEFAULT is always used.</span></span>

<span data-ttu-id="c8798-255">**Windows 2000:**  Os sinalizadores [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) devem conter os seguintes sinalizadores: LCMAP_SORTKEY, NORM_IGNORECASE, NORM_IGNOREKANATYPE e NORM_IGNOREWIDTH.</span><span class="sxs-lookup"><span data-stu-id="c8798-255">**Windows 2000:**  The [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) flags must contain the following flags: LCMAP_SORTKEY, NORM_IGNORECASE, NORM_IGNOREKANATYPE, and NORM_IGNOREWIDTH.</span></span> <span data-ttu-id="c8798-256">Além disso, os sinalizadores [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa)podem conter os seguintes sinalizadores: NORM_IGNORENONSPACE.</span><span class="sxs-lookup"><span data-stu-id="c8798-256">In addition, the [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa)flags may contain the following flags: NORM_IGNORENONSPACE.</span></span>

<span data-ttu-id="c8798-257">**Observação**  Se o seu aplicativo quiser armazenar dados Unicode, é altamente recomendável que você não confie nos parâmetros Unicode padrão para seus índices.</span><span class="sxs-lookup"><span data-stu-id="c8798-257">**Note**  If your application wishes to store Unicode data, then it is strongly recommended that you do not rely on the default Unicode parameters for your indexes.</span></span> <span data-ttu-id="c8798-258">O uso do inglês americano é equivalente o uso da localidade invariável e os sinalizadores de [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa)padrão são conhecidos por sério interferem em alguns idiomas.</span><span class="sxs-lookup"><span data-stu-id="c8798-258">The use of U.S. English is tantamount to using the invariant locale and the default [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa)flags are known to seriously interfere with some languages.</span></span> <span data-ttu-id="c8798-259">Você sempre deve especificar suas próprias configurações para os parâmetros Unicode para JetCreateIndex2 usando [JET_INDEXCREATE](./jet-indexcreate-structure.md).</span><span class="sxs-lookup"><span data-stu-id="c8798-259">You should always specify your own settings for the Unicode parameters to JetCreateIndex2 using [JET_INDEXCREATE](./jet-indexcreate-structure.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c8798-260">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="c8798-260">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="c8798-261">Especial</span><span class="sxs-lookup"><span data-stu-id="c8798-261">Special</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8798-262">Tipo:</span><span class="sxs-lookup"><span data-stu-id="c8798-262">Type:</span></span></p></td>
<td><p><span data-ttu-id="c8798-263">JET_UNICODEINDEX \* (JET_UNICODEINDEX)</span><span class="sxs-lookup"><span data-stu-id="c8798-263">JET_UNICODEINDEX\* (JET_UNICODEINDEX)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8798-264">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="c8798-264">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="c8798-265">Especial</span><span class="sxs-lookup"><span data-stu-id="c8798-265">Special</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8798-266">Escopo:</span><span class="sxs-lookup"><span data-stu-id="c8798-266">Scope:</span></span></p></td>
<td><p><span data-ttu-id="c8798-267">Instância</span><span class="sxs-lookup"><span data-stu-id="c8798-267">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8798-268">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="c8798-268">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="c8798-269">Yes</span><span class="sxs-lookup"><span data-stu-id="c8798-269">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8798-270">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="c8798-270">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="c8798-271">No</span><span class="sxs-lookup"><span data-stu-id="c8798-271">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8798-272">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="c8798-272">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="c8798-273">No</span><span class="sxs-lookup"><span data-stu-id="c8798-273">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8798-274">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="c8798-274">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="c8798-275">No</span><span class="sxs-lookup"><span data-stu-id="c8798-275">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8798-276">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="c8798-276">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="c8798-277">No</span><span class="sxs-lookup"><span data-stu-id="c8798-277">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8798-278">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="c8798-278">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="c8798-279">No</span><span class="sxs-lookup"><span data-stu-id="c8798-279">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8798-280">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="c8798-280">Availability:</span></span></p></td>
<td><p><span data-ttu-id="c8798-281">Tudo</span><span class="sxs-lookup"><span data-stu-id="c8798-281">All</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="c8798-282">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8798-282">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c8798-283"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="c8798-283"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c8798-284">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="c8798-284">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8798-285"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="c8798-285"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c8798-286">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="c8798-286">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8798-287"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="c8798-287"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c8798-288">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="c8798-288">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="c8798-289">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="c8798-289">See Also</span></span>

[<span data-ttu-id="c8798-290">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="c8798-290">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="c8798-291">JET_TUPLELIMITS</span><span class="sxs-lookup"><span data-stu-id="c8798-291">JET_TUPLELIMITS</span></span>](./jet-tuplelimits-structure.md)  
[<span data-ttu-id="c8798-292">JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="c8798-292">JET_UNICODEINDEX</span></span>](./jet-unicodeindex-structure.md)  
[<span data-ttu-id="c8798-293">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="c8798-293">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="c8798-294">JetGetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="c8798-294">JetGetSystemParameter</span></span>](./jetgetsystemparameter-function.md)  
[<span data-ttu-id="c8798-295">JetInit</span><span class="sxs-lookup"><span data-stu-id="c8798-295">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="c8798-296">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="c8798-296">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
