---
title: Amostras de mídia (SDK do Windows Media Format 11)
description: Amostras de mídia
ms.assetid: 5fe0d261-c4a8-4b8e-b5dd-668ce067723c
keywords:
- SDK do Windows Media Format, amostras de mídia
- SDK do Windows Media Format, exemplos
- ASF (Advanced Systems Format), amostras de mídia
- ASF (formato de sistemas avançados), amostras de mídia
- ASF (Advanced Systems Format), amostras
- ASF (formato de sistemas avançados), amostras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67d46a933775877f4566115ba3936c0f9f8bd7b3
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103917931"
---
# <a name="media-samples-windows-media-format-11-sdk"></a>Amostras de mídia (SDK do Windows Media Format 11)

Um exemplo de mídia, ou exemplo, é um bloco de dados de mídia digital. Um exemplo é a unidade básica que é manipulada pelos objetos de leitura e gravação do SDK do formato de mídia do Windows. O conteúdo de um exemplo individual é ditado pelo tipo de mídia associado ao exemplo. Para vídeo, cada amostra representa um único quadro. Para áudio, a quantidade de dados em um exemplo individual é definida no perfil usado para criar o arquivo ASF.

Os exemplos podem conter dados descompactados ou podem conter dados compactados; nesse caso, eles são chamados de *amostras de fluxo*. Ao criar um arquivo ASF, você passa amostras para o gravador. O gravador coordena a compactação dos exemplos com o codec apropriado e organiza os dados compactados na seção de dados do arquivo ASF. Na reprodução, o leitor lê os dados compactados, descompacta-os e fornece os dados não compactados reconstruídos como exemplos de saída.

Todos os exemplos usados pelo Windows Media Format SDK são encapsulados no objeto de buffer cuja memória é alocada automaticamente pelos componentes de tempo de execução do SDK. Você também pode alocar seus próprios buffers se precisar, usando recursos avançados do gravador e do leitor.

**Observação** O termo exemplo é usado neste SDK para se referir a um exemplo de mídia, não a um exemplo de áudio. Em codificação de áudio, um exemplo refere-se a um único valor de áudio codificado. Normalmente, a qualidade do áudio codificado é especificada por um número de amostras por segundo. Por exemplo, o som de qualidade do CD é registrado em 44.100 amostras por segundo. Esse valor é geralmente abreviado com a notação Hz, de modo que 44.100 amostras por segundo seriam 44.100 Hz ou 44,1 kHz.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Conceitos**](concepts.md)
</dt> <dt>

[**Interface INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)
</dt> <dt>

[**Entradas, fluxos e saídas**](inputs-streams-and-outputs.md)
</dt> </dl>

 

 




