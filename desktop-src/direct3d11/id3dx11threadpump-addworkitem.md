---
title: Método AddWorkItem ID3DX11ThreadPump (D3DX11core. h)
description: Observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Adiciona um item de trabalho à bomba do thread.
ms.assetid: 2578506c-6175-457a-bf10-94929bb3c0c4
keywords:
- Método AddWorkItem Direct3D 11
- Método AddWorkItem Direct3D 11, interface ID3DX11ThreadPump
- Interface ID3DX11ThreadPump Direct3D 11, método AddWorkItem
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump.AddWorkItem
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebf249405bd71287f93444ae8d23dab694027360
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298504"
---
# <a name="id3dx11threadpumpaddworkitem-method"></a><span data-ttu-id="70d46-107">Método ID3DX11ThreadPump:: AddWorkItem</span><span class="sxs-lookup"><span data-stu-id="70d46-107">ID3DX11ThreadPump::AddWorkItem method</span></span>

> [!Note]  
> <span data-ttu-id="70d46-108">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="70d46-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="70d46-109">Adiciona um item de trabalho à bomba do thread.</span><span class="sxs-lookup"><span data-stu-id="70d46-109">Adds a work item to the thread pump.</span></span>

## <a name="syntax"></a><span data-ttu-id="70d46-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="70d46-110">Syntax</span></span>


```C++
HRESULT AddWorkItem(
  [in]  ID3DX11DataLoader    *pDataLoader,
  [in]  ID3DX11DataProcessor *pDataProcessor,
  [in]  HRESULT              *pHResult,
  [out] void                 **ppDeviceObject
);
```



## <a name="parameters"></a><span data-ttu-id="70d46-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="70d46-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70d46-112">*pDataLoader* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="70d46-112">*pDataLoader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70d46-113">Tipo: **[ **ID3DX11DataLoader**](id3dx11dataloader.md)\***</span><span class="sxs-lookup"><span data-stu-id="70d46-113">Type: **[**ID3DX11DataLoader**](id3dx11dataloader.md)\***</span></span>

<span data-ttu-id="70d46-114">O carregador que será usado pela bomba de thread quando um item de trabalho exigir que os dados sejam carregados.</span><span class="sxs-lookup"><span data-stu-id="70d46-114">The loader that the thread pump will use when a work item requires data to be loaded.</span></span>

</dd> <dt>

<span data-ttu-id="70d46-115">*pDataProcessor* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="70d46-115">*pDataProcessor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70d46-116">Tipo: **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\***</span><span class="sxs-lookup"><span data-stu-id="70d46-116">Type: **[**ID3DX11DataProcessor**](id3dx11dataprocessor.md)\***</span></span>

<span data-ttu-id="70d46-117">O processador que a bomba de thread usará quando um item de trabalho exigir que os dados sejam processados.</span><span class="sxs-lookup"><span data-stu-id="70d46-117">The processor that the thread pump will use when a work item requires data to be processed.</span></span>

</dd> <dt>

<span data-ttu-id="70d46-118">*pHResult* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="70d46-118">*pHResult* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70d46-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="70d46-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="70d46-120">Um ponteiro para o valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="70d46-120">A pointer to the return value.</span></span> <span data-ttu-id="70d46-121">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="70d46-121">May be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="70d46-122">*ppDeviceObject* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="70d46-122">*ppDeviceObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="70d46-123">Tipo: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="70d46-123">Type: **void\*\***</span></span>

<span data-ttu-id="70d46-124">O dispositivo que usa o objeto.</span><span class="sxs-lookup"><span data-stu-id="70d46-124">The device that uses the object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70d46-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="70d46-125">Return value</span></span>

<span data-ttu-id="70d46-126">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="70d46-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="70d46-127">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="70d46-127">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="70d46-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70d46-128">Requirements</span></span>



| <span data-ttu-id="70d46-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="70d46-129">Requirement</span></span> | <span data-ttu-id="70d46-130">Valor</span><span class="sxs-lookup"><span data-stu-id="70d46-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="70d46-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="70d46-131">Header</span></span><br/>  | <dl> <span data-ttu-id="70d46-132"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="70d46-132"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="70d46-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="70d46-133">Library</span></span><br/> | <dl> <span data-ttu-id="70d46-134"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="70d46-134"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="70d46-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="70d46-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70d46-136">ID3DX11ThreadPump</span><span class="sxs-lookup"><span data-stu-id="70d46-136">ID3DX11ThreadPump</span></span>](id3dx11threadpump.md)
</dt> <dt>

[<span data-ttu-id="70d46-137">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="70d46-137">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





