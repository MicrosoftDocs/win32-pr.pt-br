---
description: 'Saiba mais sobre: estrutura de JET_CONVERT'
title: Estrutura de JET_CONVERT
TOCTitle: JET_CONVERT Structure
ms:assetid: 33a0ff95-e9af-44c0-bf80-03d785771d5e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269220(v=EXCHG.10)
ms:contentKeyID: 32765523
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
ms.openlocfilehash: c4e39548b6bcb0a4742b926c1b618b9cc899c2e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827422"
---
# <a name="jet_convert-structure"></a><span data-ttu-id="9f00c-103">Estrutura de JET_CONVERT</span><span class="sxs-lookup"><span data-stu-id="9f00c-103">JET_CONVERT Structure</span></span>


<span data-ttu-id="9f00c-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="9f00c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_convert-structure"></a><span data-ttu-id="9f00c-105">Estrutura de JET_CONVERT</span><span class="sxs-lookup"><span data-stu-id="9f00c-105">JET_CONVERT Structure</span></span>

<span data-ttu-id="9f00c-106">A estrutura de **JET_CONVERT** contém o nome de uma DLL de versão anterior do ESE que é usada para ler os bancos de dados criados com essa versão anterior.</span><span class="sxs-lookup"><span data-stu-id="9f00c-106">The **JET_CONVERT** structure contains the name of an earlier ESE version DLL that is used for reading a databases that are created with that earlier version.</span></span> <span data-ttu-id="9f00c-107">Além disso, outros sinalizadores são fornecidos para controlar a natureza da conversão.</span><span class="sxs-lookup"><span data-stu-id="9f00c-107">In addition, other flags are provided to control the nature of the conversion.</span></span>

<span data-ttu-id="9f00c-108">**Windows Server 2003:** O recurso no [JetCompact](./jetcompact-function.md) que realizou uma conversão foi removido do produto no Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="9f00c-108">**Windows Server 2003:** The feature in [JetCompact](./jetcompact-function.md) that performed a conversion was removed from the product in Windows Server 2003.</span></span> <span data-ttu-id="9f00c-109">Só há suporte para ele no Windows 2000 e no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9f00c-109">It is only supported in Windows 2000 and Windows XP.</span></span>

```cpp
    typedef struct tagCONVERT {
      tchar* SzOldDll;
      union {
        unsigned long fFlags;
        struct {
          unsigned long fSchemaChangesOnly  :1;
        };
      };
    } JET_CONVERT;
```

### <a name="members"></a><span data-ttu-id="9f00c-110">Membros</span><span class="sxs-lookup"><span data-stu-id="9f00c-110">Members</span></span>

<span data-ttu-id="9f00c-111">**SzOldDll**</span><span class="sxs-lookup"><span data-stu-id="9f00c-111">**SzOldDll**</span></span>

<span data-ttu-id="9f00c-112">O nome, incluindo informações de caminho, para a versão anterior da DLL do ESE.</span><span class="sxs-lookup"><span data-stu-id="9f00c-112">The name, including path information, to the earlier version of the ESE DLL.</span></span>

<span data-ttu-id="9f00c-113">**fFlags**</span><span class="sxs-lookup"><span data-stu-id="9f00c-113">**fFlags**</span></span>

<span data-ttu-id="9f00c-114">Reservado para uso do sistema.</span><span class="sxs-lookup"><span data-stu-id="9f00c-114">Reserved for system use.</span></span>

<span data-ttu-id="9f00c-115">**fSchemaChangesOnly**</span><span class="sxs-lookup"><span data-stu-id="9f00c-115">**fSchemaChangesOnly**</span></span>

<span data-ttu-id="9f00c-116">Reservado para uso do sistema.</span><span class="sxs-lookup"><span data-stu-id="9f00c-116">Reserved for system use.</span></span>

### <a name="requirements"></a><span data-ttu-id="9f00c-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f00c-117">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9f00c-118"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="9f00c-118"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9f00c-119">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="9f00c-119">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f00c-120"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="9f00c-120"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9f00c-121">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="9f00c-121">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f00c-122"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="9f00c-122"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9f00c-123">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="9f00c-123">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f00c-124"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="9f00c-124"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="9f00c-125">Implementado como <strong>JET_CONVERT_W</strong> (Unicode) e <strong>JET_CONVERT_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="9f00c-125">Implemented as <strong>JET_CONVERT_W</strong> (Unicode) and <strong>JET_CONVERT_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="9f00c-126">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="9f00c-126">See Also</span></span>

[<span data-ttu-id="9f00c-127">JetCompact</span><span class="sxs-lookup"><span data-stu-id="9f00c-127">JetCompact</span></span>](./jetcompact-function.md)
