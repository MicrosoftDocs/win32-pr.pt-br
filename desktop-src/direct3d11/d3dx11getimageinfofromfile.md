---
title: Função D3DX11GetImageInfoFromFile (D3DX11tex. h)
description: Observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Observação em vez de usar essa função, recomendamos que você use a biblioteca DirectXTex, GetMetadataFromXXXFile (em que XXX é o WIC, DDS ou TGA; O WIC não oferece suporte a DDS e TGA; O D3DX 9 TGA com suporte como um formato de origem de arte comum para jogos). Recupera informações sobre um determinado arquivo de imagem.
ms.assetid: 57768604-3672-49a0-8120-f09240b8fc98
keywords:
- Função D3DX11GetImageInfoFromFile Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11GetImageInfoFromFile
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8448d31a3f4fdb14855ea2c9456da87f9df1de4f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012138"
---
# <a name="d3dx11getimageinfofromfile-function"></a><span data-ttu-id="c7515-106">Função D3DX11GetImageInfoFromFile</span><span class="sxs-lookup"><span data-stu-id="c7515-106">D3DX11GetImageInfoFromFile function</span></span>

> [!Note]  
> <span data-ttu-id="c7515-107">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="c7515-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="c7515-108">Em vez de usar essa função, recomendamos que você use a biblioteca [DirectXTex](https://github.com/Microsoft/DirectXTex) , **GetMetadataFromXXXFile** (em que xxx é o WIC, DDS ou TGA; O WIC não oferece suporte a DDS e TGA; O D3DX 9 TGA com suporte como um formato de origem de arte comum para jogos).</span><span class="sxs-lookup"><span data-stu-id="c7515-108">Instead of using this function, we recommend that you use the [DirectXTex](https://github.com/Microsoft/DirectXTex) library, **GetMetadataFromXXXFile** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span>

 

<span data-ttu-id="c7515-109">Recupera informações sobre um determinado arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="c7515-109">Retrieves information about a given image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7515-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c7515-110">Syntax</span></span>


```C++
HRESULT D3DX11GetImageInfoFromFile(
  _In_  LPCTSTR           pSrcFile,
  _In_  ID3DX11ThreadPump *pPump,
  _In_  D3DX11_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="c7515-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c7515-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7515-112">*pSrcFile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c7515-112">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7515-113">Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c7515-113">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c7515-114">Nome do arquivo da imagem para recuperar informações.</span><span class="sxs-lookup"><span data-stu-id="c7515-114">File name of image to retrieve information about.</span></span> <span data-ttu-id="c7515-115">Se UNICODE ou \_ Unicode estiverem definidos, esse tipo de parâmetro será LPCWSTR, caso contrário, o tipo será LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="c7515-115">If UNICODE or \_UNICODE are defined, this parameter type is LPCWSTR, otherwise, the type is LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="c7515-116">*pPump* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c7515-116">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7515-117">Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="c7515-117">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="c7515-118">Bomba de thread opcional que pode ser usada para carregar as informações de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="c7515-118">Optional thread pump that can be used to load the info asynchronously.</span></span> <span data-ttu-id="c7515-119">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="c7515-119">Can be **NULL**.</span></span> <span data-ttu-id="c7515-120">Consulte a [**interface ID3DX11ThreadPump**](id3dx11threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="c7515-120">See [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7515-121">*pSrcInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c7515-121">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7515-122">Tipo: **[ **D3DX11 \_ Image \_ info**](d3dx11-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="c7515-122">Type: **[**D3DX11\_IMAGE\_INFO**](d3dx11-image-info.md)\***</span></span>

<span data-ttu-id="c7515-123">Ponteiro para uma [**D3DX11 \_ de \_ informações de imagem**](d3dx11-image-info.md) a ser preenchida com a descrição dos dados no arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="c7515-123">Pointer to a [**D3DX11\_IMAGE\_INFO**](d3dx11-image-info.md) to be filled with the description of the data in the source file.</span></span>

</dd> <dt>

<span data-ttu-id="c7515-124">*pHResult* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c7515-124">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c7515-125">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="c7515-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="c7515-126">Um ponteiro para o valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="c7515-126">A pointer to the return value.</span></span> <span data-ttu-id="c7515-127">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="c7515-127">May be **NULL**.</span></span> <span data-ttu-id="c7515-128">Se *pPump* não for **NULL**, *pHResult* deverá ser um local de memória válido até que a execução assíncrona seja concluída.</span><span class="sxs-lookup"><span data-stu-id="c7515-128">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7515-129">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c7515-129">Return value</span></span>

<span data-ttu-id="c7515-130">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c7515-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c7515-131">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c7515-131">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c7515-132">Se a função falhar, o valor de retorno poderá ser o seguinte: D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="c7515-132">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="c7515-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="c7515-133">Remarks</span></span>

<span data-ttu-id="c7515-134">Essa função dá suporte a cadeias de caracteres Unicode e ANSI.</span><span class="sxs-lookup"><span data-stu-id="c7515-134">This function supports both Unicode and ANSI strings.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7515-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7515-135">Requirements</span></span>



| <span data-ttu-id="c7515-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7515-136">Requirement</span></span> | <span data-ttu-id="c7515-137">Valor</span><span class="sxs-lookup"><span data-stu-id="c7515-137">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7515-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c7515-138">Header</span></span><br/>  | <dl> <span data-ttu-id="c7515-139"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7515-139"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="c7515-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c7515-140">Library</span></span><br/> | <dl> <span data-ttu-id="c7515-141"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c7515-141"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="c7515-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="c7515-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7515-143">Funções D3DX</span><span class="sxs-lookup"><span data-stu-id="c7515-143">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

