---
title: 'DXCoreAdapterProperty '
description: Define constantes que especificam as propriedades do adaptador DXCore.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: aca9093eb85971621cf232b4713d811535619b59c3d07e0b8b490d063b9d7ac3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042924"
---
# <a name="dxcoreadapterproperty-enum"></a>Enum DXCoreAdapterProperty

Define constantes que especificam as propriedades do adaptador DXCore. Passe uma dessas constantes para o método [IDXCoreAdapter::GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) para recuperar o tamanho do buffer necessário para receber o valor da propriedade correspondente; em seguida, passe a mesma constante para o método [IDXCoreAdapter::GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md) para recuperar o valor da propriedade em um buffer alocado.

## <a name="syntax"></a>Syntax

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

## <a name="constants"></a>Constantes

### <a name="instanceluid"></a>InstanceLuid

Especifica a propriedade <em>do adaptador InstanceLuid,</em> que contém um identificador local exclusivo que representa o adaptador. Esse valor permanece constante durante o tempo de vida desse adaptador. O LUID de um adaptador muda na reinicialização, na atualização do driver ou na desabilitação/habilitação do dispositivo.

A <em>propriedade do adaptador InstanceLuid</em> tem o tipo <a href="/windows/win32/api/winnt/ns-winnt-luid">LUID.</a>

### <a name="driverversion"></a>DriverVersion

Especifica a propriedade do adaptador <em>DriverVersion,</em> que contém a versão do driver, representada no <b>WORD</b>s como um <b>LARGE_INTEGER</b>.

A propriedade do adaptador <em>DriverVersion</em> tem o <b>tipo uint64_t</b>, que representa um valor booliana.

### <a name="driverdescription"></a>DriverDescription

Especifica a propriedade do adaptador <em>DriverDescription,</em> que contém uma matriz terminada em NULL de <b>CHAR</b>que descreve o driver, conforme especificado pelo driver, na codificação <a href="/windows/win32/intl/unicode">UTF-8.</a>

A <em>propriedade do adaptador DriverDescription</em> tem o tipo <b>char*.</b>

### <a name="hardwareid"></a>HardwareID

Especifica a propriedade <em>do adaptador HardwareID,</em> que representa as partes de ID de hardware pnP.

A <em>propriedade do adaptador HardwareID</em> tem o tipo <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcorehardwareid">DXCoreHardwareID</a>.

### <a name="kmdmodelversion"></a>KmdModelVersion

Especifica a propriedade <em>do adaptador KmdModelVersion,</em> que representa o modelo de driver.

A <em>propriedade do adaptador KmdModelVersion</em> tem o tipo <a href="/windows-hardware/drivers/ddi/content/d3dkmthk/ne-d3dkmthk-_qai_driverversion">D3DKMT_DRIVERVERSION</a>.

### <a name="computepreemptiongranularity"></a>ComputePreemptionGranularity

Especifica a propriedade <em>do adaptador ComputePreemptionGranularity,</em> que representa a granularidade de preempção de computação.

A <em>propriedade do adaptador ComputePreemptionGranularity</em> tem o tipo <b>uint16_t</b>, representando <a href="/windows-hardware/drivers/ddi/content/d3dkmdt/ne-d3dkmdt-_d3dkmdt_compute_preemption_granularity">um D3DKMDT_COMPUTE_PREEMPTION_GRANULARITY</a> valor.

### <a name="graphicspreemptiongranularity"></a>GraphicsPreemptionGranularity

Especifica a propriedade do adaptador <em>GraphicsPreemptionGranularity,</em> que representa a granularidade de preempção de gráficos.

A <em>propriedade do adaptador GraphicsPreemptionGranularity</em> tem o tipo <b>uint16_t</b>, representando <a href="/windows-hardware/drivers/ddi/content/d3dkmdt/ne-d3dkmdt-_d3dkmdt_graphics_preemption_granularity">um D3DKMDT_GRAPHICS_PREEMPTION_GRANULARITY</a> valor.

### <a name="dedicatedadaptermemory"></a>DedicatedAdapterMemory

Especifica a propriedade de adaptador <em>DedicatedAdapterMemory,</em> que representa o número de bytes de memória do adaptador dedicado que não são compartilhados com a CPU.

A <em>propriedade do adaptador DedicatedVideoMemory</em> tem o tipo <b>uint64_t</b>.

### <a name="dedicatedsystemmemory"></a>DedicatedSystemMemory

Especifica a propriedade de adaptador <em>DedicatedSystemMemory,</em> que representa o número de bytes de memória do sistema dedicada que não são compartilhados com a CPU. Essa memória é alocada da memória do sistema disponível no momento da inicialização.

A <em>propriedade de adaptador DedicatedSystemMemory</em> tem o tipo <b>uint64_t</b>.

### <a name="sharedsystemmemory"></a>SharedSystemMemory

Especifica a propriedade <em>do adaptador SharedSystemMemory,</em> que representa o número de bytes de memória do sistema compartilhado. Esse é o valor máximo de memória do sistema que pode ser consumido pelo adaptador durante a operação. Qualquer memória incidental consumida pelo driver à medida que ele gerencia e usa a memória de vídeo é adicional.

A propriedade do adaptador <em>SharedSystemMemory</em> tem o <b>tipo uint64_t</b>.

### <a name="acgcompatible"></a>AcgCompatible

Especifica a propriedade do adaptador <em>AcgCompatible,</em> que indica se o adaptador é compatível com processos que impõem o Code Guard Arbitrário.

A <em>propriedade do adaptador AcgCompatible</em> tem o tipo <b>bool</b>.

### <a name="ishardware"></a>IsHardware

Especifica a propriedade <em>do adaptador IsHardware,</em> que determina se este é ou não um adaptador de hardware. Um adaptador que não é um adaptador de hardware é um adaptador de software.

A <em>propriedade do adaptador IsHardware</em> tem o tipo <b>bool</b>.

### <a name="isintegrated"></a>IsIntegrated

Especifica a propriedade do adaptador <em>IsIntegrated,</em> que determina se o adaptador é relatado como um iGPU (processador gráfico integrado).

A <em>propriedade do adaptador IsIntegrated</em> tem o tipo <b>bool</b>.

### <a name="isdetachable"></a>IsDetachable

Especifica a propriedade do adaptador <em>IsDetachable,</em> que determina se o adaptador foi relatado como desa removível ou removível.

A <em>propriedade do adaptador IsDetachable</em> tem o tipo <b>bool</b>.

<b>Observe</b>. Mesmo se <a href="/windows/win32/dxcore/dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty">IDXCoreAdapter::GetProperty</a> indicar para essa propriedade, o adaptador ainda terá a capacidade de ser relatado como removido, como no caso de defeito ou atualização do `false` driver.

## <a name="see-also"></a>Confira também

[IDXCoreAdapter::GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md), [IDXCoreAdapter::GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md), [Referência de DXCore](../dxcore-reference.md), usando [DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)