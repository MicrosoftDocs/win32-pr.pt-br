---
description: Retorna o nível do driver.
ms.assetid: e8c85201-7850-4c8d-a124-ceb76d4e24d5
title: Função D3DXGetDriverLevel (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetDriverLevel
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 83f756f6b6ab5864f14e797879be243f871fb9e1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105814443"
---
# <a name="d3dxgetdriverlevel-function"></a><span data-ttu-id="9f733-103">Função D3DXGetDriverLevel</span><span class="sxs-lookup"><span data-stu-id="9f733-103">D3DXGetDriverLevel function</span></span>

<span data-ttu-id="9f733-104">Retorna o nível do driver.</span><span class="sxs-lookup"><span data-stu-id="9f733-104">Returns the driver level.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f733-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9f733-105">Syntax</span></span>


```C++
UINT D3DXGetDriverLevel(
  _In_ LPDIRECT3DDEVICE9 pDevice
);
```



## <a name="parameters"></a><span data-ttu-id="9f733-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9f733-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f733-107">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9f733-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f733-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="9f733-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="9f733-109">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9f733-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface representing the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f733-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9f733-110">Return value</span></span>

<span data-ttu-id="9f733-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9f733-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9f733-112">O nível do driver.</span><span class="sxs-lookup"><span data-stu-id="9f733-112">The driver level.</span></span> <span data-ttu-id="9f733-113">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="9f733-113">See remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f733-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="9f733-114">Remarks</span></span>

<span data-ttu-id="9f733-115">Esse método retorna a versão do driver, que é uma das seguintes:</span><span class="sxs-lookup"><span data-stu-id="9f733-115">This method returns the driver version, which is one of the following:</span></span>

-   <span data-ttu-id="9f733-116">700-driver de nível do Direct3D 7</span><span class="sxs-lookup"><span data-stu-id="9f733-116">700 - Direct3D 7 level driver</span></span>
-   <span data-ttu-id="9f733-117">800-driver de nível do Direct3D 8</span><span class="sxs-lookup"><span data-stu-id="9f733-117">800 - Direct3D 8 level driver</span></span>
-   <span data-ttu-id="9f733-118">900-Driver de nível do Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="9f733-118">900 - Direct3D 9 level driver</span></span>

## <a name="requirements"></a><span data-ttu-id="9f733-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f733-119">Requirements</span></span>



| <span data-ttu-id="9f733-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f733-120">Requirement</span></span> | <span data-ttu-id="9f733-121">Valor</span><span class="sxs-lookup"><span data-stu-id="9f733-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f733-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9f733-122">Header</span></span><br/>  | <dl> <span data-ttu-id="9f733-123"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f733-123"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="9f733-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9f733-124">Library</span></span><br/> | <dl> <span data-ttu-id="9f733-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9f733-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9f733-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="9f733-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f733-127">Funções de Uso Geral</span><span class="sxs-lookup"><span data-stu-id="9f733-127">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
