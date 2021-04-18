---
description: Crie um recurso de textura a partir de um arquivo.
ms.assetid: 23edad1f-89bb-4b62-8c48-3be1cd0690d2
title: Função D3DX10CreateTextureFromFile (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateTextureFromFile
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 27db799bfd521133a2c137556fdd7408be974854
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105781350"
---
# <a name="d3dx10createtexturefromfile-function"></a><span data-ttu-id="edca9-103">Função D3DX10CreateTextureFromFile</span><span class="sxs-lookup"><span data-stu-id="edca9-103">D3DX10CreateTextureFromFile function</span></span>

<span data-ttu-id="edca9-104">Crie um recurso de textura a partir de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="edca9-104">Create a texture resource from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="edca9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="edca9-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateTextureFromFile(
  _In_  ID3D10Device           *pDevice,
  _In_  LPCTSTR                pSrcFile,
  _In_  D3DX10_IMAGE_LOAD_INFO *pLoadInfo,
  _In_  ID3DX10ThreadPump      *pPump,
  _Out_ ID3D10Resource         **ppTexture,
  _Out_ HRESULT                *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="edca9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="edca9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edca9-107">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="edca9-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edca9-108">Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="edca9-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="edca9-109">Um ponteiro para o dispositivo (consulte a [**interface ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) que usará o recurso.</span><span class="sxs-lookup"><span data-stu-id="edca9-109">A pointer to the device (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="edca9-110">*pSrcFile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="edca9-110">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edca9-111">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="edca9-111">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="edca9-112">O nome do arquivo que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="edca9-112">The name of the file containing the resource.</span></span> <span data-ttu-id="edca9-113">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="edca9-113">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="edca9-114">Caso contrário, o tipo de dados será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="edca9-114">Otherwise, the data type resolves to LPCSTR.</span></span> <span data-ttu-id="edca9-115">Consulte Enumeração de [**\_ formato de \_ arquivo \_ de imagem D3DX10**](d3dx10-image-file-format.md) para obter uma lista dos formatos de arquivo de imagem com suporte.</span><span class="sxs-lookup"><span data-stu-id="edca9-115">See [**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md) enumeration for a list of the supported image file formats.</span></span>

</dd> <dt>

<span data-ttu-id="edca9-116">*pLoadInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="edca9-116">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edca9-117">Tipo: **[ **\_ informações de \_ carregamento \_ de imagem D3DX10**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="edca9-117">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="edca9-118">Opcional.</span><span class="sxs-lookup"><span data-stu-id="edca9-118">Optional.</span></span> <span data-ttu-id="edca9-119">Identifica as características de uma textura (consulte [**\_ informações de \_ carregamento \_ de imagem D3DX10**](d3dx10-image-load-info.md)) quando o processador de dados é criado; defina isso como **nulo** para ler as características de uma textura quando a textura for carregada.</span><span class="sxs-lookup"><span data-stu-id="edca9-119">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="edca9-120">*pPump* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="edca9-120">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edca9-121">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="edca9-121">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="edca9-122">Um ponteiro para uma interface de bombeamento de thread (consulte a [**interface ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="edca9-122">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="edca9-123">Se **NULL** for especificado, essa função se comportará de forma síncrona e não retornará até que seja concluída.</span><span class="sxs-lookup"><span data-stu-id="edca9-123">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="edca9-124">*ppTexture* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="edca9-124">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="edca9-125">Tipo: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\*\***</span><span class="sxs-lookup"><span data-stu-id="edca9-125">Type: **[**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\*\***</span></span>

<span data-ttu-id="edca9-126">O endereço de um ponteiro para o recurso de textura (consulte a [**interface ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)).</span><span class="sxs-lookup"><span data-stu-id="edca9-126">The address of a pointer to the texture resource (see [**ID3D10Resource Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)).</span></span>

</dd> <dt>

<span data-ttu-id="edca9-127">*pHResult* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="edca9-127">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="edca9-128">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="edca9-128">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="edca9-129">Um ponteiro para o valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="edca9-129">A pointer to the return value.</span></span> <span data-ttu-id="edca9-130">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="edca9-130">May be **NULL**.</span></span> <span data-ttu-id="edca9-131">Se *pPump* não for **NULL**, *pHResult* deverá ser um local de memória válido até que a execução assíncrona seja concluída.</span><span class="sxs-lookup"><span data-stu-id="edca9-131">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edca9-132">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="edca9-132">Return value</span></span>

<span data-ttu-id="edca9-133">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="edca9-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="edca9-134">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="edca9-134">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="edca9-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="edca9-135">Remarks</span></span>

<span data-ttu-id="edca9-136">Para obter uma lista de formatos de imagem com suporte, consulte [**\_ formato de \_ arquivo \_ de imagem D3DX10**](d3dx10-image-file-format.md).</span><span class="sxs-lookup"><span data-stu-id="edca9-136">For a list of supported image formats see [**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="edca9-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="edca9-137">Requirements</span></span>



| <span data-ttu-id="edca9-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="edca9-138">Requirement</span></span> | <span data-ttu-id="edca9-139">Valor</span><span class="sxs-lookup"><span data-stu-id="edca9-139">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="edca9-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="edca9-140">Header</span></span><br/>  | <dl> <span data-ttu-id="edca9-141"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="edca9-141"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="edca9-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="edca9-142">Library</span></span><br/> | <dl> <span data-ttu-id="edca9-143"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="edca9-143"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="edca9-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="edca9-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edca9-145">Funções de textura no D3DX 10</span><span class="sxs-lookup"><span data-stu-id="edca9-145">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[<span data-ttu-id="edca9-146">Funções de Uso Geral</span><span class="sxs-lookup"><span data-stu-id="edca9-146">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
