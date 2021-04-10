---
description: Extrai os coeficientes de projeção do PCA (análise de componente principal) por exemplo de um buffer de dados compactado ID3DXPRTCompBuffer e adiciona os dados a um objeto IDirect3DTexture9.
ms.assetid: 2159e57d-b8e5-421f-b20a-ac58b29e3c45
title: 'Método ID3DXPRTCompBuffer:: ExtractTexture (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractTexture
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a6a2200c680c19019375a5e33d2d8b675992dc38
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012122"
---
# <a name="id3dxprtcompbufferextracttexture-method"></a><span data-ttu-id="9eec1-103">Método ID3DXPRTCompBuffer:: ExtractTexture</span><span class="sxs-lookup"><span data-stu-id="9eec1-103">ID3DXPRTCompBuffer::ExtractTexture method</span></span>

<span data-ttu-id="9eec1-104">Extrai os coeficientes de projeção do PCA (análise de componente principal) por exemplo de um buffer de dados compactado [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) e adiciona os dados a um objeto [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) .</span><span class="sxs-lookup"><span data-stu-id="9eec1-104">Extracts the per-sample principal component analysis (PCA) projection coefficients from an [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) compressed data buffer and adds the data to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9eec1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9eec1-105">Syntax</span></span>


```C++
HRESULT ExtractTexture(
  [in] UINT               StartPCA,
  [in] UINT               NumPCA,
  [in] LPDIRECT3DTEXTURE9 pTexture
);
```



## <a name="parameters"></a><span data-ttu-id="9eec1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9eec1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9eec1-107">*StartPCA* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9eec1-107">*StartPCA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9eec1-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9eec1-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9eec1-109">Valor inicial do coeficiente de buffer do qual extrair dados de textura.</span><span class="sxs-lookup"><span data-stu-id="9eec1-109">Starting value of the buffer coefficient from which to extract texture data.</span></span>

</dd> <dt>

<span data-ttu-id="9eec1-110">*NumPCA* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9eec1-110">*NumPCA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9eec1-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9eec1-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9eec1-112">Número de coeficientes do PCA a serem extraídos do buffer.</span><span class="sxs-lookup"><span data-stu-id="9eec1-112">Number of PCA coefficients to extract from the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="9eec1-113">*pTexture* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9eec1-113">*pTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9eec1-114">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="9eec1-114">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="9eec1-115">Ponteiro para um objeto de textura [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) que armazenará os coeficientes do PCA.</span><span class="sxs-lookup"><span data-stu-id="9eec1-115">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) texture object that will store PCA coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9eec1-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9eec1-116">Return value</span></span>

<span data-ttu-id="9eec1-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9eec1-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9eec1-118">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9eec1-118">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="9eec1-119">Se o método falhar, o valor a seguir será retornado.</span><span class="sxs-lookup"><span data-stu-id="9eec1-119">If the method fails, the following value will be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="9eec1-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9eec1-120">Requirements</span></span>



| <span data-ttu-id="9eec1-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="9eec1-121">Requirement</span></span> | <span data-ttu-id="9eec1-122">Valor</span><span class="sxs-lookup"><span data-stu-id="9eec1-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9eec1-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9eec1-123">Header</span></span><br/>  | <dl> <span data-ttu-id="9eec1-124"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="9eec1-124"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="9eec1-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9eec1-125">Library</span></span><br/> | <dl> <span data-ttu-id="9eec1-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9eec1-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9eec1-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="9eec1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9eec1-128">ID3DXPRTCompBuffer</span><span class="sxs-lookup"><span data-stu-id="9eec1-128">ID3DXPRTCompBuffer</span></span>](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
