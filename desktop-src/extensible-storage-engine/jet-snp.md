---
description: 'Saiba mais sobre: JET_SNP'
title: JET_SNP
TOCTitle: JET_SNP
ms:assetid: 7f3d1cc5-7b27-454d-8dd1-584ab4b60ab0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269311(v=EXCHG.10)
ms:contentKeyID: 32765601
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
ms.openlocfilehash: 35ffb2d17c01c3d157fc7ed66a320529f844ff9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771783"
---
# <a name="jet_snp"></a><span data-ttu-id="5a5d1-103">JET_SNP</span><span class="sxs-lookup"><span data-stu-id="5a5d1-103">JET_SNP</span></span>


<span data-ttu-id="5a5d1-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="5a5d1-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_snp"></a><span data-ttu-id="5a5d1-105">JET_SNP</span><span class="sxs-lookup"><span data-stu-id="5a5d1-105">JET_SNP</span></span>

<span data-ttu-id="5a5d1-106">O **JET_SNP** grupo de constantes descreve o tipo da operação para a qual as informações de progresso serão obtidas.</span><span class="sxs-lookup"><span data-stu-id="5a5d1-106">The **JET_SNP** group of constants describe the type of the operation for which progress information is to be obtained.</span></span> <span data-ttu-id="5a5d1-107">Essas constantes são usadas como o parâmetro *SNP* da função de retorno de chamada [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) .</span><span class="sxs-lookup"><span data-stu-id="5a5d1-107">These constants are used as the *snp* parameter of the [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) callback function.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5a5d1-108">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="5a5d1-108">Constant/value</span></span></p></th>
<th><p><span data-ttu-id="5a5d1-109">Description</span><span class="sxs-lookup"><span data-stu-id="5a5d1-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5a5d1-110">JET_snpRepair</span><span class="sxs-lookup"><span data-stu-id="5a5d1-110">JET_snpRepair</span></span><br />
<span data-ttu-id="5a5d1-111">2</span><span class="sxs-lookup"><span data-stu-id="5a5d1-111">2</span></span></p></td>
<td><p><span data-ttu-id="5a5d1-112">O retorno de chamada é para uma operação de reparo.</span><span class="sxs-lookup"><span data-stu-id="5a5d1-112">The callback is for a repair operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a5d1-113">JET_snpCompact</span><span class="sxs-lookup"><span data-stu-id="5a5d1-113">JET_snpCompact</span></span><br />
<span data-ttu-id="5a5d1-114">4</span><span class="sxs-lookup"><span data-stu-id="5a5d1-114">4</span></span></p></td>
<td><p><span data-ttu-id="5a5d1-115">O retorno de chamada é para desfragmentação de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="5a5d1-115">The callback is for database defragmentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a5d1-116">JET_snpRestore</span><span class="sxs-lookup"><span data-stu-id="5a5d1-116">JET_snpRestore</span></span><br />
<span data-ttu-id="5a5d1-117">8</span><span class="sxs-lookup"><span data-stu-id="5a5d1-117">8</span></span></p></td>
<td><p><span data-ttu-id="5a5d1-118">O retorno de chamada é para uma operação de restauração.</span><span class="sxs-lookup"><span data-stu-id="5a5d1-118">The callback is for a restore operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a5d1-119">JET_snpBackup</span><span class="sxs-lookup"><span data-stu-id="5a5d1-119">JET_snpBackup</span></span><br />
<span data-ttu-id="5a5d1-120">9</span><span class="sxs-lookup"><span data-stu-id="5a5d1-120">9</span></span></p></td>
<td><p><span data-ttu-id="5a5d1-121">O retorno de chamada é para uma operação de backup.</span><span class="sxs-lookup"><span data-stu-id="5a5d1-121">The callback is for a backup operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a5d1-122">JET_snpUpgrade</span><span class="sxs-lookup"><span data-stu-id="5a5d1-122">JET_snpUpgrade</span></span><br />
<span data-ttu-id="5a5d1-123">10</span><span class="sxs-lookup"><span data-stu-id="5a5d1-123">10</span></span></p></td>
<td><p><span data-ttu-id="5a5d1-124">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="5a5d1-124">Not supported.</span></span></p>
<p><span data-ttu-id="5a5d1-125"><strong>Windows 2000:</strong>  O retorno de chamada é para a operação de atualização de formato de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="5a5d1-125"><strong>Windows 2000:</strong>  The callback is for the database format upgrade operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a5d1-126">JET_snpScrub</span><span class="sxs-lookup"><span data-stu-id="5a5d1-126">JET_snpScrub</span></span><br />
<span data-ttu-id="5a5d1-127">11</span><span class="sxs-lookup"><span data-stu-id="5a5d1-127">11</span></span></p></td>
<td><p><span data-ttu-id="5a5d1-128">O retorno de chamada é para uma operação de zero (ou seja, depuração) do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="5a5d1-128">The callback is for a database zeroing (that is, scrubbing) operation.</span></span></p>
<p><span data-ttu-id="5a5d1-129"><strong>Windows server 2003 e windows 2000 Server:</strong>  Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="5a5d1-129"><strong>Windows Server 2003 and Windows 2000 Server:</strong>  Not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a5d1-130">JET_snpUpgradeRecordFormat</span><span class="sxs-lookup"><span data-stu-id="5a5d1-130">JET_snpUpgradeRecordFormat</span></span><br />
<span data-ttu-id="5a5d1-131">12</span><span class="sxs-lookup"><span data-stu-id="5a5d1-131">12</span></span></p></td>
<td><p><span data-ttu-id="5a5d1-132">O retorno de chamada é para o processo de atualização do formato de registro de todas as páginas de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="5a5d1-132">The callback is for the process of upgrading the record format of all database pages.</span></span></p>
<p><span data-ttu-id="5a5d1-133"><strong>Windows server 2003 e windows 2000 Server:</strong>  Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="5a5d1-133"><strong>Windows Server 2003 and Windows 2000 Server:</strong>  Not supported.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="5a5d1-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a5d1-134">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5a5d1-135"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="5a5d1-135"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="5a5d1-136">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="5a5d1-136">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a5d1-137"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="5a5d1-137"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="5a5d1-138">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="5a5d1-138">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a5d1-139"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="5a5d1-139"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="5a5d1-140">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="5a5d1-140">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="5a5d1-141">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="5a5d1-141">See Also</span></span>

[<span data-ttu-id="5a5d1-142">JET_PFNSTATUS</span><span class="sxs-lookup"><span data-stu-id="5a5d1-142">JET_PFNSTATUS</span></span>](./jet-pfnstatus-callback-function.md)  
[<span data-ttu-id="5a5d1-143">JET_SNPROG</span><span class="sxs-lookup"><span data-stu-id="5a5d1-143">JET_SNPROG</span></span>](./jet-snprog-structure.md)  
[<span data-ttu-id="5a5d1-144">JET_SNT</span><span class="sxs-lookup"><span data-stu-id="5a5d1-144">JET_SNT</span></span>](./jet-snt.md)
