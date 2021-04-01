---
description: 'Saiba mais sobre: estrutura de JET_RSTINFO'
title: Estrutura de JET_RSTINFO
TOCTitle: JET_RSTINFO Structure
ms:assetid: 2f144d68-dcd9-4d0d-9d9e-a7d2a5c350fe
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269216(v=EXCHG.10)
ms:contentKeyID: 32765519
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
ms.openlocfilehash: 3a776c84d89dfc97272c65bb0c0684faba814fdf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090129"
---
# <a name="jet_rstinfo-structure"></a><span data-ttu-id="59738-103">Estrutura de JET_RSTINFO</span><span class="sxs-lookup"><span data-stu-id="59738-103">JET_RSTINFO Structure</span></span>


<span data-ttu-id="59738-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="59738-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_rstinfo-structure"></a><span data-ttu-id="59738-105">Estrutura de JET_RSTINFO</span><span class="sxs-lookup"><span data-stu-id="59738-105">JET_RSTINFO Structure</span></span>

<span data-ttu-id="59738-106">A estrutura de **JET_RSTINFO** contém informações de controle para o processo de recuperação, como informações de realocação de banco de dados e a capacidade de controlar a interrupção da recuperação.</span><span class="sxs-lookup"><span data-stu-id="59738-106">The **JET_RSTINFO** structure contains control information for the recovery process like database relocation information and ability to control stopping recovery.</span></span>

<span data-ttu-id="59738-107">**Windows Vista:** A estrutura de **JET_RSTINFO** é introduzida no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="59738-107">**Windows Vista:** The **JET_RSTINFO** structure is introduced in Windows Vista.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_RSTMAP* rgrstmap;
      long crstmap;
      JET_LGPOS lgposStop;
      JET_LOGTIME logtimeStop;
      JET_PFNSTATUS pfnStatus;
    } JET_RSTINFO;
```

### <a name="members"></a><span data-ttu-id="59738-108">Membros</span><span class="sxs-lookup"><span data-stu-id="59738-108">Members</span></span>

<span data-ttu-id="59738-109">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="59738-109">**cbStruct**</span></span>

<span data-ttu-id="59738-110">O tamanho da estrutura.</span><span class="sxs-lookup"><span data-stu-id="59738-110">The size of the structure.</span></span>

<span data-ttu-id="59738-111">**rgrstmap**</span><span class="sxs-lookup"><span data-stu-id="59738-111">**rgrstmap**</span></span>

<span data-ttu-id="59738-112">A estrutura que descreve o caminho novo e antigo de um banco de dados restaurado.</span><span class="sxs-lookup"><span data-stu-id="59738-112">The structure that describes the old and new path of a restored database.</span></span>

<span data-ttu-id="59738-113">**crstmap**</span><span class="sxs-lookup"><span data-stu-id="59738-113">**crstmap**</span></span>

<span data-ttu-id="59738-114">Contagem de entradas de matriz no rgrstmap.</span><span class="sxs-lookup"><span data-stu-id="59738-114">Count of array entries in the rgrstmap.</span></span>

<span data-ttu-id="59738-115">**lgposStop**</span><span class="sxs-lookup"><span data-stu-id="59738-115">**lgposStop**</span></span>

<span data-ttu-id="59738-116">A posição do log para parar a recuperação em.</span><span class="sxs-lookup"><span data-stu-id="59738-116">The log position to stop recovery at.</span></span> <span data-ttu-id="59738-117">Nenhum desfazer será feito.</span><span class="sxs-lookup"><span data-stu-id="59738-117">No undo will be done.</span></span>

<span data-ttu-id="59738-118">**logtimeStop**</span><span class="sxs-lookup"><span data-stu-id="59738-118">**logtimeStop**</span></span>

<span data-ttu-id="59738-119">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="59738-119">Reserved for future use.</span></span>

<span data-ttu-id="59738-120">**pfnStatus**</span><span class="sxs-lookup"><span data-stu-id="59738-120">**pfnStatus**</span></span>

<span data-ttu-id="59738-121">Uma função de status para relatar o status da recuperação.</span><span class="sxs-lookup"><span data-stu-id="59738-121">A status function for reporting status of recovery.</span></span>

### <a name="requirements"></a><span data-ttu-id="59738-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59738-122">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="59738-123"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="59738-123"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="59738-124">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="59738-124">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59738-125"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="59738-125"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="59738-126">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="59738-126">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59738-127"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="59738-127"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="59738-128">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="59738-128">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59738-129"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="59738-129"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="59738-130">Implementado como <strong>JET_RSTINFO_W</strong> (Unicode) e <strong>JET_RSTINFO_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="59738-130">Implemented as <strong>JET_RSTINFO_W</strong> (Unicode) and <strong>JET_RSTINFO_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="59738-131">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="59738-131">See Also</span></span>

[<span data-ttu-id="59738-132">JetInit3</span><span class="sxs-lookup"><span data-stu-id="59738-132">JetInit3</span></span>](./jetinit3-function.md)
