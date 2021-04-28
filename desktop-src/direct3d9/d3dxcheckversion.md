---
description: Função D3DXCheckVersion – Verifique se a versão do D3DX que você compilou com o é a versão que você está executando.
ms.assetid: a4e745dd-d573-4e8f-9516-f6a7475f5cc5
title: Função D3DXCheckVersion (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCheckVersion
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 077d64a67a46080a0f7ac9194c684f6fe8470453
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115974"
---
# <a name="d3dxcheckversion-function"></a><span data-ttu-id="e191b-103">Função D3DXCheckVersion</span><span class="sxs-lookup"><span data-stu-id="e191b-103">D3DXCheckVersion function</span></span>

<span data-ttu-id="e191b-104">Verifique se a versão do D3DX que você compilou com o é a versão que você está executando.</span><span class="sxs-lookup"><span data-stu-id="e191b-104">Verify that the version of D3DX you compiled with is the version that you are running.</span></span>

## <a name="syntax"></a><span data-ttu-id="e191b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e191b-105">Syntax</span></span>


```C++
BOOL D3DXCheckVersion(
  _In_ UINT D3DSDKVersion,
  _In_ UINT D3DXSDKVersion
);
```



## <a name="parameters"></a><span data-ttu-id="e191b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e191b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e191b-107">*D3DSDKVersion* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e191b-107">*D3DSDKVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e191b-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e191b-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e191b-109">Use a \_ versão do SDK do D3D \_ .</span><span class="sxs-lookup"><span data-stu-id="e191b-109">Use D3D\_SDK\_VERSION.</span></span> <span data-ttu-id="e191b-110">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="e191b-110">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="e191b-111">*D3DXSDKVersion* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e191b-111">*D3DXSDKVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e191b-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e191b-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e191b-113">Use a \_ versão do SDK do D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="e191b-113">Use D3DX\_SDK\_VERSION.</span></span> <span data-ttu-id="e191b-114">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="e191b-114">See remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e191b-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="e191b-115">Return value</span></span>

<span data-ttu-id="e191b-116">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e191b-116">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e191b-117">Retornará **true** se a versão do D3DX que você compilou for a versão com a qual você está executando; caso contrário, **false** será retornado.</span><span class="sxs-lookup"><span data-stu-id="e191b-117">Returns **TRUE** if the version of D3DX you compiled against is the version you are running with; otherwise, **FALSE** is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="e191b-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="e191b-118">Remarks</span></span>

<span data-ttu-id="e191b-119">Use essa função durante a inicialização do seu aplicativo da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="e191b-119">Use this function during the initialization of your application like this:</span></span>


```
HRESULT CD3DXMyApplication::Initialize(HINSTANCE hInstance, 
  LPCSTR szWindowName, LPCSTR szClassName, UINT uWidth, UINT uHeight)
{
    HRESULT hr;
    
    if (!D3DXCheckVersion(D3D_SDK_VERSION, D3DX_SDK_VERSION))
        return E_FAIL;
    
    ...
}
```



<span data-ttu-id="e191b-120">Use [**Direct3DCreate9**](/windows/win32/api/d3d9/nf-d3d9-direct3dcreate9) para verificar se o tempo de execução correto está instalado.</span><span class="sxs-lookup"><span data-stu-id="e191b-120">Use [**Direct3DCreate9**](/windows/win32/api/d3d9/nf-d3d9-direct3dcreate9) to verify that the correct runtime is installed.</span></span>

## <a name="requirements"></a><span data-ttu-id="e191b-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e191b-121">Requirements</span></span>



| <span data-ttu-id="e191b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e191b-122">Requirement</span></span> | <span data-ttu-id="e191b-123">Valor</span><span class="sxs-lookup"><span data-stu-id="e191b-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e191b-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e191b-124">Header</span></span><br/>  | <dl> <span data-ttu-id="e191b-125"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="e191b-125"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="e191b-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e191b-126">Library</span></span><br/> | <dl> <span data-ttu-id="e191b-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e191b-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e191b-128">Consulte também</span><span class="sxs-lookup"><span data-stu-id="e191b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e191b-129">Funções de Uso Geral</span><span class="sxs-lookup"><span data-stu-id="e191b-129">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
