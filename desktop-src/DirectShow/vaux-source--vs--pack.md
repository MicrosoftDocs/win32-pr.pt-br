---
description: Pacote de origem do VAUX (VS)
ms.assetid: 5ffd2883-0e56-459f-b229-cc014b894237
title: Pacote de origem do VAUX (VS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28f7ad2a91f1be1291b564013041e6dfa23bb014
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780037"
---
# <a name="vaux-source-vs-pack"></a>Pacote de origem do VAUX (VS)

As tabelas a seguir listam os valores usados pelo driver MSDV para preencher o membro **dwDVVAuxSrc** da estrutura [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) . Para obter mais informações, consulte [configurações de campo DVINFO no driver MSDV](dvinfo-field-settings-in-the-msdv-driver.md).

**Configurações de DVCR**



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

CANAL DE TV (8)

1111:1111

1111:1111

1111:1111

1111:1111

B/W (1)

1

1

1

1

EN (1)

1

1

1

1

CLF (2)

11

11

11

11

CANAL DE TV (4)

1111

1111

1111

1111

CÓDIGO-FONTE (2)

11

11

11

11

50/60 (1)

0

1

0

1

STYPE (5)

0:0001

0:0001

0:0000

0:0000

CATEGORIA DO SINTONIZADOR (8)

1111:1111

1111:1111

1111:1111

1111:1111

Pacote do VS

0xFFC1FFFF

0xFFE1FFFF

0xFFC0FFFF

0xFFE0FFFF



 

**Configurações do DVCPRO 25 e DVCPRO 50 (planejadas)**



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

Reservado (8)

1111:1111

1111:1111

1111:1111

1111:1111

B/W (1)

1

1

1

1

EN (1)

1

1

1

1

CLF (2)

11

11

11

11

Reservado (4)

1111

1111

1111

1111

Reservado (2)

11

11

11

11

50/60 (1)

0

1

0

1

STYPE (5)

0:0000

0:0000

0:0100

0:0100

VISC (8)

1111:1111

1111:1111

1111:1111

1111:1111

Pacote do VS

0x7FC0FFFF

0x7FE0FFFF

0x7FC4FFFF

0x7FE4FFFF



 

**Configurações do DVCR 100 (planejadas)**



DV Standard

DVCPRO 100 – planejado

FOURCC

dvh1

Sistema

1080-60i

720-60P

1080-50i

Reservado (8)

1111:1111

1111:1111

1111:1111

B/W (1)

1

1

1

EN (1)

1

1

1

CLF (2)

11

11

11

Reservado (4)

1111

1111

1111

Reservado (2)

11

11

11

50/60 (1)

0

0

1

STYPE (5)

1:0100

1:1000

1:0100

VISC (8)

1111:1111

1111:1111

1111:1111

Pacote do VS

0x7FD4FFFF

0x7FD8FFFF

0x7FF4FFFF



 

## <a name="remarks"></a>Comentários

Os códigos de campo a seguir são de interesse:

-   **B/W**: sinalizador preto e branco. 1 = cor.
-   **50/60**: número de campos.
    -   0 = 60 campos
    -   1 = 50 campos
-   **Stype**: tipo de sinal.

    Definição de IEC 61834:

    -   0:0000 = 525-60 ou 625-50, dvsd
    -   0:0001 = 525-60 ou 625-50, dvsl (conforme definido em IEC 61883-5)

    Definição de 314M SMPTE:

    -   0:0000 = compactação 4:1:1
    -   0:0100 = compactação 4:2:2

    Definição de SMPTE 370:

    -   1:0100 = 1080/60i (60 Hz) ou 1080/50i (50 Hz)
    -   1:1000 = 720/60P

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Vídeo digital no DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[Configurações de campo DVINFO no driver MSDV](dvinfo-field-settings-in-the-msdv-driver.md)
</dt> </dl>

 

 



