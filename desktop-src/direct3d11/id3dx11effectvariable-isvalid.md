---
title: Método IsValid ID3DX11EffectVariable (D3dx11effect. h)
description: Compare o tipo de dados com os dados armazenados.
ms.assetid: 3384afa3-6ae5-4c7c-b95d-4fe3c87cc2fe
keywords:
- Método IsValid Direct3D 11
- Método IsValid Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, método IsValid
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.IsValid
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5136005e675a6f5e54cc3863ef2d80ffadfb7c5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989380"
---
# <a name="id3dx11effectvariableisvalid-method"></a><span data-ttu-id="cc827-106">Método ID3DX11EffectVariable:: IsValid</span><span class="sxs-lookup"><span data-stu-id="cc827-106">ID3DX11EffectVariable::IsValid method</span></span>

<span data-ttu-id="cc827-107">Compare o tipo de dados com os dados armazenados.</span><span class="sxs-lookup"><span data-stu-id="cc827-107">Compare the data type with the data stored.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc827-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cc827-108">Syntax</span></span>


```C++
BOOL IsValid();
```



## <a name="parameters"></a><span data-ttu-id="cc827-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cc827-109">Parameters</span></span>

<span data-ttu-id="cc827-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="cc827-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cc827-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cc827-111">Return value</span></span>

<span data-ttu-id="cc827-112">Tipo: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="cc827-112">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="cc827-113">**True** se a sintaxe for válida; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="cc827-113">**TRUE** if the syntax is valid; otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc827-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="cc827-114">Remarks</span></span>

<span data-ttu-id="cc827-115">Esse método verifica se o tipo de dados corresponde aos dados armazenados após a conversão de uma interface para outra (usando qualquer um dos métodos as).</span><span class="sxs-lookup"><span data-stu-id="cc827-115">This method checks that the data type matches the data stored after casting one interface to another (using any of the As methods).</span></span>

> [!Note]  
> <span data-ttu-id="cc827-116">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="cc827-116">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="cc827-117">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="cc827-117">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="cc827-118">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="cc827-118">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cc827-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc827-119">Requirements</span></span>



| <span data-ttu-id="cc827-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc827-120">Requirement</span></span> | <span data-ttu-id="cc827-121">Valor</span><span class="sxs-lookup"><span data-stu-id="cc827-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc827-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cc827-122">Header</span></span><br/>  | <dl> <span data-ttu-id="cc827-123"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc827-123"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="cc827-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cc827-124">Library</span></span><br/> | <dl> <span data-ttu-id="cc827-125"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="cc827-125"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc827-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="cc827-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc827-127">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="cc827-127">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

