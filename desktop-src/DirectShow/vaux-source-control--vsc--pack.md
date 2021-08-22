---
description: Pacote VSC (controle do código-fonte) V LTD
ms.assetid: 9d5dd89e-9084-409d-86c0-30b57645d33d
title: Pacote VSC (controle do código-fonte) V LTD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcdc91d5c4b2cea460c85b696c59bfce7799d39aed0a6bfcbc03f3d3c522a6ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072070"
---
# <a name="vaux-source-control-vsc-pack"></a>Pacote VSC (controle do código-fonte) V LTD

As tabelas a seguir listam os valores usados pelo driver MSDV para preencher o membro **dwDVVVpCtl** da estrutura [**DVINFO.**](/windows/desktop/api/strmif/ns-strmif-dvinfo) Para obter mais informações, [consulte Campo DVINFO Configurações no Driver MSDV](dvinfo-field-settings-in-the-msdv-driver.md).

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

Reservado (1)

1

1

1

1

MODO REC (2)

00

00

00

00

Reservado (1)

1

1

1

1

DISP (3)

000

000

000

000

FF (1)

1

1

1

1

FS (1)

1

1

1

1

FC (1)

1

1

1

1

IL (1)

1

1

1

1

ST (1)

1

1

1

1

SC (1)

1

1

1

1

BCSYS (2)

00

01

00

01

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

Pacote de VSC

0xFFFCC83F

0xFFFDC83F

0xFFFCC83F

0xFFFDC83F



 

**DVCPRO 25 e DVCPRO 50 Configurações (planejado)**



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

Reservado (6)

11:1111

11:1111

11:1111

11:1111

Reservado (2)

11

11

11

11

Reservado (2)

00

00

00

00

Reservado (1)

1

1

1

1

DISP (3)

000

000

000

000

FF (1)

1

1

1

1

FS (1)

1

1

1

1

FC (1)

1

1

1

1

IL (1)

1

1

1

1

Reservado (2)

11

11

11

11

Reservado (2)

00

00

00

00

Reservado (8)

1111:1111

1111:1111

1111:1111

1111:1111

Pacote de VSC

0xFFFCC83F

0xFFFCC83F

0xFFFCC83F

0xFFFCC83F



 

**Configurações DVCPRO 100 (planejado)**



DV Standard

DVCPRO 100 – planejado

FOURCC

dvh1

Sistema

1080-60i

720p-60P

1080-50i

CGMS (2)

00

00

00

Reservado (6)

11:1111

11:1111

11:1111

Reservado (2)

11

11

11

Reservado (2)

00

00

00

Reservado (1)

1

1

1

DISP (3)

010

010

010

FF (1)

1

1

1

FS (1)

1

1

1

FC (1)

1

1

1

IL (1)

1

1

1

Reservado (2)

11

11

11

Reservado (2)

00

00

00

Reservado (8)

1111:1111

1111:1111

1111:1111

Pacote VSC

0xFFFCCA3F

0xFFFCCA3F

0xFFFCCA3F



 

## <a name="remarks"></a>Comentários

Os seguintes códigos de campo são de interesse:

-   **CGMS:** copiar o sistema de gerenciamento de geração. 0 = cópia permitida sem restrição.

    Os pacotes VSC reais no fluxo DV podem conter valores diferentes.

<!-- -->

-   **MODO REC:** modo de gravação. 1 = Original.
-   **DISP:** exibe o modo de seleção. 000 = taxa de proporção 4:3, formato completo; 010 = taxa de proporção de 16:9.
-   **BCSYS:** sistema de difusão. Esse campo define o tipo de informações de sinalização de tela larga.
    -   0 = tipo 0 (consulte IEC 61880)
    -   1 = tipo 1 (consulte ETSI EN 300 294)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Vídeo digital no DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[Campo DVINFO Configurações no Driver MSDV](dvinfo-field-settings-in-the-msdv-driver.md)
</dt> </dl>

 

 



