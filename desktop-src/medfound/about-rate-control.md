---
description: Sobre o controle de taxa
ms.assetid: 509b2cc8-6017-41a9-ae80-9af21dce9367
title: Sobre o controle de taxa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3757e4d1d8a374061ff0c0e7fe02ba3c62243c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105772945"
---
# <a name="about-rate-control"></a>Sobre o controle de taxa

No Media Foundation, a *taxa de reprodução* é expressa como a taxa da taxa de reprodução atual para a taxa de reprodução normal. Por exemplo, uma taxa de 2,0 é duas vezes a velocidade normal e 0,5 é a metade da velocidade normal. Valores negativos indicam reprodução reversa. Uma taxa de reprodução de-2,0 é reproduzida por meio do fluxo em duas vezes a velocidade normal. Uma taxa de zero faz com que um quadro seja renderizado; Depois disso, o relógio de apresentação não avança. Para obter outro quadro com a taxa de zero, o aplicativo deve procurar uma nova posição.

Os aplicativos usam as seguintes interfaces para controlar a taxa de reprodução.

-   [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport). Usado para descobrir as taxas de reprodução mais rápidas e mais lentas possíveis.
-   [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol). Usado para alterar a taxa de reprodução.

Para obter essas duas interfaces, chame [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) na sessão de mídia. O identificador de serviço é o serviço de controle de taxa de MF \_ \_ \_ .

Usando o serviço de controle de taxa, um aplicativo pode implementar a reprodução rápida e inversa.

## <a name="thinning"></a>Finamento

A *fina* é qualquer processo que reduz o número de amostras em um fluxo, a fim de reduzir a taxa geral de bits. Para vídeo, o estreitamento geralmente é feito removendo os quadros Delta e entregando apenas os quadros-chave. Geralmente, o pipeline pode dar suporte a taxas de reprodução mais rápidas usando reprodução fina, porque a taxa de dados é menor porque os quadros Delta não são decodificados.

A fina não altera os carimbos de data/hora ou as durações nos exemplos. Por exemplo, se a taxa nominal do fluxo de vídeo for de 25 quadros por segundo, a duração de cada quadro ainda será marcada como 40 milissegundos, mesmo que a origem da mídia esteja removendo todos os quadros Delta. Isso significa que haverá uma lacuna de tempo entre o final de um quadro e o início do próximo.

## <a name="scrubbing"></a>Anulação

A *depuração* é o processo de busca instantânea de pontos específicos no fluxo interagindo com uma barra de rolagem, linha do tempo ou outra representação visual do tempo. O termo vem da era dos players de fita de rolo a rolo quando um rolo para frente e para trás para localizar uma seção era como depurar o cabeçote de reprodução com a fita.

A depuração é implementada no Media Foundation definindo a taxa de reprodução como zero. Para obter mais informações, consulte [como executar a depuração](how-to-perform-scrubbing.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Controle de taxa](rate-control.md)
</dt> <dt>

[Busca, avanço rápido e reprodução reversa](seeking--fast-forward--and-reverse-play.md)
</dt> <dt>

[Interfaces de serviço](service-interfaces.md)
</dt> </dl>

 

 



