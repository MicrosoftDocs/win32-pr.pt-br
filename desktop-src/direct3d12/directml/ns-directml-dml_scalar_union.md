---
UID: NS:directml.DML_SCALAR_UNION
title: DML_SCALAR_UNION
description: Uma união de tipos escalares.
helpviewer_keywords:
- DML_SCALAR_UNION
- DML_SCALAR_UNION structure
- direct3d12.dml_scalar_union
- directml/DML_SCALAR_UNION
ms.topic: reference
tech.root: directml
ms.date: 10/30/2020
ms.keywords: DML_SCALAR_UNION, DML_SCALAR_UNION structure, direct3d12.dml_scalar_union, directml/DML_SCALAR_UNION
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DML_SCALAR_UNION
- directml/DML_SCALAR_UNION
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- DirectML.h
api_name:
- DML_SCALAR_UNION
ms.openlocfilehash: d53ec7025d3da5a07a648849e366d436755ad3f1
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417023"
---
# <a name="dml_scalar_union-union-directmlh"></a><span data-ttu-id="3a8cc-103">DML_SCALAR_UNION união (directml.h)</span><span class="sxs-lookup"><span data-stu-id="3a8cc-103">DML_SCALAR_UNION union (directml.h)</span></span>
<span data-ttu-id="3a8cc-104">Uma união de tipos escalares.</span><span class="sxs-lookup"><span data-stu-id="3a8cc-104">A union of scalar types.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3a8cc-105">Essa API está disponível como parte do pacote redistribuível autônomo directML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1.4 e posterior).</span><span class="sxs-lookup"><span data-stu-id="3a8cc-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="3a8cc-106">Consulte também [Histórico de versão do DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="3a8cc-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3a8cc-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3a8cc-107">Syntax</span></span>
```cpp
union DML_SCALAR_UNION {
  BYTE   Bytes[8];
  INT8   Int8;
  UINT8  UInt8;
  INT16  Int16;
  UINT16 UInt16;
  INT32  Int32;
  UINT32 UInt32;
  INT64  Int64;
  UINT64 UInt64;
  FLOAT  Float32;
  DOUBLE Float64;
};
```



## <a name="members"></a><span data-ttu-id="3a8cc-108">Membros</span><span class="sxs-lookup"><span data-stu-id="3a8cc-108">Members</span></span>

`Bytes`

<span data-ttu-id="3a8cc-109">Uma matriz de 8 byte.</span><span class="sxs-lookup"><span data-stu-id="3a8cc-109">An 8-byte array.</span></span>


`Int8`

<span data-ttu-id="3a8cc-110">Um inteiro com sinal de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="3a8cc-110">An 8-bit signed integer.</span></span>


`UInt8`

<span data-ttu-id="3a8cc-111">Um inteiro de 8 bits sem sinal.</span><span class="sxs-lookup"><span data-stu-id="3a8cc-111">An 8-bit unsigned integer.</span></span>


`Int16`

<span data-ttu-id="3a8cc-112">Um inteiro de 16 bits com sinal.</span><span class="sxs-lookup"><span data-stu-id="3a8cc-112">A 16-bit signed integer.</span></span>


`UInt16`

<span data-ttu-id="3a8cc-113">Um inteiro sem sinal de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="3a8cc-113">A 16-bit unsigned integer.</span></span>


`Int32`

<span data-ttu-id="3a8cc-114">Um inteiro com sinal de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="3a8cc-114">A 32-bit signed integer.</span></span>


`UInt32`

<span data-ttu-id="3a8cc-115">Um inteiro sem sinal de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="3a8cc-115">A 32-bit unsigned integer.</span></span>


`Int64`

<span data-ttu-id="3a8cc-116">Um inteiro com sinal de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="3a8cc-116">A 64-bit signed integer.</span></span>


`UInt64`

<span data-ttu-id="3a8cc-117">Um inteiro sem sinal de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="3a8cc-117">A 64-bit unsigned integer.</span></span>


`Float32`

<span data-ttu-id="3a8cc-118">Um número de ponto flutuante de precisão simples.</span><span class="sxs-lookup"><span data-stu-id="3a8cc-118">A single precision floating-point number.</span></span>


`Float64`

<span data-ttu-id="3a8cc-119">Um número de ponto flutuante de precisão dupla.</span><span class="sxs-lookup"><span data-stu-id="3a8cc-119">A double precision floating-point number.</span></span>



## <a name="requirements"></a><span data-ttu-id="3a8cc-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a8cc-120">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="3a8cc-121">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="3a8cc-121">**Header**</span></span> | <span data-ttu-id="3a8cc-122">directml.h</span><span class="sxs-lookup"><span data-stu-id="3a8cc-122">directml.h</span></span> |