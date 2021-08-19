---
description: Vs (Pacote de Origem V LTDA)
ms.assetid: 5ffd2883-0e56-459f-b229-cc014b894237
title: Vs (Pacote de Origem V LTDA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 477e7a3257c11d6d8b42e16d2f066251452bc42a489abe9e666e374a565fa77c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072090"
---
# <a name="vaux-source-vs-pack"></a>Vs (Pacote de Origem V LTDA)

As tabelas a seguir listam os valores usados pelo driver MSDV para preencher o membro **dwDVVVpSrc** da estrutura [**DVINFO.**](/windows/desktop/api/strmif/ns-strmif-dvinfo) Para obter mais informações, [consulte Campo DVINFO Configurações no Driver MSDV](dvinfo-field-settings-in-the-msdv-driver.md).

**DVCR Configurações**



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

CATEGORIA DO TUNER (8)

1111:1111

1111:1111

1111:1111

1111:1111

VS Pack

0xFFC1FFFF

0xFFE1FFFF

0xFFC0FFFF

0xFFE0FFFF



 

**DVCPRO 25 e DVCPRO 50 Configurações (Planejado)**



DV Standard

DVCPRO (SMPTE 314M) — Planejado

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



 

**Configurações DVCR 100 (planejado)**



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

[Configurações de campo DVINFO no Driver MSDV](dvinfo-field-settings-in-the-msdv-driver.md)
</dt> </dl>

 

 



