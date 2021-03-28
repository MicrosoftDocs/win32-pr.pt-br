---
title: Função D3DX11CreateShaderResourceViewFromResource (D3DX11tex. h)
description: Observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Observação em vez de usar essa função, recomendamos que você use funções de recurso, então essa biblioteca DirectXTK (tempo de execução), CreateXXXTextureFromMemory (em que XXX é DDS ou WIC) DirectXTex library (Tools), LoadFromXXXMemory (em que XXX é WIC, DDS ou TGA; O WIC não oferece suporte a DDS e TGA; D3DX 9 o TGA com suporte como um formato de origem de arte comum para jogos), então, CreateShaderResourceView criar uma exibição de recurso de sombreador de um recurso.
ms.assetid: 64620e6d-fc0d-4411-8744-d9d8ffe6ccb8
keywords:
- Função D3DX11CreateShaderResourceViewFromResource Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateShaderResourceViewFromResource
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb374bd569cb58451461a7fe269c58c200895b7a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989339"
---
# <a name="d3dx11createshaderresourceviewfromresource-function"></a><span data-ttu-id="c6a3e-105">Função D3DX11CreateShaderResourceViewFromResource</span><span class="sxs-lookup"><span data-stu-id="c6a3e-105">D3DX11CreateShaderResourceViewFromResource function</span></span>

> [!Note]  
> <span data-ttu-id="c6a3e-106">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="c6a3e-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="c6a3e-107">Em vez de usar essa função, recomendamos que você use [funções de recurso](/windows/desktop/menurc/resources-functions)e, em seguida, estas:</span><span class="sxs-lookup"><span data-stu-id="c6a3e-107">Instead of using this function, we recommend that you use [resource functions](/windows/desktop/menurc/resources-functions), then these:</span></span>
>
> -   <span data-ttu-id="c6a3e-108">[DirectXTK](https://github.com/Microsoft/DirectXTK) library (Runtime), **CreateXXXTextureFromMemory** (em que xxx é DDS ou WIC)</span><span class="sxs-lookup"><span data-stu-id="c6a3e-108">[DirectXTK](https://github.com/Microsoft/DirectXTK) library (runtime), **CreateXXXTextureFromMemory** (where XXX is DDS or WIC)</span></span>
> -   <span data-ttu-id="c6a3e-109">Biblioteca [DirectXTex](https://github.com/Microsoft/DirectXTex) (ferramentas), **LoadFromXXXMemory** (em que xxx é WIC, DDS ou TGA; O WIC não oferece suporte a DDS e TGA; O D3DX 9 TGA com suporte como um formato de origem de arte comum para jogos) e, em seguida, **CreateShaderResourceView**</span><span class="sxs-lookup"><span data-stu-id="c6a3e-109">[DirectXTex](https://github.com/Microsoft/DirectXTex) library (tools), **LoadFromXXXMemory** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games) then **CreateShaderResourceView**</span></span>

 

<span data-ttu-id="c6a3e-110">Criar um sombreador – modo de exibição de recursos de um recurso.</span><span class="sxs-lookup"><span data-stu-id="c6a3e-110">Create a shader-resource view from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6a3e-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c6a3e-111">Syntax</span></span>


```C++
HRESULT D3DX11CreateShaderResourceViewFromResource(
  _In_  ID3D11Device             *pDevice,
  _In_  HMODULE                  hSrcModule,
  _In_  LPCTSTR                  pSrcResource,
  _In_  D3DX11_IMAGE_LOAD_INFO   *pLoadInfo,
  _In_  ID3DX11ThreadPump        *pPump,
  _Out_ ID3D11ShaderResourceView **ppShaderResourceView,
  _Out_ HRESULT                  *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="c6a3e-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c6a3e-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6a3e-113">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c6a3e-113">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6a3e-114">Tipo: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span><span class="sxs-lookup"><span data-stu-id="c6a3e-114">Type: **[**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span></span>

<span data-ttu-id="c6a3e-115">Um ponteiro para o dispositivo (consulte [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) que usará o recurso.</span><span class="sxs-lookup"><span data-stu-id="c6a3e-115">A pointer to the device (see [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="c6a3e-116">*hSrcModule* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c6a3e-116">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6a3e-117">Tipo: **[ **HMODULE**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c6a3e-117">Type: **[**HMODULE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c6a3e-118">Identificador para o módulo de recurso que contém a exibição do sombreador-recurso.</span><span class="sxs-lookup"><span data-stu-id="c6a3e-118">Handle to the resource module containing the shader-resource view.</span></span> <span data-ttu-id="c6a3e-119">HMODULE pode ser obtido com a [função GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span><span class="sxs-lookup"><span data-stu-id="c6a3e-119">HMODULE can be obtained with [GetModuleHandle Function](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="c6a3e-120">*pSrcResource* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c6a3e-120">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6a3e-121">Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c6a3e-121">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c6a3e-122">Nome da exibição de recurso do sombreador em hSrcModule.</span><span class="sxs-lookup"><span data-stu-id="c6a3e-122">Name of the shader resource view in hSrcModule.</span></span> <span data-ttu-id="c6a3e-123">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="c6a3e-123">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="c6a3e-124">Caso contrário, o tipo de dados será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="c6a3e-124">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="c6a3e-125">*pLoadInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c6a3e-125">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6a3e-126">Tipo: **[ **\_ informações de \_ carregamento \_ de imagem D3DX11**](d3dx11-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="c6a3e-126">Type: **[**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)\***</span></span>

<span data-ttu-id="c6a3e-127">Opcional.</span><span class="sxs-lookup"><span data-stu-id="c6a3e-127">Optional.</span></span> <span data-ttu-id="c6a3e-128">Identifica as características de uma textura (consulte [**\_ informações de \_ carregamento \_ de imagem D3DX11**](d3dx11-image-load-info.md)) quando o processador de dados é criado; defina isso como **nulo** para ler as características de uma textura quando a textura for carregada.</span><span class="sxs-lookup"><span data-stu-id="c6a3e-128">Identifies the characteristics of a texture (see [**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="c6a3e-129">*pPump* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c6a3e-129">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6a3e-130">Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="c6a3e-130">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="c6a3e-131">Um ponteiro para uma interface de bombeamento de thread (consulte a [**interface ID3DX11ThreadPump**](id3dx11threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="c6a3e-131">A pointer to a thread pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="c6a3e-132">Se **NULL** for especificado, essa função se comportará de forma síncrona e não retornará até que seja concluída.</span><span class="sxs-lookup"><span data-stu-id="c6a3e-132">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="c6a3e-133">*ppShaderResourceView* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c6a3e-133">*ppShaderResourceView* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c6a3e-134">Tipo: **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***</span><span class="sxs-lookup"><span data-stu-id="c6a3e-134">Type: **[**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***</span></span>

<span data-ttu-id="c6a3e-135">Endereço de um ponteiro para a exibição de recurso do sombreador (consulte [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)).</span><span class="sxs-lookup"><span data-stu-id="c6a3e-135">Address of a pointer to the shader-resource view (see [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)).</span></span>

</dd> <dt>

<span data-ttu-id="c6a3e-136">*pHResult* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c6a3e-136">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c6a3e-137">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="c6a3e-137">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="c6a3e-138">Um ponteiro para o valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="c6a3e-138">A pointer to the return value.</span></span> <span data-ttu-id="c6a3e-139">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="c6a3e-139">May be **NULL**.</span></span> <span data-ttu-id="c6a3e-140">Se *pPump* não for **NULL**, *pHResult* deverá ser um local de memória válido até que a execução assíncrona seja concluída.</span><span class="sxs-lookup"><span data-stu-id="c6a3e-140">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6a3e-141">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c6a3e-141">Return value</span></span>

<span data-ttu-id="c6a3e-142">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c6a3e-142">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c6a3e-143">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="c6a3e-143">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c6a3e-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6a3e-144">Requirements</span></span>



| <span data-ttu-id="c6a3e-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6a3e-145">Requirement</span></span> | <span data-ttu-id="c6a3e-146">Valor</span><span class="sxs-lookup"><span data-stu-id="c6a3e-146">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c6a3e-147">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c6a3e-147">Header</span></span><br/>  | <dl> <span data-ttu-id="c6a3e-148"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6a3e-148"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="c6a3e-149">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c6a3e-149">Library</span></span><br/> | <dl> <span data-ttu-id="c6a3e-150"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c6a3e-150"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="c6a3e-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="c6a3e-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6a3e-152">Funções D3DX</span><span class="sxs-lookup"><span data-stu-id="c6a3e-152">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

