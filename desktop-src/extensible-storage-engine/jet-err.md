---
description: 'Saiba mais sobre: JET_ERR'
title: JET_ERR
TOCTitle: JET_ERR
ms:assetid: cd9cb876-251c-458d-a015-8e9045e77fc9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294092(v=EXCHG.10)
ms:contentKeyID: 32765707
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
ms.openlocfilehash: 35120be9a26dcbdc8d012cd12c871ddcf8f71555
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "105812239"
---
# <a name="jet_err"></a><span data-ttu-id="42c1f-103">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="42c1f-103">JET_ERR</span></span>


<span data-ttu-id="42c1f-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="42c1f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_err"></a><span data-ttu-id="42c1f-105">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="42c1f-105">JET_ERR</span></span>

<span data-ttu-id="42c1f-106">O tipo de dados **JET_ERR** contém um [código de erro do mecanismo de armazenamento extensível](./extensible-storage-engine-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="42c1f-106">The **JET_ERR** data type contains an [Extensible Storage Engine error code](./extensible-storage-engine-error-codes.md).</span></span>

```cpp
typedef long JET_ERR;
```

### <a name="data-types"></a><span data-ttu-id="42c1f-107">Tipos de dados</span><span class="sxs-lookup"><span data-stu-id="42c1f-107">Data Types</span></span>

<span data-ttu-id="42c1f-108">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="42c1f-108">JET_ERR</span></span>

<span data-ttu-id="42c1f-109">Um valor zero (correspondente a JET_errSuccess) indica que a chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="42c1f-109">A zero value (corresponding to JET_errSuccess) indicates that the call succeeded.</span></span> <span data-ttu-id="42c1f-110">Um valor positivo avisa sobre uma condição não fatal que ocorreu durante uma chamada com êxito.</span><span class="sxs-lookup"><span data-stu-id="42c1f-110">A positive value warns of a non-fatal condition that occurred during an otherwise successful call.</span></span> <span data-ttu-id="42c1f-111">Um valor negativo indica que a chamada falhou.</span><span class="sxs-lookup"><span data-stu-id="42c1f-111">A negative value indicates that the call failed.</span></span>

### <a name="remarks"></a><span data-ttu-id="42c1f-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="42c1f-112">Remarks</span></span>

<span data-ttu-id="42c1f-113">Para obter informações sobre como retornar erros como HRESULTs, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md).</span><span class="sxs-lookup"><span data-stu-id="42c1f-113">For information about returning errors as HRESULTs, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md).</span></span> <span data-ttu-id="42c1f-114">Para obter informações sobre sinalizadores para configurar o banco de dados para lidar com erros, consulte [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="42c1f-114">For information about flags for configuring the database to handle errors, see [Error Handling Parameters](./error-handling-parameters.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="42c1f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42c1f-115">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="42c1f-116"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="42c1f-116"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="42c1f-117">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="42c1f-117">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42c1f-118"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="42c1f-118"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="42c1f-119">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="42c1f-119">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42c1f-120"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="42c1f-120"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="42c1f-121">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="42c1f-121">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="42c1f-122">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="42c1f-122">See Also</span></span>

[<span data-ttu-id="42c1f-123">Erros do mecanismo de armazenamento extensível</span><span class="sxs-lookup"><span data-stu-id="42c1f-123">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="42c1f-124">Códigos de erro do mecanismo de armazenamento extensível</span><span class="sxs-lookup"><span data-stu-id="42c1f-124">Extensible Storage Engine Error Codes</span></span>](./extensible-storage-engine-error-codes.md)  
[<span data-ttu-id="42c1f-125">Parâmetros de tratamento de erros</span><span class="sxs-lookup"><span data-stu-id="42c1f-125">Error Handling Parameters</span></span>](./error-handling-parameters.md)
