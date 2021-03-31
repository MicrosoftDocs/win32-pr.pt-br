---
description: Recupera informações sobre uma determinada imagem em um recurso.
ms.assetid: 1f811b1e-f0bd-4f64-a4c9-caf899470940
title: Função D3DXGetImageInfoFromResource (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetImageInfoFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6875719123fe0b4dca4405570703b2587492975b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664003"
---
# <a name="d3dxgetimageinfofromresource-function"></a><span data-ttu-id="1e287-103">Função D3DXGetImageInfoFromResource</span><span class="sxs-lookup"><span data-stu-id="1e287-103">D3DXGetImageInfoFromResource function</span></span>

<span data-ttu-id="1e287-104">Recupera informações sobre uma determinada imagem em um recurso.</span><span class="sxs-lookup"><span data-stu-id="1e287-104">Retrieves information about a given image in a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e287-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1e287-105">Syntax</span></span>


```C++
HRESULT D3DXGetImageInfoFromResource(
  _In_ HMODULE        hSrcModule,
  _In_ LPCTSTR        pSrcFile,
  _In_ D3DXIMAGE_INFO *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="1e287-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1e287-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e287-107">*hSrcModule* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1e287-107">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e287-108">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1e287-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1e287-109">Módulo em que o recurso está carregado.</span><span class="sxs-lookup"><span data-stu-id="1e287-109">Module where the resource is loaded.</span></span> <span data-ttu-id="1e287-110">Defina esse parâmetro como **NULL** para especificar o módulo associado à imagem que o sistema operacional usou para criar o processo atual.</span><span class="sxs-lookup"><span data-stu-id="1e287-110">Set this parameter to **NULL** to specify the module associated with the image that the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="1e287-111">*pSrcFile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1e287-111">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e287-112">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1e287-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1e287-113">Ponteiro para uma cadeia de caracteres que especifica o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="1e287-113">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="1e287-114">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="1e287-114">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="1e287-115">Caso contrário, o tipo de dados String será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="1e287-115">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="1e287-116">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="1e287-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="1e287-117">*pSrcInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1e287-117">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e287-118">Tipo: **[ **\_ informações de D3DXIMAGE**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="1e287-118">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="1e287-119">Ponteiro para uma estrutura de [**\_ informações de D3DXIMAGE**](d3dximage-info.md) a ser preenchida com a descrição dos dados no arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="1e287-119">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with the description of the data in the source file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e287-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1e287-120">Return value</span></span>

<span data-ttu-id="1e287-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1e287-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1e287-122">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1e287-122">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1e287-123">Se a função falhar, o valor de retorno poderá ser o seguinte: D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="1e287-123">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="1e287-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="1e287-124">Remarks</span></span>

<span data-ttu-id="1e287-125">A configuração do compilador também determina a versão da função.</span><span class="sxs-lookup"><span data-stu-id="1e287-125">The compiler setting also determines the function version.</span></span> <span data-ttu-id="1e287-126">Se o Unicode for definido, a chamada de função será resolvida como D3DXGetImageInfoFromResourceW.</span><span class="sxs-lookup"><span data-stu-id="1e287-126">If Unicode is defined, the function call resolves to D3DXGetImageInfoFromResourceW.</span></span> <span data-ttu-id="1e287-127">Caso contrário, a chamada de função é resolvida como D3DXGetImageInfoFromResourceA porque as cadeias de caracteres ANSI estão sendo usadas.</span><span class="sxs-lookup"><span data-stu-id="1e287-127">Otherwise, the function call resolves to D3DXGetImageInfoFromResourceA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e287-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e287-128">Requirements</span></span>



| <span data-ttu-id="1e287-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e287-129">Requirement</span></span> | <span data-ttu-id="1e287-130">Valor</span><span class="sxs-lookup"><span data-stu-id="1e287-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1e287-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1e287-131">Header</span></span><br/>  | <dl> <span data-ttu-id="1e287-132"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e287-132"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="1e287-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1e287-133">Library</span></span><br/> | <dl> <span data-ttu-id="1e287-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1e287-134"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="1e287-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="1e287-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e287-136">Funções de textura no D3DX 9</span><span class="sxs-lookup"><span data-stu-id="1e287-136">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="1e287-137">**D3DXGetImageInfoFromFile**</span><span class="sxs-lookup"><span data-stu-id="1e287-137">**D3DXGetImageInfoFromFile**</span></span>](d3dxgetimageinfofromfile.md)
</dt> <dt>

[<span data-ttu-id="1e287-138">**D3DXGetImageInfoFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="1e287-138">**D3DXGetImageInfoFromFileInMemory**</span></span>](d3dxgetimageinfofromfileinmemory.md)
</dt> </dl>

 

 
