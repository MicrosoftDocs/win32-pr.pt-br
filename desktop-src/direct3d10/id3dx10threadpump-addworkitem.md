---
description: Adicione um item de trabalho à bomba do thread.
ms.assetid: f07789dc-a3d5-4bad-9768-527e701271b8
title: 'Método ID3DX10ThreadPump:: AddWorkItem (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10ThreadPump.AddWorkItem
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: aaf5286ca6cf7b61b0027b176d9a9261bd0beaa8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105810792"
---
# <a name="id3dx10threadpumpaddworkitem-method"></a><span data-ttu-id="f0220-103">Método ID3DX10ThreadPump:: AddWorkItem</span><span class="sxs-lookup"><span data-stu-id="f0220-103">ID3DX10ThreadPump::AddWorkItem method</span></span>

<span data-ttu-id="f0220-104">Adicione um item de trabalho à bomba do thread.</span><span class="sxs-lookup"><span data-stu-id="f0220-104">Add a work item to the thread pump.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0220-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f0220-105">Syntax</span></span>


```C++
HRESULT AddWorkItem(
  [in]  ID3DX10DataLoader    *pDataLoader,
  [in]  ID3DX10DataProcessor *pDataProcessor,
  [in]  HRESULT              *pHResult,
  [out] void                 **ppDeviceObject
);
```



## <a name="parameters"></a><span data-ttu-id="f0220-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f0220-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0220-107">*pDataLoader* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f0220-107">*pDataLoader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0220-108">Tipo: **[ **ID3DX10DataLoader**](id3dx10dataloader.md)\***</span><span class="sxs-lookup"><span data-stu-id="f0220-108">Type: **[**ID3DX10DataLoader**](id3dx10dataloader.md)\***</span></span>

<span data-ttu-id="f0220-109">O carregador que será usado pela bomba de thread quando um item de trabalho exigir que os dados sejam carregados.</span><span class="sxs-lookup"><span data-stu-id="f0220-109">The loader that the thread pump will use when a work item requires data to be loaded.</span></span>

</dd> <dt>

<span data-ttu-id="f0220-110">*pDataProcessor* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f0220-110">*pDataProcessor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0220-111">Tipo: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\***</span><span class="sxs-lookup"><span data-stu-id="f0220-111">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\***</span></span>

<span data-ttu-id="f0220-112">O processador que a bomba de thread usará quando um item de trabalho exigir que os dados sejam processados.</span><span class="sxs-lookup"><span data-stu-id="f0220-112">The processor that the thread pump will use when a work item requires data to be processed.</span></span>

</dd> <dt>

<span data-ttu-id="f0220-113">*pHResult* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f0220-113">*pHResult* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0220-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="f0220-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="f0220-115">Um ponteiro para o valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="f0220-115">A pointer to the return value.</span></span> <span data-ttu-id="f0220-116">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="f0220-116">May be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f0220-117">*ppDeviceObject* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f0220-117">*ppDeviceObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0220-118">Tipo: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="f0220-118">Type: **void\*\***</span></span>

<span data-ttu-id="f0220-119">O dispositivo que usa o objeto.</span><span class="sxs-lookup"><span data-stu-id="f0220-119">The device that uses the object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0220-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f0220-120">Return value</span></span>

<span data-ttu-id="f0220-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f0220-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f0220-122">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="f0220-122">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f0220-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0220-123">Requirements</span></span>



| <span data-ttu-id="f0220-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0220-124">Requirement</span></span> | <span data-ttu-id="f0220-125">Valor</span><span class="sxs-lookup"><span data-stu-id="f0220-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f0220-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f0220-126">Header</span></span><br/>  | <dl> <span data-ttu-id="f0220-127"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0220-127"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="f0220-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f0220-128">Library</span></span><br/> | <dl> <span data-ttu-id="f0220-129"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f0220-129"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0220-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="f0220-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0220-131">ID3DX10ThreadPump</span><span class="sxs-lookup"><span data-stu-id="f0220-131">ID3DX10ThreadPump</span></span>](id3dx10threadpump.md)
</dt> <dt>

[<span data-ttu-id="f0220-132">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="f0220-132">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




