---
title: Índices
description: Índices
ms.assetid: 54c694f6-3c10-4d7c-bcd1-f2b17d652e8e
keywords:
- Windows SDK do formato de mídia, índices
- ASF (Advanced Systems Format), índices
- ASF (formato de sistemas avançados), índices
- Windows SDK do formato de mídia, índices temporais
- ASF (Advanced Systems Format), índices temporais
- ASF (formato de sistemas avançados), índices temporais
- Windows SDK do formato de mídia, índices baseados em quadros
- ASF (Advanced Systems Format), índices baseados em quadros
- ASF (formato de sistemas avançados), índices baseados em quadros
- Windows SDK do formato de mídia, códigos de tempo SMPTE
- Formato de sistema avançado (ASF), códigos de tempo SMPTE
- ASF (formato de sistemas avançados), códigos de tempo SMPTE
- índices, sobre
- índices temporais
- índices baseados em quadros
- Códigos de tempo SMPTE, índices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71af891ba2986d3ece1eb2d4cc7eb7ff4086c06eee1f60eabb2210bdc8b6bacd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118702479"
---
# <a name="indexes"></a>Índices

Um requisito comum para aplicativos que lêem arquivos de mídia digital é a capacidade de buscar um ponto específico no conteúdo. A busca pode ser difícil porque não há nenhuma garantia de que os vários fluxos em um arquivo tenham amostras com horas de início simultâneas. Esse problema é resolvido com o uso de *índices*. Um índice é um objeto em um arquivo ASF que equivale a exemplos de vídeo com seus tempos de apresentação. Nenhum índice é necessário para fluxos de áudio porque os dados de áudio estão mais bem conectados com o tempo de apresentação do que os dados de vídeo.

o objeto indexador do SDK do formato de mídia Windows pode criar três tipos diferentes de índices: índices temporais, índices baseados em quadros e índices de código de tempo SMPTE.

Os índices temporais são o tipo mais comum. Eles simplesmente correspondem a exemplos de vídeo com os tempos de apresentação correspondentes.

Um índice baseado em quadros é igual a exemplos de vídeo com números de quadros de vídeo e tempos de apresentação. Os números de quadro são particularmente úteis em aplicativos que editam vídeo.

Um índice de código de tempo de SMTP é o tipo mais raro de índice. Ele usa o código de tempo SMPTE como a base do índice e pode ser usado somente em fluxos que têm carimbos de data/hora SMPTE incluídos com seus exemplos. Para obter mais informações sobre o código de tempo SMPTE, consulte [suporte ao código de tempo SMPTE](smpte-time-code-support.md).

Um arquivo ASF pode conter um índice de cada tipo para cada fluxo de vídeo que ele contém. Como padrão, um índice temporal é incluído para cada fluxo de vídeo em arquivos criados pelo objeto gravador. Você pode alterar as configurações de indexação automática para seus arquivos de acordo com suas necessidades.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recursos de arquivo ASF**](asf-file-features.md)
</dt> <dt>

[**Trabalhando com índices**](working-with-indexes.md)
</dt> <dt>

[**Lendo arquivos com o leitor assíncrono**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Lendo arquivos com o leitor síncrono**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




