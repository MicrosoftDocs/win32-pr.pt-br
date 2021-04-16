---
description: Define o conteúdo do buffer para a tabela de constantes.
ms.assetid: 6058795c-fa32-42aa-9a36-af0b7f6eed1d
title: 'Método ID3DXConstantTable:: SetValue (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetValue
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e5e02c43e0d0ad84615650bc0b1c0d5fd5654e38
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105765227"
---
# <a name="id3dxconstanttablesetvalue-method"></a><span data-ttu-id="af7cf-103">Método ID3DXConstantTable:: SetValue</span><span class="sxs-lookup"><span data-stu-id="af7cf-103">ID3DXConstantTable::SetValue method</span></span>

<span data-ttu-id="af7cf-104">Define o conteúdo do buffer para a tabela de constantes.</span><span class="sxs-lookup"><span data-stu-id="af7cf-104">Sets the contents of the buffer to the constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="af7cf-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="af7cf-105">Syntax</span></span>


```C++
HRESULT SetValue(
  [in] LPDIRECT3DDEVICE9 pDevice,
  [in] D3DXHANDLE        hConstant,
  [in] LPCVOID           pData,
  [in] UINT              Bytes
);
```



## <a name="parameters"></a><span data-ttu-id="af7cf-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="af7cf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af7cf-107">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="af7cf-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af7cf-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="af7cf-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="af7cf-109">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , representando o dispositivo associado à tabela constante.</span><span class="sxs-lookup"><span data-stu-id="af7cf-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="af7cf-110">*hConstant* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="af7cf-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af7cf-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="af7cf-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="af7cf-112">Identificador exclusivo para uma constante.</span><span class="sxs-lookup"><span data-stu-id="af7cf-112">Unique identifier to a constant.</span></span> <span data-ttu-id="af7cf-113">Consulte [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="af7cf-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="af7cf-114">*pData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="af7cf-114">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af7cf-115">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="af7cf-115">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="af7cf-116">Buffer que contém dados.</span><span class="sxs-lookup"><span data-stu-id="af7cf-116">Buffer containing data.</span></span>

</dd> <dt>

<span data-ttu-id="af7cf-117">*Bytes* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="af7cf-117">*Bytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af7cf-118">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="af7cf-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="af7cf-119">Tamanho do buffer, em bytes.</span><span class="sxs-lookup"><span data-stu-id="af7cf-119">Size of the buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af7cf-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="af7cf-120">Return value</span></span>

<span data-ttu-id="af7cf-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="af7cf-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="af7cf-122">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="af7cf-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="af7cf-123">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="af7cf-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="af7cf-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af7cf-124">Requirements</span></span>



| <span data-ttu-id="af7cf-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="af7cf-125">Requirement</span></span> | <span data-ttu-id="af7cf-126">Valor</span><span class="sxs-lookup"><span data-stu-id="af7cf-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="af7cf-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="af7cf-127">Header</span></span><br/>  | <dl> <span data-ttu-id="af7cf-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="af7cf-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="af7cf-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="af7cf-129">Library</span></span><br/> | <dl> <span data-ttu-id="af7cf-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="af7cf-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="af7cf-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="af7cf-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af7cf-132">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="af7cf-132">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
