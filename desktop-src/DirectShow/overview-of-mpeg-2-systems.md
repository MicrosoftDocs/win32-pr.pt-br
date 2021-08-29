---
description: Visão geral dos sistemas MPEG-2
ms.assetid: 1ebfb194-002f-40ac-9be5-267861b6687b
title: Visão geral dos sistemas MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d36b0ce6d98024187c9f194065520d388406f4feb95af6fd4df43b7a79e244e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148549"
---
# <a name="overview-of-mpeg-2-systems"></a>Visão geral dos sistemas MPEG-2

Esta seção fornece uma visão geral e não técnica da camada de Sistemas MPEG-2. Os sistemas MPEG-2 são o padrão que define como os fluxos de áudio e vídeo são multiplexados no MPEG-2.

**Dados básicos Fluxos**

A multiplexação mpEG-2 começa com um ou mais fluxos de byte, chamados de ES (fluxos elementares), que contêm vídeo, áudio ou outros dados. Por exemplo, um vídeo ES contém quadros de vídeo compactados, além de headers de sequência, gop (grupo de imagens) e qualquer outra coisa necessária para decodificar o fluxo. A camada Sistemas não define o conteúdo do fluxo de byte do ES.

Um fluxo elementar é dividido em pacotes, formar um PES *(fluxo elementar) em pacotes.* Os pacotes PES têm comprimento variável. O conteúdo do pacote é chamado *de conteúdo*. Cada pacote PES também inclui um header. O multiplexador atribui uma ID de fluxo de 1 byte a cada PES; os pacotes PES individuais são identificados pela ID de fluxo no header do pacote. Para fluxos de áudio, a ID do fluxo tem o formato 110 *xxxxx.* Para vídeo, a ID do fluxo tem o formato 1110 *aaaa*.

O padrão MPEG-2 define duas maneiras de fornecer fluxos elementares em pacotes: *fluxos* de programas e *fluxos de transporte.*

**Programa Fluxos**

Os fluxos de programas são projetados para ambientes que são relativamente livres de erros, como o armazenamento de arquivos local. Em um fluxo de programa, os pacotes pes são multiplexados e organizados em unidades chamadas *pacotes*. Todos os fluxos de PES em um fluxo de programa são sincronizados com o mesmo relógio.

**Transporte Fluxos**

Os fluxos de transporte (TS) são projetados para ambientes não confiáveis ou propensos a erros, como transmissões de rede. Além disso, eles podem conter vários programas que são sincronizados com relógios diferentes. Um fluxo de transporte adiciona uma segunda camada de empacotamento – os fluxos de PES são empacotados dentro de pacotes de fluxo de transporte, que têm um tamanho fixo de 188 bytes por pacote. Os pacotes TS também podem conter fluxos de informações do programa, que são descritos na seção a seguir.

Cada pacote TS tem um header de 4 byte, além de um campo de adaptação opcional que contém informações de header adicionais. O multiplexador atribui uma ID do programa (PID) a cada fluxo de PES ou fluxo de informações do programa. Os PIDs são usados para identificar os pacotes TS, semelhantes à maneira como as IDs de fluxo identificam pacotes PES. (Se um fluxo de transporte  contiver vários programas, as IDs de fluxo poderão não ser exclusivas, mas as atribuições de PID serão exclusivas dentro do fluxo de transporte.)

**Informações específicas do programa**

Como um fluxo de transporte pode transportar vários programas, deve haver uma maneira de associar os vários pacotes PES aos programas aos seus programas. Isso é feito usando tabelas que identificam os fluxos do programa. Coletivamente, esses dados são chamados de PSI (Informações Específicas do Programa). Os dados PSI são carregados em pacotes TS, assim como os dados do PES. Há vários tipos de dados PSI, incluindo:

-   PAT (Tabela de Associação de Programas). O PAT sempre é atribuído ao PID 0x000. Cada entrada no PAT é um PID que identifica os pacotes PMT para esse programa (consulte o próximo item).
-   Tabela de Mapa do Programa (PMT). Cada PMT define um programa. O PMT contém uma lista de fluxos; cada entrada de tabela fornece o PID para esse fluxo, além de um código que identifica o tipo de fluxo. ISO/IEC 13818-1 define alguns tipos de fluxo padrão; uma lista abreviada é mostrada na tabela a seguir.

    | tipo \_ de fluxo | Descrição  |
    |--------------|--------------|
    | 0x01         | Vídeo do MPEG-1 |
    | 0x02         | Vídeo do MPEG-2 |
    | 0x03         | Áudio MPEG-1 |
    | 0x04         | Áudio MPEG-2 |
    | 0x80 - 0xFF  | Privado do usuário |

    

     

    Outros padrões baseados no MPEG-2, como ATSC, podem definir tipos de fluxo adicionais no intervalo "privado do usuário". Por exemplo, a ATSC define 0x81 como áudio AC-3 do Dolby.

-   CAT (Tabelas de Acesso Condicional)
-   NIT (Tabelas de Identificação de Rede)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Suporte a MPEG-2 no DirectShow](mpeg-2-support-in-directshow.md)
</dt> </dl>

 

 



