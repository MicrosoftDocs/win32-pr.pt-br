---
description: Criar um sombreador – modo de exibição de recursos de um recurso.
ms.assetid: 207cda5f-5b7e-420a-988f-135cd2a04eb0
title: Função D3DX10CreateShaderResourceViewFromResource (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateShaderResourceViewFromResource
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 12de92153b6f812b4f014f53e918e7a97000eda6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105771586"
---
# <a name="d3dx10createshaderresourceviewfromresource-function"></a><span data-ttu-id="ae7a6-103">Função D3DX10CreateShaderResourceViewFromResource</span><span class="sxs-lookup"><span data-stu-id="ae7a6-103">D3DX10CreateShaderResourceViewFromResource function</span></span>

<span data-ttu-id="ae7a6-104">Criar um sombreador – modo de exibição de recursos de um recurso.</span><span class="sxs-lookup"><span data-stu-id="ae7a6-104">Create a shader-resource view from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae7a6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ae7a6-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateShaderResourceViewFromResource(
  _In_  ID3D10Device             *pDevice,
  _In_  HMODULE                  hSrcModule,
  _In_  LPCTSTR                  pSrcResource,
  _In_  D3DX10_IMAGE_LOAD_INFO   *pLoadInfo,
  _In_  ID3DX10ThreadPump        *pPump,
  _Out_ ID3D10ShaderResourceView **ppShaderResourceView,
  _Out_ HRESULT                  *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="ae7a6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ae7a6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae7a6-107">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ae7a6-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae7a6-108">Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="ae7a6-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="ae7a6-109">Um ponteiro para o dispositivo (consulte a [**interface ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) que usará o recurso.</span><span class="sxs-lookup"><span data-stu-id="ae7a6-109">A pointer to the device (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="ae7a6-110">*hSrcModule* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ae7a6-110">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae7a6-111">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ae7a6-111">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ae7a6-112">Identificador para o módulo de recurso que contém a exibição do sombreador-recurso.</span><span class="sxs-lookup"><span data-stu-id="ae7a6-112">Handle to the resource module containing the shader-resource view.</span></span> <span data-ttu-id="ae7a6-113">HMODULE pode ser obtido com a [função GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span><span class="sxs-lookup"><span data-stu-id="ae7a6-113">HMODULE can be obtained with [GetModuleHandle Function](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="ae7a6-114">*pSrcResource* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ae7a6-114">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae7a6-115">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ae7a6-115">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ae7a6-116">Nome da exibição de recurso do sombreador em hSrcModule.</span><span class="sxs-lookup"><span data-stu-id="ae7a6-116">Name of the shader resource view in hSrcModule.</span></span> <span data-ttu-id="ae7a6-117">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="ae7a6-117">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="ae7a6-118">Caso contrário, o tipo de dados será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="ae7a6-118">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="ae7a6-119">*pLoadInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ae7a6-119">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae7a6-120">Tipo: **[ **\_ informações de \_ carregamento \_ de imagem D3DX10**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="ae7a6-120">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="ae7a6-121">Opcional.</span><span class="sxs-lookup"><span data-stu-id="ae7a6-121">Optional.</span></span> <span data-ttu-id="ae7a6-122">Identifica as características de uma textura (consulte [**\_ informações de \_ carregamento \_ de imagem D3DX10**](d3dx10-image-load-info.md)) quando o processador de dados é criado; defina isso como **nulo** para ler as características de uma textura quando a textura for carregada.</span><span class="sxs-lookup"><span data-stu-id="ae7a6-122">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="ae7a6-123">*pPump* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ae7a6-123">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae7a6-124">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="ae7a6-124">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="ae7a6-125">Um ponteiro para uma interface de bombeamento de thread (consulte a [**interface ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="ae7a6-125">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="ae7a6-126">Se **NULL** for especificado, essa função se comportará de forma síncrona e não retornará até que seja concluída.</span><span class="sxs-lookup"><span data-stu-id="ae7a6-126">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="ae7a6-127">*ppShaderResourceView* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ae7a6-127">*ppShaderResourceView* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ae7a6-128">Tipo: **[ **ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***</span><span class="sxs-lookup"><span data-stu-id="ae7a6-128">Type: **[**ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***</span></span>

<span data-ttu-id="ae7a6-129">Endereço de um ponteiro para a exibição de recurso do sombreador (consulte a [**interface ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)).</span><span class="sxs-lookup"><span data-stu-id="ae7a6-129">Address of a pointer to the shader-resource view (see [**ID3D10ShaderResourceView Interface**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)).</span></span>

</dd> <dt>

<span data-ttu-id="ae7a6-130">*pHResult* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ae7a6-130">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ae7a6-131">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="ae7a6-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="ae7a6-132">Um ponteiro para o valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="ae7a6-132">A pointer to the return value.</span></span> <span data-ttu-id="ae7a6-133">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="ae7a6-133">May be **NULL**.</span></span> <span data-ttu-id="ae7a6-134">Se *pPump* não for **NULL**, *pHResult* deverá ser um local de memória válido até que a execução assíncrona seja concluída.</span><span class="sxs-lookup"><span data-stu-id="ae7a6-134">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae7a6-135">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ae7a6-135">Return value</span></span>

<span data-ttu-id="ae7a6-136">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ae7a6-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ae7a6-137">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="ae7a6-137">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ae7a6-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae7a6-138">Requirements</span></span>



| <span data-ttu-id="ae7a6-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae7a6-139">Requirement</span></span> | <span data-ttu-id="ae7a6-140">Valor</span><span class="sxs-lookup"><span data-stu-id="ae7a6-140">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae7a6-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ae7a6-141">Header</span></span><br/>  | <dl> <span data-ttu-id="ae7a6-142"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae7a6-142"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="ae7a6-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ae7a6-143">Library</span></span><br/> | <dl> <span data-ttu-id="ae7a6-144"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ae7a6-144"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="ae7a6-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="ae7a6-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae7a6-146">Funções de textura no D3DX 10</span><span class="sxs-lookup"><span data-stu-id="ae7a6-146">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[<span data-ttu-id="ae7a6-147">Funções de Uso Geral</span><span class="sxs-lookup"><span data-stu-id="ae7a6-147">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
