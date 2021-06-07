---
UID: NF:directml.DMLCreateDevice1
title: Função DMLCreateDevice1
description: Cria um dispositivo DirectML para um determinado dispositivo Direct3D 12.
helpviewer_keywords:
- DMLCreateDevice1
- DMLCreateDevice1 function
- direct3d12.dmlcreatedevice1
- directml/DMLCreateDevice1
ms.topic: reference
tech.root: directml
ms.date: 11/04/2020
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: DirectML.lib
req.dll: DirectML.dll
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DMLCreateDevice1
- directml/DMLCreateDevice1
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- DirectML.dll
api_name:
- DMLCreateDevice1
ms.openlocfilehash: f722b12208bd808f01e177feb907f94c33541496
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111416921"
---
# <a name="dmlcreatedevice1-function-directmlh"></a><span data-ttu-id="035da-103">Função DMLCreateDevice1 (directml. h)</span><span class="sxs-lookup"><span data-stu-id="035da-103">DMLCreateDevice1 function (directml.h)</span></span>

<span data-ttu-id="035da-104">Cria um dispositivo DirectML para um determinado dispositivo Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="035da-104">Creates a DirectML device for a given Direct3D 12 device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="035da-105">Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1,4 e posterior.</span><span class="sxs-lookup"><span data-stu-id="035da-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="035da-106">Consulte também o [histórico de versão do DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="035da-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="035da-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="035da-107">Syntax</span></span>

```cpp
HRESULT DMLCreateDevice1(
  ID3D12Device            *d3d12Device,
  DML_CREATE_DEVICE_FLAGS flags,
  DML_FEATURE_LEVEL       minimumFeatureLevel,
  REFIID                  riid,
  void                    **ppv
);
```

## <a name="parameters"></a><span data-ttu-id="035da-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="035da-108">Parameters</span></span>

`d3d12Device`

<span data-ttu-id="035da-109">Tipo: <b> <a href="/windows/win32/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>\*</b></span><span class="sxs-lookup"><span data-stu-id="035da-109">Type: <b><a href="/windows/win32/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>\*</b></span></span>

<span data-ttu-id="035da-110">Um ponteiro para um [ID3D12Device](/windows/win32/api/d3d12/nn-d3d12-id3d12device) que representa o dispositivo Direct3D 12 para criar o dispositivo DirectML.</span><span class="sxs-lookup"><span data-stu-id="035da-110">A pointer to an [ID3D12Device](/windows/win32/api/d3d12/nn-d3d12-id3d12device) representing the Direct3D 12 device to create the DirectML device over.</span></span> <span data-ttu-id="035da-111">O DirectML dá suporte a qualquer nível de recurso do D3D e a dispositivos Direct3D 12 criados em qualquer adaptador, incluindo WARPing.</span><span class="sxs-lookup"><span data-stu-id="035da-111">DirectML supports any D3D feature level, and Direct3D 12 devices created on any adapter, including WARP.</span></span> <span data-ttu-id="035da-112">No entanto, nem todos os recursos do DirectML podem estar disponíveis dependendo dos recursos do dispositivo Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="035da-112">However, not all features in DirectML may be available depending on the capabilities of the Direct3D 12 device.</span></span> <span data-ttu-id="035da-113">Consulte [IDMLDevice:: CheckFeatureSupport](/windows/win32/api/directml/nf-directml-idmldevice-checkfeaturesupport) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="035da-113">See [IDMLDevice::CheckFeatureSupport](/windows/win32/api/directml/nf-directml-idmldevice-checkfeaturesupport) for more info.</span></span>

<span data-ttu-id="035da-114">Se a chamada para **DMLCreateDevice1** for bem-sucedida, o dispositivo DirectML manterá uma referência forte para o dispositivo Direct3D 12 fornecido.</span><span class="sxs-lookup"><span data-stu-id="035da-114">If the call to **DMLCreateDevice1** is successful, then the DirectML device maintains a strong reference to the supplied Direct3D 12 device.</span></span>

`flags`

<span data-ttu-id="035da-115">Tipo: <b>DML_CREATE_DEVICE_FLAGS</b></span><span class="sxs-lookup"><span data-stu-id="035da-115">Type: <b>DML_CREATE_DEVICE_FLAGS</b></span></span>

<span data-ttu-id="035da-116">Um valor [DML_CREATE_DEVICE_FLAGS](/windows/win32/api/directml/ne-directml-dml_create_device_flags) especificando opções de criação de dispositivo adicionais.</span><span class="sxs-lookup"><span data-stu-id="035da-116">A [DML_CREATE_DEVICE_FLAGS](/windows/win32/api/directml/ne-directml-dml_create_device_flags) value specifying additional device creation options.</span></span>

`minimumFeatureLevel`

<span data-ttu-id="035da-117">Tipo: <b>DML_FEATURE_LEVEL</b></span><span class="sxs-lookup"><span data-stu-id="035da-117">Type: <b>DML_FEATURE_LEVEL</b></span></span>

<span data-ttu-id="035da-118">Um valor [DML_FEATURE_LEVEL](/windows/win32/api/directml/ne-directml-dml_feature_level) especificando o suporte mínimo de nível de recurso necessário.</span><span class="sxs-lookup"><span data-stu-id="035da-118">A [DML_FEATURE_LEVEL](/windows/win32/api/directml/ne-directml-dml_feature_level) value specifying the minimum feature level support required.</span></span>

<span data-ttu-id="035da-119">Esse parâmetro pode ser útil para chamadores que exigem uma versão específica do DirectML, mas que podem se chamar em uma versão mais antiga do DirectML.</span><span class="sxs-lookup"><span data-stu-id="035da-119">This parameter can be useful for callers that require a specific version of DirectML, but who may find themselves calling into an older version of DirectML.</span></span> <span data-ttu-id="035da-120">Isso pode acontecer, por exemplo, quando o usuário executa seu aplicativo em uma versão mais antiga do Windows 10.</span><span class="sxs-lookup"><span data-stu-id="035da-120">This can happen, for example, when the user runs your application on an older version of Windows 10.</span></span>

<span data-ttu-id="035da-121">Os aplicativos que dependem explicitamente da funcionalidade introduzida em um nível de recurso específico podem especificá-lo como um *minimumFeatureLevel*.</span><span class="sxs-lookup"><span data-stu-id="035da-121">Applications that explicitly depend on functionality introduced in a particular feature level can specify it as a *minimumFeatureLevel*.</span></span> <span data-ttu-id="035da-122">Isso garantirá que o **DMLCreateDevice1** não terá sucesso, a menos que a implementação subjacente seja *pelo menos* compatível com o nível de recurso mínimo solicitado.</span><span class="sxs-lookup"><span data-stu-id="035da-122">This will guarantee that **DMLCreateDevice1** won't succeed unless the underlying implementation is *at least* as capable as this requested minimum feature level.</span></span>

<span data-ttu-id="035da-123">Observe que, como esse parâmetro especifica um nível de recurso *mínimo* , o dispositivo DirectML subjacente pode, na verdade, dar suporte a um nível de recurso mais alto do que o mínimo solicitado.</span><span class="sxs-lookup"><span data-stu-id="035da-123">Note that as this parameter specifies a *minimum* feature level, the underlying DirectML device may in fact support a higher feature level than the requested minimum.</span></span> <span data-ttu-id="035da-124">Depois que a criação do dispositivo for realizada com sucesso, você poderá consultar todos os níveis de recurso com suporte neste dispositivo usando [IDMLDevice:: CheckFeatureSupport](/windows/win32/api/directml/nf-directml-idmldevice-checkfeaturesupport).</span><span class="sxs-lookup"><span data-stu-id="035da-124">Once device creation succeeds, you can query all of the feature levels supported by this device using [IDMLDevice::CheckFeatureSupport](/windows/win32/api/directml/nf-directml-idmldevice-checkfeaturesupport).</span></span>

`riid`

<span data-ttu-id="035da-125">Tipo: <b>REFIID</b></span><span class="sxs-lookup"><span data-stu-id="035da-125">Type: <b>REFIID</b></span></span>

<span data-ttu-id="035da-126">Uma referência ao GUID (identificador global exclusivo) da interface que você deseja retornar no <i>dispositivo</i>.</span><span class="sxs-lookup"><span data-stu-id="035da-126">A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in <i>device</i>.</span></span> <span data-ttu-id="035da-127">Espera-se que seja o GUID de [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice).</span><span class="sxs-lookup"><span data-stu-id="035da-127">This is expected to be the GUID of [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice).</span></span>

`ppv`

<span data-ttu-id="035da-128">Tipo: \_ com \_ Outptr \_ opt \_ <b>void \* \*</b></span><span class="sxs-lookup"><span data-stu-id="035da-128">Type: \_COM\_Outptr\_opt\_ <b>void\*\*</b></span></span>

<span data-ttu-id="035da-129">Um ponteiro para um bloco de memória que recebe um ponteiro para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="035da-129">A pointer to a memory block that receives a pointer to the device.</span></span> <span data-ttu-id="035da-130">Esse é o endereço de um ponteiro para um [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice), representando o dispositivo DirectML criado.</span><span class="sxs-lookup"><span data-stu-id="035da-130">This is the address of a pointer to an [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice), representing  the DirectML device created.</span></span>


## <a name="return-value"></a><span data-ttu-id="035da-131">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="035da-131">Return value</span></span>

<span data-ttu-id="035da-132">Tipo: [ **HRESULT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="035da-132">Type: [**HRESULT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="035da-133">Se a função for realizada com sucesso, ela retornará <b>S_OK</b>.</span><span class="sxs-lookup"><span data-stu-id="035da-133">If the function succeeds, it returns <b>S_OK</b>.</span></span> <span data-ttu-id="035da-134">Caso contrário, ele retorna um código de erro [HRESULT](/windows/desktop/winprog/windows-data-types) .</span><span class="sxs-lookup"><span data-stu-id="035da-134">Otherwise, it returns an [HRESULT](/windows/desktop/winprog/windows-data-types) error code.</span></span>

<span data-ttu-id="035da-135">Se esta versão do DirectML não oferecer suporte ao *minimumFeatureLevel* solicitado, essa função retornará **DXGI_ERROR_UNSUPPORTED**.</span><span class="sxs-lookup"><span data-stu-id="035da-135">If this version of DirectML doesn't support the *minimumFeatureLevel* requested, then this function will return **DXGI_ERROR_UNSUPPORTED**.</span></span>

<span data-ttu-id="035da-136">O FOD (recurso de ferramentas de gráficos sob demanda) deve ser instalado para usar as camadas de depuração do DirectML.</span><span class="sxs-lookup"><span data-stu-id="035da-136">The Graphics Tools Feature on Demand (FOD) must be installed in order to use the DirectML debug layers.</span></span> <span data-ttu-id="035da-137">Se o sinalizador de [DML_CREATE_DEVICE_FLAG_DEBUG](/windows/win32/api/directml/ne-directml-dml_create_device_flags) for especificado em *flags* e as camadas de depuração não estiverem instaladas, **DMLCreateDevice1** retornará **DXGI_ERROR_SDK_COMPONENT_MISSING**.</span><span class="sxs-lookup"><span data-stu-id="035da-137">If the [DML_CREATE_DEVICE_FLAG_DEBUG](/windows/win32/api/directml/ne-directml-dml_create_device_flags) flag is specified in *flags* and the debug layers are not installed, then **DMLCreateDevice1** returns **DXGI_ERROR_SDK_COMPONENT_MISSING**.</span></span>

## <a name="remarks"></a><span data-ttu-id="035da-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="035da-138">Remarks</span></span>

<span data-ttu-id="035da-139">Uma versão mais recente dessa função, [DMLCreateDevice1](), foi introduzida no DirectML versão 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="035da-139">A newer version of this function, [DMLCreateDevice1](), was introduced in DirectML version 1.1.0.</span></span> <span data-ttu-id="035da-140">**DMLCreateDevice1** é equivalente a chamar **DMLCreateDevice1** e fornecer um *minimumFeatureLevel* de [DML_FEATURE_LEVEL_1_0](/windows/win32/api/directml/ne-directml-dml_feature_level).</span><span class="sxs-lookup"><span data-stu-id="035da-140">**DMLCreateDevice1** is equivalent to calling **DMLCreateDevice1** and supplying a *minimumFeatureLevel* of [DML_FEATURE_LEVEL_1_0](/windows/win32/api/directml/ne-directml-dml_feature_level).</span></span>

## <a name="availability"></a><span data-ttu-id="035da-141">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="035da-141">Availability</span></span>

<span data-ttu-id="035da-142">Essa API foi introduzida na versão DirectML `1.1.0` .</span><span class="sxs-lookup"><span data-stu-id="035da-142">This API was introduced in DirectML version `1.1.0`.</span></span>

## <a name="requirements"></a><span data-ttu-id="035da-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="035da-143">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="035da-144">**Plataforma de Destino**</span><span class="sxs-lookup"><span data-stu-id="035da-144">**Target Platform**</span></span> | <span data-ttu-id="035da-145">Windows</span><span class="sxs-lookup"><span data-stu-id="035da-145">Windows</span></span> |
| <span data-ttu-id="035da-146">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="035da-146">**Header**</span></span> | <span data-ttu-id="035da-147">directml. h</span><span class="sxs-lookup"><span data-stu-id="035da-147">directml.h</span></span> |
| <span data-ttu-id="035da-148">**Biblioteca**</span><span class="sxs-lookup"><span data-stu-id="035da-148">**Library**</span></span> | <span data-ttu-id="035da-149">DirectML. lib</span><span class="sxs-lookup"><span data-stu-id="035da-149">DirectML.lib</span></span> |
| <span data-ttu-id="035da-150">**DLL**</span><span class="sxs-lookup"><span data-stu-id="035da-150">**DLL**</span></span> | <span data-ttu-id="035da-151">DirectML.dll</span><span class="sxs-lookup"><span data-stu-id="035da-151">DirectML.dll</span></span> |

## <a name="see-also"></a><span data-ttu-id="035da-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="035da-152">See also</span></span>

* [<span data-ttu-id="035da-153">Enumeração de DML_FEATURE_LEVEL</span><span class="sxs-lookup"><span data-stu-id="035da-153">DML_FEATURE_LEVEL enumeration</span></span>](/windows/win32/api/directml/ne-directml-dml_feature_level)
* [<span data-ttu-id="035da-154">Histórico de versão do DirectML</span><span class="sxs-lookup"><span data-stu-id="035da-154">DirectML version history</span></span>](../dml-version-history.md)
* [<span data-ttu-id="035da-155">Histórico do nível de recurso do DirectML</span><span class="sxs-lookup"><span data-stu-id="035da-155">DirectML feature level history</span></span>](/windows/win32/direct3d12/dml-feature_level-history)    
* [<span data-ttu-id="035da-156">Usando a camada de depuração DirectML</span><span class="sxs-lookup"><span data-stu-id="035da-156">Using the DirectML debug layer</span></span>](../dml-debug-layer.md)