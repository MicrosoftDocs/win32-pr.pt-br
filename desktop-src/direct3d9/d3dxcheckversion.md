---
description: Verifique se a versão do D3DX que você compilou com o é a versão que você está executando.
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
ms.openlocfilehash: 7b392d706e54780924115471906096f6b63d1a80
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105752367"
---
# <a name="d3dxcheckversion-function"></a><span data-ttu-id="fb6a3-103">Função D3DXCheckVersion</span><span class="sxs-lookup"><span data-stu-id="fb6a3-103">D3DXCheckVersion function</span></span>

<span data-ttu-id="fb6a3-104">Verifique se a versão do D3DX que você compilou com o é a versão que você está executando.</span><span class="sxs-lookup"><span data-stu-id="fb6a3-104">Verify that the version of D3DX you compiled with is the version that you are running.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb6a3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fb6a3-105">Syntax</span></span>


```C++
BOOL D3DXCheckVersion(
  _In_ UINT D3DSDKVersion,
  _In_ UINT D3DXSDKVersion
);
```



## <a name="parameters"></a><span data-ttu-id="fb6a3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fb6a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb6a3-107">*D3DSDKVersion* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fb6a3-107">*D3DSDKVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb6a3-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fb6a3-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fb6a3-109">Use a \_ versão do SDK do D3D \_ .</span><span class="sxs-lookup"><span data-stu-id="fb6a3-109">Use D3D\_SDK\_VERSION.</span></span> <span data-ttu-id="fb6a3-110">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="fb6a3-110">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="fb6a3-111">*D3DXSDKVersion* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fb6a3-111">*D3DXSDKVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb6a3-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fb6a3-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fb6a3-113">Use a \_ versão do SDK do D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="fb6a3-113">Use D3DX\_SDK\_VERSION.</span></span> <span data-ttu-id="fb6a3-114">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="fb6a3-114">See remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb6a3-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fb6a3-115">Return value</span></span>

<span data-ttu-id="fb6a3-116">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fb6a3-116">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fb6a3-117">Retornará **true** se a versão do D3DX que você compilou for a versão com a qual você está executando; caso contrário, **false** será retornado.</span><span class="sxs-lookup"><span data-stu-id="fb6a3-117">Returns **TRUE** if the version of D3DX you compiled against is the version you are running with; otherwise, **FALSE** is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb6a3-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="fb6a3-118">Remarks</span></span>

<span data-ttu-id="fb6a3-119">Use essa função durante a inicialização do seu aplicativo da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="fb6a3-119">Use this function during the initialization of your application like this:</span></span>


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



<span data-ttu-id="fb6a3-120">Use [**Direct3DCreate9**](/windows/win32/api/d3d9/nf-d3d9-direct3dcreate9) para verificar se o tempo de execução correto está instalado.</span><span class="sxs-lookup"><span data-stu-id="fb6a3-120">Use [**Direct3DCreate9**](/windows/win32/api/d3d9/nf-d3d9-direct3dcreate9) to verify that the correct runtime is installed.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb6a3-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb6a3-121">Requirements</span></span>



| <span data-ttu-id="fb6a3-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb6a3-122">Requirement</span></span> | <span data-ttu-id="fb6a3-123">Valor</span><span class="sxs-lookup"><span data-stu-id="fb6a3-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb6a3-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fb6a3-124">Header</span></span><br/>  | <dl> <span data-ttu-id="fb6a3-125"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb6a3-125"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="fb6a3-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fb6a3-126">Library</span></span><br/> | <dl> <span data-ttu-id="fb6a3-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fb6a3-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fb6a3-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="fb6a3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb6a3-129">Funções de Uso Geral</span><span class="sxs-lookup"><span data-stu-id="fb6a3-129">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
