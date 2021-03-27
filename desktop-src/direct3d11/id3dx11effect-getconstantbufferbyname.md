---
title: Método ID3DX11Effect GetConstantBufferByName (D3dx11effect. h)
description: Obtenha um buffer constante por nome.
ms.assetid: 11757615-4068-430d-9ab0-f83f02af8e55
keywords:
- Método GetConstantBufferByName Direct3D 11
- Método GetConstantBufferByName Direct3D 11, interface ID3DX11Effect
- Interface ID3DX11Effect Direct3D 11, método GetConstantBufferByName
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetConstantBufferByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa01d20bfeebfa3f689a58aae5c5face8b879e3c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103837966"
---
# <a name="id3dx11effectgetconstantbufferbyname-method"></a><span data-ttu-id="f36b0-106">Método ID3DX11Effect:: GetConstantBufferByName</span><span class="sxs-lookup"><span data-stu-id="f36b0-106">ID3DX11Effect::GetConstantBufferByName method</span></span>

<span data-ttu-id="f36b0-107">Obtenha um buffer constante por nome.</span><span class="sxs-lookup"><span data-stu-id="f36b0-107">Get a constant buffer by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="f36b0-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f36b0-108">Syntax</span></span>


```C++
ID3DX11EffectConstantBuffer* GetConstantBufferByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="f36b0-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f36b0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f36b0-110">*Nome*</span><span class="sxs-lookup"><span data-stu-id="f36b0-110">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="f36b0-111">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f36b0-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f36b0-112">O nome do buffer de constantes.</span><span class="sxs-lookup"><span data-stu-id="f36b0-112">The constant-buffer name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f36b0-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f36b0-113">Return value</span></span>

<span data-ttu-id="f36b0-114">Tipo: **[ **ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="f36b0-114">Type: **[**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***</span></span>

<span data-ttu-id="f36b0-115">Um ponteiro para o buffer de constantes indicado pelo nome.</span><span class="sxs-lookup"><span data-stu-id="f36b0-115">A pointer to the constant buffer indicated by the Name.</span></span> <span data-ttu-id="f36b0-116">Consulte [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="f36b0-116">See [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f36b0-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="f36b0-117">Remarks</span></span>

<span data-ttu-id="f36b0-118">Um efeito que contém uma variável que será lida/gravada por um aplicativo requer pelo menos um buffer constante.</span><span class="sxs-lookup"><span data-stu-id="f36b0-118">An effect that contains a variable that will be read/written by an application requires at least one constant buffer.</span></span> <span data-ttu-id="f36b0-119">Para obter um melhor desempenho, um efeito deve organizar variáveis em um ou mais buffers constantes com base em sua frequência de atualização.</span><span class="sxs-lookup"><span data-stu-id="f36b0-119">For best performance, an effect should organize variables into one or more constant buffers based on their frequency of update.</span></span>

> [!Note]  
> <span data-ttu-id="f36b0-120">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="f36b0-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="f36b0-121">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="f36b0-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="f36b0-122">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="f36b0-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f36b0-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f36b0-123">Requirements</span></span>



| <span data-ttu-id="f36b0-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f36b0-124">Requirement</span></span> | <span data-ttu-id="f36b0-125">Valor</span><span class="sxs-lookup"><span data-stu-id="f36b0-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f36b0-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f36b0-126">Header</span></span><br/>  | <dl> <span data-ttu-id="f36b0-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="f36b0-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="f36b0-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f36b0-128">Library</span></span><br/> | <dl> <span data-ttu-id="f36b0-129"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="f36b0-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f36b0-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="f36b0-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f36b0-131">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="f36b0-131">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

