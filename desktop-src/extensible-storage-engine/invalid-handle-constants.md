---
description: 'Saiba mais sobre: constantes de identificador inválidas'
title: Constantes de identificador inválidas
TOCTitle: Invalid Handle Constants
ms:assetid: 594d7804-725f-4f72-b5f0-56f099c1c17b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269256(v=EXCHG.10)
ms:contentKeyID: 32765558
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
ms.openlocfilehash: f5614b36acfca8b5be4c13849d459d25f984336a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011648"
---
# <a name="invalid-handle-constants"></a><span data-ttu-id="03ffb-103">Constantes de identificador inválidas</span><span class="sxs-lookup"><span data-stu-id="03ffb-103">Invalid Handle Constants</span></span>


<span data-ttu-id="03ffb-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="03ffb-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="invalid-handle-constants"></a><span data-ttu-id="03ffb-105">Constantes de identificador inválidas</span><span class="sxs-lookup"><span data-stu-id="03ffb-105">Invalid Handle Constants</span></span>

<span data-ttu-id="03ffb-106">As constantes a seguir indicam identificadores inválidos para diferentes aspectos do ESE.</span><span class="sxs-lookup"><span data-stu-id="03ffb-106">The following constants indicate invalid handles for different aspects of ESE.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="03ffb-107">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="03ffb-107">Constant/value</span></span></p></th>
<th><p><span data-ttu-id="03ffb-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="03ffb-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="03ffb-109">JET_instanceNil</span><span class="sxs-lookup"><span data-stu-id="03ffb-109">JET_instanceNil</span></span><br />
<span data-ttu-id="03ffb-110">(~ (JET_INSTANCE) 0)</span><span class="sxs-lookup"><span data-stu-id="03ffb-110">(~(JET_INSTANCE)0)</span></span></p></td>
<td><p><span data-ttu-id="03ffb-111">Um identificador inválido para uma instância de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="03ffb-111">An invalid handle for a database instance.</span></span><br /><span data-ttu-id="03ffb-112">
<strong>Windows XP:</strong> Introduzido no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="03ffb-112">
<strong>Windows XP:</strong> Introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03ffb-113">JET_sesidNil</span><span class="sxs-lookup"><span data-stu-id="03ffb-113">JET_sesidNil</span></span><br />
<span data-ttu-id="03ffb-114">(~ (JET_SESID) 0)</span><span class="sxs-lookup"><span data-stu-id="03ffb-114">(~(JET_SESID)0)</span></span></p></td>
<td><p><span data-ttu-id="03ffb-115">Um identificador inválido para uma ID de sessão.</span><span class="sxs-lookup"><span data-stu-id="03ffb-115">An invalid handle for a session ID.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03ffb-116">JET_tableidNil</span><span class="sxs-lookup"><span data-stu-id="03ffb-116">JET_tableidNil</span></span><br />
<span data-ttu-id="03ffb-117">(~ (JET_TABLEID) 0)</span><span class="sxs-lookup"><span data-stu-id="03ffb-117">(~(JET_TABLEID)0)</span></span></p></td>
<td><p><span data-ttu-id="03ffb-118">Um identificador inválido para uma ID de tabela.</span><span class="sxs-lookup"><span data-stu-id="03ffb-118">An invalid handle for a table ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03ffb-119">JET_bitNil</span><span class="sxs-lookup"><span data-stu-id="03ffb-119">JET_bitNil</span></span><br />
<span data-ttu-id="03ffb-120">((JET_GRBIT) 0)</span><span class="sxs-lookup"><span data-stu-id="03ffb-120">((JET_GRBIT)0)</span></span></p></td>
<td><p><span data-ttu-id="03ffb-121">Um identificador inválido para um grupo de bits.</span><span class="sxs-lookup"><span data-stu-id="03ffb-121">An invalid handle for a group of bits.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03ffb-122">JET_LSNil</span><span class="sxs-lookup"><span data-stu-id="03ffb-122">JET_LSNil</span></span><br />
<span data-ttu-id="03ffb-123">(~ (JET_LS) 0)</span><span class="sxs-lookup"><span data-stu-id="03ffb-123">(~(JET_LS)0)</span></span></p></td>
<td><p><span data-ttu-id="03ffb-124">Um identificador inválido para o armazenamento local.</span><span class="sxs-lookup"><span data-stu-id="03ffb-124">An invalid handle for the Local Storage.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03ffb-125">JET_dbidNil</span><span class="sxs-lookup"><span data-stu-id="03ffb-125">JET_dbidNil</span></span><br />
<span data-ttu-id="03ffb-126">((JET_DBID) 0xFFFFFFFF)</span><span class="sxs-lookup"><span data-stu-id="03ffb-126">((JET_DBID) 0xFFFFFFFF)</span></span></p></td>
<td><p><span data-ttu-id="03ffb-127">Um identificador inválido para a ID do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="03ffb-127">An invalid handle for the database ID.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="03ffb-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03ffb-128">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="03ffb-129"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="03ffb-129"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="03ffb-130">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="03ffb-130">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03ffb-131"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="03ffb-131"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="03ffb-132">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="03ffb-132">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03ffb-133"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="03ffb-133"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="03ffb-134">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="03ffb-134">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

