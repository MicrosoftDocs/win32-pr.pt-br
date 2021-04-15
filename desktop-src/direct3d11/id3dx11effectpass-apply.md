---
title: Método ID3DX11EffectPass Apply (D3dx11effect. h)
description: Defina o estado contido em uma passagem para o dispositivo.
ms.assetid: d67fe968-bfb2-4f3a-b393-3f72f680211f
keywords:
- Aplicar o método Direct3D 11
- Aplicar o método Direct3D 11, interface ID3DX11EffectPass
- Interface ID3DX11EffectPass Direct3D 11, método Apply
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.Apply
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a061609953e164524e16722222a5ecea81f275b3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968598"
---
# <a name="id3dx11effectpassapply-method"></a><span data-ttu-id="4df93-106">Método ID3DX11EffectPass:: apply</span><span class="sxs-lookup"><span data-stu-id="4df93-106">ID3DX11EffectPass::Apply method</span></span>

<span data-ttu-id="4df93-107">Defina o estado contido em uma passagem para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4df93-107">Set the state contained in a pass to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="4df93-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4df93-108">Syntax</span></span>


```C++
HRESULT Apply(
   UINT                Flags,
   ID3D11DeviceContext *pContext
);
```



## <a name="parameters"></a><span data-ttu-id="4df93-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4df93-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4df93-110">*Sinalizadores*</span><span class="sxs-lookup"><span data-stu-id="4df93-110">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="4df93-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4df93-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="4df93-112">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="4df93-112">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="4df93-113">*pContext*</span><span class="sxs-lookup"><span data-stu-id="4df93-113">*pContext*</span></span> 
</dt> <dd>

<span data-ttu-id="4df93-114">Tipo: **[ **ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span><span class="sxs-lookup"><span data-stu-id="4df93-114">Type: **[**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span></span>

<span data-ttu-id="4df93-115">O [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) para aplicar a passagem.</span><span class="sxs-lookup"><span data-stu-id="4df93-115">The [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) to apply the pass to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4df93-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4df93-116">Return value</span></span>

<span data-ttu-id="4df93-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4df93-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4df93-118">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="4df93-118">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4df93-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="4df93-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4df93-120">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="4df93-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="4df93-121">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="4df93-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="4df93-122">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="4df93-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4df93-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4df93-123">Requirements</span></span>



| <span data-ttu-id="4df93-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="4df93-124">Requirement</span></span> | <span data-ttu-id="4df93-125">Valor</span><span class="sxs-lookup"><span data-stu-id="4df93-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4df93-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4df93-126">Header</span></span><br/>  | <dl> <span data-ttu-id="4df93-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="4df93-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="4df93-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4df93-128">Library</span></span><br/> | <dl> <span data-ttu-id="4df93-129"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="4df93-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4df93-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="4df93-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4df93-131">ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="4df93-131">ID3DX11EffectPass</span></span>](id3dx11effectpass.md)
</dt> </dl>

 

