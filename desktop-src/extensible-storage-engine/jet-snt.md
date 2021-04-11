---
description: 'Saiba mais sobre: JET_SNT'
title: JET_SNT
TOCTitle: JET_SNT
ms:assetid: 74ac5142-8102-4dd3-8f2a-786a7a2ac78f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269294(v=EXCHG.10)
ms:contentKeyID: 32765586
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
ms.openlocfilehash: 5d1d4fa75c8a41528e9868bc94fa638042d01cff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164266"
---
# <a name="jet_snt"></a><span data-ttu-id="48cd7-103">JET_SNT</span><span class="sxs-lookup"><span data-stu-id="48cd7-103">JET_SNT</span></span>


<span data-ttu-id="48cd7-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="48cd7-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_snt"></a><span data-ttu-id="48cd7-105">JET_SNT</span><span class="sxs-lookup"><span data-stu-id="48cd7-105">JET_SNT</span></span>

<span data-ttu-id="48cd7-106">O [JET_SNT]() grupo de constantes descreve os pontos do progresso de uma operação sobre a qual as informações são solicitadas em uma chamada para a função de retorno de chamada [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) .</span><span class="sxs-lookup"><span data-stu-id="48cd7-106">The [JET_SNT]() group of constants describe the points of the progress of an operation about which information is requested in a call to the [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) callback function.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="48cd7-107">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="48cd7-107">Constant/value</span></span></p></th>
<th><p><span data-ttu-id="48cd7-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="48cd7-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="48cd7-109">JET_sntBegin</span><span class="sxs-lookup"><span data-stu-id="48cd7-109">JET_sntBegin</span></span><br />
<span data-ttu-id="48cd7-110">5</span><span class="sxs-lookup"><span data-stu-id="48cd7-110">5</span></span></p></td>
<td><p><span data-ttu-id="48cd7-111">O início de uma operação</span><span class="sxs-lookup"><span data-stu-id="48cd7-111">The beginning of an operation</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48cd7-112">JET_sntRequirements</span><span class="sxs-lookup"><span data-stu-id="48cd7-112">JET_sntRequirements</span></span><br />
<span data-ttu-id="48cd7-113">7</span><span class="sxs-lookup"><span data-stu-id="48cd7-113">7</span></span></p></td>
<td><p><span data-ttu-id="48cd7-114">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="48cd7-114">Not supported.</span></span></p>
<p><span data-ttu-id="48cd7-115"><strong>Servidor do Windows 2000:</strong>  A operação foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="48cd7-115"><strong>Windows 2000 Server:</strong>  The operation is started.</span></span> <span data-ttu-id="48cd7-116">Nesse caso, o último parâmetro da função de retorno de chamada deve ser um ponteiro válido para uma estrutura de <a href="gg269328(v=exchg.10).md">JET_SNPROG</a> indicando o número total de unidades a serem executadas.</span><span class="sxs-lookup"><span data-stu-id="48cd7-116">In this case, the last parameter of the callback function should be a valid pointer to a <a href="gg269328(v=exchg.10).md">JET_SNPROG</a> structure indicating the total number of units to be executed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48cd7-117">JET_sntProgress</span><span class="sxs-lookup"><span data-stu-id="48cd7-117">JET_sntProgress</span></span><br />
<span data-ttu-id="48cd7-118">0</span><span class="sxs-lookup"><span data-stu-id="48cd7-118">0</span></span></p></td>
<td><p><span data-ttu-id="48cd7-119">O número de unidades concluídas e o número de unidades que ainda serão feitas.</span><span class="sxs-lookup"><span data-stu-id="48cd7-119">The number of units completed and number of units yet to be done.</span></span> <span data-ttu-id="48cd7-120">Essas informações são retornadas nos membros de uma estrutura de <a href="gg269328(v=exchg.10).md">JET_SNPROG</a> .</span><span class="sxs-lookup"><span data-stu-id="48cd7-120">This information is returned in the members of a <a href="gg269328(v=exchg.10).md">JET_SNPROG</a> structure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48cd7-121">JET_sntComplete</span><span class="sxs-lookup"><span data-stu-id="48cd7-121">JET_sntComplete</span></span><br />
<span data-ttu-id="48cd7-122">6</span><span class="sxs-lookup"><span data-stu-id="48cd7-122">6</span></span></p></td>
<td><p><span data-ttu-id="48cd7-123">A conclusão de uma operação.</span><span class="sxs-lookup"><span data-stu-id="48cd7-123">The completion of an operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48cd7-124">JET_sntFail</span><span class="sxs-lookup"><span data-stu-id="48cd7-124">JET_sntFail</span></span><br />
<span data-ttu-id="48cd7-125">3</span><span class="sxs-lookup"><span data-stu-id="48cd7-125">3</span></span></p></td>
<td><p><span data-ttu-id="48cd7-126">A falha de uma operação.</span><span class="sxs-lookup"><span data-stu-id="48cd7-126">The failure of an operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48cd7-127">JET_sntRecoveryStep</span><span class="sxs-lookup"><span data-stu-id="48cd7-127">JET_sntRecoveryStep</span></span><br />
<span data-ttu-id="48cd7-128">8</span><span class="sxs-lookup"><span data-stu-id="48cd7-128">8</span></span></p></td>
<td><p><span data-ttu-id="48cd7-129">O controle de recuperação de uma operação.</span><span class="sxs-lookup"><span data-stu-id="48cd7-129">The recovery control of an operation.</span></span></p>
<div class="alert">

> [!NOTE]
> <P><span data-ttu-id="48cd7-130">Esse valor não é aplicável a versões do sistema operacional Windows a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="48cd7-130">This value is not applicable to versions of the Windows operating system starting with Windows 8.</span></span></P>


</div></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="48cd7-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48cd7-131">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="48cd7-132"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="48cd7-132"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="48cd7-133">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="48cd7-133">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48cd7-134"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="48cd7-134"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="48cd7-135">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="48cd7-135">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48cd7-136"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="48cd7-136"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="48cd7-137">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="48cd7-137">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="48cd7-138">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="48cd7-138">See Also</span></span>

[<span data-ttu-id="48cd7-139">JET_PFNSTATUS</span><span class="sxs-lookup"><span data-stu-id="48cd7-139">JET_PFNSTATUS</span></span>](./jet-pfnstatus-callback-function.md)  
[<span data-ttu-id="48cd7-140">JET_SNP</span><span class="sxs-lookup"><span data-stu-id="48cd7-140">JET_SNP</span></span>](./jet-snp.md)  
[<span data-ttu-id="48cd7-141">JET_SNPROG</span><span class="sxs-lookup"><span data-stu-id="48cd7-141">JET_SNPROG</span></span>](./jet-snprog-structure.md)
