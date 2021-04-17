---
UID: NS:directml.DML_SCALAR_UNION
title: DML_SCALAR_UNION
description: Uma União de tipos escalares.
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
ms.openlocfilehash: 0abef8cd5a694fa82e0e54e334834773f1f75e20
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "105766581"
---
# <a name="dml_scalar_union-union-directmlh"></a><span data-ttu-id="820a6-103">União de DML_SCALAR_UNION (directml. h)</span><span class="sxs-lookup"><span data-stu-id="820a6-103">DML_SCALAR_UNION union (directml.h)</span></span>
<span data-ttu-id="820a6-104">Uma União de tipos escalares.</span><span class="sxs-lookup"><span data-stu-id="820a6-104">A union of scalar types.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="820a6-105">Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="820a6-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="820a6-106">Consulte também o [histórico de versão do DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="820a6-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="820a6-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="820a6-107">Syntax</span></span>
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



## <a name="members"></a><span data-ttu-id="820a6-108">Membros</span><span class="sxs-lookup"><span data-stu-id="820a6-108">Members</span></span>

`Bytes`

<span data-ttu-id="820a6-109">Uma matriz de 8 bytes.</span><span class="sxs-lookup"><span data-stu-id="820a6-109">An 8-byte array.</span></span>


`Int8`

<span data-ttu-id="820a6-110">Um inteiro com sinal de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="820a6-110">An 8-bit signed integer.</span></span>


`UInt8`

<span data-ttu-id="820a6-111">Um inteiro de 8 bits sem sinal.</span><span class="sxs-lookup"><span data-stu-id="820a6-111">An 8-bit unsigned integer.</span></span>


`Int16`

<span data-ttu-id="820a6-112">Um inteiro de 16 bits com sinal.</span><span class="sxs-lookup"><span data-stu-id="820a6-112">A 16-bit signed integer.</span></span>


`UInt16`

<span data-ttu-id="820a6-113">Um inteiro sem sinal de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="820a6-113">A 16-bit unsigned integer.</span></span>


`Int32`

<span data-ttu-id="820a6-114">Um inteiro com sinal de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="820a6-114">A 32-bit signed integer.</span></span>


`UInt32`

<span data-ttu-id="820a6-115">Um inteiro sem sinal de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="820a6-115">A 32-bit unsigned integer.</span></span>


`Int64`

<span data-ttu-id="820a6-116">Um inteiro com sinal de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="820a6-116">A 64-bit signed integer.</span></span>


`UInt64`

<span data-ttu-id="820a6-117">Um inteiro sem sinal de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="820a6-117">A 64-bit unsigned integer.</span></span>


`Float32`

<span data-ttu-id="820a6-118">Um número de ponto flutuante de precisão simples.</span><span class="sxs-lookup"><span data-stu-id="820a6-118">A single precision floating-point number.</span></span>


`Float64`

<span data-ttu-id="820a6-119">Um número de ponto flutuante de precisão dupla.</span><span class="sxs-lookup"><span data-stu-id="820a6-119">A double precision floating-point number.</span></span>



## <a name="requirements"></a><span data-ttu-id="820a6-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="820a6-120">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="820a6-121">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="820a6-121">**Header**</span></span> | <span data-ttu-id="820a6-122">directml. h</span><span class="sxs-lookup"><span data-stu-id="820a6-122">directml.h</span></span> |