---
description: Introdução aos serviços de edição do DirectShow
ms.assetid: 247c4ba9-53c1-46ed-83ef-a454351920e3
title: Introdução aos serviços de edição do DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c75d9cf22eba81ebb9794310f63983b991bcf22
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456598"
---
# <a name="introduction-to-directshow-editing-services"></a>Introdução aos serviços de edição do DirectShow

\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]

O núcleo do DirectShow é uma arquitetura poderosa para lidar com mídias de streaming. Um aplicativo pode usá-lo para reproduzir conteúdo multimídia criado em uma ampla variedade de formatos, sem que o desenvolvedor precise se preocupar com a compactação de arquivos e outros detalhes entediantes. Antes [dos serviços de edição do DirectShow](directshow-editing-services.md) (des), no entanto, o DirectShow não tinha a flexibilidade necessária para edição não linear.

Por exemplo, suponha que você quisesse criar uma sequência de vídeo consistindo de 4 segundos da origem A, seguida de 10 segundos da origem B e terminando com 5 segundos da fonte C. Você poderia fazer isso com muito facilidade usando apenas a API do DirectShow principal.

Mas e se você decidiu que a fonte C deveria vir antes da origem B, não após; que a sequência deve usar 8 segundos da origem A, não 4; e que toda a produção precisava de uma faixa de áudio separada tocando em segundo plano? Até mesmo alterações secundárias, como essas podem ser difíceis de implementar. Mas o cenário que acabei de descrever é um projeto de edição trivial no DES — você pode fazer isso com algumas chamadas de método.

Aqui estão alguns dos recursos que o DES traz para o DirectShow:

-   Um modelo de linha do tempo que organiza faixas de áudio e vídeo em camadas aninhadas, facilitando a manipulação da produção final
-   A capacidade de Visualizar um projeto de vídeo em tempo real
-   Persistência do projeto por meio de um formato baseado em XML
-   Suporte para efeitos de vídeo e áudio, bem como transições entre faixas de vídeo (como fade e borrachas)
-   Mais de 100 de apagamentos padrão, conforme definido pela sociedade de imagem e engenheiros de televisão (SMPTE)
-   Inserindo com base em matiz, luminância, valor RGB ou valor alfa
-   Conversão automática de taxas de quadros e taxas de amostragem de áudio, permitindo que uma produção use fontes heterogêneas
-   Redimensionamento ou corte de vídeo

Limitações:

-   O DES não oferece suporte a fontes de vídeo MPEG-2 ou H. 264.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Serviços de edição do DirectShow](directshow-editing-services.md)
</dt> </dl>

 

 



