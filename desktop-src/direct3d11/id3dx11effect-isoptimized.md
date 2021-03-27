---
title: Método isoptimized ID3DX11Effect (D3dx11effect. h)
description: Teste um efeito para ver se os metadados de reflexão foram removidos da memória.
ms.assetid: fb0a876b-7419-45b7-97fe-8352dd97d8c5
keywords:
- Método isoptimized Direct3D 11
- Método isoptimized Direct3D 11, interface ID3DX11Effect
- Interface ID3DX11Effect Direct3D 11, método isoptimized
topic_type:
- apiref
api_name:
- ID3DX11Effect.IsOptimized
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18be8901a58715e3bd8aaaa49ae40be07e7e9dc8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298757"
---
# <a name="id3dx11effectisoptimized-method"></a><span data-ttu-id="5920b-106">Método ID3DX11Effect:: isoptimized</span><span class="sxs-lookup"><span data-stu-id="5920b-106">ID3DX11Effect::IsOptimized method</span></span>

<span data-ttu-id="5920b-107">Teste um efeito para ver se os metadados de reflexão foram removidos da memória.</span><span class="sxs-lookup"><span data-stu-id="5920b-107">Test an effect to see if the reflection metadata has been removed from memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="5920b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5920b-108">Syntax</span></span>


```C++
BOOL IsOptimized();
```



## <a name="parameters"></a><span data-ttu-id="5920b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5920b-109">Parameters</span></span>

<span data-ttu-id="5920b-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="5920b-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5920b-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5920b-111">Return value</span></span>

<span data-ttu-id="5920b-112">Tipo: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="5920b-112">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="5920b-113">**True** se o efeito for otimizado; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="5920b-113">**TRUE** if the effect is optimized; otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5920b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="5920b-114">Remarks</span></span>

<span data-ttu-id="5920b-115">Um efeito usa o espaço de memória de duas maneiras diferentes: armazenar as informações exigidas pelo tempo de execução para executar um efeito e armazenar os metadados necessários para refletir informações de volta para um aplicativo usando a API.</span><span class="sxs-lookup"><span data-stu-id="5920b-115">An effect uses memory space two different ways: to store the information required by the runtime to execute an effect, and to store the metadata required to reflect information back to an application using the API.</span></span> <span data-ttu-id="5920b-116">Você pode minimizar a quantidade de memória exigida por um efeito chamando [**ID3DX11Effect:: Optimize**](id3dx11effect-optimize.md) , que remove os metadados de reflexão da memória.</span><span class="sxs-lookup"><span data-stu-id="5920b-116">You can minimize the amount of memory required by an effect by calling [**ID3DX11Effect::Optimize**](id3dx11effect-optimize.md) which removes the reflection metadata from memory.</span></span> <span data-ttu-id="5920b-117">É claro que os métodos de API para ler variáveis não funcionarão mais quando os dados de reflexão tiverem sido removidos.</span><span class="sxs-lookup"><span data-stu-id="5920b-117">Of course, API methods to read variables will no longer work once reflection data has been removed.</span></span>

> [!Note]  
> <span data-ttu-id="5920b-118">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="5920b-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="5920b-119">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="5920b-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="5920b-120">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="5920b-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5920b-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5920b-121">Requirements</span></span>



| <span data-ttu-id="5920b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5920b-122">Requirement</span></span> | <span data-ttu-id="5920b-123">Valor</span><span class="sxs-lookup"><span data-stu-id="5920b-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5920b-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5920b-124">Header</span></span><br/>  | <dl> <span data-ttu-id="5920b-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="5920b-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="5920b-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5920b-126">Library</span></span><br/> | <dl> <span data-ttu-id="5920b-127"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="5920b-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5920b-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="5920b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5920b-129">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="5920b-129">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

