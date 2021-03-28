---
title: Método IsValid ID3DX11Effect (D3dx11effect. h)
description: Teste um efeito para ver se ele contém uma sintaxe válida. | Método IsValid ID3DX11Effect (D3dx11effect. h)
ms.assetid: 42bf0069-1828-4f55-99f5-d0f81eb04336
keywords:
- Método IsValid Direct3D 11
- Método IsValid Direct3D 11, interface ID3DX11Effect
- Interface ID3DX11Effect Direct3D 11, método IsValid
topic_type:
- apiref
api_name:
- ID3DX11Effect.IsValid
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea88aef9e3864fc77380b3459860178c8537a6a5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989368"
---
# <a name="id3dx11effectisvalid-method"></a><span data-ttu-id="46ffe-107">Método ID3DX11Effect:: IsValid</span><span class="sxs-lookup"><span data-stu-id="46ffe-107">ID3DX11Effect::IsValid method</span></span>

<span data-ttu-id="46ffe-108">Teste um efeito para ver se ele contém uma sintaxe válida.</span><span class="sxs-lookup"><span data-stu-id="46ffe-108">Test an effect to see if it contains valid syntax.</span></span>

## <a name="syntax"></a><span data-ttu-id="46ffe-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="46ffe-109">Syntax</span></span>


```C++
BOOL IsValid();
```



## <a name="parameters"></a><span data-ttu-id="46ffe-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="46ffe-110">Parameters</span></span>

<span data-ttu-id="46ffe-111">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="46ffe-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="46ffe-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="46ffe-112">Return value</span></span>

<span data-ttu-id="46ffe-113">Tipo: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="46ffe-113">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="46ffe-114">**True** se a sintaxe do código for válida; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="46ffe-114">**TRUE** if the code syntax is valid; otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="46ffe-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="46ffe-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="46ffe-116">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="46ffe-116">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="46ffe-117">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="46ffe-117">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="46ffe-118">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="46ffe-118">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="46ffe-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46ffe-119">Requirements</span></span>



| <span data-ttu-id="46ffe-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="46ffe-120">Requirement</span></span> | <span data-ttu-id="46ffe-121">Valor</span><span class="sxs-lookup"><span data-stu-id="46ffe-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46ffe-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="46ffe-122">Header</span></span><br/>  | <dl> <span data-ttu-id="46ffe-123"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="46ffe-123"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="46ffe-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="46ffe-124">Library</span></span><br/> | <dl> <span data-ttu-id="46ffe-125"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="46ffe-125"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46ffe-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="46ffe-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46ffe-127">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="46ffe-127">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

