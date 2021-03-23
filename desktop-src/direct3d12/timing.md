---
title: Tempo (gráficos do Direct3D 12)
description: Esta seção aborda a consulta de carimbos de data/hora e a calibragem dos contadores de timestamp e da CPU.
ms.assetid: CC1E5BAB-4363-43FF-BF5B-6C9AEBECD6CA
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 979c51b3c88be184cb23afaa2008e90eaec1f9c5
ms.sourcegitcommit: a1f58e231315e95bbf9178994f8c52303fc0d4a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/21/2020
ms.locfileid: "104548321"
---
# <a name="timing-direct3d-12-graphics"></a>Tempo (gráficos do Direct3D 12)

Esta seção aborda a consulta de carimbos de data/hora e a calibragem dos contadores de timestamp e da CPU.

## <a name="timestamp-frequency"></a>Frequência de carimbo de hora

Seu aplicativo pode consultar a frequência de carimbo de data/hora de GPU em uma base de fila por comando (consulte o método [**ID3D12CommandQueue:: GetTimestampFrequency**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-gettimestampfrequency) ).

A frequência retornada é medida em Hz (tiques/s). Se a fila de comandos especificada não oferecer suporte a carimbos de data/hora (consulte a tabela na seção [consultas](queries.md) ), essa API falhará (e retornará **E_FAIL**). [**D3D12_COMMAND_LIST_TYPE_DIRECT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) e [**D3D12_COMMAND_LIST_TYPE_COMPUTE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) sempre dão suporte a carimbos de data/hora. [**D3D12_COMMAND_LIST_TYPE_COPY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) opcionalmente dá suporte a carimbos de data/hora se o membro [**D3D12_FEATURE_DATA_D3D12_OPTIONS3:: CopyQueueTimestampQueriesSupported**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3) for **verdadeiro**.

## <a name="timestamp-calibration"></a>Calibragem de timestamp

O D3D12 permite que os aplicativos correlacionem os resultados obtidos de consultas de carimbo de data/hora com os resultados obtidos da chamada `QueryPerformanceCounter` . Isso é habilitado pela chamada [**ID3D12CommandQueue:: GetClockCalibration**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration).

[**GetClockCalibration**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration) amostra o contador de carimbo de data/hora da GPU para uma determinada fila de comandos e amostra o contador de CPU via `QueryPerformanceCounter` quase ao mesmo tempo. Novamente, essa API falhará (retornando E \_ falhará) se a fila de comandos especificada não oferecer suporte a carimbos de data/hora (consulte a tabela no tópico [consultas](queries.md) ).

Observe que os contadores de carimbo de data/hora da GPU e da CPU não estão necessariamente diretamente relacionados à velocidade do relógio desses processadores, mas sim para trabalhar com tiques de carimbo de data/hora.

## <a name="timestamp-queries"></a>Consultas de carimbo de hora

Você pode obter carimbos de data/hora como parte de uma lista de comandos (em vez de uma chamada do lado da CPU em uma fila de comando) por meio de consultas de carimbo de data/hora. (Consulte [consultas](queries.md) para obter mais informações sobre consultas em geral). 

Todas as consultas de carimbo de data/hora usam o tipo [**D3D12_QUERY_TYPE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_type) para a consulta real. No entanto, devido a limitações de hardware, [**D3D12_COMMAND_LIST_TYPE_DIRECT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) e [**D3D12_COMMAND_LIST_TYPE_COMPUTE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) usar um [**D3D12_QUERY_HEAP_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type) diferente daquele que [**D3D12_COMMAND_LIST_TYPE_COPY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) usa.

As filas de computação e diretas usam [**D3D12_QUERY_HEAP_TYPE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type).

As filas de cópia usam [**D3D12_QUERY_HEAP_TYPE_COPY_QUEUE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type).

As consultas de fila de cópia só têm suporte se o membro [**D3D12_FEATURE_DATA_D3D12_OPTIONS3:: CopyQueueTimestampQueriesSupported**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3) for **verdadeiro**.

As consultas de carimbo de data/hora, uma vez resolvidas por meio de [**ID3D12GraphicsCommandList:: ResolveQueryData**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata), são um **UINT64** que representa tiques, como é retornado por [**ID3D12CommandQueue:: GetClockCalibration**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration), e como tal, ele deve ser dividido pela frequência de fila para obter o comprimento em segundos.

> [!IMPORTANT]
> Para exatidão, use a aritmética de ponto flutuante ao calcular o segundo ou intervalos de milissegundos de carimbos de data/hora. Por exemplo, use `queriedTicks / (double)Frequency` ao invés de `queriedTicks / Frequency`.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Contadores e consultas](counters-and-queries.md)
</dt> <dt>

[**ID3D12Device::SetStablePowerState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-setstablepowerstate)
</dt> <dt>

[**ID3D12Object:: SetName**](/windows/desktop/api/d3d12/nf-d3d12-id3d12object-setname)
</dt> <dt>

[**ID3DUserDefinedAnnotation**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3duserdefinedannotation)
</dt> <dt>

[Medição de desempenho](performance-measurement.md)
</dt> </dl>
