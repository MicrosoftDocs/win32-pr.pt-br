---
description: Obtém uma constante procurando seu nome.
ms.assetid: 785a2d4f-6391-4419-a0b8-d8244a03ceae
title: 'Método ID3DXConstantTable:: GetConstantByName (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetConstantByName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3df4fc2cf44e035daf208d5dd14602e89b528ed1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105813352"
---
# <a name="id3dxconstanttablegetconstantbyname-method"></a><span data-ttu-id="8163f-103">Método ID3DXConstantTable:: GetConstantByName</span><span class="sxs-lookup"><span data-stu-id="8163f-103">ID3DXConstantTable::GetConstantByName method</span></span>

<span data-ttu-id="8163f-104">Obtém uma constante procurando seu nome.</span><span class="sxs-lookup"><span data-stu-id="8163f-104">Gets a constant by looking up its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="8163f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8163f-105">Syntax</span></span>


```C++
D3DXHANDLE GetConstantByName(
  [in] D3DXHANDLE hConstant,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="8163f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8163f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8163f-107">*hConstant* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8163f-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8163f-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="8163f-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="8163f-109">Identificador exclusivo para a estrutura de dados pai.</span><span class="sxs-lookup"><span data-stu-id="8163f-109">Unique identifier to the parent data structure.</span></span> <span data-ttu-id="8163f-110">Se a constante for um parâmetro de nível superior (não há nenhuma estrutura de dados pai), use **NULL**.</span><span class="sxs-lookup"><span data-stu-id="8163f-110">If the constant is a top-level parameter (there is no parent data structure), use **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8163f-111">*pname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8163f-111">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8163f-112">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8163f-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8163f-113">Nome da constante.</span><span class="sxs-lookup"><span data-stu-id="8163f-113">Name of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8163f-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8163f-114">Return value</span></span>

<span data-ttu-id="8163f-115">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="8163f-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="8163f-116">Retorna um identificador exclusivo para a constante.</span><span class="sxs-lookup"><span data-stu-id="8163f-116">Returns a unique identifier to the constant.</span></span>

## <a name="requirements"></a><span data-ttu-id="8163f-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8163f-117">Requirements</span></span>



| <span data-ttu-id="8163f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8163f-118">Requirement</span></span> | <span data-ttu-id="8163f-119">Valor</span><span class="sxs-lookup"><span data-stu-id="8163f-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8163f-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8163f-120">Header</span></span><br/>  | <dl> <span data-ttu-id="8163f-121"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="8163f-121"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="8163f-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8163f-122">Library</span></span><br/> | <dl> <span data-ttu-id="8163f-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8163f-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="8163f-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="8163f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8163f-125">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="8163f-125">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
