---
title: Método ID3DX11Effect GetConstantBufferByIndex (D3dx11effect. h)
description: Obtenha um buffer constante por índice.
ms.assetid: 146b146b-89ff-4d56-9ac7-e67a92a30e26
keywords:
- Método GetConstantBufferByIndex Direct3D 11
- Método GetConstantBufferByIndex Direct3D 11, interface ID3DX11Effect
- Interface ID3DX11Effect Direct3D 11, método GetConstantBufferByIndex
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetConstantBufferByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfbc44b2d9ceea1bcfbf854a8d3c6998d03e3eec
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968656"
---
# <a name="id3dx11effectgetconstantbufferbyindex-method"></a><span data-ttu-id="c68be-106">Método ID3DX11Effect:: GetConstantBufferByIndex</span><span class="sxs-lookup"><span data-stu-id="c68be-106">ID3DX11Effect::GetConstantBufferByIndex method</span></span>

<span data-ttu-id="c68be-107">Obtenha um buffer constante por índice.</span><span class="sxs-lookup"><span data-stu-id="c68be-107">Get a constant buffer by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="c68be-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c68be-108">Syntax</span></span>


```C++
ID3DX11EffectConstantBuffer* GetConstantBufferByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="c68be-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c68be-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c68be-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="c68be-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="c68be-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c68be-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c68be-112">Um índice de base zero.</span><span class="sxs-lookup"><span data-stu-id="c68be-112">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c68be-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c68be-113">Return value</span></span>

<span data-ttu-id="c68be-114">Tipo: **[ **ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="c68be-114">Type: **[**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***</span></span>

<span data-ttu-id="c68be-115">Um ponteiro para um [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="c68be-115">A pointer to a [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c68be-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="c68be-116">Remarks</span></span>

<span data-ttu-id="c68be-117">Um efeito que contém uma variável que será lida/gravada por um aplicativo requer pelo menos um buffer constante.</span><span class="sxs-lookup"><span data-stu-id="c68be-117">An effect that contains a variable that will be read/written by an application requires at least one constant buffer.</span></span> <span data-ttu-id="c68be-118">Para obter um melhor desempenho, um efeito deve organizar variáveis em um ou mais buffers constantes com base em sua frequência de atualização.</span><span class="sxs-lookup"><span data-stu-id="c68be-118">For best performance, an effect should organize variables into one or more constant buffers based on their frequency of update.</span></span>

> [!Note]  
> <span data-ttu-id="c68be-119">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="c68be-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="c68be-120">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="c68be-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="c68be-121">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="c68be-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c68be-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c68be-122">Requirements</span></span>



| <span data-ttu-id="c68be-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c68be-123">Requirement</span></span> | <span data-ttu-id="c68be-124">Valor</span><span class="sxs-lookup"><span data-stu-id="c68be-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c68be-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c68be-125">Header</span></span><br/>  | <dl> <span data-ttu-id="c68be-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c68be-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="c68be-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c68be-127">Library</span></span><br/> | <dl> <span data-ttu-id="c68be-128"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="c68be-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c68be-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="c68be-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c68be-130">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="c68be-130">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

