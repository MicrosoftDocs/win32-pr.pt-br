---
description: Habilitar ou desabilitar mensagens de depuração.
ms.assetid: 5c2aa3cf-ee6a-40fd-b300-67cb6ce691b6
title: Função D3DX10DebugMute (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10DebugMute
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 6f331e3f074a4b77a1f1a7f1a8117cf660940f7d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105814542"
---
# <a name="d3dx10debugmute-function"></a><span data-ttu-id="3c55d-103">Função D3DX10DebugMute</span><span class="sxs-lookup"><span data-stu-id="3c55d-103">D3DX10DebugMute function</span></span>

<span data-ttu-id="3c55d-104">Habilitar ou desabilitar mensagens de depuração.</span><span class="sxs-lookup"><span data-stu-id="3c55d-104">Enable or disable debug messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c55d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3c55d-105">Syntax</span></span>


```C++
HRESULT D3DX10DebugMute(
  _In_ BOOL Mute
);
```



## <a name="parameters"></a><span data-ttu-id="3c55d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3c55d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c55d-107">*Sem áudio* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3c55d-107">*Mute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c55d-108">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3c55d-108">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3c55d-109">Defina como **true** para habilitar mensagens de depuração; Defina como **false** para desabilitar as mensagens de depuração.</span><span class="sxs-lookup"><span data-stu-id="3c55d-109">Set to **TRUE** to enable debug messages; set to **FALSE** to disable debug messages.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c55d-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3c55d-110">Return value</span></span>

<span data-ttu-id="3c55d-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3c55d-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3c55d-112">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="3c55d-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3c55d-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="3c55d-113">Remarks</span></span>

<span data-ttu-id="3c55d-114">Use esta função para desabilitar mensagens de erro para APIs D3DX10 durante a depuração; o uso dessa função deve ser protegido pela opção de compilador do D3D10 \_ debug.</span><span class="sxs-lookup"><span data-stu-id="3c55d-114">Use this function to disable error messages for D3DX10 APIs during debug; the use of this function should be guarded by the D3D10\_DEBUG compiler switch.</span></span>


```
#ifdef D3D10_DEBUG
  BOOL WINAPI D3DX10DebugMute(BOOL Mute);  
#endif
```



<span data-ttu-id="3c55d-115">O estado padrão é **true** para uma compilação de depuração.</span><span class="sxs-lookup"><span data-stu-id="3c55d-115">The default state is **TRUE** for a debug build.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c55d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c55d-116">Requirements</span></span>



| <span data-ttu-id="3c55d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c55d-117">Requirement</span></span> | <span data-ttu-id="3c55d-118">Valor</span><span class="sxs-lookup"><span data-stu-id="3c55d-118">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c55d-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3c55d-119">Header</span></span><br/>  | <dl> <span data-ttu-id="3c55d-120"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c55d-120"><dt>D3DX10Core.h</dt></span></span> </dl> |
| <span data-ttu-id="3c55d-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3c55d-121">Library</span></span><br/> | <dl> <span data-ttu-id="3c55d-122"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c55d-122"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3c55d-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="3c55d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c55d-124">Funções de Uso Geral</span><span class="sxs-lookup"><span data-stu-id="3c55d-124">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
