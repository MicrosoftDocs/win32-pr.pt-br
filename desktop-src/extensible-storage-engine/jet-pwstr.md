---
description: 'Saiba mais sobre: JET_PWSTR'
title: JET_PWSTR
TOCTitle: JET_PWSTR
ms:assetid: 6575f0f0-d022-4e70-9f17-c1d884d9e226
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269271(v=EXCHG.10)
ms:contentKeyID: 32765573
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
ms.openlocfilehash: 536ef3bba465f6d152e3483436c1dc1e82277339
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761223"
---
# <a name="jet_pwstr"></a><span data-ttu-id="65bc4-103">JET_PWSTR</span><span class="sxs-lookup"><span data-stu-id="65bc4-103">JET_PWSTR</span></span>


<span data-ttu-id="65bc4-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="65bc4-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_pwstr"></a><span data-ttu-id="65bc4-105">JET_PWSTR</span><span class="sxs-lookup"><span data-stu-id="65bc4-105">JET_PWSTR</span></span>

<span data-ttu-id="65bc4-106">O tipo de dados **JET_PWSTR** contém uma cadeia de caracteres **Unicode** terminada em nulo (Char \* ).</span><span class="sxs-lookup"><span data-stu-id="65bc4-106">The **JET_PWSTR** data type contains a null-terminated **Unicode** string (char \*).</span></span>

<span data-ttu-id="65bc4-107">**Windows Vista: a JET_PWSTR** é introduzida no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="65bc4-107">**Windows Vista:  JET_PWSTR** is introduced in Windows Vista.</span></span>

```cpp
    typedef __nullterminated WCHAR * JET_PWSTR;
```

### <a name="data-types"></a><span data-ttu-id="65bc4-108">Tipos de dados</span><span class="sxs-lookup"><span data-stu-id="65bc4-108">Data Types</span></span>

<span data-ttu-id="65bc4-109">JET_PWSTR</span><span class="sxs-lookup"><span data-stu-id="65bc4-109">JET_PWSTR</span></span>

<span data-ttu-id="65bc4-110">Terminação nula, Cadeia de caracteres Unicode (Char \* ).</span><span class="sxs-lookup"><span data-stu-id="65bc4-110">Null-terminated, Unicode string (char \*).</span></span>

### <a name="requirements"></a><span data-ttu-id="65bc4-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65bc4-111">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="65bc4-112"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="65bc4-112"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="65bc4-113">Requer o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="65bc4-113">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65bc4-114"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="65bc4-114"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="65bc4-115">Requer o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="65bc4-115">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65bc4-116"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="65bc4-116"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="65bc4-117">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="65bc4-117">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

