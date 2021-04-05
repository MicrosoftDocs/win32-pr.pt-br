---
description: Pacote de controle do código-fonte AAUX (ASC)
ms.assetid: 3df80895-81e1-42a4-a095-913e77b199e5
title: Pacote de controle do código-fonte AAUX (ASC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eab942ccff1cf38e6962d508c9c9bfc99ea9fed6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103646070"
---
# <a name="aaux-source-control-asc-pack"></a>Pacote de controle do código-fonte AAUX (ASC)

As tabelas a seguir listam os valores usados pelo driver MSDV para preencher o **dwDVAAuxCtl** e

**dwDVAAuxCtl1** membros da estrutura [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) . Para obter mais informações, consulte [configurações de campo DVINFO no driver MSDV](dvinfo-field-settings-in-the-msdv-driver.md).

Configurações de DVCR



DV Standard

DVCR (IEC 61834)

FOURCC

dvsl

dvsd

Sistema

525-60

625-50

525-60

625-50

CGMS (2)

00

00

00

00

ISR (2)

11

11

11

11

CMP (2)

11

11

11

11

SS (2)

11

11

11

11

REC ST (1)

1

1

1

1

TÉRMINO DO REC (1)

1

1

1

1

MODO DE REC (3)

001

001

001

001

INSERIR CH (3)

111

111

111

111

DRF (1)

1

1

1

1

VELOCIDADE (7)

010:0000

010:0000

010:0000

010:0000

Reservado (1)

1

1

1

1

GÊNERO (7)

111:1111

111:1111

111:1111

111:1111

Pacote ASC (ambos os blocos de áudio)\*

0xFFA0CF3F

0xFFA0CF3F

0xFFA0CF3F

0xFFA0CF3F



 

Configurações do DVCR 25 e DVCPRO 50 (planejadas)



DV Standard

DVCPRO (SMPTE 314M) – planejado

FOURCC

dv25

dv50

Sistema

525-60

625-50

525-60

625-50

CGMS (2)

00

00

00

00

Reservado (4)

1111

1111

1111

1111

EFC (2)

00

00

00

00

REC ST (1)

1

1

1

1

TÉRMINO DO REC (1)

1

1

1

1

FADE ST (1)

1

1

1

1

FIM DA FADE (1)

1

1

1

1

Reservado (4)

1111

1111

1111

1111

DRF (1)

1

1

1

1

VELOCIDADE (7)

111:1000

110:0100

111:1000

110:0100

Reservado (8)

1111:1111

1111:1111

1111:1111

1111:1111

Pacote ASC (ambos os blocos de áudio)\*

0xFFA0CF3F

0xFFA0CF3F

0xFFA0CF3F

0xFFA0CF3F



 

\* A estrutura *DVINFO* contém dois AAUX como pacotes para os blocos de áudio 1 e 2. DV50 tem quatro blocos de áudio; os blocos 3 e 4 não são representados na estrutura *DVINFO* .

Configurações do DVCR 100 (planejadas)



DV Standard

DVCPRO 100 – planejado

FOURCC

dvh1

Sistema

1080-60i

720-60P

1080-50i

CGMS (2)

00

00

00

Reservado (4)

1111

1111

1111

EFC (2)

00

00

00

REC ST (1)

1

1

1

TÉRMINO DO REC (1)

1

1

1

FADE ST (1)

1

1

1

FIM DA FADE (1)

1

1

1

Reservado (4)

1111

1111

1111

DRF (1)

1

1

1

VELOCIDADE (7)

111:1000

111:1000

110:0100

Reservado (8)

1111:1111

1111:1111

1111:1111

Pacote ASC (ambos os blocos de áudio)\*

0xFFF8FF3C

0xFFF8FF3C

0xFFE4FF3C



 

\* O DVCPRO 100 tem 8 blocos de áudio; os blocos de 3 a 8 não são representados na estrutura *DVINFO* .

## <a name="remarks"></a>Comentários

Os códigos de campo a seguir são de interesse:

-   **CGMS**: sistema de gerenciamento de geração de cópia. 0 = cópia permitida sem restrição.

    Os pacotes ASC reais no fluxo de DV podem conter valores diferentes.

<!-- -->

-   **Modo** de registro: modo de gravação. 1 = original
-   **Velocidade**: velocidade de reprodução do VTR.

    Definição de IEC 61834:

    -   010:0000 = velocidade normal, 525-60 ou 625-50

    Definição de 314M SMPTE:

    -   111:1000 = velocidade normal, 525-60
    -   110:0100 = velocidade normal, 625-50

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Vídeo digital no DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[Configurações de campo DVINFO no driver MSDV](dvinfo-field-settings-in-the-msdv-driver.md)
</dt> </dl>

 

 



