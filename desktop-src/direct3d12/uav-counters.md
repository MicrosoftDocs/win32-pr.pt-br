---
title: Contadores de UAV
description: Você pode usar os contadores UAV (unordened-Access-View) para associar um contador atômico de 32 bits a um UAV (não ordenado-Access-View).
ms.assetid: 0B77E238-E8CF-466B-9188-3DE96AF97F42
ms.localizationpriority: high
ms.topic: article
ms.date: 02/10/2020
ms.openlocfilehash: 94bc1492e3b984d96c76788430d2e63c0672ca76
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2020
ms.locfileid: "104548241"
---
# <a name="uav-counters"></a>Contadores de UAV
Você pode usar os contadores UAV (unordened-Access-View) para associar um contador atômico de 32 bits a um UAV (não ordenado-Access-View).

## <a name="differences-in-uav-counters-from-direct3d-11-to-direct3d-12"></a>Diferenças nos contadores de UAV do Direct3D 11 para o Direct3D 12
Aplicativos Direct3D 12 e Direct3D 11 usam as mesmas funções de sombreador HLSL (linguagem de sombreamento de alto nível) para acessar os contadores UAV.

-   **IncrementCounter**
-   **DecrementCounter**
-   **Append**
-   **Consumir**

### <a name="direct3d-12"></a>Direct3D 12
No Direct3D 12, os valores de 32 bits são alocados pelo aplicativo, de modo que os valores de 32 bits podem ser lidos e gravados pela CPU ou pela GPU, assim como qualquer outro recurso do Direct3D 12.

### <a name="direct3d-11"></a>Direct3D 11
Fora dos sombreadores, com o Direct3D 11, você precisa chamar métodos de API para acessar os contadores (por exemplo, [ID3D11DeviceContext:: CopyStructureCount](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-copystructurecount)).

## <a name="using-uav-counters"></a>Usando contadores do UAV
Seu aplicativo é responsável por alocar 32 bits de armazenamento para contadores de UAV. Esse armazenamento pode ser alocado em um recurso diferente como aquele que contém os dados acessíveis por meio do UAV.

Consulte [**CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview), [**D3D12 \_ buffer \_ UAV \_ flags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_uav_flags) e [**D3D12 \_ buffer \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_uav).

Se *pCounterResource* for especificado na chamada para [**CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview), haverá um contador associado ao UAV. Nesse caso:

-   *StructureByteStride* deve ser maior que zero
-   O formato deve ser um \_ formato dxgi \_ desconhecido
-   O sinalizador bruto não deve ser definido
-   Ambos os recursos devem ser buffers
-   *CounterOffsetInBytes* deve ser um múltiplo de 4 bytes
-   *CounterOffsetInBytes* deve estar dentro do intervalo do recurso do contador
-   *pDesc* não pode ser nulo
-   a *origem* não pode ser nula

E observe os seguintes casos de uso:

-   Se *pCounterResource* não for especificado, *CounterOffsetInBytes* deverá ser 0.
-   Se o sinalizador bruto estiver definido, o formato deverá ser sem \_ tipo de formato dxgi \_ R32 \_ e o recurso UAV deverá ser um buffer.
-   Se *pCounterResource* não for definido, *CounterOffsetInBytes* deverá ser 0.
-   Se o sinalizador bruto não for definido e *StructureByteStride* = 0, o formato deverá ser um formato UAV válido.

O Direct3D 12 remove a distinção entre Append e Counter UAVs (embora a distinção ainda exista no código de bytes HLSL).

O tempo de execução principal validará essas restrições dentro de [**CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview).

Durante o empate/expedição, o recurso de contador deve estar no estado D3D12 recurso de estado de [**\_ \_ \_ \_ acesso não ordenado**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states). Além disso, em uma única chamada de emissão/expedição, é inválido para um aplicativo acessar o mesmo local de memória de 32 bits por meio de dois contadores de UAV separados. A camada de depuração emitirá erros se um deles for detectado.

Não há nenhum método "SetUnorderedAccessViewCounterValue" ou "CopyStructureCount" porque os aplicativos podem simplesmente copiar dados de e para o valor do contador diretamente.

Há suporte para a indexação dinâmica de UAVs com contadores.

Se um sombreador tentar acessar o contador de um UAV que não tem um contador associado, a camada de depuração emitirá um aviso e uma falha de página de GPU ocorrerá, fazendo com que o dispositivo do aplicativo seja removido.

Os contadores UAV têm suporte em todos os tipos de heap (padrão, upload, readback).

## <a name="related-topics"></a>Tópicos relacionados

* [Contadores e consultas](counters-and-queries.md)