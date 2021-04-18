---
description: Obtenha um ponteiro de interface de dispositivo do Direct3D 10,1 de um ponteiro de interface do Direct3D 10,0.
ms.assetid: cf31a67f-0493-4e79-8e73-0297ab93bbae
title: Função D3DX10GetFeatureLevel1 (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10GetFeatureLevel1
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 817eb4dd68ce797da76c0609e2ead01a21b5b270
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105780276"
---
# <a name="d3dx10getfeaturelevel1-function"></a><span data-ttu-id="3398a-103">Função D3DX10GetFeatureLevel1</span><span class="sxs-lookup"><span data-stu-id="3398a-103">D3DX10GetFeatureLevel1 function</span></span>

<span data-ttu-id="3398a-104">Obtenha um ponteiro de interface de dispositivo do Direct3D 10,1 de um ponteiro de interface do Direct3D 10,0.</span><span class="sxs-lookup"><span data-stu-id="3398a-104">Get a Direct3D 10.1 device interface pointer from a Direct3D 10.0 interface pointer.</span></span>

## <a name="syntax"></a><span data-ttu-id="3398a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3398a-105">Syntax</span></span>


```C++
HRESULT D3DX10GetFeatureLevel1(
  _In_  ID3D10Device  *pDevice,
  _Out_ ID3D10Device1 **ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="3398a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3398a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3398a-107">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3398a-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3398a-108">Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="3398a-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="3398a-109">Ponteiro para o dispositivo Direct3D 10,0 (consulte a interface [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) ).</span><span class="sxs-lookup"><span data-stu-id="3398a-109">Pointer to the Direct3D 10.0 device (see the [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) interface).</span></span>

</dd> <dt>

<span data-ttu-id="3398a-110">*ppDevice* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3398a-110">*ppDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3398a-111">Tipo: **[ **ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1)\*\***</span><span class="sxs-lookup"><span data-stu-id="3398a-111">Type: **[**ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1)\*\***</span></span>

<span data-ttu-id="3398a-112">Ponteiro para o dispositivo Direct3D 10,1 (consulte a interface [**ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) ).</span><span class="sxs-lookup"><span data-stu-id="3398a-112">Pointer to the Direct3D 10.1 device (see the [**ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) interface).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3398a-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3398a-113">Return value</span></span>

<span data-ttu-id="3398a-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3398a-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3398a-115">Essa função retorna um dos seguintes [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="3398a-115">This function returns one of the following [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span> <span data-ttu-id="3398a-116">Se uma interface de dispositivo do Direct3D 10,1 puder ser adquirida, essa função terá sucesso e passará um ponteiro para a interface 10,1 usando o parâmetro *ppDevice* .</span><span class="sxs-lookup"><span data-stu-id="3398a-116">If a Direct3D 10.1 device interface can be acquired, this function succeeds and passes a pointer to the 10.1 interface using the *ppDevice* parameter.</span></span> <span data-ttu-id="3398a-117">Se uma interface de dispositivo Direct3D 10,1 não puder ser adquirida, essa função retornará E \_ falhará e não retornará nada para o parâmetro *ppDevice* .</span><span class="sxs-lookup"><span data-stu-id="3398a-117">If a Direct3D 10.1 device interface cannot be acquired, this function returns E\_FAIL, and will not return anything for the *ppDevice* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="3398a-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="3398a-118">Remarks</span></span>

<span data-ttu-id="3398a-119">Para que essa função tenha sucesso, você deve ter adquirido o ponteiro [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) fornecido usando uma chamada para a função [**D3DX10CreateDevice**](d3dx10createdevice.md) , a função [**D3DX10CreateDeviceAndSwapChain**](d3dx10createdeviceandswapchain.md) , a função [**D3D10CreateDevice1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdevice1) ou a função [**D3D10CreateDeviceAndSwapChain1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdeviceandswapchain1) .</span><span class="sxs-lookup"><span data-stu-id="3398a-119">For this function to succeed, you must have acquired the supplied [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) pointer using a call to the [**D3DX10CreateDevice**](d3dx10createdevice.md) function, the [**D3DX10CreateDeviceAndSwapChain**](d3dx10createdeviceandswapchain.md) function, the [**D3D10CreateDevice1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdevice1) function, or the [**D3D10CreateDeviceAndSwapChain1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdeviceandswapchain1) function.</span></span>

<span data-ttu-id="3398a-120">Você só pode criar um dispositivo Direct3D 10,1 em computadores que executam o Windows Vista Service Pack 1 ou posterior e com hardware compatível com Direct3D 10,1 instalado.</span><span class="sxs-lookup"><span data-stu-id="3398a-120">You can only create a Direct3D 10.1 device on computers running Windows Vista Service Pack 1 or later, and with Direct3D 10.1-compatible hardware installed.</span></span> <span data-ttu-id="3398a-121">Essa função retornará E \_ falhará em qualquer computador que não atenda a esses requisitos.</span><span class="sxs-lookup"><span data-stu-id="3398a-121">This function will return E\_FAIL on any computer not meeting these requirements.</span></span> <span data-ttu-id="3398a-122">No entanto, você pode chamar essa função em qualquer versão do Windows que tenha a DLL D3DX10 instalada.</span><span class="sxs-lookup"><span data-stu-id="3398a-122">However, you can call this function on any version of Windows that has the D3DX10 DLL installed.</span></span>

## <a name="requirements"></a><span data-ttu-id="3398a-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3398a-123">Requirements</span></span>



| <span data-ttu-id="3398a-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="3398a-124">Requirement</span></span> | <span data-ttu-id="3398a-125">Valor</span><span class="sxs-lookup"><span data-stu-id="3398a-125">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3398a-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3398a-126">Header</span></span><br/> | <dl> <span data-ttu-id="3398a-127"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="3398a-127"><dt>D3DX10Core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3398a-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="3398a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3398a-129">Funções de Uso Geral</span><span class="sxs-lookup"><span data-stu-id="3398a-129">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 




