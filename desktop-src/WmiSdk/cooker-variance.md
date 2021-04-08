---
description: A fórmula do tipo de contador de variância de COOKER \_ fornece variabilidade que usa para caracterizar a dispersão para um conjunto de observações brutas de uma propriedade em uma instância do Win32 \_ PerfRawData.
ms.assetid: 6b184a36-7d22-41ab-98e7-b185d1063bcb
ms.tgt_platform: multiple
title: COOKER_VARIANCE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef0f9de6c5241ccd486e4da76864139e3e54f5a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010820"
---
# <a name="cooker_variance"></a>variância de COOKER \_

A fórmula do tipo de contador de variância de COOKER \_ fornece variabilidade que usa para caracterizar a dispersão para um conjunto de observações brutas de uma propriedade em uma instância do [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) . A variação é calculada pela divisão da soma do quadrado do desvio da média de cada contador pelo número de contadores. Em outras palavras, a variação é a média dos desvios quadrados da média de cada contador. Esse tipo de contador é definido somente dentro do WMI e não está disponível para as tecnologias de monitoramento de desempenho, como [contadores de desempenho versão 6,0](/windows/desktop/PerfCtrs/performance-counters-portal).

Para obter mais informações sobre a fórmula de tipo de contador, consulte [tipos de contador](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)).

Para obter mais informações sobre provedores de alto desempenho e scripts, consulte [tipos de contador de desempenho WMI](wmi-performance-counter-types.md).

## <a name="example-code"></a>Código de exemplo

Para obter exemplos de código, consulte [obtendo dados de desempenho estatísticos](obtaining-statistical-performance-data.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de contadores estatísticos](statistical-counter-types.md)
</dt> <dt>

[Monitorando dados de desempenho](monitoring-performance-data.md)
</dt> </dl>

 

 
