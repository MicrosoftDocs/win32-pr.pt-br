---
description: Obtém uma descrição da tabela de constantes.
ms.assetid: 3a7396c6-3a3e-44c2-96b7-60339015b376
title: 'Método ID3DXConstantTable:: GetDesc (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 71eeb951ec73fbeb9942f52e30ab9ad59e374ee7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103837939"
---
# <a name="id3dxconstanttablegetdesc-method"></a><span data-ttu-id="f678c-103">Método ID3DXConstantTable:: GetDesc</span><span class="sxs-lookup"><span data-stu-id="f678c-103">ID3DXConstantTable::GetDesc method</span></span>

<span data-ttu-id="f678c-104">Obtém uma descrição da tabela de constantes.</span><span class="sxs-lookup"><span data-stu-id="f678c-104">Gets a description of the constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="f678c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f678c-105">Syntax</span></span>


```C++
HRESULT GetDesc(
  [in] D3DXCONSTANTTABLE_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="f678c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f678c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f678c-107">*pDesc* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f678c-107">*pDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f678c-108">Tipo: **[ **D3DXCONSTANTTABLE \_ desc**](d3dxconstanttable-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="f678c-108">Type: **[**D3DXCONSTANTTABLE\_DESC**](d3dxconstanttable-desc.md)\***</span></span>

<span data-ttu-id="f678c-109">Descrição da tabela de constantes.</span><span class="sxs-lookup"><span data-stu-id="f678c-109">Description of the constant table.</span></span> <span data-ttu-id="f678c-110">Consulte [**D3DXCONSTANTTABLE \_ desc**](d3dxconstanttable-desc.md).</span><span class="sxs-lookup"><span data-stu-id="f678c-110">See [**D3DXCONSTANTTABLE\_DESC**](d3dxconstanttable-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f678c-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f678c-111">Return value</span></span>

<span data-ttu-id="f678c-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f678c-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f678c-113">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f678c-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f678c-114">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="f678c-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="f678c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f678c-115">Requirements</span></span>



| <span data-ttu-id="f678c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f678c-116">Requirement</span></span> | <span data-ttu-id="f678c-117">Valor</span><span class="sxs-lookup"><span data-stu-id="f678c-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f678c-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f678c-118">Header</span></span><br/>  | <dl> <span data-ttu-id="f678c-119"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="f678c-119"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="f678c-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f678c-120">Library</span></span><br/> | <dl> <span data-ttu-id="f678c-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f678c-121"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="f678c-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="f678c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f678c-123">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="f678c-123">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> <dt>

[<span data-ttu-id="f678c-124">**ID3DXConstantTable::GetConstantDesc**</span><span class="sxs-lookup"><span data-stu-id="f678c-124">**ID3DXConstantTable::GetConstantDesc**</span></span>](id3dxconstanttable--getconstantdesc.md)
</dt> </dl>

 

 




