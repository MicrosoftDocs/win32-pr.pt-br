---
description: 'Saiba mais sobre: JET_INSTANCE'
title: JET_INSTANCE
TOCTitle: JET_INSTANCE
ms:assetid: a4136bec-95b3-42d7-b21b-1df09197bb11
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294048(v=EXCHG.10)
ms:contentKeyID: 32765647
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
ms.openlocfilehash: 6e1fde3e01c8328d2fdaf6609c6772fda9cd1428
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922280"
---
# <a name="jet_instance"></a><span data-ttu-id="f78ce-103">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="f78ce-103">JET_INSTANCE</span></span>


<span data-ttu-id="f78ce-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="f78ce-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_instance"></a><span data-ttu-id="f78ce-105">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="f78ce-105">JET_INSTANCE</span></span>

<span data-ttu-id="f78ce-106">O tipo de dados **JET_INSTANCE** contém um identificador para a instância do banco de dado a ser usado para uma chamada para a API do Jet.</span><span class="sxs-lookup"><span data-stu-id="f78ce-106">The **JET_INSTANCE** data type contains a handle to the instance of the database to use for a call to the JET API.</span></span>

```cpp
    typedef JET_API_PTR JET_INSTANCE;
```

### <a name="data-types"></a><span data-ttu-id="f78ce-107">Tipos de dados</span><span class="sxs-lookup"><span data-stu-id="f78ce-107">Data Types</span></span>

<span data-ttu-id="f78ce-108">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="f78ce-108">JET_INSTANCE</span></span>

<span data-ttu-id="f78ce-109">**Nulo** ou [JET_instanceNil](./invalid-handle-constants.md) pode ser usado para indicar um identificador de instância inválido.</span><span class="sxs-lookup"><span data-stu-id="f78ce-109">Either **NULL** or [JET_instanceNil](./invalid-handle-constants.md) can be used to indicate an invalid instance handle.</span></span>

### <a name="remarks"></a><span data-ttu-id="f78ce-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="f78ce-110">Remarks</span></span>

<span data-ttu-id="f78ce-111">Esse identificador é obtido quando você cria uma instância do banco de dados chamando as funções [JetCreateInstance](./jetcreateinstance-function.md), [JetCreateInstance2](./jetcreateinstance2-function.md), [JetInit](./jetinit-function.md)ou [JetInit2](./jetinit2-function.md) .</span><span class="sxs-lookup"><span data-stu-id="f78ce-111">This handle is obtained when you create an instance of the database by calling the [JetCreateInstance](./jetcreateinstance-function.md), [JetCreateInstance2](./jetcreateinstance2-function.md), [JetInit](./jetinit-function.md), or [JetInit2](./jetinit2-function.md) functions.</span></span>

<span data-ttu-id="f78ce-112">**Windows XP:**  O uso explícito de instâncias só tem suporte no Windows XP e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="f78ce-112">**Windows XP:**  The explicit use of instances is only supported on Windows XP and later releases.</span></span>

<span data-ttu-id="f78ce-113">**Windows 2000:**  Há suporte apenas para uma instância global por processo.</span><span class="sxs-lookup"><span data-stu-id="f78ce-113">**Windows 2000:**  Only one global instance is supported per process.</span></span>

### <a name="requirements"></a><span data-ttu-id="f78ce-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f78ce-114">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f78ce-115"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="f78ce-115"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f78ce-116">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="f78ce-116">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f78ce-117"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="f78ce-117"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f78ce-118">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="f78ce-118">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f78ce-119"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="f78ce-119"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f78ce-120">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="f78ce-120">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="f78ce-121">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="f78ce-121">See Also</span></span>

[<span data-ttu-id="f78ce-122">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="f78ce-122">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="f78ce-123">JetCreateInstance2</span><span class="sxs-lookup"><span data-stu-id="f78ce-123">JetCreateInstance2</span></span>](./jetcreateinstance2-function.md)  
[<span data-ttu-id="f78ce-124">JetInit</span><span class="sxs-lookup"><span data-stu-id="f78ce-124">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="f78ce-125">JetInit2</span><span class="sxs-lookup"><span data-stu-id="f78ce-125">JetInit2</span></span>](./jetinit2-function.md)
