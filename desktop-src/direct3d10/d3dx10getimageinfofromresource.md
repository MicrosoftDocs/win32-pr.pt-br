---
description: Função D3DX10GetImageInfoFromResource – recupera informações sobre uma determinada imagem em um recurso.
ms.assetid: d413d887-77e0-43cc-a30e-67c3c40772f0
title: Função D3DX10GetImageInfoFromResource (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10GetImageInfoFromResource
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 650d05f379be634bfdd9dfb0908153260f795b00
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098364"
---
# <a name="d3dx10getimageinfofromresource-function"></a><span data-ttu-id="b5a1a-103">Função D3DX10GetImageInfoFromResource</span><span class="sxs-lookup"><span data-stu-id="b5a1a-103">D3DX10GetImageInfoFromResource function</span></span>

<span data-ttu-id="b5a1a-104">Recupera informações sobre uma determinada imagem em um recurso.</span><span class="sxs-lookup"><span data-stu-id="b5a1a-104">Retrieves information about a given image in a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5a1a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b5a1a-105">Syntax</span></span>


```C++
HRESULT D3DX10GetImageInfoFromResource(
  _In_  HMODULE           hSrcModule,
  _In_  LPCTSTR           pSrcResource,
  _In_  ID3DX10ThreadPump *pPump,
  _In_  D3DX10_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="b5a1a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b5a1a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5a1a-107">*hSrcModule* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b5a1a-107">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5a1a-108">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b5a1a-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b5a1a-109">Módulo em que o recurso está carregado.</span><span class="sxs-lookup"><span data-stu-id="b5a1a-109">Module where the resource is loaded.</span></span> <span data-ttu-id="b5a1a-110">Defina esse parâmetro como **NULL** para especificar o módulo associado à imagem que o sistema operacional usou para criar o processo atual.</span><span class="sxs-lookup"><span data-stu-id="b5a1a-110">Set this parameter to **NULL** to specify the module associated with the image that the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="b5a1a-111">*pSrcResource* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b5a1a-111">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5a1a-112">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b5a1a-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b5a1a-113">Ponteiro para uma cadeia de caracteres que especifica o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="b5a1a-113">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="b5a1a-114">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="b5a1a-114">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="b5a1a-115">Caso contrário, o tipo de dados será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="b5a1a-115">Otherwise, the data type resolves to LPCSTR.</span></span> <span data-ttu-id="b5a1a-116">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="b5a1a-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="b5a1a-117">*pPump* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b5a1a-117">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5a1a-118">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="b5a1a-118">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="b5a1a-119">Bomba de thread opcional que pode ser usada para carregar as informações de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="b5a1a-119">Optional thread pump that can be used to load the info asynchronously.</span></span> <span data-ttu-id="b5a1a-120">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="b5a1a-120">Can be **NULL**.</span></span> <span data-ttu-id="b5a1a-121">Consulte [**ID3DX10ThreadPump**](id3dx10threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="b5a1a-121">See [**ID3DX10ThreadPump**](id3dx10threadpump.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5a1a-122">*pSrcInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b5a1a-122">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5a1a-123">Tipo: **[ **D3DX10 \_ Image \_ info**](d3dx10-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="b5a1a-123">Type: **[**D3DX10\_IMAGE\_INFO**](d3dx10-image-info.md)\***</span></span>

<span data-ttu-id="b5a1a-124">Ponteiro para uma \_ \_ estrutura de informações de imagem D3DX10 a ser preenchida com a descrição dos dados no arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="b5a1a-124">Pointer to a D3DX10\_IMAGE\_INFO structure to be filled with the description of the data in the source file.</span></span>

</dd> <dt>

<span data-ttu-id="b5a1a-125">*pHResult* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b5a1a-125">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5a1a-126">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="b5a1a-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="b5a1a-127">Um ponteiro para o valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="b5a1a-127">A pointer to the return value.</span></span> <span data-ttu-id="b5a1a-128">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="b5a1a-128">May be **NULL**.</span></span> <span data-ttu-id="b5a1a-129">Se *pPump* não for **NULL**, *pHResult* deverá ser um local de memória válido até que a execução assíncrona seja concluída.</span><span class="sxs-lookup"><span data-stu-id="b5a1a-129">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5a1a-130">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="b5a1a-130">Return value</span></span>

<span data-ttu-id="b5a1a-131">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b5a1a-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b5a1a-132">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b5a1a-132">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b5a1a-133">Se a função falhar, o valor de retorno poderá ser o seguinte: D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="b5a1a-133">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="b5a1a-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="b5a1a-134">Remarks</span></span>

<span data-ttu-id="b5a1a-135">A configuração do compilador também determina a versão da função.</span><span class="sxs-lookup"><span data-stu-id="b5a1a-135">The compiler setting also determines the function version.</span></span> <span data-ttu-id="b5a1a-136">Se o Unicode for definido, a chamada de função será resolvida como D3DX10GetImageInfoFromResourceW.</span><span class="sxs-lookup"><span data-stu-id="b5a1a-136">If Unicode is defined, the function call resolves to D3DX10GetImageInfoFromResourceW.</span></span> <span data-ttu-id="b5a1a-137">Caso contrário, a chamada de função é resolvida como D3DX10GetImageInfoFromResourceA porque as cadeias de caracteres ANSI estão sendo usadas.</span><span class="sxs-lookup"><span data-stu-id="b5a1a-137">Otherwise, the function call resolves to D3DX10GetImageInfoFromResourceA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5a1a-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5a1a-138">Requirements</span></span>



| <span data-ttu-id="b5a1a-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5a1a-139">Requirement</span></span> | <span data-ttu-id="b5a1a-140">Valor</span><span class="sxs-lookup"><span data-stu-id="b5a1a-140">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5a1a-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b5a1a-141">Header</span></span><br/>  | <dl> <span data-ttu-id="b5a1a-142"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5a1a-142"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="b5a1a-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b5a1a-143">Library</span></span><br/> | <dl> <span data-ttu-id="b5a1a-144"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b5a1a-144"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="b5a1a-145">Consulte também</span><span class="sxs-lookup"><span data-stu-id="b5a1a-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5a1a-146">Funções de textura no D3DX 10</span><span class="sxs-lookup"><span data-stu-id="b5a1a-146">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
