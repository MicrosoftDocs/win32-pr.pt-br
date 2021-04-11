---
description: Pacote de origem do AAUX (AS)
ms.assetid: 0e173fe5-0b9d-48e8-bcbd-403614d51558
title: Pacote de origem do AAUX (AS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe479a0740da08f42ca5d80e1f0b6f5174f6917b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104163860"
---
# <a name="aaux-source-as-pack"></a>Pacote de origem do AAUX (AS)

As tabelas a seguir listam os valores usados pelo driver MSDV para preencher os membros **dwDVAAuxSrc** e **DwDVAAuxSrc1** da estrutura [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) . Para obter mais informações, consulte [configurações de campo DVINFO no driver MSDV](dvinfo-field-settings-in-the-msdv-driver.md).

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

LF (1)

1

1

1

1

Reservado (1)

1

1

1

1

TAMANHO DA AF (6)

00:1111

01:0000

00:1111

01:0000

SM (1)

0

0

0

0

CHN (2)

01

01

01

01

PA (1)

1

1

1

1

MODO DE ÁUDIO (4)

    Audio Block 1\*

0000

0000

0000

0000

    Audio Block 2\*

0000

0000

1111

1111

Reservado (1)

1

1

1

1

ML (1)

1

1

1

1

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

EF (1)

1

1

1

1

TC (1)

1

1

1

1

SMP (3)

010

010

010

010

T (3)

001

001

001

001

Como pacote

    Audio Block 1\*

0xD1C130CF

0xD1E130D0

0xD1C030CF

0xD1E030D0

    Audio Block 2\*

0x00000000

0x00000000

0xD1C03FCF

0xD1E03FD0



 

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

LF (1)

0

0

0

0

Reservado (1)

1

1

1

1

TAMANHO DA AF (6)

01:0110

01:1000

01:0110

01:1000

Reservado (1)

0

0

0

0

CHN (2)

00

00

00

00

Reservado (1)

1

1

1

1

MODO DE ÁUDIO (4)

    Audio Block 1\*

0000

0000

0000

0000

    Audio Block 2\*

0001

0001

0001

0001

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

0:0010

0:0010

Reservado (2)

11

11

11

11

SMP (3)

000

000

000

000

T (3)

000

000

000

000

Como pacote

    Audio Block 1\*

0xC0C01056

0xC0E01058

0xC0C21056

0xC0E21058

    Audio Block 2\*

0xC0C01156

0xC0E01158

0xC0C21156

0xC0E21158



 

> [!Note]  
> \* A estrutura [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) contém dois AAUX como pacotes para os blocos de áudio 1 e 2. DV50 tem quatro blocos de áudio; os blocos 3 e 4 não são representados na estrutura **DVINFO** .

 

Configurações do DVCR 100 (planejadas)



DV Standard

DVCPRO 100 – planejado

FOURCC

dvh1

Sistema

1080-60i

720-60P

1080-50i

LF (1)

0

0

0

Reservado (1)

1

1

1

TAMANHO DA AF (6)

01:0110

01:0110

01:1000

Reservado (1)

0

0

0

CHN (2)

00

00

00

Reservado (1)

1

1

1

MODO DE ÁUDIO (4)

    Audio Block 1\*

0000

0000

0000

    Audio Block 2\*

0001

0001

0001

Reservado (2)

11

11

11

50/60 (1)

0

0

1

STYPE (5)

0:0011

0:0011

0:0011

Reservado (2)

11

11

11

SMP (3)

000

000

000

T (3)

000

000

000

Como pacote

    Audio Block 1\*

0xC0C31056

0xC0C31056

0xC0D31058

    Audio Block 2\*

0xC0C31156

0xC0C31156

0xC0D31158



 

> [!Note]  
> \* O DVCPRO 100 tem 8 blocos de áudio; os blocos de 3 a 8 não são representados na estrutura [DVINFO](dvinfo-field-settings-in-the-msdv-driver.md) .

 

## <a name="remarks"></a>Comentários

Os códigos de campo a seguir são de interesse:

-   LF: sinalizador de modo bloqueado. Indica se o áudio está bloqueado.
    -   0 = bloqueado
    -   1 = desbloqueado
-   TAMANHO do AF: tamanho do quadro de áudio. Especifica o número de amostras de áudio por quadro.

    Definição de IEC 61834:

    -   00:1111 = 1068 amostras por quadro
    -   01:0000 = 1280 amostras por quadro

    Definição de 314M SMPTE:

    -   01:0110 = 1602 amostras por quadro
    -   01:1000 = 1920 amostras por quadro

    Dependendo da taxa de quadros, o número exato de amostras em um quadro pode variar. Por exemplo, NTSC é de 30000/1001 quadros por segundo (29,97 fps). Com áudio de 32-kHz, há cerca de 1067,73 amostras de áudio por quadro. Portanto, a taxa nominal é 1068, mas o número real varia por quadro. Além disso, com áudio desbloqueado, o número de amostras de áudio por quadro tem permissão para variar dentro de um determinado intervalo ao longo do tempo.

<!-- -->

-   SM: modo estéreo.
    -   0 = estéreo
    -   1 = mono
-   CHN: número de canais de áudio por bloco de áudio.
    -   0 = um canal por bloco de áudio
    -   1 = dois canais por bloco de áudio
-   MODO de áudio: indica o conteúdo do sinal de áudio em cada canal. A interpretação desse campo depende de quais valores são colocados nos campos SM e CHN. As definições fornecidas abaixo são para os valores usados por MSDV; Consulte as especificações para obter mais informações.

    Definição de IEC 61834:

    -   0000 = ch a/c/e/g é o canal esquerdo, ch b/d/f/h é o canal correto
    -   1111 = não há dados de áudio

    Definição de 314M SMPTE:

    -   0000 = CH1 (CH3)
    -   0001 = CH2 (CH4)

-   50/60: número de campos.
    -   0 = 60 campos
    -   1 = 50 campos
-   STYPE: tipo de sistema.

    Definição de IEC 61834:

    -   00000 = 525-60 ou 625-50, dvsd
    -   00001 = 525-60 ou 625-50, dvsl (consulte IEC 61883-5)

    Definição de 314M/SPMTE 370 SMPTE:

    -   00000 = 2 blocos de áudio por quadro de vídeo
    -   00010 = 4 blocos de áudio por quadro de vídeo
    -   00011 = 8 blocos de áudio por quadro de vídeo

-   SMP: frequência de amostragem.
    -   000 = 48 kHz
    -   010 = 32 kHz
-   T: quantização.
    -   0 = 16 bits linear
    -   1 = 12 bits não lineares

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Vídeo digital no DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[Configurações de campo DVINFO no driver MSDV](dvinfo-field-settings-in-the-msdv-driver.md)
</dt> </dl>

 

 



