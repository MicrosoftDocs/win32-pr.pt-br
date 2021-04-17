---
description: 'Saiba mais sobre: Enumeração StopServiceGrbit'
title: Enumeração StopServiceGrbit (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: StopServiceGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.stopservicegrbit(v=EXCHG.10)
ms:contentKeyID: 55104330
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.All
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.BackgroundUserTasks
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.QuiesceCaches
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.Resume
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.BackgroundUserTasks
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.All
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.QuiesceCaches
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.Resume
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 54e54576dfb1023ec4e3bc55ddd198a77f0ddf25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761197"
---
# <a name="stopservicegrbit-enumeration"></a><span data-ttu-id="a4d25-103">Enumeração StopServiceGrbit</span><span class="sxs-lookup"><span data-stu-id="a4d25-103">StopServiceGrbit enumeration</span></span>

<span data-ttu-id="a4d25-104">Opções para [JetStopServiceInstance2 (JET_INSTANCE, StopServiceGrbit)](./windows8api.jetstopserviceinstance2-method.md).</span><span class="sxs-lookup"><span data-stu-id="a4d25-104">Options for [JetStopServiceInstance2(JET_INSTANCE, StopServiceGrbit)](./windows8api.jetstopserviceinstance2-method.md).</span></span>

<span data-ttu-id="a4d25-105">Esta enumeração tem um atributo [FlagsAttribute](/dotnet/api/system.flagsattribute) que permite uma combinação bit a bit dos valores membros dela.</span><span class="sxs-lookup"><span data-stu-id="a4d25-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="a4d25-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a4d25-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="a4d25-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a4d25-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a4d25-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a4d25-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration StopServiceGrbit
'Usage
Dim instance As StopServiceGrbit
```

``` csharp
[FlagsAttribute]
public enum StopServiceGrbit
```

## <a name="members"></a><span data-ttu-id="a4d25-109">Membros</span><span class="sxs-lookup"><span data-stu-id="a4d25-109">Members</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="a4d25-110">Nome do membro</span><span class="sxs-lookup"><span data-stu-id="a4d25-110">Member name</span></span></th>
<th><span data-ttu-id="a4d25-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="a4d25-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="a4d25-112">Tudo</span><span class="sxs-lookup"><span data-stu-id="a4d25-112">All</span></span></td>
<td><span data-ttu-id="a4d25-113">Interrompe todos os serviços ESE para a instância especificada.</span><span class="sxs-lookup"><span data-stu-id="a4d25-113">Stops all ESE services for the specified instance.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="a4d25-114">BackgroundUserTasks</span><span class="sxs-lookup"><span data-stu-id="a4d25-114">BackgroundUserTasks</span></span></td>
<td><span data-ttu-id="a4d25-115">Interrompe tarefas de manutenção em segundo plano específicas do cliente reiniciáveis (desfragmentação da árvore B +).</span><span class="sxs-lookup"><span data-stu-id="a4d25-115">Stops restartable client specificed background maintenance tasks (B+ Tree Defrag).</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="a4d25-116">QuiesceCaches</span><span class="sxs-lookup"><span data-stu-id="a4d25-116">QuiesceCaches</span></span></td>
<td><span data-ttu-id="a4d25-117">Quiesces todos os caches sujos em disco.</span><span class="sxs-lookup"><span data-stu-id="a4d25-117">Quiesces all dirty caches to disk.</span></span> <span data-ttu-id="a4d25-118">Assíncrono.</span><span class="sxs-lookup"><span data-stu-id="a4d25-118">Asynchronous.</span></span> <span data-ttu-id="a4d25-119">O fechamento em pausa será cancelado se o bit de retomação for chamado posteriormente.</span><span class="sxs-lookup"><span data-stu-id="a4d25-119">Quiescing is cancelled if the Resume bit is called subsequently.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="a4d25-120">Retomar</span><span class="sxs-lookup"><span data-stu-id="a4d25-120">Resume</span></span></td>
<td><span data-ttu-id="a4d25-121">Retoma as operações StopService emitidas anteriormente, ou seja, &quot; reinicia o serviço &quot; .</span><span class="sxs-lookup"><span data-stu-id="a4d25-121">Resumes previously issued StopService operations, i.e. &quot;restarts service&quot;.</span></span> <span data-ttu-id="a4d25-122">Pode ser combinado com grbits acima para retomar serviços específicos ou com 0x0 retoma todos os serviços interrompidos anteriormente.</span><span class="sxs-lookup"><span data-stu-id="a4d25-122">Can be combined with above grbits to Resume specific services, or with 0x0 Resumes all previous stopped services.</span></span>
<p><span data-ttu-id="a4d25-123">Aviso: esse bit só pode ser usado para retomar JET_bitStopServiceBackground e JET_bitStopServiceQuiesceCaches, se você fez uma JET_bitStopServiceAll ou JET_bitStopServiceAPI, a tentativa de usar JET_bitStopServiceResume falhará.</span><span class="sxs-lookup"><span data-stu-id="a4d25-123">Warning: This bit can only be used to resume JET_bitStopServiceBackground and JET_bitStopServiceQuiesceCaches, if you did a JET_bitStopServiceAll or JET_bitStopServiceAPI, attempting to use JET_bitStopServiceResume will fail.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="a4d25-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="a4d25-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a4d25-125">Referência</span><span class="sxs-lookup"><span data-stu-id="a4d25-125">Reference</span></span>

[<span data-ttu-id="a4d25-126">Namespace Microsoft. ISAM. ESENT. Interop. windows8</span><span class="sxs-lookup"><span data-stu-id="a4d25-126">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
