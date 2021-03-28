---
title: Função D3DX11GetImageInfoFromResource (D3DX11tex. h)
description: Observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Observação em vez de usar essa função, recomendamos que você use funções de recurso e, em seguida, use DirectXTex library (Tools), LoadFromXXXMemory (em que XXX é WIC, DDS ou TGA; O WIC não oferece suporte a DDS e TGA; O D3DX 9 TGA com suporte como um formato de origem de arte comum para jogos). Recupera informações sobre uma determinada imagem em um recurso.
ms.assetid: e4752eb3-38d5-4922-b3c8-5fdcd0cc0610
keywords:
- Função D3DX11GetImageInfoFromResource Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11GetImageInfoFromResource
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 967a7b2c2ff03faefc12a48be18a4756e4ed3962
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968624"
---
# <a name="d3dx11getimageinfofromresource-function"></a><span data-ttu-id="67b4b-106">Função D3DX11GetImageInfoFromResource</span><span class="sxs-lookup"><span data-stu-id="67b4b-106">D3DX11GetImageInfoFromResource function</span></span>

> [!Note]  
> <span data-ttu-id="67b4b-107">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="67b4b-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="67b4b-108">Em vez de usar essa função, recomendamos que você use [funções de recurso](/windows/desktop/menurc/resources-functions)e, em seguida, use [DirectXTex](https://github.com/Microsoft/DirectXTex) library (Tools), **LoadFromXXXMemory** (em que xxx é WIC, DDS ou TGA; O WIC não oferece suporte a DDS e TGA; O D3DX 9 TGA com suporte como um formato de origem de arte comum para jogos).</span><span class="sxs-lookup"><span data-stu-id="67b4b-108">Instead of using this function, we recommend that you use [resource functions](/windows/desktop/menurc/resources-functions), then use [DirectXTex](https://github.com/Microsoft/DirectXTex) library (tools), **LoadFromXXXMemory** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span>

 

<span data-ttu-id="67b4b-109">Recupera informações sobre uma determinada imagem em um recurso.</span><span class="sxs-lookup"><span data-stu-id="67b4b-109">Retrieves information about a given image in a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="67b4b-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="67b4b-110">Syntax</span></span>


```C++
HRESULT D3DX11GetImageInfoFromResource(
  _In_  HMODULE           hSrcModule,
  _In_  LPCTSTR           pSrcResource,
  _In_  ID3DX11ThreadPump *pPump,
  _In_  D3DX11_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="67b4b-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="67b4b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67b4b-112">*hSrcModule* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="67b4b-112">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67b4b-113">Tipo: **[ **HMODULE**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="67b4b-113">Type: **[**HMODULE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="67b4b-114">Módulo em que o recurso está carregado.</span><span class="sxs-lookup"><span data-stu-id="67b4b-114">Module where the resource is loaded.</span></span> <span data-ttu-id="67b4b-115">Defina esse parâmetro como **NULL** para especificar o módulo associado à imagem que o sistema operacional usou para criar o processo atual.</span><span class="sxs-lookup"><span data-stu-id="67b4b-115">Set this parameter to **NULL** to specify the module associated with the image that the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="67b4b-116">*pSrcResource* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="67b4b-116">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67b4b-117">Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="67b4b-117">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="67b4b-118">Ponteiro para uma cadeia de caracteres que especifica o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="67b4b-118">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="67b4b-119">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="67b4b-119">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="67b4b-120">Caso contrário, o tipo de dados será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="67b4b-120">Otherwise, the data type resolves to LPCSTR.</span></span> <span data-ttu-id="67b4b-121">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="67b4b-121">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="67b4b-122">*pPump* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="67b4b-122">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67b4b-123">Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="67b4b-123">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="67b4b-124">Bomba de thread opcional que pode ser usada para carregar as informações de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="67b4b-124">Optional thread pump that can be used to load the info asynchronously.</span></span> <span data-ttu-id="67b4b-125">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="67b4b-125">Can be **NULL**.</span></span> <span data-ttu-id="67b4b-126">Consulte a [**interface ID3DX11ThreadPump**](id3dx11threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="67b4b-126">See [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md).</span></span>

</dd> <dt>

<span data-ttu-id="67b4b-127">*pSrcInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="67b4b-127">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67b4b-128">Tipo: **[ **D3DX11 \_ Image \_ info**](d3dx11-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="67b4b-128">Type: **[**D3DX11\_IMAGE\_INFO**](d3dx11-image-info.md)\***</span></span>

<span data-ttu-id="67b4b-129">Ponteiro para uma \_ \_ estrutura de informações de imagem D3DX11 a ser preenchida com a descrição dos dados no arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="67b4b-129">Pointer to a D3DX11\_IMAGE\_INFO structure to be filled with the description of the data in the source file.</span></span>

</dd> <dt>

<span data-ttu-id="67b4b-130">*pHResult* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="67b4b-130">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="67b4b-131">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="67b4b-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="67b4b-132">Um ponteiro para o valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="67b4b-132">A pointer to the return value.</span></span> <span data-ttu-id="67b4b-133">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="67b4b-133">May be **NULL**.</span></span> <span data-ttu-id="67b4b-134">Se *pPump* não for **NULL**, *pHResult* deverá ser um local de memória válido até que a execução assíncrona seja concluída.</span><span class="sxs-lookup"><span data-stu-id="67b4b-134">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67b4b-135">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="67b4b-135">Return value</span></span>

<span data-ttu-id="67b4b-136">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="67b4b-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="67b4b-137">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="67b4b-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="67b4b-138">Se a função falhar, o valor de retorno poderá ser o seguinte: D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="67b4b-138">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="67b4b-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="67b4b-139">Remarks</span></span>

<span data-ttu-id="67b4b-140">A configuração do compilador também determina a versão da função.</span><span class="sxs-lookup"><span data-stu-id="67b4b-140">The compiler setting also determines the function version.</span></span> <span data-ttu-id="67b4b-141">Se o Unicode for definido, a chamada de função será resolvida como **D3DX11GetImageInfoFromResourceW**.</span><span class="sxs-lookup"><span data-stu-id="67b4b-141">If Unicode is defined, the function call resolves to **D3DX11GetImageInfoFromResourceW**.</span></span> <span data-ttu-id="67b4b-142">Caso contrário, a chamada de função é resolvida como **D3DX11GetImageInfoFromResourceA** porque as cadeias de caracteres ANSI estão sendo usadas.</span><span class="sxs-lookup"><span data-stu-id="67b4b-142">Otherwise, the function call resolves to **D3DX11GetImageInfoFromResourceA** because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="67b4b-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67b4b-143">Requirements</span></span>



| <span data-ttu-id="67b4b-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="67b4b-144">Requirement</span></span> | <span data-ttu-id="67b4b-145">Valor</span><span class="sxs-lookup"><span data-stu-id="67b4b-145">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="67b4b-146">parâmetro</span><span class="sxs-lookup"><span data-stu-id="67b4b-146">Header</span></span><br/>  | <dl> <span data-ttu-id="67b4b-147"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="67b4b-147"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="67b4b-148">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="67b4b-148">Library</span></span><br/> | <dl> <span data-ttu-id="67b4b-149"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="67b4b-149"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="67b4b-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="67b4b-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67b4b-151">Funções D3DX</span><span class="sxs-lookup"><span data-stu-id="67b4b-151">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

