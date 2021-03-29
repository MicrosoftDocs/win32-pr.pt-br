---
title: Método setbool ID3DX11EffectScalarVariable (D3dx11effect. h)
description: Defina uma variável booliana.
ms.assetid: b5385ed3-6e65-4d65-bb8e-835967e6f610
keywords:
- Método setbool Direct3D 11
- Método setbool Direct3D 11, interface ID3DX11EffectScalarVariable
- Interface ID3DX11EffectScalarVariable Direct3D 11, método setbool
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.SetBool
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e1d3670b3a41f47bf1b5ec7ac3d2fb93441e72f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968652"
---
# <a name="id3dx11effectscalarvariablesetbool-method"></a><span data-ttu-id="65653-106">Método ID3DX11EffectScalarVariable:: setbool</span><span class="sxs-lookup"><span data-stu-id="65653-106">ID3DX11EffectScalarVariable::SetBool method</span></span>

<span data-ttu-id="65653-107">Defina uma variável booliana.</span><span class="sxs-lookup"><span data-stu-id="65653-107">Set a boolean variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="65653-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="65653-108">Syntax</span></span>


```C++
HRESULT SetBool(
   BOOL Value
);
```



## <a name="parameters"></a><span data-ttu-id="65653-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="65653-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65653-110">*Valor*</span><span class="sxs-lookup"><span data-stu-id="65653-110">*Value*</span></span> 
</dt> <dd>

<span data-ttu-id="65653-111">Tipo: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="65653-111">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="65653-112">Um ponteiro para a variável.</span><span class="sxs-lookup"><span data-stu-id="65653-112">A pointer to the variable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65653-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="65653-113">Return value</span></span>

<span data-ttu-id="65653-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="65653-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="65653-115">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="65653-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="65653-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="65653-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="65653-117">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="65653-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="65653-118">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="65653-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="65653-119">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="65653-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="65653-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65653-120">Requirements</span></span>



| <span data-ttu-id="65653-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="65653-121">Requirement</span></span> | <span data-ttu-id="65653-122">Valor</span><span class="sxs-lookup"><span data-stu-id="65653-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65653-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="65653-123">Header</span></span><br/>  | <dl> <span data-ttu-id="65653-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="65653-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="65653-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="65653-125">Library</span></span><br/> | <dl> <span data-ttu-id="65653-126"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="65653-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65653-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="65653-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65653-128">ID3DX11EffectScalarVariable</span><span class="sxs-lookup"><span data-stu-id="65653-128">ID3DX11EffectScalarVariable</span></span>](id3dx11effectscalarvariable.md)
</dt> </dl>

 

