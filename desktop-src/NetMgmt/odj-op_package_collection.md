---
title: OP_PACKAGE_PART_COLLECTION
description: Definição de IDL de OP_PACKAGE_PART_COLLECTION
ms.assetid: a7abf011-0335-4869-b4d9-144b2f392241
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: f8eb61397045a382fe5933025a4eeda2f563e838
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/14/2020
ms.locfileid: "104008553"
---
# <a name="op_package_part_collection-structure"></a><span data-ttu-id="8529e-103">Estrutura de OP_PACKAGE_PART_COLLECTION</span><span class="sxs-lookup"><span data-stu-id="8529e-103">OP_PACKAGE_PART_COLLECTION structure</span></span>

<span data-ttu-id="8529e-104">Especifica uma estrutura que contém uma matriz de estruturas de OP_PACKAGE_PART.</span><span class="sxs-lookup"><span data-stu-id="8529e-104">Specifies a structure that contains an array of OP_PACKAGE_PART structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="8529e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8529e-105">Syntax</span></span>

```C++
typedef struct _OP_PACKAGE_PART_COLLECTION
{
    ULONG                                 cParts;
    [size_is(cParts)]   POP_PACKAGE_PART  pParts;
    OP_BLOB                               Extension;
} OP_PACKAGE_PART_COLLECTION, *POP_PACKAGE_PART_COLLECTION;
```

## <a name="members"></a><span data-ttu-id="8529e-106">Membros</span><span class="sxs-lookup"><span data-stu-id="8529e-106">Members</span></span>

### <a name="cparts"></a><span data-ttu-id="8529e-107">cParts</span><span class="sxs-lookup"><span data-stu-id="8529e-107">cParts</span></span>

<span data-ttu-id="8529e-108">Contém o número de elementos em pParts.</span><span class="sxs-lookup"><span data-stu-id="8529e-108">Contains the number of elements in pParts.</span></span>

### <a name="pparts"></a><span data-ttu-id="8529e-109">pParts</span><span class="sxs-lookup"><span data-stu-id="8529e-109">pParts</span></span>

<span data-ttu-id="8529e-110">Contém uma matriz de estruturas de OP_PACKAGE_PART.</span><span class="sxs-lookup"><span data-stu-id="8529e-110">Contains an array of OP_PACKAGE_PART structures.</span></span>

### <a name="extension"></a><span data-ttu-id="8529e-111">Extensão</span><span class="sxs-lookup"><span data-stu-id="8529e-111">Extension</span></span>

<span data-ttu-id="8529e-112">Reservado para uso futuro e deve ser definido como todos os zeros.</span><span class="sxs-lookup"><span data-stu-id="8529e-112">Reserved for future use and MUST be set to all zeros.</span></span>

## <a name="see-also"></a><span data-ttu-id="8529e-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="8529e-113">See also</span></span>

[<span data-ttu-id="8529e-114">**Definições de IDL de ingresso no domínio offline**</span><span class="sxs-lookup"><span data-stu-id="8529e-114">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="8529e-115">**\_parte do pacote de op \_**</span><span class="sxs-lookup"><span data-stu-id="8529e-115">**OP\_PACKAGE\_PART**</span></span>](odj-op_package_part.md)

[<span data-ttu-id="8529e-116">**BLOB de OP \_**</span><span class="sxs-lookup"><span data-stu-id="8529e-116">**OP\_BLOB**</span></span>](odj-op_blob.md)

