---
title: Método ID3DX11Effect GetVariableByName (D3dx11effect. h)
description: Obter uma variável por nome.
ms.assetid: d20c5a85-51a5-482f-b5b0-197d8e993910
keywords:
- Método GetVariableByName Direct3D 11
- Método GetVariableByName Direct3D 11, interface ID3DX11Effect
- Interface ID3DX11Effect Direct3D 11, método GetVariableByName
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetVariableByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e6079e7f45c21d9d7326021b2c439ab12e4e031
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989369"
---
# <a name="id3dx11effectgetvariablebyname-method"></a><span data-ttu-id="cba28-106">Método ID3DX11Effect:: GetVariableByName</span><span class="sxs-lookup"><span data-stu-id="cba28-106">ID3DX11Effect::GetVariableByName method</span></span>

<span data-ttu-id="cba28-107">Obter uma variável por nome.</span><span class="sxs-lookup"><span data-stu-id="cba28-107">Get a variable by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="cba28-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cba28-108">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetVariableByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="cba28-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cba28-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cba28-110">*Nome*</span><span class="sxs-lookup"><span data-stu-id="cba28-110">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="cba28-111">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="cba28-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="cba28-112">O nome da variável.</span><span class="sxs-lookup"><span data-stu-id="cba28-112">The variable name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cba28-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cba28-113">Return value</span></span>

<span data-ttu-id="cba28-114">Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="cba28-114">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="cba28-115">Um ponteiro para um [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="cba28-115">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="cba28-116">Retorna uma variável inválida se o nome especificado não puder ser encontrado.</span><span class="sxs-lookup"><span data-stu-id="cba28-116">Returns an invalid variable if the specified name cannot be found.</span></span>

## <a name="remarks"></a><span data-ttu-id="cba28-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="cba28-117">Remarks</span></span>

<span data-ttu-id="cba28-118">Um efeito pode conter uma ou mais variáveis.</span><span class="sxs-lookup"><span data-stu-id="cba28-118">An effect may contain one or more variables.</span></span> <span data-ttu-id="cba28-119">Variáveis fora de uma técnica são consideradas globais para todos os efeitos, aquelas localizadas dentro de uma técnica são locais para essa técnica.</span><span class="sxs-lookup"><span data-stu-id="cba28-119">Variables outside of a technique are considered global to all effects, those located inside of a technique are local to that technique.</span></span> <span data-ttu-id="cba28-120">Você pode acessar uma variável de efeito usando seu nome ou com um índice.</span><span class="sxs-lookup"><span data-stu-id="cba28-120">You can access an effect variable using its name or with an index.</span></span>

<span data-ttu-id="cba28-121">O método retorna um ponteiro para uma [**interface de variável de efeito,**](id3dx11effectvariable.md) independentemente de uma variável ser ou não encontrada.</span><span class="sxs-lookup"><span data-stu-id="cba28-121">The method returns a pointer to an [**effect-variable interface**](id3dx11effectvariable.md) whether or not a variable is found.</span></span> <span data-ttu-id="cba28-122">[**ID3DX11Effect:: IsValid**](id3dx11effect-isvalid.md) deve ser chamado para verificar se o nome existe ou não.</span><span class="sxs-lookup"><span data-stu-id="cba28-122">[**ID3DX11Effect::IsValid**](id3dx11effect-isvalid.md) should be called to verify whether or not the name exists.</span></span>

> [!Note]  
> <span data-ttu-id="cba28-123">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="cba28-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="cba28-124">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="cba28-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="cba28-125">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="cba28-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cba28-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cba28-126">Requirements</span></span>



| <span data-ttu-id="cba28-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="cba28-127">Requirement</span></span> | <span data-ttu-id="cba28-128">Valor</span><span class="sxs-lookup"><span data-stu-id="cba28-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cba28-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cba28-129">Header</span></span><br/>  | <dl> <span data-ttu-id="cba28-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="cba28-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="cba28-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cba28-131">Library</span></span><br/> | <dl> <span data-ttu-id="cba28-132"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="cba28-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cba28-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="cba28-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cba28-134">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="cba28-134">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

