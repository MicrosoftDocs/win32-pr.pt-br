---
title: Método ID3DX11EffectVariable GetRawValue (D3dx11effect. h)
description: Obter dados.
ms.assetid: 1b2a319c-880c-4f5a-b4e9-17405351b7d9
keywords:
- Método GetRawValue Direct3D 11
- Método GetRawValue Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, método GetRawValue
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetRawValue
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be03051433e3ae4fd5891d1859529bb305b08bb0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968672"
---
# <a name="id3dx11effectvariablegetrawvalue-method"></a><span data-ttu-id="62016-106">Método ID3DX11EffectVariable:: GetRawValue</span><span class="sxs-lookup"><span data-stu-id="62016-106">ID3DX11EffectVariable::GetRawValue method</span></span>

<span data-ttu-id="62016-107">Obter dados.</span><span class="sxs-lookup"><span data-stu-id="62016-107">Get data.</span></span>

## <a name="syntax"></a><span data-ttu-id="62016-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="62016-108">Syntax</span></span>


```C++
HRESULT GetRawValue(
   void *pData,
   UINT Offset,
   UINT Count
);
```



## <a name="parameters"></a><span data-ttu-id="62016-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="62016-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62016-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="62016-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="62016-111">Tipo: **void \***</span><span class="sxs-lookup"><span data-stu-id="62016-111">Type: **void\***</span></span>

<span data-ttu-id="62016-112">Um ponteiro para a variável.</span><span class="sxs-lookup"><span data-stu-id="62016-112">A pointer to the variable.</span></span>

</dd> <dt>

<span data-ttu-id="62016-113">*Deslocamento*</span><span class="sxs-lookup"><span data-stu-id="62016-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="62016-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="62016-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="62016-115">O deslocamento (em bytes) desde o início do ponteiro até os dados.</span><span class="sxs-lookup"><span data-stu-id="62016-115">The offset (in bytes) from the beginning of the pointer to the data.</span></span>

</dd> <dt>

<span data-ttu-id="62016-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="62016-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="62016-117">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="62016-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="62016-118">O número de bytes a serem obtidos.</span><span class="sxs-lookup"><span data-stu-id="62016-118">The number of bytes to get.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62016-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="62016-119">Return value</span></span>

<span data-ttu-id="62016-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="62016-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="62016-121">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="62016-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="62016-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="62016-122">Remarks</span></span>

<span data-ttu-id="62016-123">Esse método não faz conversão ou verificação de tipo; Portanto, é uma maneira muito rápida de acessar itens de matriz.</span><span class="sxs-lookup"><span data-stu-id="62016-123">This method does no conversion or type checking; it is therefore a very quick way to access array items.</span></span>

> [!Note]  
> <span data-ttu-id="62016-124">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="62016-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="62016-125">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="62016-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="62016-126">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="62016-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="62016-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62016-127">Requirements</span></span>



| <span data-ttu-id="62016-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="62016-128">Requirement</span></span> | <span data-ttu-id="62016-129">Valor</span><span class="sxs-lookup"><span data-stu-id="62016-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62016-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="62016-130">Header</span></span><br/>  | <dl> <span data-ttu-id="62016-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="62016-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="62016-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="62016-132">Library</span></span><br/> | <dl> <span data-ttu-id="62016-133"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="62016-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62016-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="62016-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62016-135">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="62016-135">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

