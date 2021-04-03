---
description: Crie um recurso de textura a partir de um arquivo que reside na memória do sistema.
ms.assetid: 63eac44b-0540-457f-96c0-d151fbd44df0
title: Função D3DX10CreateTextureFromMemory (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateTextureFromMemory
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 885f734cd9caeaccbab27b2fcdb258c032c5d7c5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930570"
---
# <a name="d3dx10createtexturefrommemory-function"></a><span data-ttu-id="0d5cd-103">Função D3DX10CreateTextureFromMemory</span><span class="sxs-lookup"><span data-stu-id="0d5cd-103">D3DX10CreateTextureFromMemory function</span></span>

<span data-ttu-id="0d5cd-104">Crie um recurso de textura a partir de um arquivo que reside na memória do sistema.</span><span class="sxs-lookup"><span data-stu-id="0d5cd-104">Create a texture resource from a file residing in system memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d5cd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0d5cd-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateTextureFromMemory(
  _In_  ID3D10Device           *pDevice,
  _In_  LPCVOID                pSrcData,
  _In_  SIZE_T                 SrcDataSize,
  _In_  D3DX10_IMAGE_LOAD_INFO *pLoadInfo,
  _In_  ID3DX10ThreadPump      *pPump,
  _Out_ ID3D10Resource         **ppTexture,
  _Out_ HRESULT                *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="0d5cd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0d5cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d5cd-107">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0d5cd-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d5cd-108">Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="0d5cd-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="0d5cd-109">Um ponteiro para o dispositivo (consulte a [**interface ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) que usará o recurso.</span><span class="sxs-lookup"><span data-stu-id="0d5cd-109">A pointer to the device (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="0d5cd-110">*pSrcData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0d5cd-110">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d5cd-111">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0d5cd-111">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0d5cd-112">Ponteiro para o recurso na memória do sistema.</span><span class="sxs-lookup"><span data-stu-id="0d5cd-112">Pointer to the resource in system memory.</span></span>

</dd> <dt>

<span data-ttu-id="0d5cd-113">*SrcDataSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0d5cd-113">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d5cd-114">Tipo: **[ **tamanho \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0d5cd-114">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0d5cd-115">Tamanho do recurso na memória do sistema.</span><span class="sxs-lookup"><span data-stu-id="0d5cd-115">Size of the resource in system memory.</span></span>

</dd> <dt>

<span data-ttu-id="0d5cd-116">*pLoadInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0d5cd-116">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d5cd-117">Tipo: **[ **\_ informações de \_ carregamento \_ de imagem D3DX10**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="0d5cd-117">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="0d5cd-118">Opcional.</span><span class="sxs-lookup"><span data-stu-id="0d5cd-118">Optional.</span></span> <span data-ttu-id="0d5cd-119">Identifica as características de uma textura (consulte [**\_ informações de \_ carregamento \_ de imagem D3DX10**](d3dx10-image-load-info.md)) quando o processador de dados é criado; defina isso como **nulo** para ler as características de uma textura quando a textura for carregada.</span><span class="sxs-lookup"><span data-stu-id="0d5cd-119">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="0d5cd-120">*pPump* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0d5cd-120">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d5cd-121">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="0d5cd-121">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="0d5cd-122">Um ponteiro para uma interface de bombeamento de thread (consulte a [**interface ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="0d5cd-122">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="0d5cd-123">Se **NULL** for especificado, essa função se comportará de forma síncrona e não retornará até que seja concluída.</span><span class="sxs-lookup"><span data-stu-id="0d5cd-123">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="0d5cd-124">*ppTexture* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0d5cd-124">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d5cd-125">Tipo: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\*\***</span><span class="sxs-lookup"><span data-stu-id="0d5cd-125">Type: **[**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\*\***</span></span>

<span data-ttu-id="0d5cd-126">Endereço de um ponteiro para o recurso criado.</span><span class="sxs-lookup"><span data-stu-id="0d5cd-126">Address of a pointer to the created resource.</span></span> <span data-ttu-id="0d5cd-127">Consulte a [**interface ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span><span class="sxs-lookup"><span data-stu-id="0d5cd-127">See [**ID3D10Resource Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span></span>

</dd> <dt>

<span data-ttu-id="0d5cd-128">*pHResult* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0d5cd-128">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d5cd-129">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="0d5cd-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="0d5cd-130">Um ponteiro para o valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="0d5cd-130">A pointer to the return value.</span></span> <span data-ttu-id="0d5cd-131">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="0d5cd-131">May be **NULL**.</span></span> <span data-ttu-id="0d5cd-132">Se *pPump* não for **NULL**, *pHResult* deverá ser um local de memória válido até que a execução assíncrona seja concluída.</span><span class="sxs-lookup"><span data-stu-id="0d5cd-132">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d5cd-133">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0d5cd-133">Return value</span></span>

<span data-ttu-id="0d5cd-134">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0d5cd-134">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0d5cd-135">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="0d5cd-135">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0d5cd-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="0d5cd-136">Remarks</span></span>

<span data-ttu-id="0d5cd-137">Para obter uma lista de formatos de imagem com suporte, consulte [**\_ formato de \_ arquivo \_ de imagem D3DX10**](d3dx10-image-file-format.md).</span><span class="sxs-lookup"><span data-stu-id="0d5cd-137">For a list of supported image formats see [**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0d5cd-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d5cd-138">Requirements</span></span>



| <span data-ttu-id="0d5cd-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d5cd-139">Requirement</span></span> | <span data-ttu-id="0d5cd-140">Valor</span><span class="sxs-lookup"><span data-stu-id="0d5cd-140">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0d5cd-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0d5cd-141">Header</span></span><br/>  | <dl> <span data-ttu-id="0d5cd-142"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d5cd-142"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="0d5cd-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0d5cd-143">Library</span></span><br/> | <dl> <span data-ttu-id="0d5cd-144"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0d5cd-144"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d5cd-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="0d5cd-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d5cd-146">Funções de textura no D3DX 10</span><span class="sxs-lookup"><span data-stu-id="0d5cd-146">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[<span data-ttu-id="0d5cd-147">Funções de Uso Geral</span><span class="sxs-lookup"><span data-stu-id="0d5cd-147">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
