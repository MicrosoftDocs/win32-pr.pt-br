---
title: Para obter estatísticas do gravador
description: Para obter estatísticas do gravador
ms.assetid: 81d7f567-0d99-4199-9248-1a497dc2eaab
keywords:
- Formato de sistema avançado (ASF), estatísticas do gravador
- ASF (formato de sistemas avançados), estatísticas do gravador
- estatísticas do gravador, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8c6620a2410b08d4d605c4dc116366c24b1e52c
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "103917068"
---
# <a name="to-get-writer-statistics"></a>Para obter estatísticas do gravador

O gravador pode fornecer informações estatísticas sobre as operações de gravação. Há dois métodos para a coleta de estatísticas do gravador: [**IWMWriterAdvanced:: Getstatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getstatistics) e [**IWMWriterAdvanced3:: GetStatisticsEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced3-getstatisticsex). As informações recuperadas pelo **GetStatisticsEx** são mais específicas do que as informações recuperadas por **getstatistics**.

Ambos os métodos populam estruturas com informações estatísticas. **Getstatistics** usa a estrutura de [**\_ \_ estatísticas do gravador do WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics) e o **GetStatisticsEx** usa a estrutura de exemplo de [**estatísticas do gravador do WM \_ \_ \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics_ex) . **GetStatisticsEx** não duplica os dados obtidos por **getstatistics**. Para obter as informações mais completas, você deve chamar os dois métodos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interface IWMWriterAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[**Interface IWMWriterAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced3)
</dt> <dt>

[**Gravando arquivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




