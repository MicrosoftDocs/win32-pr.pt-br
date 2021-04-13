---
description: 'Saiba mais sobre: estrutura de JET_SNPROG'
title: Estrutura de JET_SNPROG
TOCTitle: JET_SNPROG Structure
ms:assetid: 8b4224e4-ad4d-440f-8915-8eb43b0885f0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269328(v=EXCHG.10)
ms:contentKeyID: 32765618
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
ms.openlocfilehash: 961e9cf264652924cfb1d870fa1a04aabc7fb61a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457261"
---
# <a name="jet_snprog-structure"></a><span data-ttu-id="4297b-103">Estrutura de JET_SNPROG</span><span class="sxs-lookup"><span data-stu-id="4297b-103">JET_SNPROG Structure</span></span>


<span data-ttu-id="4297b-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="4297b-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_snprog-structure"></a><span data-ttu-id="4297b-105">Estrutura de JET_SNPROG</span><span class="sxs-lookup"><span data-stu-id="4297b-105">JET_SNPROG Structure</span></span>

<span data-ttu-id="4297b-106">A estrutura de **JET_SNPROG** contém informações sobre o progresso de uma operação de execução longa.</span><span class="sxs-lookup"><span data-stu-id="4297b-106">The **JET_SNPROG** structure contains information about the progress of a long-running operation.</span></span> <span data-ttu-id="4297b-107">Quando a função de retorno de chamada é chamada para notificar o status da operação e a operação ainda está em andamento, o último parâmetro da função de retorno de chamada é um ponteiro para uma estrutura de **JET_SNPROG** .</span><span class="sxs-lookup"><span data-stu-id="4297b-107">When the callback function is called to notify the status of the operation and the operation is still in progress, the last parameter of the callback function is a pointer to a **JET_SNPROG** structure.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long cunitDone;
      unsigned long cunitTotal;
    } JET_SNPROG;
```

### <a name="members"></a><span data-ttu-id="4297b-108">Membros</span><span class="sxs-lookup"><span data-stu-id="4297b-108">Members</span></span>

<span data-ttu-id="4297b-109">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="4297b-109">**cbStruct**</span></span>

<span data-ttu-id="4297b-110">O tamanho da estrutura de **JET_SNPROG** , em bytes.</span><span class="sxs-lookup"><span data-stu-id="4297b-110">The size of the **JET_SNPROG** structure, in bytes.</span></span> <span data-ttu-id="4297b-111">Esse valor confirma a presença dos campos a seguir.</span><span class="sxs-lookup"><span data-stu-id="4297b-111">This value confirms the presence of the following fields.</span></span>

<span data-ttu-id="4297b-112">**cunitDone**</span><span class="sxs-lookup"><span data-stu-id="4297b-112">**cunitDone**</span></span>

<span data-ttu-id="4297b-113">O número de unidades de trabalho que já foram concluídas durante a função de execução longa.</span><span class="sxs-lookup"><span data-stu-id="4297b-113">The number of work units that are already completed during the long running function.</span></span>

<span data-ttu-id="4297b-114">**cunitTotal**</span><span class="sxs-lookup"><span data-stu-id="4297b-114">**cunitTotal**</span></span>

<span data-ttu-id="4297b-115">O número de unidades de trabalho que precisam ser concluídas.</span><span class="sxs-lookup"><span data-stu-id="4297b-115">The number of work units that need to be completed.</span></span> <span data-ttu-id="4297b-116">Esse valor deve ser sempre maior ou igual a **cunitDone**.</span><span class="sxs-lookup"><span data-stu-id="4297b-116">This value should always be bigger than or equal to **cunitDone**.</span></span>

### <a name="requirements"></a><span data-ttu-id="4297b-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4297b-117">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4297b-118"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="4297b-118"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="4297b-119">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="4297b-119">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4297b-120"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="4297b-120"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="4297b-121">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="4297b-121">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4297b-122"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="4297b-122"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="4297b-123">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="4297b-123">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

