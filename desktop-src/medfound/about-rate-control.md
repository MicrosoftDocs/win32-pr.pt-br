---
description: Sobre o controle de taxa
ms.assetid: 509b2cc8-6017-41a9-ae80-9af21dce9367
title: Sobre o controle de taxa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61ae8ad5bcfaaf415c888418a7a6bd5d77f72434150e30fcac071d078b8ee6d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035654"
---
# <a name="about-rate-control"></a>Sobre o controle de taxa

Em Media Foundation, a *taxa de reprodução* é expressa como a proporção da taxa de reprodução atual para a taxa de reprodução normal. Por exemplo, uma taxa de 2,0 é duas vezes a velocidade normal e 0,5 é metade da velocidade normal. Valores negativos indicam reprodução inversa. Uma taxa de reprodução de -2,0 é reproduzindo para trás pelo fluxo duas vezes a velocidade normal. Uma taxa de zero faz com que um quadro seja renderizado; depois disso, o relógio de apresentação não avança. Para obter outro quadro na taxa de zero, o aplicativo deve buscar uma nova posição.

Os aplicativos usam as interfaces a seguir para controlar a taxa de reprodução.

-   [**IMFRateSupport.**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) Usado para descobrir as taxas de reprodução mais rápidas e lentas possíveis.
-   [**IMFRateControl.**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) Usado para alterar a taxa de reprodução.

Para obter essas duas interfaces, chame [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) na Sessão de Mídia. O identificador de serviço é MF \_ RATE \_ CONTROL \_ SERVICE.

Usando o serviço de controle de taxa, um aplicativo pode implementar a reprodução rápida e inversa.

## <a name="thinning"></a>Desbaste

*O* emagrecimento é qualquer processo que reduz o número de amostras em um fluxo, para reduzir a taxa geral de bits. Para o vídeo, o emagrecimento geralmente é realizado ao soltar os quadros delta e entregar apenas os quadros-chave. Geralmente, o pipeline pode dar suporte a taxas de reprodução mais rápidas usando reprodução emagreceda, porque a taxa de dados é menor porque quadros delta não são decodificados.

A afinação não altera os carimbos de data/hora nem as durações dos exemplos. Por exemplo, se a taxa nominal do fluxo de vídeo for de 25 quadros por segundo, a duração de cada quadro ainda será marcada como 40 milissegundos, mesmo que a fonte de mídia esteja soltando todos os quadros delta. Isso significa que haverá uma lacuna de tempo entre o final de um quadro e o início do próximo.

## <a name="scrubbing"></a>Anulação

*A depuração* é o processo de buscar instantaneamente pontos específicos no fluxo interagindo com uma barra de rolagem, linha do tempo ou outra representação visual do tempo. O termo vem da era de players de fita de ponto a ponto ao rebalá-lo para localizar uma seção era como depurar a cabeça de reprodução com a fita.

A depuração é implementada Media Foundation configurando a taxa de reprodução como zero. Para obter mais informações, [consulte Como executar a depuração.](how-to-perform-scrubbing.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Controle de taxa](rate-control.md)
</dt> <dt>

[Busca, Avançar e reprodução inversa](seeking--fast-forward--and-reverse-play.md)
</dt> <dt>

[Interfaces de serviço](service-interfaces.md)
</dt> </dl>

 

 



