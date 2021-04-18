---
description: Recupera informações sobre um determinado arquivo de imagem na memória.
ms.assetid: 6363aaf1-abfc-49df-9b99-be8a1c3540e1
title: Função D3DXGetImageInfoFromFileInMemory (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetImageInfoFromFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e2bad56cb2aa769be80a6b031b1783d8717bc485
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105814442"
---
# <a name="d3dxgetimageinfofromfileinmemory-function"></a><span data-ttu-id="eb3a3-103">Função D3DXGetImageInfoFromFileInMemory</span><span class="sxs-lookup"><span data-stu-id="eb3a3-103">D3DXGetImageInfoFromFileInMemory function</span></span>

<span data-ttu-id="eb3a3-104">Recupera informações sobre um determinado arquivo de imagem na memória.</span><span class="sxs-lookup"><span data-stu-id="eb3a3-104">Retrieves information about a given image file in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb3a3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eb3a3-105">Syntax</span></span>


```C++
HRESULT D3DXGetImageInfoFromFileInMemory(
  _In_ LPCVOID        pSrcData,
  _In_ UINT           SrcDataSize,
  _In_ D3DXIMAGE_INFO *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="eb3a3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eb3a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb3a3-107">*pSrcData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="eb3a3-107">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb3a3-108">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eb3a3-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="eb3a3-109">Ponteiro VOID para o arquivo de origem na memória.</span><span class="sxs-lookup"><span data-stu-id="eb3a3-109">VOID pointer to the source file in memory.</span></span>

</dd> <dt>

<span data-ttu-id="eb3a3-110">*SrcDataSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="eb3a3-110">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb3a3-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eb3a3-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="eb3a3-112">Tamanho do arquivo na memória, em bytes.</span><span class="sxs-lookup"><span data-stu-id="eb3a3-112">Size of file in memory, in bytes.</span></span> <span data-ttu-id="eb3a3-113">.</span><span class="sxs-lookup"><span data-stu-id="eb3a3-113">.</span></span>

</dd> <dt>

<span data-ttu-id="eb3a3-114">*pSrcInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="eb3a3-114">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb3a3-115">Tipo: **[ **\_ informações de D3DXIMAGE**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="eb3a3-115">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="eb3a3-116">Ponteiro para uma estrutura de [**\_ informações de D3DXIMAGE**](d3dximage-info.md) a ser preenchida com a descrição dos dados no arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="eb3a3-116">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with the description of the data in the source file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb3a3-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="eb3a3-117">Return value</span></span>

<span data-ttu-id="eb3a3-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="eb3a3-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="eb3a3-119">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="eb3a3-119">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="eb3a3-120">Se a função falhar, o valor de retorno poderá ser o seguinte: D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="eb3a3-120">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="requirements"></a><span data-ttu-id="eb3a3-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb3a3-121">Requirements</span></span>



| <span data-ttu-id="eb3a3-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb3a3-122">Requirement</span></span> | <span data-ttu-id="eb3a3-123">Valor</span><span class="sxs-lookup"><span data-stu-id="eb3a3-123">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eb3a3-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="eb3a3-124">Header</span></span><br/>  | <dl> <span data-ttu-id="eb3a3-125"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb3a3-125"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="eb3a3-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="eb3a3-126">Library</span></span><br/> | <dl> <span data-ttu-id="eb3a3-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eb3a3-127"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="eb3a3-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="eb3a3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb3a3-129">Funções de textura no D3DX 9</span><span class="sxs-lookup"><span data-stu-id="eb3a3-129">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="eb3a3-130">**D3DXGetImageInfoFromFile**</span><span class="sxs-lookup"><span data-stu-id="eb3a3-130">**D3DXGetImageInfoFromFile**</span></span>](d3dxgetimageinfofromfile.md)
</dt> <dt>

[<span data-ttu-id="eb3a3-131">**D3DXGetImageInfoFromResource**</span><span class="sxs-lookup"><span data-stu-id="eb3a3-131">**D3DXGetImageInfoFromResource**</span></span>](d3dxgetimageinfofromresource.md)
</dt> </dl>

 

 
