---
description: 'Saiba mais sobre: WCHAR'
title: WCHAR
TOCTitle: WCHAR
ms:assetid: 922431b3-bf9a-4aba-bc67-dd33d9aeaac0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269344(v=EXCHG.10)
ms:contentKeyID: 32765633
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
ms.openlocfilehash: 1dfa86cbc771059d941027385090dcbd2f401855
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765278"
---
# <a name="wchar"></a><span data-ttu-id="6728a-103">WCHAR</span><span class="sxs-lookup"><span data-stu-id="6728a-103">WCHAR</span></span>


<span data-ttu-id="6728a-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="6728a-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="wchar"></a><span data-ttu-id="6728a-105">WCHAR</span><span class="sxs-lookup"><span data-stu-id="6728a-105">WCHAR</span></span>

<span data-ttu-id="6728a-106">O tipo de dados WCHAR contém um caractere Unicode de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="6728a-106">The WCHAR data type contains a 16-bit Unicode character.</span></span>

```cpp
    #if !defined(_NATIVE_WCHAR_T_DEFINED)
    typedef unsigned short WCHAR;
    #else
    typedef wchar_t WCHAR;
    #endif
```

### <a name="data-types"></a><span data-ttu-id="6728a-107">Tipos de dados</span><span class="sxs-lookup"><span data-stu-id="6728a-107">Data Types</span></span>

<span data-ttu-id="6728a-108">WCHAR</span><span class="sxs-lookup"><span data-stu-id="6728a-108">WCHAR</span></span>

<span data-ttu-id="6728a-109">Um caractere Unicode de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="6728a-109">A 16-bit Unicode character.</span></span>

### <a name="requirements"></a><span data-ttu-id="6728a-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6728a-110">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6728a-111"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="6728a-111"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="6728a-112">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="6728a-112">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6728a-113"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="6728a-113"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="6728a-114">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="6728a-114">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6728a-115"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="6728a-115"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="6728a-116">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="6728a-116">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

