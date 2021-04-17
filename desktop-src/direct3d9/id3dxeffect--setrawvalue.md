---
description: Defina um intervalo contíguo de constantes de sombreador com uma cópia de memória.
ms.assetid: 8a3b5141-c67a-45b9-91c2-1877642164e3
title: 'Método ID3DXEffect:: SetRawValue (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.SetRawValue
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: cc3ce5eb547032ced5d0d79c533cefd1d2daab3a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105812201"
---
# <a name="id3dxeffectsetrawvalue-method"></a><span data-ttu-id="d2717-103">Método ID3DXEffect:: SetRawValue</span><span class="sxs-lookup"><span data-stu-id="d2717-103">ID3DXEffect::SetRawValue method</span></span>

<span data-ttu-id="d2717-104">Defina um intervalo contíguo de constantes de sombreador com uma cópia de memória.</span><span class="sxs-lookup"><span data-stu-id="d2717-104">Set a contiguous range of shader constants with a memory copy.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2717-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d2717-105">Syntax</span></span>


```C++
HRESULT SetRawValue(
  [in] D3DXHANDLE Handle,
  [in] void       *pData,
  [in] DWORD      OffsetInBytes,
  [in] DWORD      Bytes
);
```



## <a name="parameters"></a><span data-ttu-id="d2717-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d2717-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2717-107">*Identificador* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="d2717-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2717-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="d2717-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="d2717-109">Manipule o valor a ser definido ou o nome do valor passado como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d2717-109">Handle to the value to set, or the name of the value passed in as a string.</span></span> <span data-ttu-id="d2717-110">A passagem de um identificador é mais eficiente.</span><span class="sxs-lookup"><span data-stu-id="d2717-110">Passing in a handle is more efficient.</span></span> <span data-ttu-id="d2717-111">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="d2717-111">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="d2717-112">*pData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d2717-112">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2717-113">Tipo: **void \***</span><span class="sxs-lookup"><span data-stu-id="d2717-113">Type: **void\***</span></span>

<span data-ttu-id="d2717-114">Ponteiro para um buffer que contém os dados a serem definidos.</span><span class="sxs-lookup"><span data-stu-id="d2717-114">Pointer to a buffer containing the data to be set.</span></span> <span data-ttu-id="d2717-115">O SetRawValue verifica a memória válida, mas não faz nenhuma verificação para dados válidos.</span><span class="sxs-lookup"><span data-stu-id="d2717-115">SetRawValue checks for valid memory, but does not do any checking for valid data.</span></span>

</dd> <dt>

<span data-ttu-id="d2717-116">*OffsetInBytes* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d2717-116">*OffsetInBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2717-117">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d2717-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d2717-118">Número de bytes entre o início dos dados de efeito e o início das constantes de efeito que você vai definir.</span><span class="sxs-lookup"><span data-stu-id="d2717-118">Number of bytes between the beginning of the effect data and the beginning of the effect constants you are going to set.</span></span>

</dd> <dt>

<span data-ttu-id="d2717-119">*Bytes* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d2717-119">*Bytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2717-120">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d2717-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d2717-121">O tamanho do buffer a ser definido, em bytes.</span><span class="sxs-lookup"><span data-stu-id="d2717-121">The size of the buffer to be set, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2717-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d2717-122">Return value</span></span>

<span data-ttu-id="d2717-123">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d2717-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d2717-124">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d2717-124">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="d2717-125">Se o método falhar, o valor de retorno poderá ser um dos seguintes: E \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="d2717-125">If the method fails, the return value can be one of the following:E\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2717-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="d2717-126">Remarks</span></span>

<span data-ttu-id="d2717-127">O SetRawValue é uma maneira muito rápida de definir constantes de efeito, pois ele executa uma cópia de memória sem executar a validação ou qualquer conversão de dados (como converter uma matriz de linha principal em uma matriz de coluna principal).</span><span class="sxs-lookup"><span data-stu-id="d2717-127">SetRawValue is a very fast way to set effect constants since it performs a memory copy without performing validation or any data conversion (like converting a row-major matrix to a column-major matrix).</span></span> <span data-ttu-id="d2717-128">Use SetRawValue para definir uma série de constantes de efeito contíguos.</span><span class="sxs-lookup"><span data-stu-id="d2717-128">Use SetRawValue to set a series of contiguous effect constants.</span></span> <span data-ttu-id="d2717-129">Por exemplo, você pode definir uma matriz de vinte matrizes com 20 chamadas para [**ID3DXBaseEffect:: setmatrix**](id3dxbaseeffect--setmatrix.md) ou usando um único SetRawValue.</span><span class="sxs-lookup"><span data-stu-id="d2717-129">For instance, you could set an array of twenty matrices with 20 calls to [**ID3DXBaseEffect::SetMatrix**](id3dxbaseeffect--setmatrix.md) or by using a single SetRawValue.</span></span>

<span data-ttu-id="d2717-130">Todos os valores devem ser matrix4x4s ou float4s e todas as matrizes devem estar na ordem de coluna principal.</span><span class="sxs-lookup"><span data-stu-id="d2717-130">All values are expected to be either matrix4x4s or float4s and all matrices are expected to be in column-major order.</span></span> <span data-ttu-id="d2717-131">Valores int ou float são convertidos em um FLOAT4; Portanto, é altamente recomendável que você use SetRawValue com apenas dados FLOAT4 ou matrix4x4.</span><span class="sxs-lookup"><span data-stu-id="d2717-131">Int or float values are cast into a float4; therefore, it is highly recommended that you use SetRawValue with only float4 or matrix4x4 data.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2717-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2717-132">Requirements</span></span>



| <span data-ttu-id="d2717-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2717-133">Requirement</span></span> | <span data-ttu-id="d2717-134">Valor</span><span class="sxs-lookup"><span data-stu-id="d2717-134">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2717-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d2717-135">Header</span></span><br/>  | <dl> <span data-ttu-id="d2717-136"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2717-136"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="d2717-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d2717-137">Library</span></span><br/> | <dl> <span data-ttu-id="d2717-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d2717-138"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="d2717-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="d2717-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2717-140">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="d2717-140">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 
