---
description: Função D3DXGetImageInfoFromFile – recupera informações sobre um determinado arquivo de imagem.
ms.assetid: 2e9d7073-4136-4fb7-8749-810aee000433
title: Função D3DXGetImageInfoFromFile (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetImageInfoFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bb03b6482d140a3b78e43d8b99c60499ae6c8b16
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114484"
---
# <a name="d3dxgetimageinfofromfile-function"></a><span data-ttu-id="6d138-103">Função D3DXGetImageInfoFromFile</span><span class="sxs-lookup"><span data-stu-id="6d138-103">D3DXGetImageInfoFromFile function</span></span>

<span data-ttu-id="6d138-104">Recupera informações sobre um determinado arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="6d138-104">Retrieves information about a given image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d138-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6d138-105">Syntax</span></span>


```C++
HRESULT D3DXGetImageInfoFromFile(
  _In_ LPCSTR         pSrcFile,
  _In_ D3DXIMAGE_INFO *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="6d138-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6d138-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d138-107">*pSrcFile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6d138-107">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d138-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6d138-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6d138-109">Nome do arquivo da imagem para recuperar informações.</span><span class="sxs-lookup"><span data-stu-id="6d138-109">File name of image to retrieve information about.</span></span> <span data-ttu-id="6d138-110">Se UNICODE ou \_ Unicode estiverem definidos, esse tipo de parâmetro será LPCWSTR, caso contrário, o tipo será LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="6d138-110">If UNICODE or \_UNICODE are defined, this parameter type is LPCWSTR, otherwise, the type is LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="6d138-111">*pSrcInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6d138-111">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d138-112">Tipo: **[ **\_ informações de D3DXIMAGE**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="6d138-112">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="6d138-113">Ponteiro para uma estrutura de [**\_ informações de D3DXIMAGE**](d3dximage-info.md) a ser preenchida com a descrição dos dados no arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="6d138-113">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with the description of the data in the source file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d138-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="6d138-114">Return value</span></span>

<span data-ttu-id="6d138-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6d138-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6d138-116">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6d138-116">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6d138-117">Se a função falhar, o valor de retorno poderá ser o seguinte: D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="6d138-117">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="6d138-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="6d138-118">Remarks</span></span>

<span data-ttu-id="6d138-119">Essa função dá suporte a cadeias de caracteres Unicode e ANSI.</span><span class="sxs-lookup"><span data-stu-id="6d138-119">This function supports both Unicode and ANSI strings.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d138-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d138-120">Requirements</span></span>



| <span data-ttu-id="6d138-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d138-121">Requirement</span></span> | <span data-ttu-id="6d138-122">Valor</span><span class="sxs-lookup"><span data-stu-id="6d138-122">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6d138-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6d138-123">Header</span></span><br/>  | <dl> <span data-ttu-id="6d138-124"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d138-124"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="6d138-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6d138-125">Library</span></span><br/> | <dl> <span data-ttu-id="6d138-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6d138-126"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="6d138-127">Consulte também</span><span class="sxs-lookup"><span data-stu-id="6d138-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d138-128">Funções de textura no D3DX 9</span><span class="sxs-lookup"><span data-stu-id="6d138-128">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="6d138-129">**D3DXGetImageInfoFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="6d138-129">**D3DXGetImageInfoFromFileInMemory**</span></span>](d3dxgetimageinfofromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="6d138-130">**D3DXGetImageInfoFromResource**</span><span class="sxs-lookup"><span data-stu-id="6d138-130">**D3DXGetImageInfoFromResource**</span></span>](d3dxgetimageinfofromresource.md)
</dt> </dl>

 

 
