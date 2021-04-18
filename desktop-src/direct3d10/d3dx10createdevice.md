---
description: Crie o melhor dispositivo Direct3D 10 que representa o adaptador de vídeo. Se um dispositivo compatível com Direct3D 10,1 puder ser criado, será possível adquirir um ponteiro de interface ID3D10Device1 do ponteiro de interface do dispositivo retornado.
ms.assetid: 1af8f4e5-a59e-403a-95d2-069b91bad93e
title: Função D3DX10CreateDevice (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateDevice
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 38236a48cdd5197f7f19ef9be3f6fc0f1faca72c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105785194"
---
# <a name="d3dx10createdevice-function"></a><span data-ttu-id="922b6-104">Função D3DX10CreateDevice</span><span class="sxs-lookup"><span data-stu-id="922b6-104">D3DX10CreateDevice function</span></span>

<span data-ttu-id="922b6-105">Crie o melhor dispositivo Direct3D 10 que representa o adaptador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="922b6-105">Create the best Direct3D 10 device that represents the display adapter.</span></span> <span data-ttu-id="922b6-106">Se um dispositivo compatível com Direct3D 10,1 puder ser criado, será possível adquirir um ponteiro de [**interface ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) do ponteiro de interface do dispositivo retornado.</span><span class="sxs-lookup"><span data-stu-id="922b6-106">If a Direct3D 10.1-compatible device can be created, it will be possible to acquire an [**ID3D10Device1 Interface**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) pointer from the returned device interface pointer.</span></span>

## <a name="syntax"></a><span data-ttu-id="922b6-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="922b6-107">Syntax</span></span>


```C++
HRESULT D3DX10CreateDevice(
  _In_  IDXGIAdapter      *pAdapter,
  _In_  D3D10_DRIVER_TYPE DriverType,
  _In_  HMODULE           Software,
  _In_  UINT              Flags,
  _Out_ ID3D10Device      **ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="922b6-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="922b6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="922b6-109">*pAdapter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="922b6-109">*pAdapter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="922b6-110">Tipo: **[ **IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter)\***</span><span class="sxs-lookup"><span data-stu-id="922b6-110">Type: **[**IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter)\***</span></span>

<span data-ttu-id="922b6-111">Ponteiro para o adaptador de vídeo (consulte a interface [**IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter) ) ao criar um dispositivo de hardware; caso contrário, defina esse parâmetro como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="922b6-111">Pointer to the display adapter (see the [**IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter) interface) when creating a hardware device; otherwise set this parameter to **NULL**.</span></span> <span data-ttu-id="922b6-112">Se **NULL** for especificado ao criar um dispositivo de hardware, o Direct3D usará o primeiro adaptador enumerado pela interface [**IDXGIFactory**](/windows/win32/api/dxgi/nn-dxgi-idxgifactory) .</span><span class="sxs-lookup"><span data-stu-id="922b6-112">If **NULL** is specified when creating a hardware device, Direct3D will use the first adapter enumerated by the [**IDXGIFactory**](/windows/win32/api/dxgi/nn-dxgi-idxgifactory) interface.</span></span>

</dd> <dt>

<span data-ttu-id="922b6-113">*DriverType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="922b6-113">*DriverType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="922b6-114">Tipo: **[ **\_ \_ tipo de driver d3d10**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type)**</span><span class="sxs-lookup"><span data-stu-id="922b6-114">Type: **[**D3D10\_DRIVER\_TYPE**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type)**</span></span>

<span data-ttu-id="922b6-115">O tipo de driver de dispositivo (consulte a enumeração de [**\_ \_ tipo de driver d3d10**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type) ).</span><span class="sxs-lookup"><span data-stu-id="922b6-115">The device-driver type (see the [**D3D10\_DRIVER\_TYPE**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type) enumeration).</span></span> <span data-ttu-id="922b6-116">O tipo de driver determina o tipo de dispositivo que você criará.</span><span class="sxs-lookup"><span data-stu-id="922b6-116">The driver type determines the type of device you will create.</span></span>

</dd> <dt>

<span data-ttu-id="922b6-117">*Software* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="922b6-117">*Software* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="922b6-118">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="922b6-118">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="922b6-119">Um identificador para um módulo carregado que implementa um driver de software (como D3D10Ref.dll).</span><span class="sxs-lookup"><span data-stu-id="922b6-119">A handle to a loaded module that implements a software driver (such as D3D10Ref.dll).</span></span> <span data-ttu-id="922b6-120">Para obter um identificador, chame a função [GetModuleHandle](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea) .</span><span class="sxs-lookup"><span data-stu-id="922b6-120">To get a handle, call the [GetModuleHandle](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea) function.</span></span>

</dd> <dt>

<span data-ttu-id="922b6-121">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="922b6-121">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="922b6-122">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="922b6-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="922b6-123">Sinalizadores de criação de dispositivo (consulte a enumeração [**\_ criar \_ \_ sinalizador de dispositivo d3d10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag) ) que habilitam [camadas de API](d3d10-graphics-programming-guide-api-features-layers.md).</span><span class="sxs-lookup"><span data-stu-id="922b6-123">Device creation flags (see the [**D3D10\_CREATE\_DEVICE\_FLAG**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag) enumeration) that enable [API layers](d3d10-graphics-programming-guide-api-features-layers.md).</span></span> <span data-ttu-id="922b6-124">Esses sinalizadores podem ser unificados ou juntos.</span><span class="sxs-lookup"><span data-stu-id="922b6-124">These flags can be bitwise OR'd together.</span></span>

</dd> <dt>

<span data-ttu-id="922b6-125">*ppDevice* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="922b6-125">*ppDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="922b6-126">Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***</span><span class="sxs-lookup"><span data-stu-id="922b6-126">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***</span></span>

<span data-ttu-id="922b6-127">Endereço de um ponteiro para o dispositivo criado (consulte a interface [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) ).</span><span class="sxs-lookup"><span data-stu-id="922b6-127">Address of a pointer to the device created (see the [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) interface).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="922b6-128">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="922b6-128">Return value</span></span>

<span data-ttu-id="922b6-129">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="922b6-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="922b6-130">Essa função retorna um dos seguintes [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="922b6-130">This function returns one of the following [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="922b6-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="922b6-131">Remarks</span></span>

<span data-ttu-id="922b6-132">Essa função tenta criar o melhor dispositivo para o hardware.</span><span class="sxs-lookup"><span data-stu-id="922b6-132">This function attempts to create the best device for the hardware.</span></span> <span data-ttu-id="922b6-133">Primeiro, a função tenta criar um dispositivo 10,1.</span><span class="sxs-lookup"><span data-stu-id="922b6-133">First, the function attempts to create a 10.1 device.</span></span> <span data-ttu-id="922b6-134">Se um dispositivo 10,1 não puder ser criado, a função tentará criar um dispositivo 10,0.</span><span class="sxs-lookup"><span data-stu-id="922b6-134">If a 10.1 device cannot be created, the function attempts to create a 10.0 device.</span></span> <span data-ttu-id="922b6-135">Se nenhum dispositivo for criado com êxito, a função retornará E \_ falhará.</span><span class="sxs-lookup"><span data-stu-id="922b6-135">If neither device is successfully created, the function returns E\_FAIL.</span></span>

<span data-ttu-id="922b6-136">Se seu aplicativo precisar criar apenas um dispositivo 10,1 ou um dispositivo 10,0, use as seguintes funções:</span><span class="sxs-lookup"><span data-stu-id="922b6-136">If your application needs to create only a 10.1 device, or a 10.0 device only, use the following functions instead:</span></span>

-   <span data-ttu-id="922b6-137">Use a função [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice) para criar apenas um dispositivo Direct3D 10,0.</span><span class="sxs-lookup"><span data-stu-id="922b6-137">Use the [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice) function to create a Direct3D 10.0 device only.</span></span>
-   <span data-ttu-id="922b6-138">Use a função [**D3D10CreateDevice1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdevice1) para criar apenas um dispositivo Direct3D 10,1.</span><span class="sxs-lookup"><span data-stu-id="922b6-138">Use the [**D3D10CreateDevice1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdevice1) function to create a Direct3D 10.1 device only.</span></span>
-   <span data-ttu-id="922b6-139">Use a função [**D3DX10GetFeatureLevel1**](d3dx10getfeaturelevel1.md) para obter um ponteiro de interface [**ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) de um ponteiro de interface [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) .</span><span class="sxs-lookup"><span data-stu-id="922b6-139">Use the [**D3DX10GetFeatureLevel1**](d3dx10getfeaturelevel1.md) function to get an [**ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) interface pointer from an [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) interface pointer.</span></span>

<span data-ttu-id="922b6-140">Um dispositivo Direct3D 10,1 só pode ser criado em computadores que executam o Windows Vista Service Pack 1 ou posterior e com hardware compatível com Direct3D 10,1 instalado.</span><span class="sxs-lookup"><span data-stu-id="922b6-140">A Direct3D 10.1 device can only be created on computers running Windows Vista Service Pack 1 or later, and with Direct3D 10.1-compatible hardware installed.</span></span> <span data-ttu-id="922b6-141">No entanto, é legal chamar essa função em computadores que executam qualquer versão do Windows que tenha a DLL D3DX10 instalada.</span><span class="sxs-lookup"><span data-stu-id="922b6-141">However, it is legal to call this function on computers running any version of Windows that has the D3DX10 DLL installed.</span></span>

## <a name="requirements"></a><span data-ttu-id="922b6-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="922b6-142">Requirements</span></span>



| <span data-ttu-id="922b6-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="922b6-143">Requirement</span></span> | <span data-ttu-id="922b6-144">Valor</span><span class="sxs-lookup"><span data-stu-id="922b6-144">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="922b6-145">parâmetro</span><span class="sxs-lookup"><span data-stu-id="922b6-145">Header</span></span><br/> | <dl> <span data-ttu-id="922b6-146"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="922b6-146"><dt>D3DX10Core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="922b6-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="922b6-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="922b6-148">Funções de Uso Geral</span><span class="sxs-lookup"><span data-stu-id="922b6-148">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
