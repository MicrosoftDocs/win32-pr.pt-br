---
title: Método ID3DX11ThreadPump GetQueueStatus (D3DX11core. h)
description: Observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Obtém o número de itens em cada uma das três filas dentro da bomba do thread.
ms.assetid: 69e1c786-6c7d-4432-bf34-3bf7606a07f6
keywords:
- Método GetQueueStatus Direct3D 11
- Método GetQueueStatus Direct3D 11, interface ID3DX11ThreadPump
- Interface ID3DX11ThreadPump Direct3D 11, método GetQueueStatus
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump.GetQueueStatus
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3c945cb2978af15263d3f72d34a47c5e8ca8a69
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968592"
---
# <a name="id3dx11threadpumpgetqueuestatus-method"></a><span data-ttu-id="e27f0-107">Método ID3DX11ThreadPump:: GetQueueStatus</span><span class="sxs-lookup"><span data-stu-id="e27f0-107">ID3DX11ThreadPump::GetQueueStatus method</span></span>

> [!Note]  
> <span data-ttu-id="e27f0-108">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="e27f0-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="e27f0-109">Obtém o número de itens em cada uma das três filas dentro da bomba do thread.</span><span class="sxs-lookup"><span data-stu-id="e27f0-109">Gets the number of items in each of the three queues inside the thread pump.</span></span>

## <a name="syntax"></a><span data-ttu-id="e27f0-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e27f0-110">Syntax</span></span>


```C++
HRESULT GetQueueStatus(
  [in] UINT *pIoQueue,
  [in] UINT *pProcessQueue,
  [in] UINT *pDeviceQueue
);
```



## <a name="parameters"></a><span data-ttu-id="e27f0-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e27f0-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e27f0-112">*pIoQueue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e27f0-112">*pIoQueue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e27f0-113">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="e27f0-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="e27f0-114">Número de itens na fila de e/s.</span><span class="sxs-lookup"><span data-stu-id="e27f0-114">Number of items in the I/O queue.</span></span>

</dd> <dt>

<span data-ttu-id="e27f0-115">*pProcessQueue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e27f0-115">*pProcessQueue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e27f0-116">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="e27f0-116">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="e27f0-117">Número de itens na fila de processos.</span><span class="sxs-lookup"><span data-stu-id="e27f0-117">Number of items in the process queue.</span></span>

</dd> <dt>

<span data-ttu-id="e27f0-118">*pDeviceQueue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e27f0-118">*pDeviceQueue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e27f0-119">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="e27f0-119">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="e27f0-120">Número de itens na fila do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e27f0-120">Number of items in the device queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e27f0-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e27f0-121">Return value</span></span>

<span data-ttu-id="e27f0-122">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e27f0-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e27f0-123">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="e27f0-123">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e27f0-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e27f0-124">Requirements</span></span>



| <span data-ttu-id="e27f0-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="e27f0-125">Requirement</span></span> | <span data-ttu-id="e27f0-126">Valor</span><span class="sxs-lookup"><span data-stu-id="e27f0-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e27f0-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e27f0-127">Header</span></span><br/>  | <dl> <span data-ttu-id="e27f0-128"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="e27f0-128"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="e27f0-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e27f0-129">Library</span></span><br/> | <dl> <span data-ttu-id="e27f0-130"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e27f0-130"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e27f0-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="e27f0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e27f0-132">ID3DX11ThreadPump</span><span class="sxs-lookup"><span data-stu-id="e27f0-132">ID3DX11ThreadPump</span></span>](id3dx11threadpump.md)
</dt> <dt>

[<span data-ttu-id="e27f0-133">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="e27f0-133">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

