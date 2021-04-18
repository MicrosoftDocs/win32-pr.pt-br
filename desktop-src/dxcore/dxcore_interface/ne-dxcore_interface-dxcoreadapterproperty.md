---
title: 'DXCoreAdapterProperty '
description: Define constantes que especificam as propriedades do adaptador DXCore.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 645f0a890aac9a50cdf2987c0736a85142a91aff
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105795486"
---
# <a name="dxcoreadapterproperty-enum"></a><span data-ttu-id="eefe2-103">DXCoreAdapterProperty enum</span><span class="sxs-lookup"><span data-stu-id="eefe2-103">DXCoreAdapterProperty enum</span></span>

<span data-ttu-id="eefe2-104">Define constantes que especificam as propriedades do adaptador DXCore.</span><span class="sxs-lookup"><span data-stu-id="eefe2-104">Defines constants that specify DXCore adapter properties.</span></span> <span data-ttu-id="eefe2-105">Passe uma dessas constantes para o método [IDXCoreAdapter:: GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) para recuperar o tamanho do buffer necessário para receber o valor da propriedade correspondente; em seguida, passe a mesma constante para o método [IDXCoreAdapter:: GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md) para recuperar o valor da propriedade em um buffer que você alocar.</span><span class="sxs-lookup"><span data-stu-id="eefe2-105">Pass one of these constants to the [IDXCoreAdapter::GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) method to retrieve the buffer size necessary to receive the value of the corresponding property; then pass the same constant to the [IDXCoreAdapter::GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md) method to retrieve the property's value in a buffer that you allocate.</span></span>

## <a name="syntax"></a><span data-ttu-id="eefe2-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="eefe2-106">Syntax</span></span>

```cpp
enum class DXCoreAdapterProperty : uint32_t
{
  InstanceLuid = 0,
  DriverVersion = 1,
  DriverDescription = 2,
  HardwareID = 3,
  KmdModelVersion = 4,
  ComputePreemptionGranularity = 5,
  GraphicsPreemptionGranularity = 6,
  DedicatedAdapterMemory = 7,
  DedicatedSystemMemory = 8,
  SharedSystemMemory = 9,
  AcgCompatible = 10,
  IsHardware = 11,
  IsIntegrated = 12,
  IsDetachable = 13
};
```

## <a name="constants"></a><span data-ttu-id="eefe2-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="eefe2-107">Constants</span></span>

### <a name="instanceluid"></a><span data-ttu-id="eefe2-108">InstanceLuid</span><span class="sxs-lookup"><span data-stu-id="eefe2-108">InstanceLuid</span></span>

<span data-ttu-id="eefe2-109">Especifica a propriedade do adaptador <em>InstanceLuid</em> , que contém um identificador local exclusivo que representa o adaptador.</span><span class="sxs-lookup"><span data-stu-id="eefe2-109">Specifies the <em>InstanceLuid</em> adapter property, which contains a locally unique identifier representing the adapter.</span></span> <span data-ttu-id="eefe2-110">Esse valor permanece constante durante o tempo de vida desse adaptador.</span><span class="sxs-lookup"><span data-stu-id="eefe2-110">This value remains constant for the lifetime of this adapter.</span></span> <span data-ttu-id="eefe2-111">A LUID de um adaptador é alterada na reinicialização, atualização de driver ou Habilitação/desabilitação de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eefe2-111">The LUID of an adapter changes on reboot, driver upgrade, or device disablement/enablement.</span></span>

<span data-ttu-id="eefe2-112">A propriedade do adaptador <em>InstanceLuid</em> tem o tipo <a href="/windows/win32/api/winnt/ns-winnt-luid">LUID</a>.</span><span class="sxs-lookup"><span data-stu-id="eefe2-112">The <em>InstanceLuid</em> adapter property has type <a href="/windows/win32/api/winnt/ns-winnt-luid">LUID</a>.</span></span>

### <a name="driverversion"></a><span data-ttu-id="eefe2-113">DriverVersion</span><span class="sxs-lookup"><span data-stu-id="eefe2-113">DriverVersion</span></span>

<span data-ttu-id="eefe2-114">Especifica a propriedade do adaptador <em>DriverVersion</em> , que contém a versão do driver, representada no <b>Word</b>s como uma <b>LARGE_INTEGER</b>.</span><span class="sxs-lookup"><span data-stu-id="eefe2-114">Specifies the <em>DriverVersion</em> adapter property, which contains the driver version, represented in <b>WORD</b>s as a <b>LARGE_INTEGER</b>.</span></span>

<span data-ttu-id="eefe2-115">A propriedade do adaptador <em>DriverVersion</em> tem o tipo <b>uint64_t</b>, representando um valor booliano.</span><span class="sxs-lookup"><span data-stu-id="eefe2-115">The <em>DriverVersion</em> adapter property has type <b>uint64_t</b>, representing a Boolean value.</span></span>

### <a name="driverdescription"></a><span data-ttu-id="eefe2-116">DriverDescription</span><span class="sxs-lookup"><span data-stu-id="eefe2-116">DriverDescription</span></span>

<span data-ttu-id="eefe2-117">Especifica a propriedade do adaptador <em>DriverDescription</em> , que contém uma matriz terminada em nulo de <b>Char</b>s que descreve o driver, conforme especificado pelo driver, na codificação <a href="/windows/win32/intl/unicode">UTF-8</a> .</span><span class="sxs-lookup"><span data-stu-id="eefe2-117">Specifies the <em>DriverDescription</em> adapter property, which contains a NULL-terminated array of <b>CHAR</b>s describing the driver, as specified by the driver, in <a href="/windows/win32/intl/unicode">UTF-8</a> encoding.</span></span>

<span data-ttu-id="eefe2-118">A propriedade do adaptador <em>DriverDescription</em> tem o tipo <b>Char \*</b>.</span><span class="sxs-lookup"><span data-stu-id="eefe2-118">The <em>DriverDescription</em> adapter property has type <b>char\*</b>.</span></span>

### <a name="hardwareid"></a><span data-ttu-id="eefe2-119">HardwareID</span><span class="sxs-lookup"><span data-stu-id="eefe2-119">HardwareID</span></span>

<span data-ttu-id="eefe2-120">Especifica a propriedade de adaptador de <em>HardwareID</em> , que representa as partes de identificação de hardware PNP.</span><span class="sxs-lookup"><span data-stu-id="eefe2-120">Specifies the <em>HardwareID</em> adapter property, which represents the PnP hardware ID parts.</span></span>

<span data-ttu-id="eefe2-121">A propriedade do adaptador <em>HardwareID</em> tem o tipo <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcorehardwareid">DXCoreHardwareID</a>.</span><span class="sxs-lookup"><span data-stu-id="eefe2-121">The <em>HardwareID</em> adapter property has type <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcorehardwareid">DXCoreHardwareID</a>.</span></span>

### <a name="kmdmodelversion"></a><span data-ttu-id="eefe2-122">KmdModelVersion</span><span class="sxs-lookup"><span data-stu-id="eefe2-122">KmdModelVersion</span></span>

<span data-ttu-id="eefe2-123">Especifica a propriedade do adaptador <em>KmdModelVersion</em> , que representa o modelo de driver.</span><span class="sxs-lookup"><span data-stu-id="eefe2-123">Specifies the <em>KmdModelVersion</em> adapter property, which represents the driver model.</span></span>

<span data-ttu-id="eefe2-124">A propriedade do adaptador <em>KmdModelVersion</em> tem o tipo <a href="/windows-hardware/drivers/ddi/content/d3dkmthk/ne-d3dkmthk-_qai_driverversion">D3DKMT_DRIVERVERSION</a>.</span><span class="sxs-lookup"><span data-stu-id="eefe2-124">The <em>KmdModelVersion</em> adapter property has type <a href="/windows-hardware/drivers/ddi/content/d3dkmthk/ne-d3dkmthk-_qai_driverversion">D3DKMT_DRIVERVERSION</a>.</span></span>

### <a name="computepreemptiongranularity"></a><span data-ttu-id="eefe2-125">ComputePreemptionGranularity</span><span class="sxs-lookup"><span data-stu-id="eefe2-125">ComputePreemptionGranularity</span></span>

<span data-ttu-id="eefe2-126">Especifica a propriedade do adaptador <em>ComputePreemptionGranularity</em> , que representa a granularidade de preempção de computação.</span><span class="sxs-lookup"><span data-stu-id="eefe2-126">Specifies the <em>ComputePreemptionGranularity</em> adapter property, which represents the compute preemption granularity.</span></span>

<span data-ttu-id="eefe2-127">A propriedade do adaptador <em>ComputePreemptionGranularity</em> tem o tipo <b>uint16_t</b>, representando um valor de <a href="/windows-hardware/drivers/ddi/content/d3dkmdt/ne-d3dkmdt-_d3dkmdt_compute_preemption_granularity">D3DKMDT_COMPUTE_PREEMPTION_GRANULARITY</a> .</span><span class="sxs-lookup"><span data-stu-id="eefe2-127">The <em>ComputePreemptionGranularity</em> adapter property has type <b>uint16_t</b>, representing a <a href="/windows-hardware/drivers/ddi/content/d3dkmdt/ne-d3dkmdt-_d3dkmdt_compute_preemption_granularity">D3DKMDT_COMPUTE_PREEMPTION_GRANULARITY</a> value.</span></span>

### <a name="graphicspreemptiongranularity"></a><span data-ttu-id="eefe2-128">GraphicsPreemptionGranularity</span><span class="sxs-lookup"><span data-stu-id="eefe2-128">GraphicsPreemptionGranularity</span></span>

<span data-ttu-id="eefe2-129">Especifica a propriedade do adaptador <em>GraphicsPreemptionGranularity</em> , que representa a granularidade da preempção de gráficos.</span><span class="sxs-lookup"><span data-stu-id="eefe2-129">Specifies the <em>GraphicsPreemptionGranularity</em> adapter property, which represents the graphics preemption granularity.</span></span>

<span data-ttu-id="eefe2-130">A propriedade do adaptador <em>GraphicsPreemptionGranularity</em> tem o tipo <b>uint16_t</b>, representando um valor de <a href="/windows-hardware/drivers/ddi/content/d3dkmdt/ne-d3dkmdt-_d3dkmdt_graphics_preemption_granularity">D3DKMDT_GRAPHICS_PREEMPTION_GRANULARITY</a> .</span><span class="sxs-lookup"><span data-stu-id="eefe2-130">The <em>GraphicsPreemptionGranularity</em> adapter property has type <b>uint16_t</b>, representing a <a href="/windows-hardware/drivers/ddi/content/d3dkmdt/ne-d3dkmdt-_d3dkmdt_graphics_preemption_granularity">D3DKMDT_GRAPHICS_PREEMPTION_GRANULARITY</a> value.</span></span>

### <a name="dedicatedadaptermemory"></a><span data-ttu-id="eefe2-131">DedicatedAdapterMemory</span><span class="sxs-lookup"><span data-stu-id="eefe2-131">DedicatedAdapterMemory</span></span>

<span data-ttu-id="eefe2-132">Especifica a propriedade do adaptador <em>DedicatedAdapterMemory</em> , que representa o número de bytes de memória do adaptador dedicado que não são compartilhados com a CPU.</span><span class="sxs-lookup"><span data-stu-id="eefe2-132">Specifies the <em>DedicatedAdapterMemory</em> adapter property, which represents the number of bytes of dedicated adapter memory that are not shared with the CPU.</span></span>

<span data-ttu-id="eefe2-133">A propriedade do adaptador <em>DedicatedVideoMemory</em> tem o tipo <b>uint64_t</b>.</span><span class="sxs-lookup"><span data-stu-id="eefe2-133">The <em>DedicatedVideoMemory</em> adapter property has type <b>uint64_t</b>.</span></span>

### <a name="dedicatedsystemmemory"></a><span data-ttu-id="eefe2-134">DedicatedSystemMemory</span><span class="sxs-lookup"><span data-stu-id="eefe2-134">DedicatedSystemMemory</span></span>

<span data-ttu-id="eefe2-135">Especifica a propriedade do adaptador <em>DedicatedSystemMemory</em> , que representa o número de bytes de memória dedicada do sistema que não são compartilhados com a CPU.</span><span class="sxs-lookup"><span data-stu-id="eefe2-135">Specifies the <em>DedicatedSystemMemory</em> adapter property, which represents the number of bytes of dedicated system memory that are not shared with the CPU.</span></span> <span data-ttu-id="eefe2-136">Essa memória é alocada da memória do sistema disponível no momento da inicialização.</span><span class="sxs-lookup"><span data-stu-id="eefe2-136">This memory is allocated from available system memory at boot time.</span></span>

<span data-ttu-id="eefe2-137">A propriedade do adaptador <em>DedicatedSystemMemory</em> tem o tipo <b>uint64_t</b>.</span><span class="sxs-lookup"><span data-stu-id="eefe2-137">The <em>DedicatedSystemMemory</em> adapter property has type <b>uint64_t</b>.</span></span>

### <a name="sharedsystemmemory"></a><span data-ttu-id="eefe2-138">SharedSystemMemory</span><span class="sxs-lookup"><span data-stu-id="eefe2-138">SharedSystemMemory</span></span>

<span data-ttu-id="eefe2-139">Especifica a propriedade do adaptador <em>SharedSystemMemory</em> , que representa o número de bytes da memória do sistema compartilhada.</span><span class="sxs-lookup"><span data-stu-id="eefe2-139">Specifies the <em>SharedSystemMemory</em> adapter property, which represents the number of bytes of shared system memory.</span></span> <span data-ttu-id="eefe2-140">Esse é o valor máximo da memória do sistema que pode ser consumida pelo adaptador durante a operação.</span><span class="sxs-lookup"><span data-stu-id="eefe2-140">This is the maximum value of system memory that may be consumed by the adapter during operation.</span></span> <span data-ttu-id="eefe2-141">Qualquer memória incidental consumida pelo driver como ele gerencia e usa a memória de vídeo é adicional.</span><span class="sxs-lookup"><span data-stu-id="eefe2-141">Any incidental memory consumed by the driver as it manages and uses video memory is additional.</span></span>

<span data-ttu-id="eefe2-142">A propriedade do adaptador <em>SharedSystemMemory</em> tem o tipo <b>uint64_t</b>.</span><span class="sxs-lookup"><span data-stu-id="eefe2-142">The <em>SharedSystemMemory</em> adapter property has type <b>uint64_t</b>.</span></span>

### <a name="acgcompatible"></a><span data-ttu-id="eefe2-143">AcgCompatible</span><span class="sxs-lookup"><span data-stu-id="eefe2-143">AcgCompatible</span></span>

<span data-ttu-id="eefe2-144">Especifica a propriedade do adaptador <em>AcgCompatible</em> , que indica se o adaptador é compatível com processos que impõem proteção de código arbitrária.</span><span class="sxs-lookup"><span data-stu-id="eefe2-144">Specifies the <em>AcgCompatible</em> adapter property, which indicates whether the adapter is compatible with processes that enforce Arbitrary Code Guard.</span></span>

<span data-ttu-id="eefe2-145">A propriedade do adaptador <em>AcgCompatible</em> tem o tipo <b>bool</b>.</span><span class="sxs-lookup"><span data-stu-id="eefe2-145">The <em>AcgCompatible</em> adapter property has type <b>bool</b>.</span></span>

### <a name="ishardware"></a><span data-ttu-id="eefe2-146">Isduro</span><span class="sxs-lookup"><span data-stu-id="eefe2-146">IsHardware</span></span>

<span data-ttu-id="eefe2-147">Especifica a propriedade do adaptador <em>Isduror</em> , que determina se este é um adaptador de hardware.</span><span class="sxs-lookup"><span data-stu-id="eefe2-147">Specifies the <em>IsHardware</em> adapter property, which determines whether or not this is a hardware adapter.</span></span> <span data-ttu-id="eefe2-148">Um adaptador que não é um adaptador de hardware é um adaptador de software.</span><span class="sxs-lookup"><span data-stu-id="eefe2-148">An adapter that's not a hardware adapter is a software adapter.</span></span>

<span data-ttu-id="eefe2-149">A propriedade do adaptador <em>Isduration</em> tem o tipo <b>bool</b>.</span><span class="sxs-lookup"><span data-stu-id="eefe2-149">The <em>IsHardware</em> adapter property has type <b>bool</b>.</span></span>

### <a name="isintegrated"></a><span data-ttu-id="eefe2-150">Isintegrated</span><span class="sxs-lookup"><span data-stu-id="eefe2-150">IsIntegrated</span></span>

<span data-ttu-id="eefe2-151">Especifica a propriedade do adaptador <em>isintegrated</em> , que determina se o adaptador é relatado como um processador gráfico integrado (iGPU).</span><span class="sxs-lookup"><span data-stu-id="eefe2-151">Specifies the <em>IsIntegrated</em> adapter property, which determines whether the adapter is reported to be an integrated graphics processor (iGPU).</span></span>

<span data-ttu-id="eefe2-152">A propriedade do adaptador <em>isintegrated</em> tem o tipo <b>bool</b>.</span><span class="sxs-lookup"><span data-stu-id="eefe2-152">The <em>IsIntegrated</em> adapter property has type <b>bool</b>.</span></span>

### <a name="isdetachable"></a><span data-ttu-id="eefe2-153">Não desanexável</span><span class="sxs-lookup"><span data-stu-id="eefe2-153">IsDetachable</span></span>

<span data-ttu-id="eefe2-154">Especifica a propriedade do adaptador <em>desanexável</em> , que determina se o adaptador foi relatado como desanexável ou removível.</span><span class="sxs-lookup"><span data-stu-id="eefe2-154">Specifies the <em>IsDetachable</em> adapter property, which determines whether the adapter has been reported to be detachable, or removable.</span></span>

<span data-ttu-id="eefe2-155">A propriedade de adaptador <em>desanexável</em> tem o tipo <b>bool</b>.</span><span class="sxs-lookup"><span data-stu-id="eefe2-155">The <em>IsDetachable</em> adapter property has type <b>bool</b>.</span></span>

<span data-ttu-id="eefe2-156"><b>Observação</b>.</span><span class="sxs-lookup"><span data-stu-id="eefe2-156"><b>Note</b>.</span></span> <span data-ttu-id="eefe2-157">Mesmo se <a href="/windows/win32/dxcore/dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty">IDXCoreAdapter:: GetProperty</a> indicar `false` para essa propriedade, o adaptador ainda terá a capacidade de ser relatada como removida, como no caso de mau funcionamento ou atualização de driver.</span><span class="sxs-lookup"><span data-stu-id="eefe2-157">Even if <a href="/windows/win32/dxcore/dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty">IDXCoreAdapter::GetProperty</a> indicates `false` for this property, the adapter still has the ability to be reported as removed, such as in the case of malfunction, or driver update.</span></span>

## <a name="see-also"></a><span data-ttu-id="eefe2-158">Consulte também</span><span class="sxs-lookup"><span data-stu-id="eefe2-158">See also</span></span>

<span data-ttu-id="eefe2-159">[IDXCoreAdapter:: GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md), [IDXCoreAdapter:: GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md), [DXCore Reference](../dxcore-reference.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="eefe2-159">[IDXCoreAdapter::GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md), [IDXCoreAdapter::GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>