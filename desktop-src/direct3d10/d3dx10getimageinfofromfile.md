---
description: Função D3DX10GetImageInfoFromFile – recupera informações sobre um determinado arquivo de imagem.
ms.assetid: 59bdce45-82d9-42da-b847-a29ca71919b5
title: Função D3DX10GetImageInfoFromFile (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10GetImageInfoFromFile
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3e11c4cb52176b0a144e164501f8c70d1e3678c1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098324"
---
# <a name="d3dx10getimageinfofromfile-function"></a><span data-ttu-id="32966-103">Função D3DX10GetImageInfoFromFile</span><span class="sxs-lookup"><span data-stu-id="32966-103">D3DX10GetImageInfoFromFile function</span></span>

<span data-ttu-id="32966-104">Recupera informações sobre um determinado arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="32966-104">Retrieves information about a given image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="32966-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="32966-105">Syntax</span></span>


```C++
HRESULT D3DX10GetImageInfoFromFile(
  _In_  LPCTSTR           pSrcFile,
  _In_  ID3DX10ThreadPump *pPump,
  _In_  D3DX10_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="32966-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="32966-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32966-107">*pSrcFile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="32966-107">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32966-108">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="32966-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="32966-109">Nome do arquivo da imagem para recuperar informações.</span><span class="sxs-lookup"><span data-stu-id="32966-109">File name of image to retrieve information about.</span></span> <span data-ttu-id="32966-110">Se UNICODE ou \_ Unicode estiverem definidos, esse tipo de parâmetro será LPCWSTR, caso contrário, o tipo será LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="32966-110">If UNICODE or \_UNICODE are defined, this parameter type is LPCWSTR, otherwise, the type is LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="32966-111">*pPump* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="32966-111">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32966-112">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="32966-112">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="32966-113">Bomba de thread opcional que pode ser usada para carregar as informações de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="32966-113">Optional thread pump that can be used to load the info asynchronously.</span></span> <span data-ttu-id="32966-114">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="32966-114">Can be **NULL**.</span></span> <span data-ttu-id="32966-115">Consulte [**ID3DX10ThreadPump**](id3dx10threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="32966-115">See [**ID3DX10ThreadPump**](id3dx10threadpump.md).</span></span>

</dd> <dt>

<span data-ttu-id="32966-116">*pSrcInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="32966-116">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32966-117">Tipo: **[ **D3DX10 \_ Image \_ info**](d3dx10-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="32966-117">Type: **[**D3DX10\_IMAGE\_INFO**](d3dx10-image-info.md)\***</span></span>

<span data-ttu-id="32966-118">Ponteiro para uma \_ \_ estrutura de informações de imagem D3DX10 a ser preenchida com a descrição dos dados no arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="32966-118">Pointer to a D3DX10\_IMAGE\_INFO structure to be filled with the description of the data in the source file.</span></span>

</dd> <dt>

<span data-ttu-id="32966-119">*pHResult* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="32966-119">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="32966-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="32966-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="32966-121">Um ponteiro para o valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="32966-121">A pointer to the return value.</span></span> <span data-ttu-id="32966-122">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="32966-122">May be **NULL**.</span></span> <span data-ttu-id="32966-123">Se *pPump* não for **NULL**, *pHResult* deverá ser um local de memória válido até que a execução assíncrona seja concluída.</span><span class="sxs-lookup"><span data-stu-id="32966-123">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32966-124">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="32966-124">Return value</span></span>

<span data-ttu-id="32966-125">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="32966-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="32966-126">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="32966-126">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="32966-127">Se a função falhar, o valor de retorno poderá ser o seguinte: D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="32966-127">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="32966-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="32966-128">Remarks</span></span>

<span data-ttu-id="32966-129">Essa função dá suporte a cadeias de caracteres Unicode e ANSI.</span><span class="sxs-lookup"><span data-stu-id="32966-129">This function supports both Unicode and ANSI strings.</span></span>

## <a name="requirements"></a><span data-ttu-id="32966-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32966-130">Requirements</span></span>



| <span data-ttu-id="32966-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="32966-131">Requirement</span></span> | <span data-ttu-id="32966-132">Valor</span><span class="sxs-lookup"><span data-stu-id="32966-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="32966-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="32966-133">Header</span></span><br/>  | <dl> <span data-ttu-id="32966-134"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="32966-134"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="32966-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="32966-135">Library</span></span><br/> | <dl> <span data-ttu-id="32966-136"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="32966-136"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="32966-137">Consulte também</span><span class="sxs-lookup"><span data-stu-id="32966-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32966-138">Funções de textura no D3DX 10</span><span class="sxs-lookup"><span data-stu-id="32966-138">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
