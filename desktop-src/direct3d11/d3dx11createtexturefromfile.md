---
title: Função D3DX11CreateTextureFromFile (D3DX11. h)
description: Observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Observação em vez de usar essa função, recomendamos que você use essas DirectXTK library (Runtime), CreateXXXTextureFromFile (em que XXX é DDS ou WIC) DirectXTex library (Tools), LoadFromXXXFile (em que XXX é WIC, DDS ou TGA; O WIC não oferece suporte a DDS e TGA; O D3DX 9 TGA com suporte como um formato de origem de arte comum para jogos) e CreateTexture cria um recurso de textura a partir de um arquivo.
ms.assetid: a84ea166-2296-48d9-a028-b65fd68f2371
keywords:
- Função D3DX11CreateTextureFromFile Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateTextureFromFile
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6ab9bedcfe44238938e47ccb402738d2694b061
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989338"
---
# <a name="d3dx11createtexturefromfile-function"></a><span data-ttu-id="a7ec9-105">Função D3DX11CreateTextureFromFile</span><span class="sxs-lookup"><span data-stu-id="a7ec9-105">D3DX11CreateTextureFromFile function</span></span>

> [!Note]  
> <span data-ttu-id="a7ec9-106">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="a7ec9-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="a7ec9-107">Em vez de usar essa função, recomendamos que você as use:</span><span class="sxs-lookup"><span data-stu-id="a7ec9-107">Instead of using this function, we recommend that you use these:</span></span>
>
> -   <span data-ttu-id="a7ec9-108">[DirectXTK](https://github.com/Microsoft/DirectXTK) library (Runtime), **CreateXXXTextureFromFile** (em que xxx é DDS ou WIC)</span><span class="sxs-lookup"><span data-stu-id="a7ec9-108">[DirectXTK](https://github.com/Microsoft/DirectXTK) library (runtime), **CreateXXXTextureFromFile** (where XXX is DDS or WIC)</span></span>
> -   <span data-ttu-id="a7ec9-109">Biblioteca [DirectXTex](https://github.com/Microsoft/DirectXTex) (ferramentas), **LoadFromXXXFile** (em que xxx é WIC, DDS ou TGA; O WIC não oferece suporte a DDS e TGA; O D3DX 9 TGA com suporte como um formato de origem de arte comum para jogos) e **CreateTexture**</span><span class="sxs-lookup"><span data-stu-id="a7ec9-109">[DirectXTex](https://github.com/Microsoft/DirectXTex) library (tools), **LoadFromXXXFile** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games) then **CreateTexture**</span></span>

 

<span data-ttu-id="a7ec9-110">Crie um recurso de textura a partir de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="a7ec9-110">Create a texture resource from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7ec9-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a7ec9-111">Syntax</span></span>


```C++
HRESULT D3DX11CreateTextureFromFile(
  _In_  ID3D11Device           *pDevice,
  _In_  LPCTSTR                pSrcFile,
  _In_  D3DX11_IMAGE_LOAD_INFO *pLoadInfo,
  _In_  ID3DX11ThreadPump      *pPump,
  _Out_ ID3D11Resource         **ppTexture,
  _Out_ HRESULT                *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="a7ec9-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a7ec9-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7ec9-113">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a7ec9-113">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7ec9-114">Tipo: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span><span class="sxs-lookup"><span data-stu-id="a7ec9-114">Type: **[**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span></span>

<span data-ttu-id="a7ec9-115">Um ponteiro para o dispositivo (consulte [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) que usará o recurso.</span><span class="sxs-lookup"><span data-stu-id="a7ec9-115">A pointer to the device (see [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="a7ec9-116">*pSrcFile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a7ec9-116">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7ec9-117">Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a7ec9-117">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a7ec9-118">O nome do arquivo que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="a7ec9-118">The name of the file containing the resource.</span></span> <span data-ttu-id="a7ec9-119">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="a7ec9-119">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="a7ec9-120">Caso contrário, o tipo de dados será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="a7ec9-120">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="a7ec9-121">*pLoadInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a7ec9-121">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7ec9-122">Tipo: **[ **\_ informações de \_ carregamento \_ de imagem D3DX11**](d3dx11-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="a7ec9-122">Type: **[**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)\***</span></span>

<span data-ttu-id="a7ec9-123">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a7ec9-123">Optional.</span></span> <span data-ttu-id="a7ec9-124">Identifica as características de uma textura (consulte [**\_ informações de \_ carregamento \_ de imagem D3DX11**](d3dx11-image-load-info.md)) quando o processador de dados é criado; defina isso como **nulo** para ler as características de uma textura quando a textura for carregada.</span><span class="sxs-lookup"><span data-stu-id="a7ec9-124">Identifies the characteristics of a texture (see [**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="a7ec9-125">*pPump* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a7ec9-125">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7ec9-126">Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="a7ec9-126">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="a7ec9-127">Um ponteiro para uma interface de bombeamento de thread (consulte a [**interface ID3DX11ThreadPump**](id3dx11threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="a7ec9-127">A pointer to a thread pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="a7ec9-128">Se **NULL** for especificado, essa função se comportará de forma síncrona e não retornará até que seja concluída.</span><span class="sxs-lookup"><span data-stu-id="a7ec9-128">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="a7ec9-129">*ppTexture* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a7ec9-129">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a7ec9-130">Tipo: **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\*\***</span><span class="sxs-lookup"><span data-stu-id="a7ec9-130">Type: **[**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\*\***</span></span>

<span data-ttu-id="a7ec9-131">O endereço de um ponteiro para o recurso de textura (consulte [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)).</span><span class="sxs-lookup"><span data-stu-id="a7ec9-131">The address of a pointer to the texture resource (see [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)).</span></span>

</dd> <dt>

<span data-ttu-id="a7ec9-132">*pHResult* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a7ec9-132">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a7ec9-133">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="a7ec9-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="a7ec9-134">Um ponteiro para o valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="a7ec9-134">A pointer to the return value.</span></span> <span data-ttu-id="a7ec9-135">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="a7ec9-135">May be **NULL**.</span></span> <span data-ttu-id="a7ec9-136">Se *pPump* não for **NULL**, *pHResult* deverá ser um local de memória válido até que a execução assíncrona seja concluída.</span><span class="sxs-lookup"><span data-stu-id="a7ec9-136">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7ec9-137">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a7ec9-137">Return value</span></span>

<span data-ttu-id="a7ec9-138">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a7ec9-138">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a7ec9-139">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="a7ec9-139">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a7ec9-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7ec9-140">Requirements</span></span>



| <span data-ttu-id="a7ec9-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7ec9-141">Requirement</span></span> | <span data-ttu-id="a7ec9-142">Valor</span><span class="sxs-lookup"><span data-stu-id="a7ec9-142">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a7ec9-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a7ec9-143">Header</span></span><br/>  | <dl> <span data-ttu-id="a7ec9-144"><dt>D3DX11. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7ec9-144"><dt>D3DX11.h</dt></span></span> </dl>   |
| <span data-ttu-id="a7ec9-145">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a7ec9-145">Library</span></span><br/> | <dl> <span data-ttu-id="a7ec9-146"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a7ec9-146"><dt>D3DX11.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7ec9-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="a7ec9-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7ec9-148">Funções D3DX</span><span class="sxs-lookup"><span data-stu-id="a7ec9-148">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

