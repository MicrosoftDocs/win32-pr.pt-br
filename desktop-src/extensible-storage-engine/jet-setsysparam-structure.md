---
description: 'Saiba mais sobre: estrutura de JET_SETSYSPARAM'
title: Estrutura de JET_SETSYSPARAM
TOCTitle: JET_SETSYSPARAM Structure
ms:assetid: 3c0fdd28-99bd-4026-b64b-6859ef9dc91b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269230(v=EXCHG.10)
ms:contentKeyID: 32765532
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
ms.openlocfilehash: 0e88795bb3ee966bf2ad7fa50cc7d2180d7264bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296247"
---
# <a name="jet_setsysparam-structure"></a><span data-ttu-id="ffe6a-103">Estrutura de JET_SETSYSPARAM</span><span class="sxs-lookup"><span data-stu-id="ffe6a-103">JET_SETSYSPARAM Structure</span></span>


<span data-ttu-id="ffe6a-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ffe6a-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_setsysparam-structure"></a><span data-ttu-id="ffe6a-105">Estrutura de JET_SETSYSPARAM</span><span class="sxs-lookup"><span data-stu-id="ffe6a-105">JET_SETSYSPARAM Structure</span></span>

<span data-ttu-id="ffe6a-106">Uma matriz de estruturas de **JET_SETSYSPARAM** indicam um conjunto específico de parâmetros de sistema global que são definidos como um argumento ao usar a função [JetEnableMultiInstance](./jetenablemultiinstance-function.md) .</span><span class="sxs-lookup"><span data-stu-id="ffe6a-106">An array of **JET_SETSYSPARAM** structures indicate a specific set of global system parameters that are set as an argument when using the [JetEnableMultiInstance](./jetenablemultiinstance-function.md) function.</span></span>

<span data-ttu-id="ffe6a-107">**Windows XP:** Essa estrutura é introduzida no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ffe6a-107">**Windows XP:** This structure is introduced in Windows XP.</span></span>

```cpp
    typedef struct {
      unsigned long paramid;
      JET_API_PTR lParam;
      const tchar* sz;
      JET_ERR err;
    } JET_SETSYSPARAM;
```

### <a name="members"></a><span data-ttu-id="ffe6a-108">Membros</span><span class="sxs-lookup"><span data-stu-id="ffe6a-108">Members</span></span>

<span data-ttu-id="ffe6a-109">**paramid**</span><span class="sxs-lookup"><span data-stu-id="ffe6a-109">**paramid**</span></span>

<span data-ttu-id="ffe6a-110">A ID do parâmetro do sistema que será definido.</span><span class="sxs-lookup"><span data-stu-id="ffe6a-110">The ID of the system parameter that will be set.</span></span>

<span data-ttu-id="ffe6a-111">Consulte [parâmetros do sistema do mecanismo de armazenamento extensível](./extensible-storage-engine-system-parameters.md) para obter uma lista completa de parâmetros do sistema e suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ffe6a-111">See [Extensible Storage Engine System Parameters](./extensible-storage-engine-system-parameters.md) for a complete list of system parameters and their properties.</span></span>

<span data-ttu-id="ffe6a-112">**lParam**</span><span class="sxs-lookup"><span data-stu-id="ffe6a-112">**lParam**</span></span>

<span data-ttu-id="ffe6a-113">O valor opcional a ser definido para o parâmetro do sistema selecionado se esse parâmetro do sistema for de um tipo inteiro.</span><span class="sxs-lookup"><span data-stu-id="ffe6a-113">The optional value to be set for the selected system parameter if that system parameter is of an integer type.</span></span>

<span data-ttu-id="ffe6a-114">**sz**</span><span class="sxs-lookup"><span data-stu-id="ffe6a-114">**sz**</span></span>

<span data-ttu-id="ffe6a-115">O valor opcional a ser definido para o parâmetro do sistema selecionado se esse parâmetro do sistema for de um tipo de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="ffe6a-115">The optional value to be set for the selected system parameter if that system parameter is of a string type.</span></span>

<span data-ttu-id="ffe6a-116">**erra**</span><span class="sxs-lookup"><span data-stu-id="ffe6a-116">**err**</span></span>

<span data-ttu-id="ffe6a-117">O erro resultante da chamada para [JetSetSystemParameter](./jetsetsystemparameter-function.md) com os parâmetros especificados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="ffe6a-117">The error resulting from the call to [JetSetSystemParameter](./jetsetsystemparameter-function.md) with the previously specified parameters.</span></span>

### <a name="requirements"></a><span data-ttu-id="ffe6a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ffe6a-118">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ffe6a-119"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="ffe6a-119"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ffe6a-120">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="ffe6a-120">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffe6a-121"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="ffe6a-121"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ffe6a-122">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="ffe6a-122">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffe6a-123"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="ffe6a-123"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ffe6a-124">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="ffe6a-124">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffe6a-125"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="ffe6a-125"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="ffe6a-126">Implementado como <strong>JET_ SETSYSPARAM_W</strong> (Unicode) e <strong>JET_ SETSYSPARAM_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="ffe6a-126">Implemented as <strong>JET_ SETSYSPARAM_W</strong> (Unicode) and <strong>JET_ SETSYSPARAM_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="ffe6a-127">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="ffe6a-127">See Also</span></span>

[<span data-ttu-id="ffe6a-128">Parâmetros do sistema do mecanismo de armazenamento extensível</span><span class="sxs-lookup"><span data-stu-id="ffe6a-128">Extensible Storage Engine System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)  
[<span data-ttu-id="ffe6a-129">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="ffe6a-129">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="ffe6a-130">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="ffe6a-130">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="ffe6a-131">JetEnableMultiInstance</span><span class="sxs-lookup"><span data-stu-id="ffe6a-131">JetEnableMultiInstance</span></span>](./jetenablemultiinstance-function.md)  
[<span data-ttu-id="ffe6a-132">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="ffe6a-132">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
