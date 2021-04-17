---
description: Remove todos os recursos do dispositivo definindo seus ponteiros como NULL. Isso deve ser chamado durante o desligamento do seu aplicativo. Ele ajuda a garantir que, quando um estiver liberando todos os seus recursos, nenhum deles esteja associado ao dispositivo.
ms.assetid: f41ce97e-5a81-43a4-a8c7-7411b43c0d61
title: Função D3DX10UnsetAllDeviceObjects (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10UnsetAllDeviceObjects
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4d3a113be935f77dbd62b2f3fac4c16c7cac9881
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105764003"
---
# <a name="d3dx10unsetalldeviceobjects-function"></a><span data-ttu-id="6995d-105">Função D3DX10UnsetAllDeviceObjects</span><span class="sxs-lookup"><span data-stu-id="6995d-105">D3DX10UnsetAllDeviceObjects function</span></span>

<span data-ttu-id="6995d-106">Remove todos os recursos do dispositivo definindo seus ponteiros como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="6995d-106">Removes all resources from the device by setting their pointers to **NULL**.</span></span> <span data-ttu-id="6995d-107">Isso deve ser chamado durante o desligamento do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6995d-107">This should be called during shutdown of your application.</span></span> <span data-ttu-id="6995d-108">Ele ajuda a garantir que, quando um estiver liberando todos os seus recursos, nenhum deles esteja associado ao dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6995d-108">It helps ensure that when one is releasing all of their resources that none of them are bound to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="6995d-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6995d-109">Syntax</span></span>


```C++
HRESULT D3DX10UnsetAllDeviceObjects(
  _In_ ID3D10Device *pDevice
);
```



## <a name="parameters"></a><span data-ttu-id="6995d-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6995d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6995d-111">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6995d-111">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6995d-112">Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="6995d-112">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="6995d-113">Ponteiro para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6995d-113">Pointer to the device.</span></span> <span data-ttu-id="6995d-114">Consulte a [**interface ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device).</span><span class="sxs-lookup"><span data-stu-id="6995d-114">See [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6995d-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6995d-115">Return value</span></span>

<span data-ttu-id="6995d-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6995d-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6995d-117">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="6995d-117">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6995d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6995d-118">Requirements</span></span>



| <span data-ttu-id="6995d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="6995d-119">Requirement</span></span> | <span data-ttu-id="6995d-120">Valor</span><span class="sxs-lookup"><span data-stu-id="6995d-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6995d-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6995d-121">Header</span></span><br/>  | <dl> <span data-ttu-id="6995d-122"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="6995d-122"><dt>D3DX10Core.h</dt></span></span> </dl> |
| <span data-ttu-id="6995d-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6995d-123">Library</span></span><br/> | <dl> <span data-ttu-id="6995d-124"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6995d-124"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6995d-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="6995d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6995d-126">Funções de Uso Geral</span><span class="sxs-lookup"><span data-stu-id="6995d-126">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 




