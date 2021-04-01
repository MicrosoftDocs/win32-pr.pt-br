---
description: 'Saiba mais sobre: parâmetros de retorno de chamada'
title: Parâmetros de retorno de chamada
TOCTitle: Callback Parameters
ms:assetid: 7f3cdc13-ffbd-4e5a-b650-1c6388e784dc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269310(v=EXCHG.10)
ms:contentKeyID: 32765600
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
ms.openlocfilehash: 4e06ed65bbeae195060e4de10424a76a4228f20f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090902"
---
# <a name="callback-parameters"></a><span data-ttu-id="60e05-103">Parâmetros de retorno de chamada</span><span class="sxs-lookup"><span data-stu-id="60e05-103">Callback Parameters</span></span>


<span data-ttu-id="60e05-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="60e05-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="callback-parameters"></a><span data-ttu-id="60e05-105">Parâmetros de retorno de chamada</span><span class="sxs-lookup"><span data-stu-id="60e05-105">Callback Parameters</span></span>

<span data-ttu-id="60e05-106">Este tópico contém parâmetros que são usados para retornos de chamada.</span><span class="sxs-lookup"><span data-stu-id="60e05-106">This topic contains parameters that are used for callbacks.</span></span>

<span data-ttu-id="60e05-107">*JET_paramDisableCallbacks*</span><span class="sxs-lookup"><span data-stu-id="60e05-107">*JET_paramDisableCallbacks*</span></span>  
<span data-ttu-id="60e05-108">65</span><span class="sxs-lookup"><span data-stu-id="60e05-108">65</span></span>  

<span data-ttu-id="60e05-109">Esse parâmetro desabilita todos os retornos de chamada do mecanismo de banco de dados para as funções fornecidas pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="60e05-109">This parameter disables all database engine callbacks to application provided functions.</span></span> <span data-ttu-id="60e05-110">Ele destina-se principalmente a dar suporte aos utilitários do mecanismo de banco de dados e não deve ser usado em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="60e05-110">It is primarily intended to support the database engine utilities and is not intended to be used in your application.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="60e05-111">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="60e05-111">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="60e05-112">Falso</span><span class="sxs-lookup"><span data-stu-id="60e05-112">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60e05-113">Tipo:</span><span class="sxs-lookup"><span data-stu-id="60e05-113">Type:</span></span></p></td>
<td><p><span data-ttu-id="60e05-114">Boolean</span><span class="sxs-lookup"><span data-stu-id="60e05-114">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60e05-115">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="60e05-115">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="60e05-116">Falso, verdadeiro</span><span class="sxs-lookup"><span data-stu-id="60e05-116">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60e05-117">Escopo:</span><span class="sxs-lookup"><span data-stu-id="60e05-117">Scope:</span></span></p></td>
<td><p><span data-ttu-id="60e05-118">Instância</span><span class="sxs-lookup"><span data-stu-id="60e05-118">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60e05-119">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="60e05-119">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="60e05-120">Sim</span><span class="sxs-lookup"><span data-stu-id="60e05-120">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60e05-121">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="60e05-121">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="60e05-122">Não</span><span class="sxs-lookup"><span data-stu-id="60e05-122">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60e05-123">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="60e05-123">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="60e05-124">Não</span><span class="sxs-lookup"><span data-stu-id="60e05-124">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60e05-125">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="60e05-125">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="60e05-126">Não</span><span class="sxs-lookup"><span data-stu-id="60e05-126">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60e05-127">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="60e05-127">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="60e05-128">Não</span><span class="sxs-lookup"><span data-stu-id="60e05-128">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60e05-129">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="60e05-129">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="60e05-130">Não</span><span class="sxs-lookup"><span data-stu-id="60e05-130">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60e05-131">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="60e05-131">Availability:</span></span></p></td>
<td><p><span data-ttu-id="60e05-132">Windows XP e versões posteriores</span><span class="sxs-lookup"><span data-stu-id="60e05-132">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="60e05-133">*JET_paramEnablePersistedCallbacks*</span><span class="sxs-lookup"><span data-stu-id="60e05-133">*JET_paramEnablePersistedCallbacks*</span></span>  
<span data-ttu-id="60e05-134">156</span><span class="sxs-lookup"><span data-stu-id="60e05-134">156</span></span>  

<span data-ttu-id="60e05-135">Esse parâmetro habilita o uso de retornos de chamada persistentes no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="60e05-135">This parameter enables the use of persistent callbacks in the database.</span></span> <span data-ttu-id="60e05-136">Em versões anteriores ao Windows Vista, o uso de retornos de chamada persistentes foi habilitado por padrão.</span><span class="sxs-lookup"><span data-stu-id="60e05-136">In releases prior to Windows Vista, the use of persistent callbacks was enabled by default.</span></span> <span data-ttu-id="60e05-137">Agora, os aplicativos devem habilitar explicitamente o uso de retornos de chamada persistentes em tempo de execução usando esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="60e05-137">Applications must now explicitly enable the use of persistent callbacks at runtime using this parameter.</span></span> <span data-ttu-id="60e05-138">Se esse parâmetro não for definido, qualquer operação de banco de dados que exija a invocação de um retorno de chamada falhará com JET_errCallbackFailed.</span><span class="sxs-lookup"><span data-stu-id="60e05-138">If this parameter is not set, then any database operation that requires the invocation of a callback will fail with JET_errCallbackFailed.</span></span> <span data-ttu-id="60e05-139">Esse parâmetro não afeta nenhum retorno de chamada especificado em tempo de execução com os seguintes mecanismos: JET_paramRuntimeCallback, [JetRegisterCallback](./jetregistercallback-function.md)ou um parâmetro de retorno de chamada explícito para uma API do Jet.</span><span class="sxs-lookup"><span data-stu-id="60e05-139">This parameter does not affect any callbacks that are specified at runtime with the following mechanisms: JET_paramRuntimeCallback, [JetRegisterCallback](./jetregistercallback-function.md), or an explicit callback parameter to a JET API.</span></span> <span data-ttu-id="60e05-140">Ainda é possível criar elementos de esquema que contenham retornos de chamada persistentes mesmo quando o uso desses retornos de chamada persistentes não é permitido.</span><span class="sxs-lookup"><span data-stu-id="60e05-140">It is still possible to create schema elements that contain persistent callbacks even when the use of those persistent callbacks is disallowed.</span></span> <span data-ttu-id="60e05-141">Quando esse parâmetro é definido como false, ele substitui JET_paramDisableCallbacks.</span><span class="sxs-lookup"><span data-stu-id="60e05-141">When this parameter is set to false it overrides JET_paramDisableCallbacks.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="60e05-142">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="60e05-142">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="60e05-143">Falso</span><span class="sxs-lookup"><span data-stu-id="60e05-143">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60e05-144">Tipo:</span><span class="sxs-lookup"><span data-stu-id="60e05-144">Type:</span></span></p></td>
<td><p><span data-ttu-id="60e05-145">Boolean</span><span class="sxs-lookup"><span data-stu-id="60e05-145">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60e05-146">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="60e05-146">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="60e05-147">Falso, verdadeiro</span><span class="sxs-lookup"><span data-stu-id="60e05-147">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60e05-148">Escopo:</span><span class="sxs-lookup"><span data-stu-id="60e05-148">Scope:</span></span></p></td>
<td><p><span data-ttu-id="60e05-149">Instância</span><span class="sxs-lookup"><span data-stu-id="60e05-149">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60e05-150">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="60e05-150">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="60e05-151">Sim</span><span class="sxs-lookup"><span data-stu-id="60e05-151">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60e05-152">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="60e05-152">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="60e05-153">Não</span><span class="sxs-lookup"><span data-stu-id="60e05-153">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60e05-154">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="60e05-154">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="60e05-155">Não</span><span class="sxs-lookup"><span data-stu-id="60e05-155">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60e05-156">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="60e05-156">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="60e05-157">Não</span><span class="sxs-lookup"><span data-stu-id="60e05-157">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60e05-158">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="60e05-158">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="60e05-159">Não</span><span class="sxs-lookup"><span data-stu-id="60e05-159">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60e05-160">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="60e05-160">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="60e05-161">Não</span><span class="sxs-lookup"><span data-stu-id="60e05-161">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60e05-162">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="60e05-162">Availability:</span></span></p></td>
<td><p><span data-ttu-id="60e05-163">Windows Vista e versões posteriores</span><span class="sxs-lookup"><span data-stu-id="60e05-163">Windows Vista and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="60e05-164">*JET_paramRuntimeCallback*</span><span class="sxs-lookup"><span data-stu-id="60e05-164">*JET_paramRuntimeCallback*</span></span>  
<span data-ttu-id="60e05-165">73</span><span class="sxs-lookup"><span data-stu-id="60e05-165">73</span></span>  

<span data-ttu-id="60e05-166">Esse parâmetro configura o mecanismo com uma função de retorno de chamada de tempo de execução implementando a interface [JET_CALLBACK](./jet-callback-callback-function.md) .</span><span class="sxs-lookup"><span data-stu-id="60e05-166">This parameter configures the engine with a runtime callback function implementing the [JET_CALLBACK](./jet-callback-callback-function.md) interface.</span></span> <span data-ttu-id="60e05-167">Esse retorno de chamada pode ser chamado pelos seguintes motivos: [JET_cbtypFreeCursorLS](./jet-cbtyp.md), [JET_cbtypFreeTableLS](./jet-cbtyp.md)ou [JET_cbtypNull](./jet-cbtyp.md).</span><span class="sxs-lookup"><span data-stu-id="60e05-167">This callback may be called for the following reasons: [JET_cbtypFreeCursorLS](./jet-cbtyp.md), [JET_cbtypFreeTableLS](./jet-cbtyp.md), or [JET_cbtypNull](./jet-cbtyp.md).</span></span> <span data-ttu-id="60e05-168">Consulte [JetSetLS](./jetsetls-function.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="60e05-168">Please see [JetSetLS](./jetsetls-function.md) for more information.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="60e05-169">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="60e05-169">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="60e05-170">NULO</span><span class="sxs-lookup"><span data-stu-id="60e05-170">NULL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60e05-171">Tipo:</span><span class="sxs-lookup"><span data-stu-id="60e05-171">Type:</span></span></p></td>
<td><p><span data-ttu-id="60e05-172">Ponteiro de função (JET_API_PTR)</span><span class="sxs-lookup"><span data-stu-id="60e05-172">Function Pointer (JET_API_PTR)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60e05-173">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="60e05-173">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="60e05-174">NULL, <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>\*</span><span class="sxs-lookup"><span data-stu-id="60e05-174">NULL, <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>\*</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60e05-175">Escopo:</span><span class="sxs-lookup"><span data-stu-id="60e05-175">Scope:</span></span></p></td>
<td><p><span data-ttu-id="60e05-176">Instância</span><span class="sxs-lookup"><span data-stu-id="60e05-176">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60e05-177">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="60e05-177">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="60e05-178">Sim</span><span class="sxs-lookup"><span data-stu-id="60e05-178">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60e05-179">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="60e05-179">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="60e05-180">Não</span><span class="sxs-lookup"><span data-stu-id="60e05-180">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60e05-181">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="60e05-181">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="60e05-182">Não</span><span class="sxs-lookup"><span data-stu-id="60e05-182">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60e05-183">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="60e05-183">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="60e05-184">Não</span><span class="sxs-lookup"><span data-stu-id="60e05-184">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60e05-185">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="60e05-185">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="60e05-186">Não</span><span class="sxs-lookup"><span data-stu-id="60e05-186">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60e05-187">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="60e05-187">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="60e05-188">Não</span><span class="sxs-lookup"><span data-stu-id="60e05-188">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60e05-189">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="60e05-189">Availability:</span></span></p></td>
<td><p><span data-ttu-id="60e05-190">Windows XP e versões posteriores</span><span class="sxs-lookup"><span data-stu-id="60e05-190">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="60e05-191">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60e05-191">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="60e05-192"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="60e05-192"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="60e05-193">Requer o Windows Vista ou o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="60e05-193">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60e05-194"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="60e05-194"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="60e05-195">Requer o Windows Server 2008 ou o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="60e05-195">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60e05-196"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="60e05-196"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="60e05-197">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="60e05-197">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="60e05-198">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="60e05-198">See Also</span></span>

[<span data-ttu-id="60e05-199">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="60e05-199">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="60e05-200">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="60e05-200">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)  
[<span data-ttu-id="60e05-201">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="60e05-201">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="60e05-202">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="60e05-202">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="60e05-203">JetInit</span><span class="sxs-lookup"><span data-stu-id="60e05-203">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="60e05-204">JetSetLS</span><span class="sxs-lookup"><span data-stu-id="60e05-204">JetSetLS</span></span>](./jetsetls-function.md)
