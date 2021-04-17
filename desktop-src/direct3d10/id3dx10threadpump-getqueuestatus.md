---
description: Obtenha o número de itens em cada uma das três filas dentro da bomba do thread.
ms.assetid: b5b829a5-5ef7-4ef5-afb4-efe1bb22ae70
title: 'Método ID3DX10ThreadPump:: GetQueueStatus (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10ThreadPump.GetQueueStatus
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4cf3b5879da0346cefbb5b8835d6922dd736cfd3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105772950"
---
# <a name="id3dx10threadpumpgetqueuestatus-method"></a><span data-ttu-id="70d02-103">Método ID3DX10ThreadPump:: GetQueueStatus</span><span class="sxs-lookup"><span data-stu-id="70d02-103">ID3DX10ThreadPump::GetQueueStatus method</span></span>

<span data-ttu-id="70d02-104">Obtenha o número de itens em cada uma das três filas dentro da bomba do thread.</span><span class="sxs-lookup"><span data-stu-id="70d02-104">Get the number of items in each of the three queues inside the thread pump.</span></span>

## <a name="syntax"></a><span data-ttu-id="70d02-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="70d02-105">Syntax</span></span>


```C++
HRESULT GetQueueStatus(
  [in] UINT *pIoQueue,
  [in] UINT *pProcessQueue,
  [in] UINT *pDeviceQueue
);
```



## <a name="parameters"></a><span data-ttu-id="70d02-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="70d02-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70d02-107">*pIoQueue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="70d02-107">*pIoQueue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70d02-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="70d02-108">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="70d02-109">Número de itens na fila de e/s.</span><span class="sxs-lookup"><span data-stu-id="70d02-109">Number of items in the I/O queue.</span></span>

</dd> <dt>

<span data-ttu-id="70d02-110">*pProcessQueue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="70d02-110">*pProcessQueue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70d02-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="70d02-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="70d02-112">Número de itens na fila de processos.</span><span class="sxs-lookup"><span data-stu-id="70d02-112">Number of items in the process queue.</span></span>

</dd> <dt>

<span data-ttu-id="70d02-113">*pDeviceQueue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="70d02-113">*pDeviceQueue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70d02-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="70d02-114">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="70d02-115">Número de itens na fila do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="70d02-115">Number of items in the device queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70d02-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="70d02-116">Return value</span></span>

<span data-ttu-id="70d02-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="70d02-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="70d02-118">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="70d02-118">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="70d02-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70d02-119">Requirements</span></span>



| <span data-ttu-id="70d02-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="70d02-120">Requirement</span></span> | <span data-ttu-id="70d02-121">Valor</span><span class="sxs-lookup"><span data-stu-id="70d02-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="70d02-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="70d02-122">Header</span></span><br/>  | <dl> <span data-ttu-id="70d02-123"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="70d02-123"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="70d02-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="70d02-124">Library</span></span><br/> | <dl> <span data-ttu-id="70d02-125"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="70d02-125"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70d02-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="70d02-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70d02-127">ID3DX10ThreadPump</span><span class="sxs-lookup"><span data-stu-id="70d02-127">ID3DX10ThreadPump</span></span>](id3dx10threadpump.md)
</dt> <dt>

[<span data-ttu-id="70d02-128">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="70d02-128">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
