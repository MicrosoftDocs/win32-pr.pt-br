---
description: Obter os nomes de amostra referenciados em um sombreador.
ms.assetid: fe769917-daac-43b8-bf63-fb337915ff53
title: Função D3DXGetShaderSamplers (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderSamplers
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2135ba36f238188c6e7817001ba89bb47e3b9998
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105793849"
---
# <a name="d3dxgetshadersamplers-function"></a><span data-ttu-id="16066-103">Função D3DXGetShaderSamplers</span><span class="sxs-lookup"><span data-stu-id="16066-103">D3DXGetShaderSamplers function</span></span>

<span data-ttu-id="16066-104">Obter os nomes de amostra referenciados em um sombreador.</span><span class="sxs-lookup"><span data-stu-id="16066-104">Get the sampler names referenced in a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="16066-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="16066-105">Syntax</span></span>


```C++
HRESULT D3DXGetShaderSamplers(
  _In_    const DWORD  *pFunction,
  _Inout_       LPCSTR *pSamplers,
  _Out_         UINT   *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="16066-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="16066-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16066-107">*pFunction* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="16066-107">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16066-108">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="16066-108">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="16066-109">Ponteiro para o fluxo DWORD da função de sombreador.</span><span class="sxs-lookup"><span data-stu-id="16066-109">Pointer to the shader function DWORD stream.</span></span>

</dd> <dt>

<span data-ttu-id="16066-110">*pSamplers* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="16066-110">*pSamplers* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="16066-111">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="16066-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="16066-112">Ponteiro para uma matriz de LPCSTRs.</span><span class="sxs-lookup"><span data-stu-id="16066-112">Pointer to an array of LPCSTRs.</span></span> <span data-ttu-id="16066-113">A função preencherá essa matriz com ponteiros para os nomes de amostra contidos em *pFunction*.</span><span class="sxs-lookup"><span data-stu-id="16066-113">The function will fill this array with pointers to the sampler names contained within *pFunction*.</span></span> <span data-ttu-id="16066-114">O tamanho máximo da matriz é o número máximo de registros de amostra (16 para vs \_ 3 \_ 0 e PS \_ 3 \_ 0).</span><span class="sxs-lookup"><span data-stu-id="16066-114">The maximum array size is the maximum number of sampler registers (16 for vs\_3\_0 and ps\_3\_0).</span></span>

<span data-ttu-id="16066-115">Para localizar o número de amostras usadas, verifique *pCount* depois de chamar **D3DXGetShaderSamplers** com pSamplers = **NULL**.</span><span class="sxs-lookup"><span data-stu-id="16066-115">To find the number of samplers used, check *pCount* after calling **D3DXGetShaderSamplers** with pSamplers = **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="16066-116">*pCount* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="16066-116">*pCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="16066-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="16066-117">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="16066-118">Retorna o número de amostras referenciadas pelo sombreador.</span><span class="sxs-lookup"><span data-stu-id="16066-118">Returns the number of samplers referenced by the shader.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16066-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="16066-119">Return value</span></span>

<span data-ttu-id="16066-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="16066-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="16066-121">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="16066-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="16066-122">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="16066-122">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="16066-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16066-123">Requirements</span></span>



| <span data-ttu-id="16066-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="16066-124">Requirement</span></span> | <span data-ttu-id="16066-125">Valor</span><span class="sxs-lookup"><span data-stu-id="16066-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="16066-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="16066-126">Header</span></span><br/>  | <dl> <span data-ttu-id="16066-127"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="16066-127"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="16066-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="16066-128">Library</span></span><br/> | <dl> <span data-ttu-id="16066-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="16066-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="16066-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="16066-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16066-131">Funções de sombreador</span><span class="sxs-lookup"><span data-stu-id="16066-131">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
