---
description: Criar um sombreador – modo de exibição de recursos de um arquivo na memória.
ms.assetid: 8316987f-75b4-4cee-a1f2-10bee77a28e6
title: Função D3DX10CreateShaderResourceViewFromMemory (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateShaderResourceViewFromMemory
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: ca3cf26d54d37ab3e3a2141ba7c3e4ea9fdd533f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103663980"
---
# <a name="d3dx10createshaderresourceviewfrommemory-function"></a><span data-ttu-id="9b73b-103">Função D3DX10CreateShaderResourceViewFromMemory</span><span class="sxs-lookup"><span data-stu-id="9b73b-103">D3DX10CreateShaderResourceViewFromMemory function</span></span>

<span data-ttu-id="9b73b-104">Criar um sombreador – modo de exibição de recursos de um arquivo na memória.</span><span class="sxs-lookup"><span data-stu-id="9b73b-104">Create a shader-resource view from a file in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b73b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9b73b-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateShaderResourceViewFromMemory(
  _In_  ID3D10Device             *pDevice,
  _In_  LPCVOID                  pSrcData,
  _In_  SIZE_T                   SrcDataSize,
  _In_  D3DX10_IMAGE_LOAD_INFO   *pLoadInfo,
  _In_  ID3DX10ThreadPump        *pPump,
  _Out_ ID3D10ShaderResourceView **ppShaderResourceView,
  _Out_ HRESULT                  *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="9b73b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9b73b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b73b-107">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9b73b-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b73b-108">Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="9b73b-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="9b73b-109">Um ponteiro para o dispositivo (consulte a [**interface ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) que usará o recurso.</span><span class="sxs-lookup"><span data-stu-id="9b73b-109">A pointer to the device (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="9b73b-110">*pSrcData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9b73b-110">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b73b-111">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9b73b-111">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9b73b-112">Ponteiro para o arquivo na memória que contém a exibição do sombreador-recurso.</span><span class="sxs-lookup"><span data-stu-id="9b73b-112">Pointer to the file in memory that contains the shader-resource view.</span></span>

</dd> <dt>

<span data-ttu-id="9b73b-113">*SrcDataSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9b73b-113">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b73b-114">Tipo: **[ **tamanho \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9b73b-114">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9b73b-115">Tamanho do arquivo na memória.</span><span class="sxs-lookup"><span data-stu-id="9b73b-115">Size of the file in memory.</span></span>

</dd> <dt>

<span data-ttu-id="9b73b-116">*pLoadInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9b73b-116">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b73b-117">Tipo: **[ **\_ informações de \_ carregamento \_ de imagem D3DX10**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="9b73b-117">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="9b73b-118">Opcional.</span><span class="sxs-lookup"><span data-stu-id="9b73b-118">Optional.</span></span> <span data-ttu-id="9b73b-119">Identifica as características de uma textura (consulte [**\_ informações de \_ carregamento \_ de imagem D3DX10**](d3dx10-image-load-info.md)) quando o processador de dados é criado; defina isso como **nulo** para ler as características de uma textura quando a textura for carregada.</span><span class="sxs-lookup"><span data-stu-id="9b73b-119">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="9b73b-120">*pPump* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9b73b-120">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b73b-121">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="9b73b-121">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="9b73b-122">Um ponteiro para uma interface de bombeamento de thread (consulte a [**interface ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="9b73b-122">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="9b73b-123">Se **NULL** for especificado, essa função se comportará de forma síncrona e não retornará até que seja concluída.</span><span class="sxs-lookup"><span data-stu-id="9b73b-123">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="9b73b-124">*ppShaderResourceView* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="9b73b-124">*ppShaderResourceView* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9b73b-125">Tipo: **[ **ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***</span><span class="sxs-lookup"><span data-stu-id="9b73b-125">Type: **[**ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***</span></span>

<span data-ttu-id="9b73b-126">Endereço de um ponteiro para o modo de exibição de recursos do sombreador recém-criado.</span><span class="sxs-lookup"><span data-stu-id="9b73b-126">Address of a pointer to the newly created shader resource view.</span></span> <span data-ttu-id="9b73b-127">Consulte a [**interface ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview).</span><span class="sxs-lookup"><span data-stu-id="9b73b-127">See [**ID3D10ShaderResourceView Interface**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview).</span></span>

</dd> <dt>

<span data-ttu-id="9b73b-128">*pHResult* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="9b73b-128">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9b73b-129">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="9b73b-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="9b73b-130">Um ponteiro para o valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="9b73b-130">A pointer to the return value.</span></span> <span data-ttu-id="9b73b-131">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="9b73b-131">May be **NULL**.</span></span> <span data-ttu-id="9b73b-132">Se *pPump* não for **NULL**, *pHResult* deverá ser um local de memória válido até que a execução assíncrona seja concluída.</span><span class="sxs-lookup"><span data-stu-id="9b73b-132">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b73b-133">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9b73b-133">Return value</span></span>

<span data-ttu-id="9b73b-134">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9b73b-134">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9b73b-135">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="9b73b-135">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9b73b-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b73b-136">Requirements</span></span>



| <span data-ttu-id="9b73b-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b73b-137">Requirement</span></span> | <span data-ttu-id="9b73b-138">Valor</span><span class="sxs-lookup"><span data-stu-id="9b73b-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b73b-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9b73b-139">Header</span></span><br/>  | <dl> <span data-ttu-id="9b73b-140"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b73b-140"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="9b73b-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9b73b-141">Library</span></span><br/> | <dl> <span data-ttu-id="9b73b-142"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9b73b-142"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="9b73b-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="9b73b-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b73b-144">Funções de textura no D3DX 10</span><span class="sxs-lookup"><span data-stu-id="9b73b-144">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[<span data-ttu-id="9b73b-145">Funções de Uso Geral</span><span class="sxs-lookup"><span data-stu-id="9b73b-145">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
