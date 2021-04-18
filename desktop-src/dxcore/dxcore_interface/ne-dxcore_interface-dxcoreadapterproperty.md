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
# <a name="dxcoreadapterproperty-enum"></a>DXCoreAdapterProperty enum

Define constantes que especificam as propriedades do adaptador DXCore. Passe uma dessas constantes para o método [IDXCoreAdapter:: GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) para recuperar o tamanho do buffer necessário para receber o valor da propriedade correspondente; em seguida, passe a mesma constante para o método [IDXCoreAdapter:: GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md) para recuperar o valor da propriedade em um buffer que você alocar.

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

Especifica a propriedade do adaptador <em>InstanceLuid</em> , que contém um identificador local exclusivo que representa o adaptador. Esse valor permanece constante durante o tempo de vida desse adaptador. A LUID de um adaptador é alterada na reinicialização, atualização de driver ou Habilitação/desabilitação de dispositivo.

A propriedade do adaptador <em>InstanceLuid</em> tem o tipo <a href="/windows/win32/api/winnt/ns-winnt-luid">LUID</a>.

### <a name="driverversion"></a>DriverVersion

Especifica a propriedade do adaptador <em>DriverVersion</em> , que contém a versão do driver, representada no <b>Word</b>s como uma <b>LARGE_INTEGER</b>.

A propriedade do adaptador <em>DriverVersion</em> tem o tipo <b>uint64_t</b>, representando um valor booliano.

### <a name="driverdescription"></a>DriverDescription

Especifica a propriedade do adaptador <em>DriverDescription</em> , que contém uma matriz terminada em nulo de <b>Char</b>s que descreve o driver, conforme especificado pelo driver, na codificação <a href="/windows/win32/intl/unicode">UTF-8</a> .

A propriedade do adaptador <em>DriverDescription</em> tem o tipo <b>Char *</b>.

### <a name="hardwareid"></a>HardwareID

Especifica a propriedade de adaptador de <em>HardwareID</em> , que representa as partes de identificação de hardware PNP.

A propriedade do adaptador <em>HardwareID</em> tem o tipo <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcorehardwareid">DXCoreHardwareID</a>.

### <a name="kmdmodelversion"></a>KmdModelVersion

Especifica a propriedade do adaptador <em>KmdModelVersion</em> , que representa o modelo de driver.

A propriedade do adaptador <em>KmdModelVersion</em> tem o tipo <a href="/windows-hardware/drivers/ddi/content/d3dkmthk/ne-d3dkmthk-_qai_driverversion">D3DKMT_DRIVERVERSION</a>.

### <a name="computepreemptiongranularity"></a>ComputePreemptionGranularity

Especifica a propriedade do adaptador <em>ComputePreemptionGranularity</em> , que representa a granularidade de preempção de computação.

A propriedade do adaptador <em>ComputePreemptionGranularity</em> tem o tipo <b>uint16_t</b>, representando um valor de <a href="/windows-hardware/drivers/ddi/content/d3dkmdt/ne-d3dkmdt-_d3dkmdt_compute_preemption_granularity">D3DKMDT_COMPUTE_PREEMPTION_GRANULARITY</a> .

### <a name="graphicspreemptiongranularity"></a>GraphicsPreemptionGranularity

Especifica a propriedade do adaptador <em>GraphicsPreemptionGranularity</em> , que representa a granularidade da preempção de gráficos.

A propriedade do adaptador <em>GraphicsPreemptionGranularity</em> tem o tipo <b>uint16_t</b>, representando um valor de <a href="/windows-hardware/drivers/ddi/content/d3dkmdt/ne-d3dkmdt-_d3dkmdt_graphics_preemption_granularity">D3DKMDT_GRAPHICS_PREEMPTION_GRANULARITY</a> .

### <a name="dedicatedadaptermemory"></a>DedicatedAdapterMemory

Especifica a propriedade do adaptador <em>DedicatedAdapterMemory</em> , que representa o número de bytes de memória do adaptador dedicado que não são compartilhados com a CPU.

A propriedade do adaptador <em>DedicatedVideoMemory</em> tem o tipo <b>uint64_t</b>.

### <a name="dedicatedsystemmemory"></a>DedicatedSystemMemory

Especifica a propriedade do adaptador <em>DedicatedSystemMemory</em> , que representa o número de bytes de memória dedicada do sistema que não são compartilhados com a CPU. Essa memória é alocada da memória do sistema disponível no momento da inicialização.

A propriedade do adaptador <em>DedicatedSystemMemory</em> tem o tipo <b>uint64_t</b>.

### <a name="sharedsystemmemory"></a>SharedSystemMemory

Especifica a propriedade do adaptador <em>SharedSystemMemory</em> , que representa o número de bytes da memória do sistema compartilhada. Esse é o valor máximo da memória do sistema que pode ser consumida pelo adaptador durante a operação. Qualquer memória incidental consumida pelo driver como ele gerencia e usa a memória de vídeo é adicional.

A propriedade do adaptador <em>SharedSystemMemory</em> tem o tipo <b>uint64_t</b>.

### <a name="acgcompatible"></a>AcgCompatible

Especifica a propriedade do adaptador <em>AcgCompatible</em> , que indica se o adaptador é compatível com processos que impõem proteção de código arbitrária.

A propriedade do adaptador <em>AcgCompatible</em> tem o tipo <b>bool</b>.

### <a name="ishardware"></a>Isduro

Especifica a propriedade do adaptador <em>Isduror</em> , que determina se este é um adaptador de hardware. Um adaptador que não é um adaptador de hardware é um adaptador de software.

A propriedade do adaptador <em>Isduration</em> tem o tipo <b>bool</b>.

### <a name="isintegrated"></a>Isintegrated

Especifica a propriedade do adaptador <em>isintegrated</em> , que determina se o adaptador é relatado como um processador gráfico integrado (iGPU).

A propriedade do adaptador <em>isintegrated</em> tem o tipo <b>bool</b>.

### <a name="isdetachable"></a>Não desanexável

Especifica a propriedade do adaptador <em>desanexável</em> , que determina se o adaptador foi relatado como desanexável ou removível.

A propriedade de adaptador <em>desanexável</em> tem o tipo <b>bool</b>.

<b>Observação</b>. Mesmo se <a href="/windows/win32/dxcore/dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty">IDXCoreAdapter:: GetProperty</a> indicar `false` para essa propriedade, o adaptador ainda terá a capacidade de ser relatada como removida, como no caso de mau funcionamento ou atualização de driver.

## <a name="see-also"></a>Consulte também

[IDXCoreAdapter:: GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md), [IDXCoreAdapter:: GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md), [DXCore Reference](../dxcore-reference.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)