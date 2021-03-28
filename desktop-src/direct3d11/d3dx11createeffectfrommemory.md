---
title: Função D3DX11CreateEffectFromMemory (D3dx11effect. h)
description: Cria um efeito de um arquivo ou efeito binário.
ms.assetid: 4aa65efb-4c6b-4faf-b48f-01329bdff6cd
keywords:
- Função D3DX11CreateEffectFromMemory Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateEffectFromMemory
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 467d2094a7124b96a08c7bab6d7a4209deee9996
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989341"
---
# <a name="d3dx11createeffectfrommemory-function"></a><span data-ttu-id="ada63-104">Função D3DX11CreateEffectFromMemory</span><span class="sxs-lookup"><span data-stu-id="ada63-104">D3DX11CreateEffectFromMemory function</span></span>

<span data-ttu-id="ada63-105">Cria um efeito de um arquivo ou efeito binário.</span><span class="sxs-lookup"><span data-stu-id="ada63-105">Creates an effect from a binary effect or file.</span></span>

## <a name="syntax"></a><span data-ttu-id="ada63-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ada63-106">Syntax</span></span>


```C++
HRESULT D3DX11CreateEffectFromMemory(
   void          *pData,
   SIZE_T        DataLength,
   UINT          FXFlags,
   ID3D11Device  *pDevice,
   ID3DX11Effect **ppEffect
);
```



## <a name="parameters"></a><span data-ttu-id="ada63-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ada63-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ada63-108">*pData*</span><span class="sxs-lookup"><span data-stu-id="ada63-108">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="ada63-109">Tipo: **void \***</span><span class="sxs-lookup"><span data-stu-id="ada63-109">Type: **void\***</span></span>

<span data-ttu-id="ada63-110">Blob de dados de efeito compilados.</span><span class="sxs-lookup"><span data-stu-id="ada63-110">Blob of compiled effect data.</span></span>

</dd> <dt>

<span data-ttu-id="ada63-111">*DataLength*</span><span class="sxs-lookup"><span data-stu-id="ada63-111">*DataLength*</span></span> 
</dt> <dd>

<span data-ttu-id="ada63-112">Tipo: **[ **tamanho \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ada63-112">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ada63-113">Comprimento do blob de dados.</span><span class="sxs-lookup"><span data-stu-id="ada63-113">Length of the data blob.</span></span>

</dd> <dt>

<span data-ttu-id="ada63-114">*FXFlags*</span><span class="sxs-lookup"><span data-stu-id="ada63-114">*FXFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="ada63-115">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ada63-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ada63-116">Não existem sinalizadores de efeito.</span><span class="sxs-lookup"><span data-stu-id="ada63-116">No effect flags exist.</span></span> <span data-ttu-id="ada63-117">Definido como zero.</span><span class="sxs-lookup"><span data-stu-id="ada63-117">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="ada63-118">*pDevice*</span><span class="sxs-lookup"><span data-stu-id="ada63-118">*pDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="ada63-119">Tipo: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span><span class="sxs-lookup"><span data-stu-id="ada63-119">Type: **[**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span></span>

<span data-ttu-id="ada63-120">Ponteiro para o [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) no qual criar recursos de efeito.</span><span class="sxs-lookup"><span data-stu-id="ada63-120">Pointer to the [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) on which to create Effect resources.</span></span>

</dd> <dt>

<span data-ttu-id="ada63-121">*ppEffect*</span><span class="sxs-lookup"><span data-stu-id="ada63-121">*ppEffect*</span></span> 
</dt> <dd>

<span data-ttu-id="ada63-122">Tipo: **[ **ID3DX11Effect**](id3dx11effect.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="ada63-122">Type: **[**ID3DX11Effect**](id3dx11effect.md)\*\***</span></span>

<span data-ttu-id="ada63-123">Endereço da interface [**ID3DX11Effect**](id3dx11effect.md) recém-criada.</span><span class="sxs-lookup"><span data-stu-id="ada63-123">Address of the newly created [**ID3DX11Effect**](id3dx11effect.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ada63-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ada63-124">Return value</span></span>

<span data-ttu-id="ada63-125">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ada63-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ada63-126">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="ada63-126">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ada63-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="ada63-127">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ada63-128">Você deve usar a [fonte Effects 11](https://github.com/Microsoft/FX11) para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="ada63-128">You must use [Effects 11 source](https://github.com/Microsoft/FX11) to build your effects-type application.</span></span> <span data-ttu-id="ada63-129">Para obter mais informações sobre como usar a fonte de efeitos 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="ada63-129">For more info about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ada63-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ada63-130">Requirements</span></span>



| <span data-ttu-id="ada63-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="ada63-131">Requirement</span></span> | <span data-ttu-id="ada63-132">Valor</span><span class="sxs-lookup"><span data-stu-id="ada63-132">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ada63-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ada63-133">Header</span></span><br/> | <dl> <span data-ttu-id="ada63-134"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="ada63-134"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ada63-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="ada63-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ada63-136">Funções do Effects 11</span><span class="sxs-lookup"><span data-stu-id="ada63-136">Effects 11 Functions</span></span>](d3d11-graphics-reference-effects11-functions.md)
</dt> </dl>

 

