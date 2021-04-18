---
title: Função D3D12DecomposeSubresource (D3dx12.h)
description: Gera a fatia MIP, a fatia da matriz e a fatia do plano que correspondem ao índice de subrecurso especificado.
ms.assetid: 89FAD7C5-E732-4E74-AC2F-DEECD6ADDA7D
keywords:
- Função D3D12DecomposeSubresource
topic_type:
- apiref
api_name:
- D3D12DecomposeSubresource
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec147833ee94969880865f679d40a198e0b22852
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105793656"
---
# <a name="d3d12decomposesubresource-function"></a><span data-ttu-id="07348-104">Função D3D12DecomposeSubresource</span><span class="sxs-lookup"><span data-stu-id="07348-104">D3D12DecomposeSubresource function</span></span>

<span data-ttu-id="07348-105">Gera a fatia MIP, a fatia da matriz e a fatia do plano que correspondem ao índice de subrecurso especificado.</span><span class="sxs-lookup"><span data-stu-id="07348-105">Outputs the mip slice, array slice, and plane slice that correspond to the specified subresource index.</span></span>

## <a name="syntax"></a><span data-ttu-id="07348-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="07348-106">Syntax</span></span>


```C++
void inline D3D12DecomposeSubresource(
        UINT Subresource,
        UINT MipLevels,
        UINT ArraySize,
  _Out_ T    &MipSlice,
  _Out_ U    &ArraySlice,
  _Out_ V    &PlaneSlice
);
```



## <a name="parameters"></a><span data-ttu-id="07348-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="07348-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07348-108">*Sub-recurso*</span><span class="sxs-lookup"><span data-stu-id="07348-108">*Subresource*</span></span> 
</dt> <dd>

<span data-ttu-id="07348-109">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="07348-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="07348-110">O índice do subrecurso.</span><span class="sxs-lookup"><span data-stu-id="07348-110">The index of the subresource.</span></span>

</dd> <dt>

<span data-ttu-id="07348-111">*MipLevels*</span><span class="sxs-lookup"><span data-stu-id="07348-111">*MipLevels*</span></span> 
</dt> <dd>

<span data-ttu-id="07348-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="07348-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="07348-113">O número máximo de níveis de mipmap no subrecurso.</span><span class="sxs-lookup"><span data-stu-id="07348-113">The maximum number of mipmap levels in the subresource.</span></span>

</dd> <dt>

<span data-ttu-id="07348-114">*ArraySize*</span><span class="sxs-lookup"><span data-stu-id="07348-114">*ArraySize*</span></span> 
</dt> <dd>

<span data-ttu-id="07348-115">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="07348-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="07348-116">O número de elementos na matriz.</span><span class="sxs-lookup"><span data-stu-id="07348-116">The number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="07348-117">*MipSlice* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="07348-117">*MipSlice* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="07348-118">Tipo: **T**</span><span class="sxs-lookup"><span data-stu-id="07348-118">Type: **T**</span></span>

<span data-ttu-id="07348-119">Gera a fatia MIP que corresponde ao índice de subrecurso fornecido.</span><span class="sxs-lookup"><span data-stu-id="07348-119">Outputs the mip slice that corresponds to the given subresource index.</span></span>

</dd> <dt>

<span data-ttu-id="07348-120">*ArraySlice* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="07348-120">*ArraySlice* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="07348-121">Tipo: **U**</span><span class="sxs-lookup"><span data-stu-id="07348-121">Type: **U**</span></span>

<span data-ttu-id="07348-122">Gera a fatia da matriz que corresponde ao índice de subrecurso fornecido.</span><span class="sxs-lookup"><span data-stu-id="07348-122">Outputs the array slice that corresponds to the given subresource index.</span></span>

</dd> <dt>

<span data-ttu-id="07348-123">*PlaneSlice* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="07348-123">*PlaneSlice* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="07348-124">Tipo: **V**</span><span class="sxs-lookup"><span data-stu-id="07348-124">Type: **V**</span></span>

<span data-ttu-id="07348-125">Gera a fatia do plano que corresponde ao índice de subrecurso fornecido.</span><span class="sxs-lookup"><span data-stu-id="07348-125">Outputs the plane slice that corresponds to the given subresource index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07348-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="07348-126">Return value</span></span>

<span data-ttu-id="07348-127">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="07348-127">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="07348-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="07348-128">Remarks</span></span>

<span data-ttu-id="07348-129">Essa função determina qual fatia MIP, fatia de matriz e fatia de plano correspondem a um determinado índice de subrecurso.</span><span class="sxs-lookup"><span data-stu-id="07348-129">This function determines which mip slice, array slice, and plane slice correspond to a given subresource index.</span></span> <span data-ttu-id="07348-130">Esse é um utilitário útil, embora seja específico ao C++.</span><span class="sxs-lookup"><span data-stu-id="07348-130">This is a useful utility, though it is C++ specific.</span></span>

<span data-ttu-id="07348-131">Essa função é declarada da seguinte maneira, com parâmetros C++ modelos para tipos **T**, **U** e **V**:</span><span class="sxs-lookup"><span data-stu-id="07348-131">This function is declared as follows, with C++ templatized parameters for types **T**, **U**, and **V**:</span></span>


```c++
template <typename T, typename U, typename V>
inline void D3D12DecomposeSubresource( UINT Subresource, UINT MipLevels, UINT ArraySize, _Out_ T& MipSlice, _Out_ U& ArraySlice, _Out_ V& PlaneSlice )
{
    MipSlice = static_cast<T>(Subresource % MipLevels);
    ArraySlice = static_cast<U>((Subresource / MipLevels) % ArraySize);
    PlaneSlice = static_cast<V>(Subresource / (MipLevels * ArraySize));
}
```



## <a name="requirements"></a><span data-ttu-id="07348-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07348-132">Requirements</span></span>



| <span data-ttu-id="07348-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="07348-133">Requirement</span></span> | <span data-ttu-id="07348-134">Valor</span><span class="sxs-lookup"><span data-stu-id="07348-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="07348-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="07348-135">Header</span></span><br/>  | <dl> <span data-ttu-id="07348-136"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="07348-136"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="07348-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="07348-137">Library</span></span><br/> | <dl> <span data-ttu-id="07348-138"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="07348-138"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="07348-139">DLL</span><span class="sxs-lookup"><span data-stu-id="07348-139">DLL</span></span><br/>     | <dl> <span data-ttu-id="07348-140"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07348-140"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07348-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="07348-141">See also</span></span>

[<span data-ttu-id="07348-142">Funções auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="07348-142">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)

[<span data-ttu-id="07348-143">Sub-recursos</span><span class="sxs-lookup"><span data-stu-id="07348-143">Subresources</span></span>](subresources.md)
