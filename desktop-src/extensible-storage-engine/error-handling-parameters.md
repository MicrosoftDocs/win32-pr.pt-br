---
description: 'Saiba mais sobre: parâmetros de tratamento de erros'
title: Parâmetros de tratamento de erros
TOCTitle: Error Handling Parameters
ms:assetid: 014996a1-5674-40c7-9538-54cae1681fec
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269173(v=EXCHG.10)
ms:contentKeyID: 32765476
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: eb225d7dbb67655286635320352060bcf2cb8a5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837247"
---
# <a name="error-handling-parameters"></a><span data-ttu-id="0af10-103">Parâmetros de tratamento de erros</span><span class="sxs-lookup"><span data-stu-id="0af10-103">Error Handling Parameters</span></span>


<span data-ttu-id="0af10-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="0af10-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="error-handling-parameters"></a><span data-ttu-id="0af10-105">Parâmetros de tratamento de erros</span><span class="sxs-lookup"><span data-stu-id="0af10-105">Error Handling Parameters</span></span>

<span data-ttu-id="0af10-106">Este tópico contém parâmetros que são usados para tratamento de erros.</span><span class="sxs-lookup"><span data-stu-id="0af10-106">This topic contains parameters that are used for error handling.</span></span>

<span data-ttu-id="0af10-107">*JET_paramErrorToString* 70</span><span class="sxs-lookup"><span data-stu-id="0af10-107">*JET_paramErrorToString* 70</span></span>  

<span data-ttu-id="0af10-108">Esse parâmetro pode ser usado para converter um [JET_ERR](./jet-err.md) em uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="0af10-108">This parameter can be used to convert a [JET_ERR](./jet-err.md) into a string.</span></span> <span data-ttu-id="0af10-109">Isso é feito usando uma chamada especial para [JetGetSystemParameter](./jetgetsystemparameter-function.md) , em que o buffer de saída de inteiro contém o valor de [JET_ERR](./jet-err.md) a ser convertido (como um parâmetro de entrada) e o buffer de saída de cadeia de caracteres retorna a cadeia de caracteres de erro correspondente.</span><span class="sxs-lookup"><span data-stu-id="0af10-109">This is done using a special call to [JetGetSystemParameter](./jetgetsystemparameter-function.md) where the integer output buffer contains the [JET_ERR](./jet-err.md) value to be converted (as an input parameter) and the string output buffer returns the matching error string.</span></span> <span data-ttu-id="0af10-110">A cadeia de caracteres terá uma aparência semelhante a esta: "JET_errSuccess, operação bem-sucedida".</span><span class="sxs-lookup"><span data-stu-id="0af10-110">The string will look something like this: "JET_errSuccess,Successful Operation".</span></span> <span data-ttu-id="0af10-111">A cadeia de caracteres é composta pelo nome simbólico para a cadeia de caracteres, uma vírgula e uma descrição de texto simples do erro.</span><span class="sxs-lookup"><span data-stu-id="0af10-111">The string is composed of the symbolic name for the string, then a comma, and then a simple text description of the error.</span></span> <span data-ttu-id="0af10-112">A cadeia de caracteres de descrição pode conter vírgulas.</span><span class="sxs-lookup"><span data-stu-id="0af10-112">The description string may itself contain commas.</span></span> <span data-ttu-id="0af10-113">Se o erro não for reconhecido, a cadeia de caracteres será "erro desconhecido, erro desconhecido".</span><span class="sxs-lookup"><span data-stu-id="0af10-113">If the error is not recognized then the string will be "Unknown Error,Unknown Error".</span></span>

<span data-ttu-id="0af10-114">**Observação**  Esse parâmetro é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="0af10-114">**Note**  This parameter is read only.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0af10-115">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="0af10-115">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="0af10-116">Especial</span><span class="sxs-lookup"><span data-stu-id="0af10-116">Special</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0af10-117">Tipo:</span><span class="sxs-lookup"><span data-stu-id="0af10-117">Type:</span></span></p></td>
<td><p><span data-ttu-id="0af10-118">Especial</span><span class="sxs-lookup"><span data-stu-id="0af10-118">Special</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0af10-119">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="0af10-119">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="0af10-120">Especial</span><span class="sxs-lookup"><span data-stu-id="0af10-120">Special</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0af10-121">Escopo:</span><span class="sxs-lookup"><span data-stu-id="0af10-121">Scope:</span></span></p></td>
<td><p><span data-ttu-id="0af10-122">Global</span><span class="sxs-lookup"><span data-stu-id="0af10-122">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0af10-123">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="0af10-123">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="0af10-124">No</span><span class="sxs-lookup"><span data-stu-id="0af10-124">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0af10-125">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="0af10-125">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="0af10-126">No</span><span class="sxs-lookup"><span data-stu-id="0af10-126">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0af10-127">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="0af10-127">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="0af10-128">No</span><span class="sxs-lookup"><span data-stu-id="0af10-128">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0af10-129">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="0af10-129">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="0af10-130">No</span><span class="sxs-lookup"><span data-stu-id="0af10-130">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0af10-131">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="0af10-131">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="0af10-132">No</span><span class="sxs-lookup"><span data-stu-id="0af10-132">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0af10-133">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="0af10-133">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="0af10-134">No</span><span class="sxs-lookup"><span data-stu-id="0af10-134">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0af10-135">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="0af10-135">Availability:</span></span></p></td>
<td><p><span data-ttu-id="0af10-136">Tudo</span><span class="sxs-lookup"><span data-stu-id="0af10-136">All</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0af10-137">*JET_paramExceptionAction*</span><span class="sxs-lookup"><span data-stu-id="0af10-137">*JET_paramExceptionAction*</span></span>  
<span data-ttu-id="0af10-138">98</span><span class="sxs-lookup"><span data-stu-id="0af10-138">98</span></span>  

<span data-ttu-id="0af10-139">Esse parâmetro controla o que acontece quando uma exceção é lançada pelo mecanismo de banco de dados ou pelo código que é chamado pelo mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="0af10-139">This parameter controls what happens when an exception is thrown by the database engine or code that is called by the database engine.</span></span> <span data-ttu-id="0af10-140">Quando definido como JET_ExceptionMsgBox, qualquer exceção será lançada para o filtro de exceção sem tratamento do Windows.</span><span class="sxs-lookup"><span data-stu-id="0af10-140">When set to JET_ExceptionMsgBox, any exception will be thrown to the Windows unhandled exception filter.</span></span> <span data-ttu-id="0af10-141">Isso fará com que a exceção seja tratada como uma falha do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0af10-141">This will result in the exception being handled as an application failure.</span></span> <span data-ttu-id="0af10-142">A intenção é impedir que o código do aplicativo tente detectar erroneamente e ignorar uma exceção gerada pelo mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="0af10-142">The intent is to prevent application code from erroneously trying to catch and ignore an exception generated by the database engine.</span></span> <span data-ttu-id="0af10-143">Isso não pode ser permitido porque a corrupção do banco de dados pode ocorrer.</span><span class="sxs-lookup"><span data-stu-id="0af10-143">This cannot be allowed because database corruption could occur.</span></span> <span data-ttu-id="0af10-144">Se o aplicativo quiser lidar corretamente com essas exceções, a proteção poderá ser desabilitada definindo esse parâmetro como JET_ExceptionNone.</span><span class="sxs-lookup"><span data-stu-id="0af10-144">If the application wishes to properly handle these exceptions then the protection can be disabled by setting this parameter to JET_ExceptionNone.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0af10-145">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="0af10-145">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="0af10-146">JET_ExceptionMsgBox</span><span class="sxs-lookup"><span data-stu-id="0af10-146">JET_ExceptionMsgBox</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0af10-147">Tipo:</span><span class="sxs-lookup"><span data-stu-id="0af10-147">Type:</span></span></p></td>
<td><p><span data-ttu-id="0af10-148">Integer</span><span class="sxs-lookup"><span data-stu-id="0af10-148">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0af10-149">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="0af10-149">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="0af10-150">JET_ExceptionMsgBox, JET_ExceptionNone</span><span class="sxs-lookup"><span data-stu-id="0af10-150">JET_ExceptionMsgBox, JET_ExceptionNone</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0af10-151">Escopo:</span><span class="sxs-lookup"><span data-stu-id="0af10-151">Scope:</span></span></p></td>
<td><p><span data-ttu-id="0af10-152">Global</span><span class="sxs-lookup"><span data-stu-id="0af10-152">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0af10-153">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="0af10-153">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="0af10-154"><strong>Windows 2000, Windows XP e Windows Server 2003:  </strong>  Não</span><span class="sxs-lookup"><span data-stu-id="0af10-154"><strong>Windows 2000, Windows XP and Windows Server 2003:  </strong>  No</span></span></p>
<p><span data-ttu-id="0af10-155"><strong>Windows Vista:</strong>  Ok</span><span class="sxs-lookup"><span data-stu-id="0af10-155"><strong>Windows Vista:</strong>  Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0af10-156">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="0af10-156">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="0af10-157"><strong>Windows 2000, Windows XP e Windows Server 2003:  </strong>  Não</span><span class="sxs-lookup"><span data-stu-id="0af10-157"><strong>Windows 2000, Windows XP and Windows Server 2003:  </strong>  No</span></span></p>
<p><span data-ttu-id="0af10-158"><strong>Windows Vista:</strong>  Ok</span><span class="sxs-lookup"><span data-stu-id="0af10-158"><strong>Windows Vista:</strong>  Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0af10-159">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="0af10-159">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="0af10-160">No</span><span class="sxs-lookup"><span data-stu-id="0af10-160">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0af10-161">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="0af10-161">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="0af10-162">Yes</span><span class="sxs-lookup"><span data-stu-id="0af10-162">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0af10-163">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="0af10-163">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="0af10-164">No</span><span class="sxs-lookup"><span data-stu-id="0af10-164">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0af10-165">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="0af10-165">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="0af10-166">No</span><span class="sxs-lookup"><span data-stu-id="0af10-166">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0af10-167">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="0af10-167">Availability:</span></span></p></td>
<td><p><span data-ttu-id="0af10-168">Tudo</span><span class="sxs-lookup"><span data-stu-id="0af10-168">All</span></span></p></td>
</tr>
</tbody>
</table>

### <a name="requirements"></a><span data-ttu-id="0af10-169">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0af10-169">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0af10-170"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="0af10-170"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="0af10-171">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="0af10-171">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0af10-172"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="0af10-172"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="0af10-173">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="0af10-173">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0af10-174"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="0af10-174"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="0af10-175">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="0af10-175">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

### <a name="see-also"></a><span data-ttu-id="0af10-176">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="0af10-176">See Also</span></span>

[<span data-ttu-id="0af10-177">Constantes de tratamento de erro</span><span class="sxs-lookup"><span data-stu-id="0af10-177">Error Handling Constants</span></span>](./error-handling-constants.md)  
[<span data-ttu-id="0af10-178">Códigos de erro do mecanismo de armazenamento extensível</span><span class="sxs-lookup"><span data-stu-id="0af10-178">Extensible Storage Engine Error Codes</span></span>](./extensible-storage-engine-error-codes.md)  
[<span data-ttu-id="0af10-179">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="0af10-179">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="0af10-180">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="0af10-180">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="0af10-181">JetInit</span><span class="sxs-lookup"><span data-stu-id="0af10-181">JetInit</span></span>](./jetinit-function.md)
