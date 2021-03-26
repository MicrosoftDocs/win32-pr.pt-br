---
title: Método GetString ID3DX11EffectStringVariable (D3dx11effect. h)
description: Obter a cadeia de caracteres.
ms.assetid: ce96ae18-d316-41ba-9b2a-eac084b86098
keywords:
- Método GetString Direct3D 11
- Método GetString Direct3D 11, interface ID3DX11EffectStringVariable
- Interface ID3DX11EffectStringVariable Direct3D 11, método GetString
topic_type:
- apiref
api_name:
- ID3DX11EffectStringVariable.GetString
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15d15666bd70bf00395b7052b7820981dd8d0dcd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968562"
---
# <a name="id3dx11effectstringvariablegetstring-method"></a><span data-ttu-id="2dd45-106">Método ID3DX11EffectStringVariable:: GetString</span><span class="sxs-lookup"><span data-stu-id="2dd45-106">ID3DX11EffectStringVariable::GetString method</span></span>

<span data-ttu-id="2dd45-107">Obter a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="2dd45-107">Get the string.</span></span>

## <a name="syntax"></a><span data-ttu-id="2dd45-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2dd45-108">Syntax</span></span>


```C++
HRESULT GetString(
   LPCSTR *ppString
);
```



## <a name="parameters"></a><span data-ttu-id="2dd45-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2dd45-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2dd45-110">*ppString*</span><span class="sxs-lookup"><span data-stu-id="2dd45-110">*ppString*</span></span> 
</dt> <dd>

<span data-ttu-id="2dd45-111">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="2dd45-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="2dd45-112">Um ponteiro para a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="2dd45-112">A pointer to the string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2dd45-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2dd45-113">Return value</span></span>

<span data-ttu-id="2dd45-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2dd45-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2dd45-115">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="2dd45-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2dd45-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="2dd45-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2dd45-117">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="2dd45-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="2dd45-118">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="2dd45-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="2dd45-119">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="2dd45-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2dd45-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2dd45-120">Requirements</span></span>



| <span data-ttu-id="2dd45-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="2dd45-121">Requirement</span></span> | <span data-ttu-id="2dd45-122">Valor</span><span class="sxs-lookup"><span data-stu-id="2dd45-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2dd45-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2dd45-123">Header</span></span><br/>  | <dl> <span data-ttu-id="2dd45-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="2dd45-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="2dd45-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2dd45-125">Library</span></span><br/> | <dl> <span data-ttu-id="2dd45-126"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="2dd45-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2dd45-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="2dd45-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2dd45-128">ID3DX11EffectStringVariable</span><span class="sxs-lookup"><span data-stu-id="2dd45-128">ID3DX11EffectStringVariable</span></span>](id3dx11effectstringvariable.md)
</dt> </dl>

 

