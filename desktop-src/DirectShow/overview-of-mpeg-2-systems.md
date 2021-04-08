---
description: Visão geral dos sistemas MPEG-2
ms.assetid: 1ebfb194-002f-40ac-9be5-267861b6687b
title: Visão geral dos sistemas MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4206b36db7b3172c6e161745922e83490855c73c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087774"
---
# <a name="overview-of-mpeg-2-systems"></a>Visão geral dos sistemas MPEG-2

Esta seção fornece uma visão geral e não técnica da camada de sistemas MPEG-2. Sistemas MPEG-2 são o padrão que define como os fluxos de áudio e vídeo são multiplexados em MPEG-2.

**Fluxos elementares**

A multiplexação MPEG-2 começa com um ou mais fluxos de bytes, chamados de fluxos elementares (ES), que contêm vídeo, áudio ou outros dados. Por exemplo, um vídeo ES contém quadros de vídeo compactados, além de cabeçalhos de sequência, cabeçalhos de grupo de imagem (GOP) e qualquer outra coisa necessária ao decodificador para decodificar o fluxo. A camada de sistemas não define o conteúdo do fluxo de s bytes.

Um fluxo elementar é dividido em pacotes, formando uma PES ( *fluxo elementar pacotes* ). Os pacotes PES têm comprimento variável. O conteúdo do pacote é chamado de *carga*. Cada pacote PES também inclui um cabeçalho. O multiplexador atribui uma ID de fluxo de 1 byte a cada PES; os pacotes PES individuais são identificados pela ID do fluxo no cabeçalho do pacote. Para fluxos de áudio, a ID do fluxo tem a forma 110 *xxxxx*. Para vídeo, a ID do fluxo tem a forma 1110 *aaaa*.

O padrão MPEG-2 define duas maneiras de entregar fluxos elementares em pacotes: *fluxos de programa* e *fluxos de transporte*.

**Fluxos do programa**

Os fluxos de programa são projetados para ambientes que são relativamente sem erros, como o armazenamento de arquivos local. Em um fluxo de programa, os pacotes PES são multiplexados e organizados em unidades chamadas *pacotes*. Todos os fluxos de PES em um fluxo de programa são sincronizados com o mesmo relógio.

**Fluxos de transporte**

Os TS (fluxos de transporte) são projetados para ambientes não confiáveis ou sujeitos a erros, como difusões de rede. Além disso, eles podem conter vários programas que são sincronizados com relógios diferentes. Um fluxo de transporte adiciona uma segunda camada de empacotamento — os fluxos PES são empacotados dentro de pacotes de fluxo de transporte, que têm um tamanho fixo de 188 bytes por pacote. Os pacotes TS também podem conter fluxos de informações de programa, que são descritos na seção a seguir.

Cada pacote TS tem um cabeçalho de 4 bytes, além de um campo de adaptação opcional que contém informações de cabeçalho adicionais. O multiplexador atribui uma ID de programa (PID) a cada fluxo de informações do programa ou fluxo do PES. Os PIDs são usados para identificar os pacotes TS, de forma semelhante à maneira como as IDs de fluxo identificam os pacotes PES. (Se um fluxo de transporte contiver vários programas, as IDs de *fluxo* poderão não ser exclusivas, mas as atribuições de PID serão exclusivas dentro do fluxo de transporte.)

**Informações específicas do programa**

Como um fluxo de transporte pode transportar vários programas, deve haver uma maneira de associar os vários pacotes PES aos programas aos quais eles pertencem. Isso é feito usando tabelas que identificam os fluxos de programa. Coletivamente, esses dados são chamados de informações específicas do programa (PSI). Os dados PSI são transmitidos em pacotes TS, assim como os dados PES. Há vários tipos de dados PSI, incluindo:

-   PAT (tabela de associação de programa). A PAT sempre é atribuída ao PID 0x000. Cada entrada no PAT é um PID que identifica os pacotes de PGTO para esse programa (consulte o próximo item).
-   Tabela de mapa de programa (PGTO). Cada PGTO define um programa. O pgto contém uma lista de fluxos; cada entrada de tabela fornece a PID para esse fluxo, além de um código que identifica o tipo de fluxo. O ISO/IEC 13818-1 define alguns tipos de fluxo padrão; uma lista abreviada é mostrada na tabela a seguir.

    | tipo de fluxo \_ | Descrição  |
    |--------------|--------------|
    | 0x01         | Vídeo MPEG-1 |
    | 0x02         | Vídeo MPEG-2 |
    | 0x03         | Áudio MPEG-1 |
    | 0x04         | Áudio MPEG-2 |
    | 0x80-0xFF  | Usuário privado |

    

     

    Outros padrões baseados em MPEG-2, como ATSC, podem definir tipos de fluxo adicionais no intervalo de "usuário privado". Por exemplo, ATSC define 0x81 como áudio Dolby AC-3.

-   CAT (tabelas de acesso condicional)
-   NIT (tabelas de identificação de rede)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Suporte a MPEG-2 no DirectShow](mpeg-2-support-in-directshow.md)
</dt> </dl>

 

 



