---
description: 'Saiba mais sobre: enumeração de JET_ERRCAT'
title: Enumeração de JET_ERRCAT (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: JET_ERRCAT enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_errcat(v=EXCHG.10)
ms:contentKeyID: 55104419
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Api
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Corruption
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Data
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Disk
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Error
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Fatal
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Fragmentation
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Inconsistent
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Memory
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Resource
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.State
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Usage
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Operation
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Obsolete
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Quota
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Max
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.IO
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Unknown
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Max
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Obsolete
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Unknown
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Operation
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Usage
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Disk
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.IO
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Error
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Resource
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Api
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Data
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Inconsistent
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Quota
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Corruption
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Fragmentation
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Memory
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Fatal
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.State
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e08ec4ce308003dc30edaa32a07000e244dc9f37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169796"
---
# <a name="jet_errcat-enumeration"></a><span data-ttu-id="caa8a-103">Enumeração de JET_ERRCAT</span><span class="sxs-lookup"><span data-stu-id="caa8a-103">JET_ERRCAT enumeration</span></span>

<span data-ttu-id="caa8a-104">A categoria de erro.</span><span class="sxs-lookup"><span data-stu-id="caa8a-104">The error category.</span></span> <span data-ttu-id="caa8a-105">A hierarquia é a seguinte: JET_errcatError | |--JET_errcatOperation | |--JET_errcatFatal | |--JET_errcatIO//problemas de e/s inválidos, pode ou não ser transitório.</span><span class="sxs-lookup"><span data-stu-id="caa8a-105">The hierarchy is as follows: JET_errcatError | |-- JET_errcatOperation | |-- JET_errcatFatal | |-- JET_errcatIO // bad IO issues, may or may not be transient.</span></span> <span data-ttu-id="caa8a-106">| |--JET_errcatResource | |--JET_errcatMemory//memória insuficiente (todas as variantes) | |--JET_errcatQuota | |--JET_errcatDisk//sem espaço em disco (todas as variantes) |--JET_errcatData | |--JET_errcatCorruption | |--JET_errcatInconsistent//normalmente causado por um usuário indisponível | |--JET_errcatFragmentation |--JET_errcatApi |--JET_errcatUsage |--JET_errcatState |--JET_errcatObsolete</span><span class="sxs-lookup"><span data-stu-id="caa8a-106">| |-- JET_errcatResource | |-- JET_errcatMemory // out of memory (all variants) | |-- JET_errcatQuota | |-- JET_errcatDisk // out of disk space (all variants) |-- JET_errcatData | |-- JET_errcatCorruption | |-- JET_errcatInconsistent // typically caused by user Mishandling | |-- JET_errcatFragmentation |-- JET_errcatApi |-- JET_errcatUsage |-- JET_errcatState |-- JET_errcatObsolete</span></span>

<span data-ttu-id="caa8a-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="caa8a-107">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="caa8a-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="caa8a-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="caa8a-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="caa8a-109">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_ERRCAT
'Usage
Dim instance As JET_ERRCAT
```

``` csharp
public enum JET_ERRCAT
```

## <a name="members"></a><span data-ttu-id="caa8a-110">Membros</span><span class="sxs-lookup"><span data-stu-id="caa8a-110">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="caa8a-111">Nome do membro</span><span class="sxs-lookup"><span data-stu-id="caa8a-111">Member name</span></span></th>
<th><span data-ttu-id="caa8a-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="caa8a-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="caa8a-113">Unknown</span><span class="sxs-lookup"><span data-stu-id="caa8a-113">Unknown</span></span></td>
<td><span data-ttu-id="caa8a-114">Categoria desconhecida.</span><span class="sxs-lookup"><span data-stu-id="caa8a-114">Unknown category.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="caa8a-115">Erro</span><span class="sxs-lookup"><span data-stu-id="caa8a-115">Error</span></span></td>
<td><span data-ttu-id="caa8a-116">Uma categoria genérica.</span><span class="sxs-lookup"><span data-stu-id="caa8a-116">A generic category.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="caa8a-117">Operação</span><span class="sxs-lookup"><span data-stu-id="caa8a-117">Operation</span></span></td>
<td><span data-ttu-id="caa8a-118">Erros que geralmente podem ocorrer a qualquer momento devido a condições não controláveis.</span><span class="sxs-lookup"><span data-stu-id="caa8a-118">Errors that can usually happen any time due to uncontrollable conditions.</span></span> <span data-ttu-id="caa8a-119">Geralmente temporário, mas nem sempre.</span><span class="sxs-lookup"><span data-stu-id="caa8a-119">Frequently temporary, but not always.</span></span> <span data-ttu-id="caa8a-120">Recuperação: provavelmente tentar novamente ou, eventualmente, informar o operador.</span><span class="sxs-lookup"><span data-stu-id="caa8a-120">Recovery: Probably retry, or eventually inform the operator.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="caa8a-121">Fatais</span><span class="sxs-lookup"><span data-stu-id="caa8a-121">Fatal</span></span></td>
<td><span data-ttu-id="caa8a-122">Esse erro de classificação ocorre somente quando o ESE encontra uma condição de erro tão grave, que não podemos continuar em uma maneira segura (geralmente transacional) e em vez de dados corrompidos que lançamos erros dessa categoria.</span><span class="sxs-lookup"><span data-stu-id="caa8a-122">This sort error happens only when ESE encounters an error condition so grave, that we can not continue on in a safe (often transactional) way, and rather than corrupt data we throw errors of this category.</span></span> <span data-ttu-id="caa8a-123">Recuperação: reinicie a instância ou o processo.</span><span class="sxs-lookup"><span data-stu-id="caa8a-123">Recovery: Restart the instance or process.</span></span> <span data-ttu-id="caa8a-124">Se o problema persistir, informe o operador.</span><span class="sxs-lookup"><span data-stu-id="caa8a-124">If the problem persists inform the operator.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="caa8a-125">IO</span><span class="sxs-lookup"><span data-stu-id="caa8a-125">IO</span></span></td>
<td><span data-ttu-id="caa8a-126">Os erros são provenientes do sistema operacional e estão fora do controle do ESE, esse tipo de erro é possivelmente temporário, possivelmente não.</span><span class="sxs-lookup"><span data-stu-id="caa8a-126">O errors come from the OS, and are out of ESE's control, this sort of error is possibly temporary, possibly not.</span></span> <span data-ttu-id="caa8a-127">Recuperação: tente novamente.</span><span class="sxs-lookup"><span data-stu-id="caa8a-127">Recovery: Retry.</span></span> <span data-ttu-id="caa8a-128">Se não for resolvido, pergunte ao operador sobre o problema do disco.</span><span class="sxs-lookup"><span data-stu-id="caa8a-128">If not resolved, ask operator about disk issue.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="caa8a-129">Recurso</span><span class="sxs-lookup"><span data-stu-id="caa8a-129">Resource</span></span></td>
<td><span data-ttu-id="caa8a-130">Essa é uma categoria que indica uma das muitas condições de fora do recurso em potencial.</span><span class="sxs-lookup"><span data-stu-id="caa8a-130">This is a category that indicates one of many potential out-of-resource conditions.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="caa8a-131">Memória</span><span class="sxs-lookup"><span data-stu-id="caa8a-131">Memory</span></span></td>
<td><span data-ttu-id="caa8a-132">Condição clássica de memória insuficiente.</span><span class="sxs-lookup"><span data-stu-id="caa8a-132">Classic out of memory condition.</span></span> <span data-ttu-id="caa8a-133">Recuperação: Aguarde um momento e tente novamente, libere memória ou saia.</span><span class="sxs-lookup"><span data-stu-id="caa8a-133">Recovery: Wait a while and retry, free up memory, or quit.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="caa8a-134">Quota</span><span class="sxs-lookup"><span data-stu-id="caa8a-134">Quota</span></span></td>
<td><span data-ttu-id="caa8a-135">Determinados &quot; &quot; recursos de especialidade estão em pools de um determinado tamanho, facilitando a detecção de vazamentos desses recursos.</span><span class="sxs-lookup"><span data-stu-id="caa8a-135">Certain &quot;specialty&quot; resources are in pools of a certain size, making it easier to detect leaks of these resources.</span></span> <span data-ttu-id="caa8a-136">Recuperação: pode exigir algumas alterações de código secundárias.</span><span class="sxs-lookup"><span data-stu-id="caa8a-136">Recovery: Might require some minor code changes.</span></span> <span data-ttu-id="caa8a-137">Seu aplicativo deve ter uma ação de depuração apenas, como uma declaração, nessas condições para detectá-los durante o desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="caa8a-137">Your application should have a debug only action, such as an Assert, on these conditions in order to detect them during development.</span></span> <span data-ttu-id="caa8a-138">Para o código de varejo, recomendamos que você trate esse erro como o erro de categoria de memória e tente novamente, libere memória ou saia da operação.</span><span class="sxs-lookup"><span data-stu-id="caa8a-138">For retail code, we recommend that you treat this error like the Memory category error and either retry, free up memory, or quit the operation.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="caa8a-139">Disco</span><span class="sxs-lookup"><span data-stu-id="caa8a-139">Disk</span></span></td>
<td><span data-ttu-id="caa8a-140">Sem condições de disco.</span><span class="sxs-lookup"><span data-stu-id="caa8a-140">Out of disk conditions.</span></span> <span data-ttu-id="caa8a-141">Recuperação: pode tentar novamente mais tarde na esperança de mais espaço disponível ou peça ao operador para liberar espaço em disco.</span><span class="sxs-lookup"><span data-stu-id="caa8a-141">Recovery: Can retry later in the hope more space is available, or ask the operator to free some disk space.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="caa8a-142">Dados</span><span class="sxs-lookup"><span data-stu-id="caa8a-142">Data</span></span></td>
<td><span data-ttu-id="caa8a-143">Um erro relacionado a dados.</span><span class="sxs-lookup"><span data-stu-id="caa8a-143">A data-related error.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="caa8a-144">Danos</span><span class="sxs-lookup"><span data-stu-id="caa8a-144">Corruption</span></span></td>
<td><span data-ttu-id="caa8a-145">Minha unidade de disco rígido me tenho minha casa.</span><span class="sxs-lookup"><span data-stu-id="caa8a-145">My hard drive ate my homework.</span></span> <span data-ttu-id="caa8a-146">Problemas de corrupção clássicos, frequentemente permanentes sem ação corretiva.</span><span class="sxs-lookup"><span data-stu-id="caa8a-146">Classic corruption issues, frequently permanent without corrective action.</span></span> <span data-ttu-id="caa8a-147">Recuperação: restauração a partir do backup, talvez a operação de reparo de utilitários ESE (que apenas recupera quais dados são deixados/perdidos). Também no caso de recuperação (JetInit), talvez a recuperação possa ser realizada, permitindo a perda de dados.</span><span class="sxs-lookup"><span data-stu-id="caa8a-147">Recovery: Restore from backup, perhaps the ese utilities repair operation (which only salvages what data is left / lossy) .Also in the case of recovery(JetInit) perhaps recovery can be performed by allowing data loss.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="caa8a-148">Inconsistente</span><span class="sxs-lookup"><span data-stu-id="caa8a-148">Inconsistent</span></span></td>
<td><span data-ttu-id="caa8a-149">Isso é semelhante à corrupção de que os arquivos de banco de dados e/ou de log estão em um estado inconsistente e não reconciliado entre si.</span><span class="sxs-lookup"><span data-stu-id="caa8a-149">This is similar to Corruption in that the database and/or log files are in a state that is inconsistent and unreconcilable with each other.</span></span> <span data-ttu-id="caa8a-150">Geralmente, isso é causado por indisponibilidade de aplicativo/administrador.</span><span class="sxs-lookup"><span data-stu-id="caa8a-150">Often this is caused by application/administrator mishandling.</span></span> <span data-ttu-id="caa8a-151">Recuperação: restauração a partir do backup, talvez a operação de reparo de utilitários ESE (que apenas recupera quais dados são deixados/perdidos).</span><span class="sxs-lookup"><span data-stu-id="caa8a-151">Recovery: Restore from backup, perhaps the ese utilities repair operation (which only salvages what data is left / lossy).</span></span> <span data-ttu-id="caa8a-152">Também no caso de recuperação (JetInit), talvez a recuperação possa ser realizada, permitindo a perda de dados.</span><span class="sxs-lookup"><span data-stu-id="caa8a-152">Also in the case of recovery(JetInit) perhaps recovery can be performed by allowing data loss.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="caa8a-153">Fragmentação</span><span class="sxs-lookup"><span data-stu-id="caa8a-153">Fragmentation</span></span></td>
<td><span data-ttu-id="caa8a-154">Essa é uma classe de erros em que algum recurso interno persistente foi executado. Recuperação: para erros de banco de dados, a desfragmentação offline corrigirá o problema, para os arquivos de log, _primeiro_ Recupere todos os bancos de dados anexados para um desligamento limpo e exclua todos os arquivos de log e o ponto de verificação.</span><span class="sxs-lookup"><span data-stu-id="caa8a-154">This is a class of errors where some persisted internal resource ran out. Recovery: For database errors, offline defragmentation will rectify the problem, for the log files _first_ recover all attached databases to a clean shutdown, and then delete all the log files and checkpoint.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="caa8a-155">API</span><span class="sxs-lookup"><span data-stu-id="caa8a-155">Api</span></span></td>
<td><span data-ttu-id="caa8a-156">Um contêiner para uso e estado.</span><span class="sxs-lookup"><span data-stu-id="caa8a-156">A container for Usage and State.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="caa8a-157">Uso</span><span class="sxs-lookup"><span data-stu-id="caa8a-157">Usage</span></span></td>
<td><span data-ttu-id="caa8a-158">Erro de uso clássico, isso significa que o código do cliente não passou os argumentos corretos para a API do JET.</span><span class="sxs-lookup"><span data-stu-id="caa8a-158">Classic usage error, this means the client code did not pass correct arguments to the JET API.</span></span> <span data-ttu-id="caa8a-159">Esse erro provavelmente não vai desaparecer com a repetição.</span><span class="sxs-lookup"><span data-stu-id="caa8a-159">This error will likely not go away with retry.</span></span> <span data-ttu-id="caa8a-160">Recuperação: o código do cliente em geral deve declarar () essa classe de erros não é retornada, de modo que os problemas podem ser detectados durante o desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="caa8a-160">Recovery: Generally speaking client code should Assert() this class of errors is not returned, so issues can be caught during development.</span></span> <span data-ttu-id="caa8a-161">No varejo, o aplicativo provavelmente terá pouca opção, mas para retornar o problema até o operador.</span><span class="sxs-lookup"><span data-stu-id="caa8a-161">In retail, the app will probably have little option but to return the issue up to the operator.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="caa8a-162">Estado</span><span class="sxs-lookup"><span data-stu-id="caa8a-162">State</span></span></td>
<td><span data-ttu-id="caa8a-163">Essa é a classificação para diferentes sinais que a API poderia retornar para descrever o estado do banco de dados, um caso clássico é JET_errRecordNotFound que pode ser retornado por JetSeek () quando o registro solicitado não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="caa8a-163">This is the classification for different signals the API could return describe the state of the database, a classic case is JET_errRecordNotFound which can be returned by JetSeek() when the record you asked for was not found.</span></span> <span data-ttu-id="caa8a-164">Recuperação: não é realmente relevante, depende muito da API.</span><span class="sxs-lookup"><span data-stu-id="caa8a-164">Recovery: Not really relevant, depends greatly on the API.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="caa8a-165">Obsoleto</span><span class="sxs-lookup"><span data-stu-id="caa8a-165">Obsolete</span></span></td>
<td><span data-ttu-id="caa8a-166">O erro é reconhecido como um erro válido, mas não se espera que ele seja retornado por esta versão da API.</span><span class="sxs-lookup"><span data-stu-id="caa8a-166">The error is recognized as a valid error, but is not expected to be returned by this version of the API.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="caa8a-167">Máx</span><span class="sxs-lookup"><span data-stu-id="caa8a-167">Max</span></span></td>
<td><span data-ttu-id="caa8a-168">O valor máximo para a enumeração.</span><span class="sxs-lookup"><span data-stu-id="caa8a-168">The maximum value for the enum.</span></span> <span data-ttu-id="caa8a-169">Isso não deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="caa8a-169">This should not be used.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="caa8a-170">Confira também</span><span class="sxs-lookup"><span data-stu-id="caa8a-170">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="caa8a-171">Referência</span><span class="sxs-lookup"><span data-stu-id="caa8a-171">Reference</span></span>

[<span data-ttu-id="caa8a-172">Namespace Microsoft. ISAM. ESENT. Interop. windows8</span><span class="sxs-lookup"><span data-stu-id="caa8a-172">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
