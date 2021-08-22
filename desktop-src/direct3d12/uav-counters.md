---
title: Contadores de UAV
description: Você pode usar contadores UAV (unordered-access-view) para associar um contador atômico de 32 bits a um UAV (exibição de acesso não organizado).
ms.assetid: 0B77E238-E8CF-466B-9188-3DE96AF97F42
ms.localizationpriority: high
ms.topic: article
ms.date: 02/10/2020
ms.openlocfilehash: c33321b02f22378f4d039137b8ff65559a25a32ed219c2bf336528913777791d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460786"
---
# <a name="uav-counters"></a>Contadores de UAV
Você pode usar contadores UAV (unordered-access-view) para associar um contador atômico de 32 bits a um UAV (exibição de acesso não organizado).

## <a name="differences-in-uav-counters-from-direct3d-11-to-direct3d-12"></a>Diferenças nos contadores UAV do Direct3D 11 para o Direct3D 12
Aplicativos Direct3D 12 e aplicativos Direct3D 11 usam as mesmas funções de sombreador de HLSL (linguagem de sombreador de alto nível) para acessar os contadores UAV.

-   **IncrementCounter**
-   **DecrementCounter**
-   **Acrescentar**
-   **Consumir**

### <a name="direct3d-12"></a>Direct3D 12
No Direct3D 12, os valores de 32 bits são alocados pelo aplicativo, portanto, os valores de 32 bits podem ser lidos e gravados pela CPU ou pela GPU, assim como qualquer outro recurso direct3D 12.

### <a name="direct3d-11"></a>Direct3D 11
Fora dos sombreadores, com o Direct3D 11, você precisa chamar métodos de API para acessar os contadores (por exemplo, [ID3D11DeviceContext::CopyStructureCount](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-copystructurecount)).

## <a name="using-uav-counters"></a>Usando contadores UAV
Seu aplicativo é responsável por alocar 32 bits de armazenamento para contadores UAV. Esse armazenamento pode ser alocado em um recurso diferente como aquele que contém dados acessíveis por meio do UAV.

Consulte [**CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview), [**D3D12 \_ BUFFER \_ UAV \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_uav_flags) e [**D3D12 \_ BUFFER \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_uav).

Se *pCounterResource* for especificado na chamada para [**CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview), haverá um contador associado ao UAV. Nesse caso:

-   *StructureByteStride* deve ser maior que zero
-   O formato deve ser FORMATO DXGI \_ \_ DESCONHECIDO
-   O sinalizador RAW não deve ser definido
-   Ambos os recursos devem ser buffers
-   *CounterOffsetInBytes* deve ser um múltiplo de 4 bytes
-   *CounterOffsetInBytes* deve estar dentro do intervalo do recurso de contador
-   *pDesc não* pode ser NULL
-   *pResource não* pode ser NULL

Observe os seguintes casos de uso:

-   Se *pCounterResource* não for especificado, *CounterOffsetInBytes* deverá ser 0.
-   Se o sinalizador RAW for definido, o formato deverá ser DXGI FORMAT R32 TYPELESS e o \_ \_ recurso \_ UAV deverá ser um buffer.
-   Se *pCounterResource* não estiver definido, *CounterOffsetInBytes* deverá ser 0.
-   Se o sinalizador RAW não estiver definido e *StructureByteStride* = 0, o formato deverá ser um formato UAV válido.

O Direct3D 12 remove a distinção entre os UAVs de anexação e de contador (embora a distinção ainda exista no código de bytecode HLSL).

O runtime principal validará essas restrições dentro de [**CreateUnorderedAccessView.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview)

Durante Draw/Dispatch, o recurso de contador deve estar no estado [**D3D12 \_ RESOURCE \_ STATE \_ UNORDERED \_ ACCESS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states). Além disso, em uma única chamada de Desenho/Expedição, é inválido para um aplicativo acessar o mesmo local de memória de 32 bits por meio de dois contadores UAV separados. A camada de depuração emitirá erros se qualquer um deles for detectado.

Não há métodos "SetUnorderedAccessViewCounterValue" ou "CopyStructureCount", pois os aplicativos podem simplesmente copiar dados de e para o valor do contador diretamente.

Há suporte para a indexação dinâmica de UAVs com contadores.

Se um sombreador tentar acessar o contador de um UAV que não tem um contador associado, a camada de depuração emitirá um aviso e ocorrerá uma falha de página de GPU, fazendo com que o dispositivo dos aplicativos seja removido.

Os contadores UAV têm suporte em todos os tipos de heap (padrão, upload, readback).

## <a name="related-topics"></a>Tópicos relacionados

* [Contadores e consultas](counters-and-queries.md)