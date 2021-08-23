---
title: Para obter estatísticas do writer
description: Para obter estatísticas do writer
ms.assetid: 81d7f567-0d99-4199-9248-1a497dc2eaab
keywords:
- ASF (Advanced Systems Format), estatísticas de autor
- ASF (Formato de Sistemas Avançados), estatísticas de autor
- estatísticas do autor, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1cedd96f1e94b8d3c9499fe08e3eeebb2100e866b141b756483cfb07bb7cb0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083961"
---
# <a name="to-get-writer-statistics"></a>Para obter estatísticas do writer

O autor pode fornecer informações estatísticas sobre operações de escrita. Há dois métodos para coletar estatísticas de autor: [**IWMWriterAdvanced::GetStatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getstatistics) e [**IWMWriterAdvanced3::GetStatisticsEx.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced3-getstatisticsex) As informações recuperadas por **GetStatisticsEx** são mais específicas do que as informações recuperadas por **GetStatistics.**

Ambos os métodos populam estruturas com informações estatísticas. **GetStatistics** usa a [**estrutura WM WRITER \_ \_ STATISTICS**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics) e **GetStatisticsEx** usa a estrutura [**WM WRITER \_ \_ STATISTICS \_ EX.**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics_ex) **GetStatisticsEx** não duplica os dados obtidos por **GetStatistics.** Para obter as informações mais completas, você deve chamar os dois métodos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IWMWriterAdvanced Interface**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[**IWMWriterAdvanced3 Interface**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced3)
</dt> <dt>

[**Escrevendo arquivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




