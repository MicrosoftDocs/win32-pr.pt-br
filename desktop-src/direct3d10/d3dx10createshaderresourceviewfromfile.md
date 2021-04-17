---
description: Criar um sombreador – modo de exibição de recursos de um arquivo.
ms.assetid: 97aa848b-e24c-4ebd-8819-b9741ea12b60
title: Função D3DX10CreateShaderResourceViewFromFile (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateShaderResourceViewFromFile
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: eb787bed64d16f7593fba1f97c96ceeaa217b4e0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104370971"
---
# <a name="d3dx10createshaderresourceviewfromfile-function"></a><span data-ttu-id="4493e-103">Função D3DX10CreateShaderResourceViewFromFile</span><span class="sxs-lookup"><span data-stu-id="4493e-103">D3DX10CreateShaderResourceViewFromFile function</span></span>

<span data-ttu-id="4493e-104">Criar um sombreador – modo de exibição de recursos de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="4493e-104">Create a shader-resource view from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="4493e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4493e-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateShaderResourceViewFromFile(
  _In_  ID3D10Device             *pDevice,
  _In_  LPCTSTR                  pSrcFile,
  _In_  D3DX10_IMAGE_LOAD_INFO   *pLoadInfo,
  _In_  ID3DX10ThreadPump        *pPump,
  _Out_ ID3D10ShaderResourceView **ppShaderResourceView,
  _Out_ HRESULT                  *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="4493e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4493e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4493e-107">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4493e-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4493e-108">Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="4493e-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="4493e-109">Um ponteiro para o dispositivo (consulte a [**interface ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) que usará o recurso.</span><span class="sxs-lookup"><span data-stu-id="4493e-109">A pointer to the device (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="4493e-110">*pSrcFile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4493e-110">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4493e-111">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4493e-111">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4493e-112">Nome do arquivo que contém o sombreador-modo de exibição de recursos.</span><span class="sxs-lookup"><span data-stu-id="4493e-112">Name of the file that contains the shader-resource view.</span></span> <span data-ttu-id="4493e-113">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="4493e-113">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="4493e-114">Caso contrário, o tipo de dados será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="4493e-114">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="4493e-115">*pLoadInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4493e-115">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4493e-116">Tipo: **[ **\_ informações de \_ carregamento \_ de imagem D3DX10**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="4493e-116">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="4493e-117">Opcional.</span><span class="sxs-lookup"><span data-stu-id="4493e-117">Optional.</span></span> <span data-ttu-id="4493e-118">Identifica as características de uma textura (consulte [**\_ informações de \_ carregamento \_ de imagem D3DX10**](d3dx10-image-load-info.md)) quando o processador de dados é criado; defina isso como **nulo** para ler as características de uma textura quando a textura for carregada.</span><span class="sxs-lookup"><span data-stu-id="4493e-118">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="4493e-119">*pPump* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4493e-119">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4493e-120">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="4493e-120">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="4493e-121">Ponteiro para uma interface de bombeamento de thread (consulte a [**interface ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="4493e-121">Pointer to a thread-pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="4493e-122">Se **NULL** for especificado, essa função se comportará de forma síncrona e não retornará até que seja concluída.</span><span class="sxs-lookup"><span data-stu-id="4493e-122">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="4493e-123">*ppShaderResourceView* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="4493e-123">*ppShaderResourceView* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4493e-124">Tipo: **[ **ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***</span><span class="sxs-lookup"><span data-stu-id="4493e-124">Type: **[**ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***</span></span>

<span data-ttu-id="4493e-125">Endereço de um ponteiro para a exibição de recurso do sombreador (consulte a [**interface ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)).</span><span class="sxs-lookup"><span data-stu-id="4493e-125">Address of a pointer to the shader-resource view (see [**ID3D10ShaderResourceView Interface**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)).</span></span>

</dd> <dt>

<span data-ttu-id="4493e-126">*pHResult* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="4493e-126">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4493e-127">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="4493e-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="4493e-128">Um ponteiro para o valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="4493e-128">A pointer to the return value.</span></span> <span data-ttu-id="4493e-129">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="4493e-129">May be **NULL**.</span></span> <span data-ttu-id="4493e-130">Se *pPump* não for **NULL**, *pHResult* deverá ser um local de memória válido até que a execução assíncrona seja concluída.</span><span class="sxs-lookup"><span data-stu-id="4493e-130">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4493e-131">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4493e-131">Return value</span></span>

<span data-ttu-id="4493e-132">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4493e-132">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4493e-133">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="4493e-133">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4493e-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="4493e-134">Remarks</span></span>

<span data-ttu-id="4493e-135">Para obter uma lista de formatos de imagem com suporte, consulte [**\_ formato de \_ arquivo \_ de imagem D3DX10**](d3dx10-image-file-format.md).</span><span class="sxs-lookup"><span data-stu-id="4493e-135">For a list of supported image formats, see [**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4493e-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4493e-136">Requirements</span></span>



| <span data-ttu-id="4493e-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="4493e-137">Requirement</span></span> | <span data-ttu-id="4493e-138">Valor</span><span class="sxs-lookup"><span data-stu-id="4493e-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4493e-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4493e-139">Header</span></span><br/>  | <dl> <span data-ttu-id="4493e-140"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="4493e-140"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="4493e-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4493e-141">Library</span></span><br/> | <dl> <span data-ttu-id="4493e-142"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4493e-142"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="4493e-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="4493e-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4493e-144">Funções de textura no D3DX 10</span><span class="sxs-lookup"><span data-stu-id="4493e-144">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[<span data-ttu-id="4493e-145">Funções de Uso Geral</span><span class="sxs-lookup"><span data-stu-id="4493e-145">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
