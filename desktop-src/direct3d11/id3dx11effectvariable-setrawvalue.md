---
title: Método ID3DX11EffectVariable SetRawValue (D3dx11effect. h)
description: Definir dados.
ms.assetid: c5d53aa6-6cd8-4a93-9851-2a93bc6a728a
keywords:
- Método SetRawValue Direct3D 11
- Método SetRawValue Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, método SetRawValue
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.SetRawValue
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b5186e55b8b1d3472cb25ea6fa067988d4fb1f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104172932"
---
# <a name="id3dx11effectvariablesetrawvalue-method"></a><span data-ttu-id="de265-106">Método ID3DX11EffectVariable:: SetRawValue</span><span class="sxs-lookup"><span data-stu-id="de265-106">ID3DX11EffectVariable::SetRawValue method</span></span>

<span data-ttu-id="de265-107">Definir dados.</span><span class="sxs-lookup"><span data-stu-id="de265-107">Set data.</span></span>

## <a name="syntax"></a><span data-ttu-id="de265-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="de265-108">Syntax</span></span>


```C++
HRESULT SetRawValue(
   void *pData,
   UINT Offset,
   UINT Count
);
```



## <a name="parameters"></a><span data-ttu-id="de265-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="de265-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de265-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="de265-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="de265-111">Tipo: **void \***</span><span class="sxs-lookup"><span data-stu-id="de265-111">Type: **void\***</span></span>

<span data-ttu-id="de265-112">Um ponteiro para a variável.</span><span class="sxs-lookup"><span data-stu-id="de265-112">A pointer to the variable.</span></span>

</dd> <dt>

<span data-ttu-id="de265-113">*Deslocamento*</span><span class="sxs-lookup"><span data-stu-id="de265-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="de265-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="de265-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="de265-115">O deslocamento (em bytes) desde o início do ponteiro até os dados.</span><span class="sxs-lookup"><span data-stu-id="de265-115">The offset (in bytes) from the beginning of the pointer to the data.</span></span>

</dd> <dt>

<span data-ttu-id="de265-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="de265-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="de265-117">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="de265-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="de265-118">O número de bytes a serem definidos.</span><span class="sxs-lookup"><span data-stu-id="de265-118">The number of bytes to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de265-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="de265-119">Return value</span></span>

<span data-ttu-id="de265-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="de265-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="de265-121">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="de265-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="de265-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="de265-122">Remarks</span></span>

<span data-ttu-id="de265-123">Esse método não faz conversão ou verificação de tipo; Portanto, é uma maneira muito rápida de acessar itens de matriz.</span><span class="sxs-lookup"><span data-stu-id="de265-123">This method does no conversion or type checking; it is therefore a very quick way to access array items.</span></span>

> [!Note]  
> <span data-ttu-id="de265-124">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="de265-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="de265-125">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="de265-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="de265-126">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="de265-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="de265-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de265-127">Requirements</span></span>



| <span data-ttu-id="de265-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="de265-128">Requirement</span></span> | <span data-ttu-id="de265-129">Valor</span><span class="sxs-lookup"><span data-stu-id="de265-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de265-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="de265-130">Header</span></span><br/>  | <dl> <span data-ttu-id="de265-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="de265-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="de265-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="de265-132">Library</span></span><br/> | <dl> <span data-ttu-id="de265-133"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="de265-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de265-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="de265-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de265-135">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="de265-135">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

