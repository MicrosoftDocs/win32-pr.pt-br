---
description: Recupera informações sobre uma determinada imagem em um recurso.
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
ms.openlocfilehash: e77efb973e20a5db708d28b49f0cee27bee7d4e5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104172955"
---
# <a name="d3dx10getimageinfofromresource-function"></a><span data-ttu-id="0e443-103">Função D3DX10GetImageInfoFromResource</span><span class="sxs-lookup"><span data-stu-id="0e443-103">D3DX10GetImageInfoFromResource function</span></span>

<span data-ttu-id="0e443-104">Recupera informações sobre uma determinada imagem em um recurso.</span><span class="sxs-lookup"><span data-stu-id="0e443-104">Retrieves information about a given image in a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e443-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0e443-105">Syntax</span></span>


```C++
HRESULT D3DX10GetImageInfoFromResource(
  _In_  HMODULE           hSrcModule,
  _In_  LPCTSTR           pSrcResource,
  _In_  ID3DX10ThreadPump *pPump,
  _In_  D3DX10_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="0e443-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0e443-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e443-107">*hSrcModule* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0e443-107">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e443-108">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0e443-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0e443-109">Módulo em que o recurso está carregado.</span><span class="sxs-lookup"><span data-stu-id="0e443-109">Module where the resource is loaded.</span></span> <span data-ttu-id="0e443-110">Defina esse parâmetro como **NULL** para especificar o módulo associado à imagem que o sistema operacional usou para criar o processo atual.</span><span class="sxs-lookup"><span data-stu-id="0e443-110">Set this parameter to **NULL** to specify the module associated with the image that the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="0e443-111">*pSrcResource* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0e443-111">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e443-112">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0e443-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0e443-113">Ponteiro para uma cadeia de caracteres que especifica o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="0e443-113">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="0e443-114">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="0e443-114">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="0e443-115">Caso contrário, o tipo de dados será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="0e443-115">Otherwise, the data type resolves to LPCSTR.</span></span> <span data-ttu-id="0e443-116">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="0e443-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="0e443-117">*pPump* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0e443-117">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e443-118">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="0e443-118">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="0e443-119">Bomba de thread opcional que pode ser usada para carregar as informações de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="0e443-119">Optional thread pump that can be used to load the info asynchronously.</span></span> <span data-ttu-id="0e443-120">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="0e443-120">Can be **NULL**.</span></span> <span data-ttu-id="0e443-121">Consulte [**ID3DX10ThreadPump**](id3dx10threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="0e443-121">See [**ID3DX10ThreadPump**](id3dx10threadpump.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e443-122">*pSrcInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0e443-122">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e443-123">Tipo: **[ **D3DX10 \_ Image \_ info**](d3dx10-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="0e443-123">Type: **[**D3DX10\_IMAGE\_INFO**](d3dx10-image-info.md)\***</span></span>

<span data-ttu-id="0e443-124">Ponteiro para uma \_ \_ estrutura de informações de imagem D3DX10 a ser preenchida com a descrição dos dados no arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="0e443-124">Pointer to a D3DX10\_IMAGE\_INFO structure to be filled with the description of the data in the source file.</span></span>

</dd> <dt>

<span data-ttu-id="0e443-125">*pHResult* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0e443-125">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0e443-126">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="0e443-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="0e443-127">Um ponteiro para o valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="0e443-127">A pointer to the return value.</span></span> <span data-ttu-id="0e443-128">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="0e443-128">May be **NULL**.</span></span> <span data-ttu-id="0e443-129">Se *pPump* não for **NULL**, *pHResult* deverá ser um local de memória válido até que a execução assíncrona seja concluída.</span><span class="sxs-lookup"><span data-stu-id="0e443-129">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e443-130">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0e443-130">Return value</span></span>

<span data-ttu-id="0e443-131">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0e443-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0e443-132">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0e443-132">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0e443-133">Se a função falhar, o valor de retorno poderá ser o seguinte: D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="0e443-133">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="0e443-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="0e443-134">Remarks</span></span>

<span data-ttu-id="0e443-135">A configuração do compilador também determina a versão da função.</span><span class="sxs-lookup"><span data-stu-id="0e443-135">The compiler setting also determines the function version.</span></span> <span data-ttu-id="0e443-136">Se o Unicode for definido, a chamada de função será resolvida como D3DX10GetImageInfoFromResourceW.</span><span class="sxs-lookup"><span data-stu-id="0e443-136">If Unicode is defined, the function call resolves to D3DX10GetImageInfoFromResourceW.</span></span> <span data-ttu-id="0e443-137">Caso contrário, a chamada de função é resolvida como D3DX10GetImageInfoFromResourceA porque as cadeias de caracteres ANSI estão sendo usadas.</span><span class="sxs-lookup"><span data-stu-id="0e443-137">Otherwise, the function call resolves to D3DX10GetImageInfoFromResourceA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e443-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e443-138">Requirements</span></span>



| <span data-ttu-id="0e443-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e443-139">Requirement</span></span> | <span data-ttu-id="0e443-140">Valor</span><span class="sxs-lookup"><span data-stu-id="0e443-140">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e443-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0e443-141">Header</span></span><br/>  | <dl> <span data-ttu-id="0e443-142"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e443-142"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="0e443-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0e443-143">Library</span></span><br/> | <dl> <span data-ttu-id="0e443-144"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0e443-144"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="0e443-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="0e443-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e443-146">Funções de textura no D3DX 10</span><span class="sxs-lookup"><span data-stu-id="0e443-146">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
