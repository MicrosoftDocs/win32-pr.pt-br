---
title: Recursos de leitura de arquivo
description: Recursos de leitura de arquivo
ms.assetid: ba6dd328-2250-4867-94e0-f66c70ac1bac
keywords:
- Windows SDK de Formato de Mídia, recursos de leitura de arquivo
- Windows SDK de Formato de Mídia, leitura de arquivo assíncrono
- Windows SDK de Formato de Mídia, leitura de arquivo síncrono
- ASF (Advanced Systems Format), recursos de leitura de arquivo
- ASF (Formato de Sistemas Avançados), recursos de leitura de arquivo
- ASF (Advanced Systems Format), leitura de arquivo assíncrona
- ASF (Formato de Sistemas Avançados), leitura de arquivo assíncrono
- ASF (Advanced Systems Format), leitura de arquivo síncrono
- ASF (Formato de Sistemas Avançados), leitura de arquivo síncrono
- leitura de arquivo assíncrona
- leitura de arquivo síncrono
- leitores síncronos, recursos de leitura de arquivo
- leitura de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e8efb7bc0fca898c1a63db586b158b39b4bb9daa9ad051e7a61fe8c4a5d6b24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930526"
---
# <a name="file-reading-features"></a>Recursos de leitura de arquivo

Ler arquivos ASF é um dos principais recursos do SDK Windows Formato de Mídia. Há suporte para dois tipos de leitura: assíncrono e síncrono. A leitura de arquivo assíncrona é manipulada pelo objeto de leitor. O objeto de leitor síncrono é usado para ler arquivos de forma síncrona. Para obter mais informações sobre os diferentes objetos de leitura, consulte [Objeto de Leitor](reader-object.md) e Objeto de Leitor [Síncrono](synchronous-reader-object.md).

No cenário de leitura de arquivo assíncrono mais básico, você deve implementar um método de retorno de chamada que o objeto de leitor chamará quando os exemplos estão prontos. Depois de começar a ler um arquivo, seu aplicativo aguarda que os exemplos sejam entregues ao método de retorno de chamada. A leitura assíncrona é útil para aplicativos de player e dá suporte a recursos não disponíveis com leitura síncrona. Se o aplicativo precisar ler arquivos de um local de rede ou interagir com um servidor que executa Windows Media Services, você deverá usar o objeto de leitor. A desvantagem do objeto de leitor é que um thread separado é usado para cada saída entregue. Além disso, o objeto de leitor não é tão flexível quanto o leitor síncrono em como ele pode fornecer exemplos.

Com o leitor síncrono, você não precisa usar nenhum método de retorno de chamada. Em vez disso, você seleciona uma parte do arquivo para ler e recuperar as amostras uma de cada vez com chamadas de método. O leitor síncrono é adequado para as necessidades de aplicativos de edição de conteúdo, em que o acesso rápido a exemplos específicos é essencial. Como nenhum método de retorno de chamada é usado pelo leitor síncrono, você pode criar aplicativos para ler arquivos ASF com um mínimo de sobrecarga de codificação. No entanto, o leitor síncrono não pode abrir um arquivo de um local de rede ou interagir com um servidor que executa Windows Media Services ou ler arquivos protegidos com [*DRM*](wmformat-glossary.md).

Os tópicos a seguir discutem os recursos do leitor e do leitor síncrono.



| Tópico                                                              | Descrição                                                                                                        |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [Suporte de exemplo alocado pelo usuário](user-allocated-sample-support.md) | Discute a alocação de buffer no leitor e no leitor síncrono e como a alocação do usuário pode melhorar o desempenho. |
| [Enumeração de formato de saída](output-format-enumeration.md)         | Discute a enumeração de formato de saída.                                                                               |



 

Além disso, os seguintes tópicos da seção escrevendo recursos também se aplicam à leitura de arquivo:

-   [Reizing de vídeo](video-resizing.md)
-   [Conversão de espaço em cores](color-space-conversion.md)
-   [Resampling de áudio](audio-resampling.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recursos**](features.md)
</dt> <dt>

[**Lendo arquivos ASF**](reading-asf-files.md)
</dt> </dl>

 

 




