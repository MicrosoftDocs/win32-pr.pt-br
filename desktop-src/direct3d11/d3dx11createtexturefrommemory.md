---
title: Função D3DX11CreateTextureFromMemory (D3DX11. h)
description: Observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Observação em vez de usar essa função, recomendamos que você use essas DirectXTK library (Runtime), CreateXXXTextureFromMemory (em que XXX é DDS ou WIC) DirectXTex library (Tools), LoadFromXXXMemory (em que XXX é WIC, DDS ou TGA; O WIC não oferece suporte a DDS e TGA; O D3DX 9 TGA com suporte como um formato de origem de arte comum para jogos). em seguida, CreateTexture cria um recurso de textura a partir de um arquivo que reside na memória do sistema.
ms.assetid: 1b07653e-8dc8-40b2-b591-bd25a54cfaa2
keywords:
- Função D3DX11CreateTextureFromMemory Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateTextureFromMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99987e882430da7f5e884f1b22e890947f7105e3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930674"
---
# <a name="d3dx11createtexturefrommemory-function"></a><span data-ttu-id="e9222-105">Função D3DX11CreateTextureFromMemory</span><span class="sxs-lookup"><span data-stu-id="e9222-105">D3DX11CreateTextureFromMemory function</span></span>

> [!Note]  
> <span data-ttu-id="e9222-106">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="e9222-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="e9222-107">Em vez de usar essa função, recomendamos que você as use:</span><span class="sxs-lookup"><span data-stu-id="e9222-107">Instead of using this function, we recommend that you use these:</span></span>
>
> -   <span data-ttu-id="e9222-108">[DirectXTK](https://github.com/Microsoft/DirectXTK) library (Runtime), **CreateXXXTextureFromMemory** (em que xxx é DDS ou WIC)</span><span class="sxs-lookup"><span data-stu-id="e9222-108">[DirectXTK](https://github.com/Microsoft/DirectXTK) library (runtime), **CreateXXXTextureFromMemory** (where XXX is DDS or WIC)</span></span>
> -   <span data-ttu-id="e9222-109">Biblioteca [DirectXTex](https://github.com/Microsoft/DirectXTex) (ferramentas), **LoadFromXXXMemory** (em que xxx é WIC, DDS ou TGA; O WIC não oferece suporte a DDS e TGA; O D3DX 9 TGA com suporte como um formato de origem de arte comum para jogos) e **CreateTexture**</span><span class="sxs-lookup"><span data-stu-id="e9222-109">[DirectXTex](https://github.com/Microsoft/DirectXTex) library (tools), **LoadFromXXXMemory** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games) then **CreateTexture**</span></span>

 

<span data-ttu-id="e9222-110">Crie um recurso de textura a partir de um arquivo que reside na memória do sistema.</span><span class="sxs-lookup"><span data-stu-id="e9222-110">Create a texture resource from a file residing in system memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9222-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e9222-111">Syntax</span></span>


```C++
HRESULT D3DX11CreateTextureFromMemory(
  _In_  ID3D11Device           *pDevice,
  _In_  LPCVOID                pSrcData,
  _In_  SIZE_T                 SrcDataSize,
  _In_  D3DX11_IMAGE_LOAD_INFO *pLoadInfo,
  _In_  ID3DX11ThreadPump      *pPump,
  _Out_ ID3D11Resource         **ppTexture,
  _Out_ HRESULT                *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="e9222-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e9222-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9222-113">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e9222-113">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9222-114">Tipo: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span><span class="sxs-lookup"><span data-stu-id="e9222-114">Type: **[**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span></span>

<span data-ttu-id="e9222-115">Um ponteiro para o dispositivo (consulte [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) que usará o recurso.</span><span class="sxs-lookup"><span data-stu-id="e9222-115">A pointer to the device (see [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="e9222-116">*pSrcData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e9222-116">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9222-117">Tipo: **[ **LPCVOID**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e9222-117">Type: **[**LPCVOID**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e9222-118">Ponteiro para o recurso na memória do sistema.</span><span class="sxs-lookup"><span data-stu-id="e9222-118">Pointer to the resource in system memory.</span></span>

</dd> <dt>

<span data-ttu-id="e9222-119">*SrcDataSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e9222-119">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9222-120">Tipo: **[ **tamanho \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e9222-120">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e9222-121">Tamanho do recurso na memória do sistema.</span><span class="sxs-lookup"><span data-stu-id="e9222-121">Size of the resource in system memory.</span></span>

</dd> <dt>

<span data-ttu-id="e9222-122">*pLoadInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e9222-122">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9222-123">Tipo: **[ **\_ informações de \_ carregamento \_ de imagem D3DX11**](d3dx11-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="e9222-123">Type: **[**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)\***</span></span>

<span data-ttu-id="e9222-124">Opcional.</span><span class="sxs-lookup"><span data-stu-id="e9222-124">Optional.</span></span> <span data-ttu-id="e9222-125">Identifica as características de uma textura (consulte [**\_ informações de \_ carregamento \_ de imagem D3DX11**](d3dx11-image-load-info.md)) quando o processador de dados é criado; defina isso como **nulo** para ler as características de uma textura quando a textura for carregada.</span><span class="sxs-lookup"><span data-stu-id="e9222-125">Identifies the characteristics of a texture (see [**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="e9222-126">*pPump* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e9222-126">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9222-127">Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="e9222-127">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="e9222-128">Um ponteiro para uma interface de bombeamento de thread (consulte a [**interface ID3DX11ThreadPump**](id3dx11threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="e9222-128">A pointer to a thread pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="e9222-129">Se **NULL** for especificado, essa função se comportará de forma síncrona e não retornará até que seja concluída.</span><span class="sxs-lookup"><span data-stu-id="e9222-129">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="e9222-130">*ppTexture* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e9222-130">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e9222-131">Tipo: **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\*\***</span><span class="sxs-lookup"><span data-stu-id="e9222-131">Type: **[**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\*\***</span></span>

<span data-ttu-id="e9222-132">Endereço de um ponteiro para o recurso criado.</span><span class="sxs-lookup"><span data-stu-id="e9222-132">Address of a pointer to the created resource.</span></span> <span data-ttu-id="e9222-133">Consulte [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span><span class="sxs-lookup"><span data-stu-id="e9222-133">See [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span></span>

</dd> <dt>

<span data-ttu-id="e9222-134">*pHResult* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e9222-134">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e9222-135">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="e9222-135">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="e9222-136">Um ponteiro para o valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="e9222-136">A pointer to the return value.</span></span> <span data-ttu-id="e9222-137">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="e9222-137">May be **NULL**.</span></span> <span data-ttu-id="e9222-138">Se *pPump* não for **NULL**, *pHResult* deverá ser um local de memória válido até que a execução assíncrona seja concluída.</span><span class="sxs-lookup"><span data-stu-id="e9222-138">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9222-139">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e9222-139">Return value</span></span>

<span data-ttu-id="e9222-140">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e9222-140">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e9222-141">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="e9222-141">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e9222-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9222-142">Requirements</span></span>



| <span data-ttu-id="e9222-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9222-143">Requirement</span></span> | <span data-ttu-id="e9222-144">Valor</span><span class="sxs-lookup"><span data-stu-id="e9222-144">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e9222-145">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e9222-145">Header</span></span><br/>  | <dl> <span data-ttu-id="e9222-146"><dt>D3DX11. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9222-146"><dt>D3DX11.h</dt></span></span> </dl>   |
| <span data-ttu-id="e9222-147">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e9222-147">Library</span></span><br/> | <dl> <span data-ttu-id="e9222-148"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e9222-148"><dt>D3DX11.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9222-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="e9222-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9222-150">Funções D3DX</span><span class="sxs-lookup"><span data-stu-id="e9222-150">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

