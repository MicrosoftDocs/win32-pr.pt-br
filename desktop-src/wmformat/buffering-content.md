---
title: Armazenando conteúdo em buffer
description: Armazenando conteúdo em buffer
ms.assetid: e14e0130-aefd-4e46-b288-4302d2333de2
keywords:
- SDK do Windows Media Format, armazenar em buffer o conteúdo
- armazenando conteúdo em buffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a06b378431653f21be742c12b4e4a5ae2a994318
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105814087"
---
# <a name="buffering-content"></a>Armazenando conteúdo em buffer

Quando o objeto do leitor abre um arquivo de streaming, ele determina o tamanho do buffer com base nas configurações no cabeçalho do arquivo. Você pode considerar o buffer como um Bucket com um orifício na parte inferior que vaza em uma taxa constante. Desde que a taxa na qual o Bucket é preenchido não seja, em média, maior do que a taxa na qual ele está vazando, o Bucket nunca será estourado.

A taxa na qual os vazamentos de Bucket imaginários é a taxa de bits do fluxo. A taxa na qual o Bucket é preenchido é a taxa de bits de streaming real. Os dados em um fluxo compactado variam de acordo com o tamanho de amostra para amostra, dependendo da quantidade de compactação obtida. Portanto, embora a taxa de bits do fluxo seja definida no perfil, ela representa a taxa média de bits, não uma constante.

A outra configuração de fluxo importante para o processo de buffer é a janela buffer. A janela buffer é medida em tempo e especifica a quantidade de conteúdo que pode ser armazenada em buffer. A capacidade do Bucket imaginário pode ser encontrada usando a janela buffer. Por exemplo, se você tiver um fluxo com uma taxa de bits de 32 kbps e uma janela de buffer de 3 segundos, o buffer será dimensionado para conter 3 segundos de conteúdo de 32 kbps ou 12.000 bytes (32.000 bits por segundo x 3 segundos/8 bits por byte). O codec limita a variação entre a taxa de bits de streaming real de amostras codificadas para que, em um período de tempo igual à janela de buffer, a taxa de bits média não seja maior do que a taxa de bits do fluxo.

Normalmente, você define a taxa de bits e a janela de buffer para um fluxo em um perfil, e o gravador lida com o restante. No entanto, ao passar amostras compactadas para o leitor, você deve garantir que os valores corretos sejam transferidos para o novo arquivo, definindo a taxa de bits e a janela de buffer para o fluxo no perfil de destino para os valores do fluxo compactado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Conceitos**](concepts.md)
</dt> <dt>

[**Amostras de mídia**](media-samples.md)
</dt> <dt>

[**Entradas, fluxos e saídas**](inputs-streams-and-outputs.md)
</dt> </dl>

 

 




