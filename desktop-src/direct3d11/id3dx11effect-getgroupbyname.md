---
title: Método getgroupbyname de ID3DX11Effect (D3dx11effect. h)
description: Obtém um grupo de efeitos por nome.
ms.assetid: 14b4b484-848a-409c-9a99-207ab25b7566
keywords:
- Método getgroupbyname Direct3D 11
- Método getgroupbyname Direct3D 11, interface ID3DX11Effect
- Interface ID3DX11Effect Direct3D 11, método getgroupbyname
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetGroupByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1c2132dedb34fe71db30bf82b1c6d336f110a8f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989375"
---
# <a name="id3dx11effectgetgroupbyname-method"></a><span data-ttu-id="64e73-106">Método ID3DX11Effect:: getgroupbyname</span><span class="sxs-lookup"><span data-stu-id="64e73-106">ID3DX11Effect::GetGroupByName method</span></span>

<span data-ttu-id="64e73-107">Obtém um grupo de efeitos por nome.</span><span class="sxs-lookup"><span data-stu-id="64e73-107">Gets an effect group by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="64e73-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="64e73-108">Syntax</span></span>


```C++
ID3DX11EffectGroup* GetGroupByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="64e73-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="64e73-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64e73-110">*Nome*</span><span class="sxs-lookup"><span data-stu-id="64e73-110">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="64e73-111">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="64e73-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="64e73-112">Nome do grupo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="64e73-112">Name of the effect group.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64e73-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="64e73-113">Return value</span></span>

<span data-ttu-id="64e73-114">Tipo: **[ **ID3DX11EffectGroup**](id3dx11effectgroup.md)\***</span><span class="sxs-lookup"><span data-stu-id="64e73-114">Type: **[**ID3DX11EffectGroup**](id3dx11effectgroup.md)\***</span></span>

<span data-ttu-id="64e73-115">Um ponteiro para uma interface [**ID3DX11EffectGroup**](id3dx11effectgroup.md) .</span><span class="sxs-lookup"><span data-stu-id="64e73-115">A pointer to an [**ID3DX11EffectGroup**](id3dx11effectgroup.md) interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="64e73-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="64e73-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="64e73-117">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="64e73-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="64e73-118">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="64e73-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="64e73-119">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="64e73-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="64e73-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64e73-120">Requirements</span></span>



| <span data-ttu-id="64e73-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="64e73-121">Requirement</span></span> | <span data-ttu-id="64e73-122">Valor</span><span class="sxs-lookup"><span data-stu-id="64e73-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64e73-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="64e73-123">Header</span></span><br/>  | <dl> <span data-ttu-id="64e73-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="64e73-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="64e73-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="64e73-125">Library</span></span><br/> | <dl> <span data-ttu-id="64e73-126"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="64e73-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64e73-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="64e73-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64e73-128">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="64e73-128">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

