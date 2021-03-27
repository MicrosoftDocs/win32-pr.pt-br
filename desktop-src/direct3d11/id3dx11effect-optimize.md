---
title: Método ID3DX11Effect Optimize (D3dx11effect. h)
description: Minimize a quantidade de memória necessária para um efeito.
ms.assetid: fa1d0769-6746-44f6-9979-31a534646884
keywords:
- Otimizar o método Direct3D 11
- Otimizar método Direct3D 11, interface ID3DX11Effect
- Interface ID3DX11Effect Direct3D 11, método Optimize
topic_type:
- apiref
api_name:
- ID3DX11Effect.Optimize
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33fd6d200f6b22af46e648040e8299f40ec9ebae
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989367"
---
# <a name="id3dx11effectoptimize-method"></a><span data-ttu-id="f8f40-106">Método ID3DX11Effect:: Optimize</span><span class="sxs-lookup"><span data-stu-id="f8f40-106">ID3DX11Effect::Optimize method</span></span>

<span data-ttu-id="f8f40-107">Minimize a quantidade de memória necessária para um efeito.</span><span class="sxs-lookup"><span data-stu-id="f8f40-107">Minimize the amount of memory required for an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8f40-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f8f40-108">Syntax</span></span>


```C++
HRESULT Optimize();
```



## <a name="parameters"></a><span data-ttu-id="f8f40-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f8f40-109">Parameters</span></span>

<span data-ttu-id="f8f40-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="f8f40-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f8f40-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f8f40-111">Return value</span></span>

<span data-ttu-id="f8f40-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f8f40-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f8f40-113">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="f8f40-113">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f8f40-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="f8f40-114">Remarks</span></span>

<span data-ttu-id="f8f40-115">Um efeito usa o espaço de memória de duas maneiras diferentes: armazenar as informações exigidas pelo tempo de execução para executar um efeito e armazenar os metadados necessários para refletir informações de volta para um aplicativo usando a API.</span><span class="sxs-lookup"><span data-stu-id="f8f40-115">An effect uses memory space two different ways: to store the information required by the runtime to execute an effect, and to store the metadata required to reflect information back to an application using the API.</span></span> <span data-ttu-id="f8f40-116">Você pode minimizar a quantidade de memória exigida por um efeito chamando **ID3DX11Effect:: Optimize** , que remove os metadados de reflexão da memória.</span><span class="sxs-lookup"><span data-stu-id="f8f40-116">You can minimize the amount of memory required by an effect by calling **ID3DX11Effect::Optimize** which removes the reflection metadata from memory.</span></span> <span data-ttu-id="f8f40-117">Os métodos de API para ler variáveis não funcionarão mais quando os dados de reflexão tiverem sido removidos.</span><span class="sxs-lookup"><span data-stu-id="f8f40-117">API methods to read variables will no longer work once reflection data has been removed.</span></span>

<span data-ttu-id="f8f40-118">Os métodos a seguir falharão depois que optimize for chamado em um efeito.</span><span class="sxs-lookup"><span data-stu-id="f8f40-118">The following methods will fail after Optimize has been called on an effect.</span></span>

-   [<span data-ttu-id="f8f40-119">**ID3DX11Effect::GetConstantBufferByIndex**</span><span class="sxs-lookup"><span data-stu-id="f8f40-119">**ID3DX11Effect::GetConstantBufferByIndex**</span></span>](id3dx11effect-getconstantbufferbyindex.md)
-   [<span data-ttu-id="f8f40-120">**ID3DX11Effect::GetConstantBufferByName**</span><span class="sxs-lookup"><span data-stu-id="f8f40-120">**ID3DX11Effect::GetConstantBufferByName**</span></span>](id3dx11effect-getconstantbufferbyname.md)
-   [<span data-ttu-id="f8f40-121">**ID3DX11Effect:: GetDesc**</span><span class="sxs-lookup"><span data-stu-id="f8f40-121">**ID3DX11Effect::GetDesc**</span></span>](id3dx11effect-getdesc.md)
-   [<span data-ttu-id="f8f40-122">**ID3DX11Effect:: GetDevice**</span><span class="sxs-lookup"><span data-stu-id="f8f40-122">**ID3DX11Effect::GetDevice**</span></span>](id3dx11effect-getdevice.md)
-   [<span data-ttu-id="f8f40-123">**ID3DX11Effect::GetTechniqueByIndex**</span><span class="sxs-lookup"><span data-stu-id="f8f40-123">**ID3DX11Effect::GetTechniqueByIndex**</span></span>](id3dx11effect-gettechniquebyindex.md)
-   [<span data-ttu-id="f8f40-124">**ID3DX11Effect::GetTechniqueByName**</span><span class="sxs-lookup"><span data-stu-id="f8f40-124">**ID3DX11Effect::GetTechniqueByName**</span></span>](id3dx11effect-gettechniquebyname.md)
-   [<span data-ttu-id="f8f40-125">**ID3DX11Effect::GetVariableByIndex**</span><span class="sxs-lookup"><span data-stu-id="f8f40-125">**ID3DX11Effect::GetVariableByIndex**</span></span>](id3dx11effect-getvariablebyindex.md)
-   [<span data-ttu-id="f8f40-126">**ID3DX11Effect::GetVariableByName**</span><span class="sxs-lookup"><span data-stu-id="f8f40-126">**ID3DX11Effect::GetVariableByName**</span></span>](id3dx11effect-getvariablebyname.md)
-   [<span data-ttu-id="f8f40-127">**ID3DX11Effect::GetVariableBySemantic**</span><span class="sxs-lookup"><span data-stu-id="f8f40-127">**ID3DX11Effect::GetVariableBySemantic**</span></span>](id3dx11effect-getvariablebysemantic.md)

> [!Note]  
> <span data-ttu-id="f8f40-128">As referências recuperadas com esses métodos antes de chamar **ID3DX11Effect:: Optimize** ainda são válidas após **ID3DX11Effect:: Optimize** ser chamado.</span><span class="sxs-lookup"><span data-stu-id="f8f40-128">References retrieved with these methods before calling **ID3DX11Effect::Optimize** are still valid after **ID3DX11Effect::Optimize** is called.</span></span> <span data-ttu-id="f8f40-129">Isso permite que o aplicativo obtenha todas as variáveis, técnicas e passes que usará, chame optimize e, em seguida, use o efeito.</span><span class="sxs-lookup"><span data-stu-id="f8f40-129">This allows the application to get all the variables, techniques, and passes it will use, call Optimize, and then use the effect.</span></span>

 

> [!Note]  
> <span data-ttu-id="f8f40-130">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="f8f40-130">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="f8f40-131">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="f8f40-131">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="f8f40-132">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="f8f40-132">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f8f40-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8f40-133">Requirements</span></span>



| <span data-ttu-id="f8f40-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8f40-134">Requirement</span></span> | <span data-ttu-id="f8f40-135">Valor</span><span class="sxs-lookup"><span data-stu-id="f8f40-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8f40-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f8f40-136">Header</span></span><br/>  | <dl> <span data-ttu-id="f8f40-137"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8f40-137"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="f8f40-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f8f40-138">Library</span></span><br/> | <dl> <span data-ttu-id="f8f40-139"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="f8f40-139"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8f40-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="f8f40-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8f40-141">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="f8f40-141">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

 





