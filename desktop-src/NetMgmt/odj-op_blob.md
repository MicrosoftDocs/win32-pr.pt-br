---
title: OP_BLOB
description: Definição de IDL de OP_BLOB
ms.assetid: c215c793-5fad-4baa-97c0-c809040dda1e
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: fab6df11be3bf719f787c40a41a50d948a865474
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/14/2020
ms.locfileid: "104366870"
---
# <a name="op_blob-structure"></a><span data-ttu-id="db522-103">Estrutura de OP_BLOB</span><span class="sxs-lookup"><span data-stu-id="db522-103">OP_BLOB structure</span></span>

<span data-ttu-id="db522-104">Contém um buffer de bytes opaco.</span><span class="sxs-lookup"><span data-stu-id="db522-104">Contains an opaque byte buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="db522-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="db522-105">Syntax</span></span>

```C++
typedef struct _OP_BLOB
{
    ULONG                       cbBlob;
    [size_is(cbBlob)]   PBYTE   pBlob;
} OP_BLOB, *POP_BLOB;
```

## <a name="members"></a><span data-ttu-id="db522-106">Membros</span><span class="sxs-lookup"><span data-stu-id="db522-106">Members</span></span>

### <a name="cbblob"></a><span data-ttu-id="db522-107">cbBlob</span><span class="sxs-lookup"><span data-stu-id="db522-107">cbBlob</span></span>

<span data-ttu-id="db522-108">Especifica o tamanho de pBlob em bytes.</span><span class="sxs-lookup"><span data-stu-id="db522-108">Specifies the the size of pBlob in bytes.</span></span>

### <a name="pblob"></a><span data-ttu-id="db522-109">pBlob</span><span class="sxs-lookup"><span data-stu-id="db522-109">pBlob</span></span>

<span data-ttu-id="db522-110">Aponta para um buffer de bytes.</span><span class="sxs-lookup"><span data-stu-id="db522-110">Points to a byte buffer.</span></span>

## <a name="see-also"></a><span data-ttu-id="db522-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="db522-111">See also</span></span>

[<span data-ttu-id="db522-112">**Definições de IDL de ingresso no domínio offline**</span><span class="sxs-lookup"><span data-stu-id="db522-112">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)
