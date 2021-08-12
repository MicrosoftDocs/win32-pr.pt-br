---
description: Os tipos de contador não computacional não têm uma fórmula associada. O valor bruto é diretamente significativo.
ms.assetid: 2a6bb3a3-0aec-437a-881a-c4e14fcff6da
ms.tgt_platform: multiple
title: Tipos de contadores não computacionais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a05da34058ceeb99ab60d8cc3d4f72cb3eec85194e48bb707a929eb2f68aa7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118555156"
---
# <a name="noncomputational-counter-types"></a>Tipos de contadores não computacionais

Os tipos de contador não computacional não têm uma fórmula associada. O valor bruto é diretamente significativo.

A propriedade **FilesToBeIndexed** na classe [**Win32 \_ PerfRawData \_ ContentIndex \_ IndexingService**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) é um exemplo do tipo de contador **contador de desempenho \_ \_ RAWCOUNT** . Ele contém uma contagem de arquivos que não foram indexados.

os tipos de contador são designados pela constante definida em Winperf. h localizada no SDK (Software Development Kit) do Microsoft Windows. A tabela a seguir lista os tipos de contadores não computacionais que são fornecidos.



| CounterType                                                                                                 | Descrição                                                                                                            |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [Desempenho \_ \_Texto do contador](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimal 2816<br/>                | Esse tipo de contador mostra uma cadeia de caracteres de texto de comprimento variável em Unicode. Ele não exibe valores calculados.               |
| [Desempenho \_ COUNTER \_ RAWCOUNT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimal 65536<br/>           | Valor de contador bruto que não requer cálculos e representa um exemplo que é o último valor observado apenas. |
| [Desempenho \_ CONTADOR \_ grande \_ RAWCOUNT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimal 65792<br/>    | O mesmo que o **contador de desempenho \_ \_ RAWCOUNT**, mas uma representação de 64 bits para valores maiores.                                    |
| [Desempenho \_ CONTADOR \_ RAWCOUNT \_ hex](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))0<br/>                  | Valor observado mais recentemente no formato hexadecimal. Ele não exibe uma média.                                    |
| [Desempenho \_ CONTADOR \_ grande \_ RAWCOUNT Decimal \_ hexadecimal](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))256<br/> | O mesmo que o **contador de desempenho \_ \_ RAWCOUNT \_ hex**, mas uma representação de 64 bits em hexadecimal para uso com valores grandes.        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de contador de desempenho WMI](wmi-performance-counter-types.md)
</dt> </dl>

 

