---
description: 'Saiba mais sobre: JET_PSTR'
title: JET_PSTR
TOCTitle: JET_PSTR
ms:assetid: acb1143f-a5ee-4088-9f05-cc2aeef23442
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294056(v=EXCHG.10)
ms:contentKeyID: 32765667
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
ms.openlocfilehash: 6bbed2cad9f9c7816d010a429b1db8eb5306fc1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811509"
---
# <a name="jet_pstr"></a><span data-ttu-id="3303b-103">JET_PSTR</span><span class="sxs-lookup"><span data-stu-id="3303b-103">JET_PSTR</span></span>


<span data-ttu-id="3303b-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="3303b-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_pstr"></a><span data-ttu-id="3303b-105">JET_PSTR</span><span class="sxs-lookup"><span data-stu-id="3303b-105">JET_PSTR</span></span>

<span data-ttu-id="3303b-106">O tipo de dados JET_PSTR contém uma cadeia de caracteres ASCII terminada em nulo (Char \* ).</span><span class="sxs-lookup"><span data-stu-id="3303b-106">The JET_PSTR data type contains a null-terminated ASCII string (char \*).</span></span>

<span data-ttu-id="3303b-107">**Windows Vista: a JET_PSTR** é introduzida no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3303b-107">**Windows Vista:  JET_PSTR** is introduced in Windows Vista.</span></span>

```cpp
    typedef __nullterminated char *  JET_PSTR;
```

### <a name="data-types"></a><span data-ttu-id="3303b-108">Tipos de dados</span><span class="sxs-lookup"><span data-stu-id="3303b-108">Data Types</span></span>

<span data-ttu-id="3303b-109">JET_PSTR</span><span class="sxs-lookup"><span data-stu-id="3303b-109">JET_PSTR</span></span>

<span data-ttu-id="3303b-110">Terminação nula, Cadeia de caracteres ASCII (Char \* ).</span><span class="sxs-lookup"><span data-stu-id="3303b-110">Null-terminated, ASCII string (char \*).</span></span>

### <a name="requirements"></a><span data-ttu-id="3303b-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3303b-111">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3303b-112"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="3303b-112"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="3303b-113">Requer o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3303b-113">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3303b-114"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="3303b-114"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="3303b-115">Requer o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="3303b-115">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3303b-116"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="3303b-116"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="3303b-117">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="3303b-117">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

