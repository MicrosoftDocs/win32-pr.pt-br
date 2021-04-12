---
description: Cria um objeto Font indiretamente para um dispositivo e uma fonte.
ms.assetid: 480f3012-8495-47ca-a649-11ce53cee06c
title: Função D3DXCreateFontIndirect (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateFontIndirect
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 086f9cb4cff7666fc3977551e2c9fd4a61150d46
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298741"
---
# <a name="d3dxcreatefontindirect-function"></a><span data-ttu-id="df933-103">Função D3DXCreateFontIndirect</span><span class="sxs-lookup"><span data-stu-id="df933-103">D3DXCreateFontIndirect function</span></span>

<span data-ttu-id="df933-104">Cria um objeto Font indiretamente para um dispositivo e uma fonte.</span><span class="sxs-lookup"><span data-stu-id="df933-104">Creates a font object indirectly for both a device and a font.</span></span>

## <a name="syntax"></a><span data-ttu-id="df933-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="df933-105">Syntax</span></span>


```C++
HRESULT D3DXCreateFontIndirect(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_  const D3DXFONT_DESC     *pDesc,
  _Out_       LPD3DXFONT        *ppFont
);
```



## <a name="parameters"></a><span data-ttu-id="df933-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="df933-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df933-107">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="df933-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df933-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="df933-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="df933-109">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , o dispositivo a ser associado ao objeto Font.</span><span class="sxs-lookup"><span data-stu-id="df933-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device to be associated with the font object.</span></span>

</dd> <dt>

<span data-ttu-id="df933-110">*pDesc* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="df933-110">*pDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df933-111">Tipo: **const [**D3DXFONT \_ desc**](d3dxfont-desc.md) \***</span><span class="sxs-lookup"><span data-stu-id="df933-111">Type: **const [**D3DXFONT\_DESC**](d3dxfont-desc.md)\***</span></span>

<span data-ttu-id="df933-112">Ponteiro para uma [**estrutura \_ desc de D3DXFONT**](d3dxfont-desc.md) , que descreve os atributos do objeto Font a ser criado.</span><span class="sxs-lookup"><span data-stu-id="df933-112">Pointer to a [**D3DXFONT\_DESC**](d3dxfont-desc.md) structure, describing the attributes of the font object to create.</span></span> <span data-ttu-id="df933-113">Se as configurações do compilador exigirem Unicode, o tipo de dados D3DXFONT \_ desc será resolvido para D3DXFONT \_ DESCW; caso contrário, o tipo de dados será resolvido para D3DXFONT \_ desca.</span><span class="sxs-lookup"><span data-stu-id="df933-113">If the compiler settings require Unicode, the data type D3DXFONT\_DESC resolves to D3DXFONT\_DESCW; otherwise, the data type resolves to D3DXFONT\_DESCA.</span></span> <span data-ttu-id="df933-114">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="df933-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="df933-115">*ppFont* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="df933-115">*ppFont* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="df933-116">Tipo: **[ **LPD3DXFONT**](id3dxfont.md)\***</span><span class="sxs-lookup"><span data-stu-id="df933-116">Type: **[**LPD3DXFONT**](id3dxfont.md)\***</span></span>

<span data-ttu-id="df933-117">Retorna um ponteiro para uma interface [**ID3DXFont**](id3dxfont.md) , representando o objeto Font criado.</span><span class="sxs-lookup"><span data-stu-id="df933-117">Returns a pointer to an [**ID3DXFont**](id3dxfont.md) interface, representing the created font object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df933-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="df933-118">Return value</span></span>

<span data-ttu-id="df933-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="df933-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="df933-120">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="df933-120">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="df933-121">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="df933-121">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="df933-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="df933-122">Remarks</span></span>

<span data-ttu-id="df933-123">A configuração do compilador também determina a versão da função.</span><span class="sxs-lookup"><span data-stu-id="df933-123">The compiler setting also determines the function version.</span></span> <span data-ttu-id="df933-124">Se o Unicode for definido, a chamada de função será resolvida como D3DXCreateFontIndirectW.</span><span class="sxs-lookup"><span data-stu-id="df933-124">If Unicode is defined, the function call resolves to D3DXCreateFontIndirectW.</span></span> <span data-ttu-id="df933-125">Caso contrário, a chamada de função é resolvida como D3DXCreateFontIndirectA porque as cadeias de caracteres ANSI estão sendo usadas.</span><span class="sxs-lookup"><span data-stu-id="df933-125">Otherwise, the function call resolves to D3DXCreateFontIndirectA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="df933-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df933-126">Requirements</span></span>



| <span data-ttu-id="df933-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="df933-127">Requirement</span></span> | <span data-ttu-id="df933-128">Valor</span><span class="sxs-lookup"><span data-stu-id="df933-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="df933-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="df933-129">Header</span></span><br/>  | <dl> <span data-ttu-id="df933-130"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="df933-130"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="df933-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="df933-131">Library</span></span><br/> | <dl> <span data-ttu-id="df933-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="df933-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="df933-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="df933-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df933-134">Funções de Uso Geral</span><span class="sxs-lookup"><span data-stu-id="df933-134">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
