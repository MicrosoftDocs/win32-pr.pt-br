---
description: Define um ponteiro para uma função de retorno de chamada opcional que calcula a porcentagem de cálculos de harmônica esférica (SH) concluídas e dá ao chamador a opção de anular o simulador.
ms.assetid: 0a47610d-fa4e-4094-9adb-4fd9306b8a12
title: 'Método ID3DXPRTEngine:: SetCallback (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetCallBack
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e9c2cfe710bc41ff71267e381fa0bf576688f9df
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105797676"
---
# <a name="id3dxprtenginesetcallback-method"></a><span data-ttu-id="fd956-103">Método ID3DXPRTEngine:: SetCallback</span><span class="sxs-lookup"><span data-stu-id="fd956-103">ID3DXPRTEngine::SetCallBack method</span></span>

<span data-ttu-id="fd956-104">Define um ponteiro para uma função de retorno de chamada opcional que calcula a porcentagem de cálculos de harmônica esférica (SH) concluídas e dá ao chamador a opção de anular o simulador.</span><span class="sxs-lookup"><span data-stu-id="fd956-104">Sets a pointer to an optional callback function that computes the percentage of spherical harmonic (SH) computations completed and gives the caller the option of aborting the simulator.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd956-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fd956-105">Syntax</span></span>


```C++
HRESULT SetCallBack(
  [in] LPD3DXSHPRTSIMCB pCB,
  [in] FLOAT            Frequency,
  [in] LPVOID           lpUserContext
);
```



## <a name="parameters"></a><span data-ttu-id="fd956-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fd956-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd956-107">*pCB* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fd956-107">*pCB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd956-108">Tipo: **[LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md)**</span><span class="sxs-lookup"><span data-stu-id="fd956-108">Type: **[LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md)**</span></span>

<span data-ttu-id="fd956-109">Ponteiro para a função de retorno de chamada [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) que computa a porcentagem de cálculos de SH concluídos.</span><span class="sxs-lookup"><span data-stu-id="fd956-109">Pointer to the [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) callback function that computes the percentage of SH computations completed.</span></span> <span data-ttu-id="fd956-110">A função de retorno de chamada deve ser implementada para retornar S \_ OK para continuar executando o simulador.</span><span class="sxs-lookup"><span data-stu-id="fd956-110">The callback function must be implemented to return S\_OK to keep running the simulator.</span></span> <span data-ttu-id="fd956-111">Qualquer outro valor anulará o simulador.</span><span class="sxs-lookup"><span data-stu-id="fd956-111">Any other value will abort the simulator.</span></span>

</dd> <dt>

<span data-ttu-id="fd956-112">*Frequência* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="fd956-112">*Frequency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd956-113">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fd956-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fd956-114">Frequência de chamadas de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="fd956-114">Frequency of callback calls.</span></span> <span data-ttu-id="fd956-115">O inverso da frequência é aproximadamente o número de vezes que a função de retorno de chamada será chamada.</span><span class="sxs-lookup"><span data-stu-id="fd956-115">The inverse of Frequency is approximately the number of times the callback function will be called.</span></span>

</dd> <dt>

<span data-ttu-id="fd956-116">*lpUserContext* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fd956-116">*lpUserContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd956-117">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fd956-117">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fd956-118">Ponteiro para um valor definido pelo usuário que é passado para a função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="fd956-118">Pointer to a user-defined value which is passed to the callback function.</span></span> <span data-ttu-id="fd956-119">Normalmente usado por um aplicativo para passar um ponteiro para uma estrutura de dados que fornece informações de contexto para a função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="fd956-119">Typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd956-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fd956-120">Return value</span></span>

<span data-ttu-id="fd956-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fd956-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fd956-122">O valor de retorno é S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fd956-122">The return value is S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd956-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd956-123">Requirements</span></span>



| <span data-ttu-id="fd956-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd956-124">Requirement</span></span> | <span data-ttu-id="fd956-125">Valor</span><span class="sxs-lookup"><span data-stu-id="fd956-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd956-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fd956-126">Header</span></span><br/>  | <dl> <span data-ttu-id="fd956-127"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd956-127"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="fd956-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fd956-128">Library</span></span><br/> | <dl> <span data-ttu-id="fd956-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fd956-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fd956-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="fd956-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd956-131">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="fd956-131">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
