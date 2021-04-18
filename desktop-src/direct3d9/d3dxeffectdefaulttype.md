---
description: Tipos de dados de efeito. Os dados estão contidos no membro de uma D3DXEFFECTDEFAULT.
ms.assetid: d698ad6e-2ce2-48d6-90be-49bc08f172a9
title: Enumeração D3DXEFFECTDEFAULTTYPE (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEFFECTDEFAULTTYPE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: ffd31167d712a8270011c061cd6328aa9214352e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105763904"
---
# <a name="d3dxeffectdefaulttype-enumeration"></a><span data-ttu-id="52a00-104">Enumeração D3DXEFFECTDEFAULTTYPE</span><span class="sxs-lookup"><span data-stu-id="52a00-104">D3DXEFFECTDEFAULTTYPE enumeration</span></span>

<span data-ttu-id="52a00-105">Tipos de dados de efeito.</span><span class="sxs-lookup"><span data-stu-id="52a00-105">Effect data types.</span></span> <span data-ttu-id="52a00-106">Os dados estão contidos no membro de uma [**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md).</span><span class="sxs-lookup"><span data-stu-id="52a00-106">The data is contained in the pValue member of [**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="52a00-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="52a00-107">Syntax</span></span>


```C++
typedef enum D3DXEFFECTDEFAULTTYPE { 
  D3DXEDT_STRING      = 1,
  D3DXEDT_FLOATS      = 2,
  D3DXEDT_DWORD       = 3,
  D3DXEDT_FORCEDWORD  = 0x7fffffff
} D3DXEFFECTDEFAULTTYPE, *LPD3DXEFFECTDEFAULTTYPE;
```



## <a name="constants"></a><span data-ttu-id="52a00-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="52a00-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="52a00-109"><span id="D3DXEDT_STRING"></span><span id="d3dxedt_string"></span>**\_Cadeia de caracteres D3DXEDT**</span><span class="sxs-lookup"><span data-stu-id="52a00-109"><span id="D3DXEDT_STRING"></span><span id="d3dxedt_string"></span>**D3DXEDT\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="52a00-110">O tipo de dados é uma cadeia de caracteres de texto ASCII terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="52a00-110">The data type is a NULL-terminated ASCII text string.</span></span>

</dd> <dt>

<span data-ttu-id="52a00-111"><span id="D3DXEDT_FLOATS"></span><span id="d3dxedt_floats"></span>**D3DXEDT \_ floats**</span><span class="sxs-lookup"><span data-stu-id="52a00-111"><span id="D3DXEDT_FLOATS"></span><span id="d3dxedt_floats"></span>**D3DXEDT\_FLOATS**</span></span>
</dt> <dd>

<span data-ttu-id="52a00-112">O tipo de dados é uma matriz do tipo float.</span><span class="sxs-lookup"><span data-stu-id="52a00-112">The data type is an array of type float.</span></span> <span data-ttu-id="52a00-113">O número de tipos float na matriz é especificado por NumBytes em [**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md).</span><span class="sxs-lookup"><span data-stu-id="52a00-113">The number of float types in the array is specified by NumBytes in [**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md).</span></span>

</dd> <dt>

<span data-ttu-id="52a00-114"><span id="D3DXEDT_DWORD"></span><span id="d3dxedt_dword"></span>**D3DXEDT \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="52a00-114"><span id="D3DXEDT_DWORD"></span><span id="d3dxedt_dword"></span>**D3DXEDT\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="52a00-115">O tipo de dados é um DWORD.</span><span class="sxs-lookup"><span data-stu-id="52a00-115">The data type is a DWORD.</span></span>

</dd> <dt>

<span data-ttu-id="52a00-116"><span id="D3DXEDT_FORCEDWORD"></span><span id="d3dxedt_forcedword"></span>**D3DXEDT \_ FORCEDWORD**</span><span class="sxs-lookup"><span data-stu-id="52a00-116"><span id="D3DXEDT_FORCEDWORD"></span><span id="d3dxedt_forcedword"></span>**D3DXEDT\_FORCEDWORD**</span></span>
</dt> <dd>

<span data-ttu-id="52a00-117">Força essa enumeração a compilar a 32 bits de tamanho.</span><span class="sxs-lookup"><span data-stu-id="52a00-117">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="52a00-118">Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="52a00-118">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="52a00-119">Este valor não é usado.</span><span class="sxs-lookup"><span data-stu-id="52a00-119">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="52a00-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52a00-120">Requirements</span></span>



| <span data-ttu-id="52a00-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="52a00-121">Requirement</span></span> | <span data-ttu-id="52a00-122">Valor</span><span class="sxs-lookup"><span data-stu-id="52a00-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="52a00-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="52a00-123">Header</span></span><br/> | <dl> <span data-ttu-id="52a00-124"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="52a00-124"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52a00-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="52a00-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52a00-126">Enumerações D3DX</span><span class="sxs-lookup"><span data-stu-id="52a00-126">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




