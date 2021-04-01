---
description: Defina o intervalo de uma matriz para passar para o dispositivo.
ms.assetid: 43f1c258-770c-4756-9033-e5667b379fe6
title: 'Método ID3DXBaseEffect:: SetArrayRange (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetArrayRange
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 59b981c1f2aff18d4bdb57f5726136945203f5fe
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104091939"
---
# <a name="id3dxbaseeffectsetarrayrange-method"></a><span data-ttu-id="c675f-103">Método ID3DXBaseEffect:: SetArrayRange</span><span class="sxs-lookup"><span data-stu-id="c675f-103">ID3DXBaseEffect::SetArrayRange method</span></span>

<span data-ttu-id="c675f-104">Defina o intervalo de uma matriz para passar para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c675f-104">Set the range of an array to pass to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="c675f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c675f-105">Syntax</span></span>


```C++
HRESULT SetArrayRange(
  [in] D3DXHANDLE hParameter,
  [in] UINT       Start,
  [in] UINT       Stop
);
```



## <a name="parameters"></a><span data-ttu-id="c675f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c675f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c675f-107">*hParameter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c675f-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c675f-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="c675f-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="c675f-109">Identificador exclusivo.</span><span class="sxs-lookup"><span data-stu-id="c675f-109">Unique identifier.</span></span> <span data-ttu-id="c675f-110">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="c675f-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="c675f-111">*Iniciar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c675f-111">*Start* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c675f-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c675f-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c675f-113">Índice de início.</span><span class="sxs-lookup"><span data-stu-id="c675f-113">Start index.</span></span>

</dd> <dt>

<span data-ttu-id="c675f-114">*Parar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c675f-114">*Stop* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c675f-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c675f-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c675f-116">Parar índice.</span><span class="sxs-lookup"><span data-stu-id="c675f-116">Stop index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c675f-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c675f-117">Return value</span></span>

<span data-ttu-id="c675f-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c675f-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c675f-119">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c675f-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c675f-120">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="c675f-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="c675f-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c675f-121">Requirements</span></span>



| <span data-ttu-id="c675f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c675f-122">Requirement</span></span> | <span data-ttu-id="c675f-123">Valor</span><span class="sxs-lookup"><span data-stu-id="c675f-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c675f-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c675f-124">Header</span></span><br/>  | <dl> <span data-ttu-id="c675f-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="c675f-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="c675f-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c675f-126">Library</span></span><br/> | <dl> <span data-ttu-id="c675f-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c675f-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c675f-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="c675f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c675f-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="c675f-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
