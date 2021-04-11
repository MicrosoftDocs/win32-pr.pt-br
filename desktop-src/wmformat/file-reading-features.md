---
title: Recursos de leitura de arquivo
description: Recursos de leitura de arquivo
ms.assetid: ba6dd328-2250-4867-94e0-f66c70ac1bac
keywords:
- SDK do Windows Media Format, recursos de leitura de arquivos
- SDK do Windows Media Format, leitura de arquivo assíncrono
- SDK do Windows Media Format, leitura de arquivos síncrona
- ASF (Advanced Systems Format), recursos de leitura de arquivos
- ASF (formato de sistemas avançados), recursos de leitura de arquivos
- ASF (Advanced Systems Format), leitura de arquivos assíncronos
- ASF (formato de sistemas avançados), leitura de arquivo assíncrono
- ASF (Advanced Systems Format), leitura síncrona de arquivos
- ASF (formato de sistemas avançados), leitura síncrona de arquivos
- leitura de arquivo assíncrono
- leitura de arquivo síncrona
- leitores síncronos, recursos de leitura de arquivos
- leitura de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a83d3ce112d0d9e47626b4f7850f760da5c6583e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292769"
---
# <a name="file-reading-features"></a>Recursos de leitura de arquivo

A leitura de arquivos ASF é um dos principais recursos do SDK do Windows Media Format. Há suporte para dois tipos de leitura: assíncrono e síncrono. A leitura de arquivos assíncronos é tratada pelo objeto leitor. O objeto leitor síncrono é usado para ler arquivos de forma síncrona. Para obter mais informações sobre os diferentes objetos de leitura, consulte [objeto leitor](reader-object.md) e [objeto leitor síncrono](synchronous-reader-object.md).

No cenário de leitura de arquivo assíncrono mais básico, você deve implementar um método de retorno de chamada que o objeto leitor chamará quando as amostras estiverem prontas. Depois de começar a ler um arquivo, seu aplicativo aguardará que os exemplos sejam entregues ao seu método de retorno de chamada. A leitura assíncrona é útil para aplicativos de Player e oferece suporte a recursos não disponíveis com leitura síncrona. Se seu aplicativo precisar ler arquivos de um local de rede ou interagir com um servidor que executa o Windows Media Services, você deverá usar o objeto leitor. A desvantagem do objeto leitor é que um thread separado é usado para cada saída entregue. Além disso, o objeto leitor não é tão flexível quanto o leitor síncrono em como ele pode fornecer exemplos.

Com o leitor síncrono, você não precisa usar nenhum método de retorno de chamada. Em vez disso, você seleciona uma parte do arquivo para ler e recuperar os exemplos, um por vez, com chamadas de método. O leitor síncrono é adequado às necessidades dos aplicativos de edição de conteúdo, onde o acesso rápido a amostras específicas é essencial. Como nenhum método de retorno de chamada é usado pelo leitor síncrono, você pode criar aplicativos para ler arquivos ASF com um mínimo de sobrecarga de codificação. No entanto, o leitor síncrono não pode abrir um arquivo de um local de rede ou interagir com um servidor que executa o Windows Media Services ou ler arquivos protegidos com [*DRM*](wmformat-glossary.md).

Os tópicos a seguir abordam os recursos do leitor e do leitor síncrono.



| Tópico                                                              | Descrição                                                                                                        |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [Suporte de amostra alocado pelo usuário](user-allocated-sample-support.md) | Discute a alocação de buffer no leitor e no leitor síncrono e como a alocação do usuário pode melhorar o desempenho. |
| [Enumeração de formato de saída](output-format-enumeration.md)         | Discute a enumeração de formato de saída.                                                                               |



 

Além disso, os tópicos a seguir da seção recursos de escrita também se aplicam à leitura de arquivos:

-   [Redimensionamento de vídeo](video-resizing.md)
-   [Conversão de espaço de cor](color-space-conversion.md)
-   [Reamostragem de áudio](audio-resampling.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recursos**](features.md)
</dt> <dt>

[**Lendo arquivos ASF**](reading-asf-files.md)
</dt> </dl>

 

 




