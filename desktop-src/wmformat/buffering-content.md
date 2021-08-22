---
title: Conteúdo de buffer
description: Conteúdo de buffer
ms.assetid: e14e0130-aefd-4e46-b288-4302d2333de2
keywords:
- Windows SDK de Formato de Mídia, conteúdo de buffer
- conteúdo de buffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3005895f7a196073566c32bb455f5808bf6f11feb491000b140e1bbf88b94b7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586986"
---
# <a name="buffering-content"></a>Conteúdo de buffer

Quando o objeto de leitor abre um arquivo de streaming, ele determina o tamanho do buffer com base nas configurações no header do arquivo. Você pode pensar no buffer como um bucket com um orifício na parte inferior que vaza em uma taxa constante. Desde que a taxa na qual o bucket seja preenchido não seja, em média, maior que a taxa na qual ele está vazando, o bucket nunca vai estourar.

A taxa na qual o bucket imaginário vaza é a taxa de bits do fluxo. A taxa na qual o bucket é preenchida é a taxa de bits de streaming real. Os dados em um fluxo compactado variam de tamanho de amostra para amostra, dependendo da quantidade de compactação que foi atingida. Portanto, embora a taxa de bits do fluxo seja definida no perfil, ela representa a taxa média de bits, não uma constante.

A outra configuração de fluxo importante para o processo de buffer é a janela de buffer. A janela de buffer é medida no tempo e especifica quanto conteúdo pode ser armazenado em buffer. A capacidade do bucket imaginário pode ser encontrada usando a janela do buffer. Por exemplo, se você tiver um fluxo com uma taxa de bits de 32 Kbps e uma janela de buffer de 3 segundos, o buffer será dimensionado para conter 3 segundos de conteúdo de 32 Kbps ou 12.000 bytes (32.000 bits por segundo x 3 segundos/8 bits por byte). O codec limita a variação entre a taxa de bits de streaming real de amostras codificadas para que, ao longo de um período igual à janela de buffer, a taxa média de bits não seja maior que a taxa de bits do fluxo.

Normalmente, você configura a taxa de bits e a janela de buffer para um fluxo em um perfil e o autor trata o restante. No entanto, ao passar amostras compactadas para o leitor, você deve garantir que os valores corretos sejam transferidos para o novo arquivo definindo a taxa de bits e a janela de buffer para o fluxo no perfil de destino para os valores do fluxo compactado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Conceitos**](concepts.md)
</dt> <dt>

[**Exemplos de mídia**](media-samples.md)
</dt> <dt>

[**Entradas, Fluxos e saídas**](inputs-streams-and-outputs.md)
</dt> </dl>

 

 




