---
description: Crie uma textura de outro recurso.
ms.assetid: 9758968a-652f-42bb-8c81-ad7816c57b17
title: Função D3DX10CreateTextureFromResource (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateTextureFromResource
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 22be3b54c7aa9090fd95624a51bc248b01003dcc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105810671"
---
# <a name="d3dx10createtexturefromresource-function"></a><span data-ttu-id="02723-103">Função D3DX10CreateTextureFromResource</span><span class="sxs-lookup"><span data-stu-id="02723-103">D3DX10CreateTextureFromResource function</span></span>

<span data-ttu-id="02723-104">Crie uma textura de outro recurso.</span><span class="sxs-lookup"><span data-stu-id="02723-104">Create a texture from another resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="02723-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="02723-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateTextureFromResource(
  _In_  ID3D10Device           *pDevice,
  _In_  HMODULE                hSrcModule,
  _In_  LPCTSTR                pSrcResource,
  _In_  D3DX10_IMAGE_LOAD_INFO *pLoadInfo,
  _In_  ID3DX10ThreadPump      *pPump,
  _Out_ ID3D10Resource         **ppTexture,
  _Out_ HRESULT                *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="02723-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="02723-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02723-107">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="02723-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02723-108">Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="02723-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="02723-109">Um ponteiro para o dispositivo (consulte a [**interface ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) que usará o recurso.</span><span class="sxs-lookup"><span data-stu-id="02723-109">A pointer to the device (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="02723-110">*hSrcModule* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="02723-110">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02723-111">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="02723-111">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="02723-112">Um identificador para o recurso de origem.</span><span class="sxs-lookup"><span data-stu-id="02723-112">A handle to the source resource.</span></span> <span data-ttu-id="02723-113">HMODULE pode ser obtido com a [função GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span><span class="sxs-lookup"><span data-stu-id="02723-113">HMODULE can be obtained with [GetModuleHandle Function](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="02723-114">*pSrcResource* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="02723-114">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02723-115">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="02723-115">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="02723-116">Uma cadeia de caracteres que contém o nome do recurso de origem.</span><span class="sxs-lookup"><span data-stu-id="02723-116">A string that contains the name of the source resource.</span></span> <span data-ttu-id="02723-117">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="02723-117">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="02723-118">Caso contrário, o tipo de dados será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="02723-118">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="02723-119">*pLoadInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="02723-119">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02723-120">Tipo: **[ **\_ informações de \_ carregamento \_ de imagem D3DX10**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="02723-120">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="02723-121">Opcional.</span><span class="sxs-lookup"><span data-stu-id="02723-121">Optional.</span></span> <span data-ttu-id="02723-122">Identifica as características de uma textura (consulte [**\_ informações de \_ carregamento \_ de imagem D3DX10**](d3dx10-image-load-info.md)) quando o processador de dados é criado; defina isso como **nulo** para ler as características de uma textura quando a textura for carregada.</span><span class="sxs-lookup"><span data-stu-id="02723-122">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="02723-123">*pPump* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="02723-123">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02723-124">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="02723-124">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="02723-125">Um ponteiro para uma interface de bombeamento de thread (consulte a [**interface ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="02723-125">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="02723-126">Se **NULL** for especificado, essa função se comportará de forma síncrona e não retornará até que seja concluída.</span><span class="sxs-lookup"><span data-stu-id="02723-126">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="02723-127">*ppTexture* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="02723-127">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="02723-128">Tipo: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\*\***</span><span class="sxs-lookup"><span data-stu-id="02723-128">Type: **[**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\*\***</span></span>

<span data-ttu-id="02723-129">O endereço de um ponteiro para o recurso de textura (consulte a [**interface ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)).</span><span class="sxs-lookup"><span data-stu-id="02723-129">The address of a pointer to the texture resource (see [**ID3D10Resource Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)).</span></span>

</dd> <dt>

<span data-ttu-id="02723-130">*pHResult* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="02723-130">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="02723-131">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="02723-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="02723-132">Um ponteiro para o valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="02723-132">A pointer to the return value.</span></span> <span data-ttu-id="02723-133">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="02723-133">May be **NULL**.</span></span> <span data-ttu-id="02723-134">Se *pPump* não for **NULL**, *pHResult* deverá ser um local de memória válido até que a execução assíncrona seja concluída.</span><span class="sxs-lookup"><span data-stu-id="02723-134">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02723-135">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="02723-135">Return value</span></span>

<span data-ttu-id="02723-136">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="02723-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="02723-137">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="02723-137">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="02723-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="02723-138">Remarks</span></span>

<span data-ttu-id="02723-139">Para obter uma lista de formatos de imagem com suporte, consulte [**\_ formato de \_ arquivo \_ de imagem D3DX10**](d3dx10-image-file-format.md).</span><span class="sxs-lookup"><span data-stu-id="02723-139">For a list of supported image formats see [**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="02723-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02723-140">Requirements</span></span>



| <span data-ttu-id="02723-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="02723-141">Requirement</span></span> | <span data-ttu-id="02723-142">Valor</span><span class="sxs-lookup"><span data-stu-id="02723-142">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="02723-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="02723-143">Header</span></span><br/>  | <dl> <span data-ttu-id="02723-144"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="02723-144"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="02723-145">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="02723-145">Library</span></span><br/> | <dl> <span data-ttu-id="02723-146"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="02723-146"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02723-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="02723-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02723-148">Funções de textura no D3DX 10</span><span class="sxs-lookup"><span data-stu-id="02723-148">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[<span data-ttu-id="02723-149">Funções de Uso Geral</span><span class="sxs-lookup"><span data-stu-id="02723-149">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
