---
description: Ativa ou desativa a saída de depuração de D3DX.
ms.assetid: e35cbfd2-401e-47ec-9f5b-e2ed63ea1fcd
title: Função D3DXDebugMute (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXDebugMute
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9259fa43a6a64829e42cbaa661aa7223a958f22d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173007"
---
# <a name="d3dxdebugmute-function"></a><span data-ttu-id="820c7-103">Função D3DXDebugMute</span><span class="sxs-lookup"><span data-stu-id="820c7-103">D3DXDebugMute function</span></span>

<span data-ttu-id="820c7-104">Ativa ou desativa a saída de depuração de D3DX.</span><span class="sxs-lookup"><span data-stu-id="820c7-104">Turns on or off all D3DX debug output.</span></span>

## <a name="syntax"></a><span data-ttu-id="820c7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="820c7-105">Syntax</span></span>


```C++
BOOL D3DXDebugMute(
  _In_ BOOL Mute
);
```



## <a name="parameters"></a><span data-ttu-id="820c7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="820c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="820c7-107">*Sem áudio* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="820c7-107">*Mute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="820c7-108">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="820c7-108">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="820c7-109">Se **for true**, a saída do depurador será interrompida; Se for **false**, a saída de depuração será habilitada.</span><span class="sxs-lookup"><span data-stu-id="820c7-109">If **TRUE**, debugger output is halted; if **FALSE**, debug output is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="820c7-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="820c7-110">Return value</span></span>

<span data-ttu-id="820c7-111">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="820c7-111">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="820c7-112">Retorna o valor anterior de mudo.</span><span class="sxs-lookup"><span data-stu-id="820c7-112">Returns the previous value of Mute.</span></span>

## <a name="requirements"></a><span data-ttu-id="820c7-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="820c7-113">Requirements</span></span>



| <span data-ttu-id="820c7-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="820c7-114">Requirement</span></span> | <span data-ttu-id="820c7-115">Valor</span><span class="sxs-lookup"><span data-stu-id="820c7-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="820c7-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="820c7-116">Header</span></span><br/>  | <dl> <span data-ttu-id="820c7-117"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="820c7-117"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="820c7-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="820c7-118">Library</span></span><br/> | <dl> <span data-ttu-id="820c7-119"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="820c7-119"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="820c7-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="820c7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="820c7-121">Funções de Uso Geral</span><span class="sxs-lookup"><span data-stu-id="820c7-121">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
