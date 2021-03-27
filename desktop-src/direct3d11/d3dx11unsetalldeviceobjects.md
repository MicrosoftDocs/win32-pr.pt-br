---
title: Função D3DX11UnsetAllDeviceObjects (D3DX11core. h)
description: Observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Observação em vez de usar essa função, recomendamos que você use o método Clearstate ID3D11DeviceContext.
ms.assetid: 0e52bbca-f171-477f-89b0-ba56a2cfa096
keywords:
- Função D3DX11UnsetAllDeviceObjects Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11UnsetAllDeviceObjects
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8ac7e33bfef7f8470f616ac07b3aa90463f3f3a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298717"
---
# <a name="d3dx11unsetalldeviceobjects-function"></a><span data-ttu-id="c3dd9-105">Função D3DX11UnsetAllDeviceObjects</span><span class="sxs-lookup"><span data-stu-id="c3dd9-105">D3DX11UnsetAllDeviceObjects function</span></span>

> [!Note]  
> <span data-ttu-id="c3dd9-106">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="c3dd9-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="c3dd9-107">Em vez de usar essa função, recomendamos que você use o método [**ID3D11DeviceContext:: clearstate**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-clearstate) .</span><span class="sxs-lookup"><span data-stu-id="c3dd9-107">Instead of using this function, we recommend that you use the [**ID3D11DeviceContext::ClearState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-clearstate) method.</span></span>

 

<span data-ttu-id="c3dd9-108">Remove todos os recursos do dispositivo definindo seus ponteiros como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="c3dd9-108">Removes all resources from the device by setting their pointers to **NULL**.</span></span> <span data-ttu-id="c3dd9-109">Isso deve ser chamado durante o desligamento do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c3dd9-109">This should be called during shutdown of your application.</span></span> <span data-ttu-id="c3dd9-110">Ele ajuda a garantir que, quando um estiver liberando todos os seus recursos, nenhum deles esteja associado ao dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c3dd9-110">It helps ensure that when one is releasing all of their resources that none of them are bound to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3dd9-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c3dd9-111">Syntax</span></span>


```C++
HRESULT D3DX11UnsetAllDeviceObjects(
  _In_ ID3D11DeviceContext *pContext
);
```



## <a name="parameters"></a><span data-ttu-id="c3dd9-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c3dd9-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3dd9-113">*pContext* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c3dd9-113">*pContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3dd9-114">Tipo: **[ **ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span><span class="sxs-lookup"><span data-stu-id="c3dd9-114">Type: **[**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span></span>

<span data-ttu-id="c3dd9-115">Ponteiro para um objeto [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .</span><span class="sxs-lookup"><span data-stu-id="c3dd9-115">Pointer to an [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3dd9-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c3dd9-116">Return value</span></span>

<span data-ttu-id="c3dd9-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c3dd9-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c3dd9-118">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="c3dd9-118">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c3dd9-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3dd9-119">Requirements</span></span>



| <span data-ttu-id="c3dd9-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3dd9-120">Requirement</span></span> | <span data-ttu-id="c3dd9-121">Valor</span><span class="sxs-lookup"><span data-stu-id="c3dd9-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c3dd9-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c3dd9-122">Header</span></span><br/>  | <dl> <span data-ttu-id="c3dd9-123"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3dd9-123"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="c3dd9-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c3dd9-124">Library</span></span><br/> | <dl> <span data-ttu-id="c3dd9-125"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c3dd9-125"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c3dd9-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="c3dd9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3dd9-127">Funções D3DX</span><span class="sxs-lookup"><span data-stu-id="c3dd9-127">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

 





