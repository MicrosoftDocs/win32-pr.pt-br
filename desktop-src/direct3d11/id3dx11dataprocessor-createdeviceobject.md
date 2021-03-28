---
title: Método deviceobject ID3DX11DataProcessor (D3DX11core. h)
description: Observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Cria um objeto de dispositivo.
ms.assetid: 797d216b-2f54-4d24-aa97-04be0c71f909
keywords:
- Método createdeviceobject Direct3D 11
- Método deviceobject Direct3D 11, interface ID3DX11DataProcessor
- Interface ID3DX11DataProcessor Direct3D 11, método deviceobject
topic_type:
- apiref
api_name:
- ID3DX11DataProcessor.CreateDeviceObject
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6ff178cec1830d1b0213af23a2a70654416d35e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298856"
---
# <a name="id3dx11dataprocessorcreatedeviceobject-method"></a><span data-ttu-id="5a9db-107">Método ID3DX11DataProcessor:: deviceobject</span><span class="sxs-lookup"><span data-stu-id="5a9db-107">ID3DX11DataProcessor::CreateDeviceObject method</span></span>

> [!Note]  
> <span data-ttu-id="5a9db-108">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="5a9db-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="5a9db-109">Cria um objeto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5a9db-109">Creates a device object.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a9db-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5a9db-110">Syntax</span></span>


```C++
HRESULT CreateDeviceObject(
  [out] void **ppDataObject
);
```



## <a name="parameters"></a><span data-ttu-id="5a9db-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5a9db-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a9db-112">*ppDataObject* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5a9db-112">*ppDataObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a9db-113">Tipo: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="5a9db-113">Type: **void\*\***</span></span>

<span data-ttu-id="5a9db-114">Endereço de um ponteiro para o objeto de dispositivo criado.</span><span class="sxs-lookup"><span data-stu-id="5a9db-114">Address of a pointer to the created device object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a9db-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5a9db-115">Return value</span></span>

<span data-ttu-id="5a9db-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5a9db-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5a9db-117">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="5a9db-117">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5a9db-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="5a9db-118">Remarks</span></span>

<span data-ttu-id="5a9db-119">Esse método é usado por uma [**interface ID3DX11ThreadPump**](id3dx11threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="5a9db-119">This method is used by an [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5a9db-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a9db-120">Requirements</span></span>



| <span data-ttu-id="5a9db-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a9db-121">Requirement</span></span> | <span data-ttu-id="5a9db-122">Valor</span><span class="sxs-lookup"><span data-stu-id="5a9db-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a9db-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5a9db-123">Header</span></span><br/>  | <dl> <span data-ttu-id="5a9db-124"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a9db-124"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="5a9db-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5a9db-125">Library</span></span><br/> | <dl> <span data-ttu-id="5a9db-126"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5a9db-126"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5a9db-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="5a9db-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a9db-128">ID3DX11DataProcessor</span><span class="sxs-lookup"><span data-stu-id="5a9db-128">ID3DX11DataProcessor</span></span>](id3dx11dataprocessor.md)
</dt> <dt>

[<span data-ttu-id="5a9db-129">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="5a9db-129">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





