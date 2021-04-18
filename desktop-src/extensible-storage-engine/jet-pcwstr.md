---
description: 'Saiba mais sobre: JET_PCWSTR'
title: JET_PCWSTR
TOCTitle: JET_PCWSTR
ms:assetid: fef64bb9-c2e0-4cfb-8138-c98ae6f50952
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294145(v=EXCHG.10)
ms:contentKeyID: 32765759
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
ms.openlocfilehash: 51cd0dab17096fb8f7371a01ebabfca3abc595be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105796217"
---
# <a name="jet_pcwstr"></a><span data-ttu-id="006ff-103">JET_PCWSTR</span><span class="sxs-lookup"><span data-stu-id="006ff-103">JET_PCWSTR</span></span>


<span data-ttu-id="006ff-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="006ff-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_pcwstr"></a><span data-ttu-id="006ff-105">JET_PCWSTR</span><span class="sxs-lookup"><span data-stu-id="006ff-105">JET_PCWSTR</span></span>

<span data-ttu-id="006ff-106">O tipo de dados **JET_PCWSTR** contém uma cadeia de caracteres **Unicode** (Char) constante terminada em nulo \* .</span><span class="sxs-lookup"><span data-stu-id="006ff-106">The **JET_PCWSTR** data type contains a null-terminated, constant **Unicode** string (char \*).</span></span>

<span data-ttu-id="006ff-107">**Windows Vista: a JET_PCWSTR** é introduzida no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="006ff-107">**Windows Vista:  JET_PCWSTR** is introduced in Windows Vista.</span></span>

```cpp
    typedef __nullterminated const WCHAR * JET_PCWSTR;
```

### <a name="data-types"></a><span data-ttu-id="006ff-108">Tipos de dados</span><span class="sxs-lookup"><span data-stu-id="006ff-108">Data Types</span></span>

<span data-ttu-id="006ff-109">JET_PCWSTR</span><span class="sxs-lookup"><span data-stu-id="006ff-109">JET_PCWSTR</span></span>

<span data-ttu-id="006ff-110">Cadeia de caracteres Unicode (Char) constante terminada em nulo \* .</span><span class="sxs-lookup"><span data-stu-id="006ff-110">Null-terminated, constant Unicode string (char \*).</span></span>

### <a name="requirements"></a><span data-ttu-id="006ff-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="006ff-111">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="006ff-112"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="006ff-112"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="006ff-113">Requer o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="006ff-113">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="006ff-114"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="006ff-114"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="006ff-115">Requer o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="006ff-115">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="006ff-116"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="006ff-116"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="006ff-117">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="006ff-117">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

