---
description: Criar uma bomba de thread.
ms.assetid: a7a016e2-784d-4d7a-8058-88895bf3c4e2
title: Função D3DX10CreateThreadPump (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateThreadPump
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8a27f8df1f4eaa8e7f41e863d703063308f9c595
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930715"
---
# <a name="d3dx10createthreadpump-function"></a><span data-ttu-id="c5ea4-103">Função D3DX10CreateThreadPump</span><span class="sxs-lookup"><span data-stu-id="c5ea4-103">D3DX10CreateThreadPump function</span></span>

<span data-ttu-id="c5ea4-104">Criar uma bomba de thread.</span><span class="sxs-lookup"><span data-stu-id="c5ea4-104">Create a thread pump.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5ea4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c5ea4-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateThreadPump(
  _In_  UINT              cIoThreads,
  _In_  UINT              cProcThreads,
  _Out_ ID3DX10ThreadPump **ppThreadPump
);
```



## <a name="parameters"></a><span data-ttu-id="c5ea4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c5ea4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5ea4-107">*cIoThreads* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c5ea4-107">*cIoThreads* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5ea4-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c5ea4-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c5ea4-109">O número de threads de e/s a serem criados.</span><span class="sxs-lookup"><span data-stu-id="c5ea4-109">The number of I/O threads to create.</span></span> <span data-ttu-id="c5ea4-110">Se 0 for especificado, o Direct3D tentará calcular o número ideal de threads com base na configuração de hardware.</span><span class="sxs-lookup"><span data-stu-id="c5ea4-110">If 0 is specified, Direct3D will attempt to calculate the optimal number of threads based on the hardware configuration.</span></span>

</dd> <dt>

<span data-ttu-id="c5ea4-111">*cProcThreads* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c5ea4-111">*cProcThreads* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5ea4-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c5ea4-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c5ea4-113">O número de threads de processo a serem criados.</span><span class="sxs-lookup"><span data-stu-id="c5ea4-113">The number of process threads to create.</span></span> <span data-ttu-id="c5ea4-114">Se 0 for especificado, o Direct3D tentará calcular o número ideal de threads com base na configuração de hardware.</span><span class="sxs-lookup"><span data-stu-id="c5ea4-114">If 0 is specified, Direct3D will attempt to calculate the optimal number of threads based on the hardware configuration.</span></span>

</dd> <dt>

<span data-ttu-id="c5ea4-115">*ppThreadPump* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c5ea4-115">*ppThreadPump* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5ea4-116">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="c5ea4-116">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\*\***</span></span>

<span data-ttu-id="c5ea4-117">A bomba de thread criada.</span><span class="sxs-lookup"><span data-stu-id="c5ea4-117">The created thread pump.</span></span> <span data-ttu-id="c5ea4-118">Consulte a [**interface ID3DX10ThreadPump**](id3dx10threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="c5ea4-118">See [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5ea4-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c5ea4-119">Return value</span></span>

<span data-ttu-id="c5ea4-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c5ea4-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c5ea4-121">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="c5ea4-121">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c5ea4-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="c5ea4-122">Remarks</span></span>

<span data-ttu-id="c5ea4-123">Uma bomba de thread é um objeto com uso intensivo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c5ea4-123">A thread pump is a very resource-intensive object.</span></span> <span data-ttu-id="c5ea4-124">Somente uma bomba de thread deve ser criada por aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c5ea4-124">Only one thread pump should be created per application.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5ea4-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5ea4-125">Requirements</span></span>



| <span data-ttu-id="c5ea4-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5ea4-126">Requirement</span></span> | <span data-ttu-id="c5ea4-127">Valor</span><span class="sxs-lookup"><span data-stu-id="c5ea4-127">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c5ea4-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c5ea4-128">Header</span></span><br/>  | <dl> <span data-ttu-id="c5ea4-129"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5ea4-129"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="c5ea4-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c5ea4-130">Library</span></span><br/> | <dl> <span data-ttu-id="c5ea4-131"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c5ea4-131"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5ea4-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="c5ea4-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5ea4-133">Funções de Uso Geral</span><span class="sxs-lookup"><span data-stu-id="c5ea4-133">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
