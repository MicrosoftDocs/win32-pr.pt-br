---
title: Exemplos de mídia (Windows formato de mídia 11 SDK)
description: Saiba mais sobre exemplos de mídia no SDK Windows Media Format 11. Um exemplo de mídia é um objeto que contém uma lista ordenada de zero ou mais buffers.
ms.assetid: 5fe0d261-c4a8-4b8e-b5dd-668ce067723c
keywords:
- Windows SDK de Formato de Mídia, exemplos de mídia
- Windows SDK de Formato de Mídia, exemplos
- FORMATO DE SISTEMAS Avançados (ASF), exemplos de mídia
- ASF (Formato de Sistemas Avançados), exemplos de mídia
- ASF (Advanced Systems Format), samples
- ASF (Formato de Sistemas Avançados), exemplos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 741641bfa326357114f5a02e81a32ac47691661f331355d91a2c3e187ad4233b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117654580"
---
# <a name="media-samples-windows-media-format-11-sdk"></a>Exemplos de mídia (Windows formato de mídia 11 SDK)

Um exemplo de mídia, ou exemplo, é um bloco de dados de mídia digital. Um exemplo é a unidade básica que é manipulada pela leitura e pela escrita de objetos do SDK Windows Formato de Mídia. O conteúdo de um exemplo individual é ditado pelo tipo de mídia associado ao exemplo. Para vídeo, cada exemplo representa um único quadro. Para áudio, a quantidade de dados em um exemplo individual é definida no perfil usado para criar o arquivo ASF.

Os exemplos podem conter dados descompactados ou podem conter dados compactados; nesse caso, eles são chamados de *amostras de fluxo.* Ao criar um arquivo ASF, você passa amostras para o autor. O autor coordena a compactação dos exemplos com o codec apropriado e organiza os dados compactados na seção de dados do arquivo ASF. Na reprodução, o leitor lê os dados compactados, os descompacta e fornece os dados descompactados reconstruídos como exemplos de saída.

Todos os exemplos usados pelo SDK Windows Formato de Mídia são encapsulados no objeto de buffer cuja memória é alocada automaticamente pelos componentes de tempo de run time do SDK. Você também pode alocar seus próprios buffers se precisar, usando recursos avançados do leitor e do autor.

**Observação** O termo exemplo é usado neste SDK para se referir a um exemplo de mídia, não a um exemplo de áudio. Na codificação de áudio, um exemplo refere-se a um único valor de áudio codificado. Normalmente, a qualidade do áudio codificado é especificada por um número de amostras por segundo. Por exemplo, o som de qualidade de CD é registrado em 44.100 amostras por segundo. Esse valor geralmente é abreviado com a notação de Hz, portanto, 44.100 amostras por segundo seriam 44.100 Hz ou 44,1 kHz.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Conceitos**](concepts.md)
</dt> <dt>

[**INSSBuffer Interface**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)
</dt> <dt>

[**Entradas, Fluxos e saídas**](inputs-streams-and-outputs.md)
</dt> </dl>

 

 




