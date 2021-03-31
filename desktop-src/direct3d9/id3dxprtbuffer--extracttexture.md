---
description: Extrai dados de coeficiente de um canal de cor do buffer para um intervalo especificado de coeficientes e adiciona os dados a um objeto IDirect3DTexture9.
ms.assetid: 75854676-706a-4675-857e-4f2f8fc8365b
title: 'Método ID3DXPRTBuffer:: ExtractTexture (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.ExtractTexture
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2ea6cfdc8fb6ec83f847ccf37d06972974ea4de8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930644"
---
# <a name="id3dxprtbufferextracttexture-method"></a><span data-ttu-id="15d83-103">Método ID3DXPRTBuffer:: ExtractTexture</span><span class="sxs-lookup"><span data-stu-id="15d83-103">ID3DXPRTBuffer::ExtractTexture method</span></span>

<span data-ttu-id="15d83-104">Extrai dados de coeficiente de um canal de cor do buffer para um intervalo especificado de coeficientes e adiciona os dados a um objeto [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) .</span><span class="sxs-lookup"><span data-stu-id="15d83-104">Extracts coefficient data from a color channel of the buffer for a specified range of coefficients, and adds the data to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="15d83-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="15d83-105">Syntax</span></span>


```C++
HRESULT ExtractTexture(
  [in] UINT               Channel,
  [in] UINT               StartCoefficient,
  [in] UINT               NumCoefficients,
  [in] LPDIRECT3DTEXTURE9 pTexture
);
```



## <a name="parameters"></a><span data-ttu-id="15d83-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="15d83-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15d83-107">*Canal* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="15d83-107">*Channel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15d83-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="15d83-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="15d83-109">Canal de cores do buffer do qual extrair dados de textura.</span><span class="sxs-lookup"><span data-stu-id="15d83-109">Buffer color channel from which to extract texture data.</span></span>

</dd> <dt>

<span data-ttu-id="15d83-110">*StartCoefficient* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="15d83-110">*StartCoefficient* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15d83-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="15d83-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="15d83-112">Valor inicial do coeficiente de buffer do qual extrair dados de textura.</span><span class="sxs-lookup"><span data-stu-id="15d83-112">Starting value of the buffer coefficient from which to extract texture data.</span></span>

</dd> <dt>

<span data-ttu-id="15d83-113">*NumCoefficients* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="15d83-113">*NumCoefficients* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15d83-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="15d83-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="15d83-115">Número de escalares, começando em StartCoefficient, do qual extrair dados de textura.</span><span class="sxs-lookup"><span data-stu-id="15d83-115">Number of scalars, beginning at StartCoefficient, from which to extract texture data.</span></span>

</dd> <dt>

<span data-ttu-id="15d83-116">*pTexture* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="15d83-116">*pTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15d83-117">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="15d83-117">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="15d83-118">Ponteiro para um objeto de textura [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) que armazenará coeficientes.</span><span class="sxs-lookup"><span data-stu-id="15d83-118">Pointer to a [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) texture object that will store coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15d83-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="15d83-119">Return value</span></span>

<span data-ttu-id="15d83-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="15d83-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="15d83-121">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="15d83-121">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="15d83-122">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="15d83-122">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="15d83-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15d83-123">Requirements</span></span>



| <span data-ttu-id="15d83-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="15d83-124">Requirement</span></span> | <span data-ttu-id="15d83-125">Valor</span><span class="sxs-lookup"><span data-stu-id="15d83-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="15d83-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="15d83-126">Header</span></span><br/>  | <dl> <span data-ttu-id="15d83-127"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="15d83-127"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="15d83-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="15d83-128">Library</span></span><br/> | <dl> <span data-ttu-id="15d83-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="15d83-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="15d83-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="15d83-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15d83-131">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="15d83-131">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> </dl>

 

 
