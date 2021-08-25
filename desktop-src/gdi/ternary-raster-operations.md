---
description: Esta seção lista os códigos de operação de varredura Ternário usados pelas funções BitBlt, PatBlt e StretchBlt. Os códigos de operação de varredura Ternário definem como a GDI combina os bits em um bitmap de origem com os bits no bitmap de destino.
ms.assetid: 538f3580-d6a7-4dae-8185-802eb9c96735
title: Operações de rasterização ternário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58a6dd0009a9be4a1fe062dbb2ab40766a7b01a565b80a7b866c0ce1af40ca48
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119889006"
---
# <a name="ternary-raster-operations"></a>Operações de rasterização ternário

Esta seção lista os códigos de operação de varredura Ternário usados pelas funções [**BitBlt**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt), [**PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt)e [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) . Os códigos de operação de varredura Ternário definem como a GDI combina os bits em um bitmap de origem com os bits no bitmap de destino.

Cada código de operação de varredura representa uma operação booliana na qual os valores dos pixels na origem, o pincel selecionado e o destino são combinados. A seguir estão os três operandos usados nessas operações.



| Operando | Significado                              |
|---------|--------------------------------------|
| D       | Bitmap de destino                   |
| P       | Pincel selecionado (também chamado de padrão) |
| S       | Bitmap de origem                        |



 

Os operadores boolianos usados nessas operações são os seguintes.



| Operador | Significado                    |
|----------|----------------------------|
| um        | AND bit a bit                |
| n        | Não-bit (inverso)      |
| o        | OR bit a bit                 |
| x        | Or exclusivo de bit (XOR) |



 

Todas as operações boolianas são apresentadas em notação de polonês reverso. Por exemplo, a operação a seguir substitui os valores dos pixels no bitmap de destino por uma combinação dos valores de pixel da fonte e do pincel:


```C++
PSo 
```



A operação a seguir combina os valores dos pixels na origem e no pincel com os valores de pixel do bitmap de destino (há grafias alternativas da mesma função, portanto, embora uma grafia específica possa não estar na lista, um formato equivalente seria):


```C++
DPSoo 
```



Cada código de operação de rasterização é um inteiro de 32 bits cuja palavra de ordem superior é um índice de operação booliano e cuja palavra de ordem inferior é o código de operação. O índice de operação de 16 bits é um valor de 8 bits de extensão zero que representa o resultado da operação booliana em valores de pincel, origem e destino predefinidos. Por exemplo, os índices de operação para as operações PSo e DPSoo são mostrados na lista a seguir.



| P                | S   | D   | PSo   | DPSoo |
|------------------|-----|-----|-------|-------|
| 0                | 0   | 0   | 0     | 0     |
| 0                | 0   | 1   | 0     | 1     |
| 0                | 1   | 0   | 1     | 1     |
| 0                | 1   | 1   | 1     | 1     |
| 1                | 0   | 0   | 1     | 1     |
| 1                | 0   | 1   | 1     | 1     |
| 1                | 1   | 0   | 1     | 1     |
| 1                | 1   | 1   | 1     | 1     |
| Índice de operação: |     |     | 00FCh | 00FEh |



 

Nesse caso, PSo tem o índice de operação 00FC (leitura de baixo para cima); DPSoo tem o índice de operação 00FE. Esses valores definem o local dos códigos de operação de varredura correspondentes, conforme mostrado na tabela A. 1, "códigos de operação de varredura". A operação PSo está na linha 252 (00FCh) da tabela; DPSoo está na linha 254 (00FEh).

As operações de varredura mais comumente usadas receberam nomes especiais no arquivo de cabeçalho do SDK, WINDOWS. H. Você deve usar esses nomes sempre que possível em seus aplicativos.

Quando os bitmaps de origem e de destino são monocromáticos, um valor de bit igual a zero representa um pixel preto e um valor de bit 1 representa um pixel branco. Quando os bitmaps de origem e de destino são coloridos, essas cores são representadas com valores RGB. Para obter mais informações sobre valores RGB, consulte [**RGB**](/windows/desktop/api/Wingdi/nf-wingdi-rgb).

**Raster-códigos de operação**



| Função booliana (hexadecimal) | Operação de rasterização (hexadecimal) | Função booliana em polonês reverso | Nome comum    |
|--------------------------------|--------------------------------|------------------------------------|----------------|
| 00                             | 00000042                       | 0                                  | ESCURIDÃO      |
| 01                             | 00010289                       | DPSoon                             |                |
| 02                             | 00020C89                       | DPSona                             |                |
| 03                             | 000300AA                       | PSon                               |                |
| 04                             | 00040C88                       | SDPona                             |                |
| 05                             | 000500A9                       | DPon                               |                |
| 06                             | 00060865                       | PDSxnon                            |                |
| 07                             | 000702C5                       | PDSaon                             |                |
| 08                             | 00080F08                       | SDPnaa                             |                |
| 9                             | 00090245                       | PDSxon                             |                |
| 0A                             | 000A0329                       | DPna                               |                |
| 0B                             | 000B0B2A                       | PSDnaon                            |                |
| 0C                             | 000C0324                       | SPna                               |                |
| 0D                             | 000D0B25                       | PDSnaon                            |                |
| 0E                             | 000E08A5                       | PDSonon                            |                |
| 0F                             | 000F0001                       | NP                                 |                |
| 10                             | 00100C85                       | PDSona                             |                |
| 11                             | 001100A6                       | DSon                               | NOTSRCERASE    |
| 12                             | 00120868                       | SDPxnon                            |                |
| 13                             | 001302C8                       | SDPaon                             |                |
| 14                             | 00140869                       | DPSxnon                            |                |
| 15                             | 001502C9                       | DPSaon                             |                |
| 16                             | 00165CCA                       | PSDPSanaxx                         |                |
| 17                             | 00171D54                       | SSPxDSxaxn                         |                |
| 18                             | 00180D59                       | SPxPDxa                            |                |
| 19                             | 00191CC8                       | SDPSanaxn                          |                |
| 1A                             | 001A06C5                       | PDSPaox                            |                |
| 1B                             | 001B0768                       | SDPSxaxn                           |                |
| 1C                             | 001C06CA                       | PSDPaox                            |                |
| 1D                             | 001D0766                       | DSPDxaxn                           |                |
| 1E                             | 001E01A5                       | PDSox                              |                |
| 1F                             | 001F0385                       | PDSoan                             |                |
| 20                             | 00200F09                       | DPSnaa                             |                |
| 21                             | 00210248                       | SDPxon                             |                |
| 22                             | 00220326                       | DSna                               |                |
| 23                             | 00230B24                       | SPDnaon                            |                |
| 24                             | 00240D55                       | SPxDSxa                            |                |
| 25                             | 00251CC5                       | PDSPanaxn                          |                |
| 26                             | 002606C8                       | SDPSaox                            |                |
| 27                             | 00271868                       | SDPSxnox                           |                |
| 28                             | 00280369                       | DPSxa                              |                |
| 29                             | 002916CA                       | PSDPSaoxxn                         |                |
| 2A                             | 002A0CC9                       | DPSana                             |                |
| 2B                             | 002B1D58                       | SSPxPDxaxn                         |                |
| 2C                             | 002C0784                       | SPDSoax                            |                |
| 2D                             | 002D060A                       | PSDnox                             |                |
| 2E                             | 002E064A                       | PSDPxox                            |                |
| 2F                             | 002F0E2A                       | PSDnoan                            |                |
| 30                             | 0030032A                       | PSna                               |                |
| 31                             | 00310B28                       | SDPnaon                            |                |
| 32                             | 00320688                       | SDPSoox                            |                |
| 33                             | 00330008                       | Sn                                 | NOTSRCCOPY     |
| 34                             | 003406C4                       | SPDSaox                            |                |
| 35                             | 00351864                       | SPDSxnox                           |                |
| 36                             | 003601A8                       | SD Ltda                              |                |
| 37                             | 00370388                       | SDPoan                             |                |
| 38                             | 0038078A                       | PSDPoax                            |                |
| 39                             | 00390604                       | SPDnox                             |                |
| 3A                             | 003A0644                       | SPDSxox                            |                |
| 3B                             | 003B0E24                       | SPDnoan                            |                |
| 3C                             | 003C004A                       | Psx                                |                |
| 3D                             | 003D18A4                       | SPDSonox                           |                |
| 3E                             | 003E1B24                       | SPDSnaox                           |                |
| 3F                             | 003F00EA                       | PSan                               |                |
| 40                             | 00400F0A                       | PSDnaa                             |                |
| 41                             | 00410249                       | DPSax                             |                |
| 42                             | 00420D5D                       | SDxPDxa                            |                |
| 43                             | 00431CC4                       | SPDSanaxn                          |                |
| 44                             | 00440328                       | SDna                               | SRCERASE       |
| 45                             | 00450B29                       | DPSnaon                            |                |
| 46                             | 004606C6                       | DSPDaox                            |                |
| 47                             | 0047076A                       | PSDPxaxn                           |                |
| 48                             | 00480368                       | SDPxa                              |                |
| 49                             | 004916C5                       | PDSPDaoxxn                         |                |
| 4A                             | 004A0789                       | DPSDoax                            |                |
| 4B                             | 004B0605                       | PDSnox                             |                |
| 4C                             | 004C0CC8                       | SDPana                             |                |
| 4D                             | 004D1954                       | SSPxDSxoxn                         |                |
| 4E                             | 004E0645                       | PDSPxox                            |                |
| 4F                             | 004F0E25                       | PDSnoan                            |                |
| 50                             | 00500325                       | PDna                               |                |
| 51                             | 00510B26                       | DSPnaon                            |                |
| 52                             | 005206C9                       | DPSDaox                            |                |
| 53                             | 00530764                       | SPDSxaxn                           |                |
| 54                             | 005408A9                       | DPSonon                            |                |
| 55                             | 00550009                       | Dn                                 | DSTINVERT      |
| 56                             | 005601A9                       | DPSox                              |                |
| 57                             | 00570389                       | DPSoan                             |                |
| 58                             | 00580785                       | PDSPoax                            |                |
| 59                             | 00590609                       | DPSnox                             |                |
| 5A                             | 005A0049                       | DPx                                | PATINVERT      |
| 5B                             | 005B18A9                       | DPSDonox                           |                |
| 5C                             | 005C0649                       | DPSDxox                            |                |
| 5D                             | 005D0E29                       | DPSnoan                            |                |
| 5E                             | 005E1B29                       | DPSDnaox                           |                |
| 5F                             | 005F00E9                       | DPan                               |                |
| 60                             | 00600365                       | PDSxa                              |                |
| 61                             | 006116C6                       | DSPDSaoxxn                         |                |
| 62                             | 00620786                       | DSPDoax                            |                |
| 63                             | 00630608                       | SDPnox                             |                |
| 64                             | 00640788                       | SDPSoax                            |                |
| 65                             | 00650606                       | DSPnox                             |                |
| 66                             | 00660046                       | DSx                                | SRCINVERT      |
| 67                             | 006718A8                       | SDPSonox                           |                |
| 68                             | 006858A6                       | DSPDSonoxxn                        |                |
| 69                             | 00690145                       | PDSxxn                             |                |
| 6A                             | 006A01E9                       | DPSax                              |                |
| 6b                             | 006B178A                       | PSDPSoaxxn                         |                |
| 6C                             | 006C01E8                       | SDPax                              |                |
| 6d                             | 006D1785                       | PDSPDoaxxn                         |                |
| 6E                             | 006E1E28                       | SDPSnoax                           |                |
| 6f                             | 006F0C65                       | PDSxnan                            |                |
| 70                             | 00700CC5                       | PDSana                             |                |
| 71                             | 00711D5C                       | SSDxPDxaxn                         |                |
| 72                             | 00720648                       | SDPSxox                            |                |
| 73                             | 00730E28                       | SDPnoan                            |                |
| 74                             | 00740646                       | DSPDxox                            |                |
| 75                             | 00750E26                       | DSPnoan                            |                |
| 76                             | 00761B28                       | SDPSnaox                           |                |
| 77                             | 007700E6                       | DSan                               |                |
| 78                             | 007801E5                       | PDSax                              |                |
| 79                             | 00791786                       | DSPDSoaxxn                         |                |
| 7a                             | 007A1E29                       | DPSDnoax                           |                |
| 7b                             | 007B0C68                       | SDPxnan                            |                |
| 7C                             | 007C1E24                       | SPDSnoax                           |                |
| 7d                             | 007D0C69                       | DPSxnan                            |                |
| 7E                             | 007E0955                       | SPxDSxo                            |                |
| 7f                             | 007F03C9                       | DPSaan                             |                |
| 80                             | 008003E9                       | DPSaa                              |                |
| 81                             | 00810975                       | SPxDSpx                           |                |
| 82                             | 00820C49                       | DPSxna                             |                |
| 83                             | 00831E04                       | SPDSnoaxn                          |                |
| 84                             | 00840C48                       | SDPxna                             |                |
| 85                             | 00851E05                       | PDSPnoaxn                          |                |
| 86                             | 008617A6                       | DSPDSoaxx                          |                |
| 87                             | 008701C5                       | PDSaxn                             |                |
| 88                             | 008800C6                       | DSa                                | SRCAND         |
| 89                             | 00891B08                       | SDPSnaoxn                          |                |
| 8A                             | 008A0E06                       | DSPnoa                             |                |
| 8B                             | 008B0666                       | DSPDxoxn                           |                |
| 8C                             | 008C0E08                       | SDPnoa                             |                |
| 8D                             | 008D0668                       | SDPSxoxn                           |                |
| 8E                             | 008E1D7C                       | SSDxPDxax                          |                |
| 8F                             | 008F0CE5                       | PDSanan                            |                |
| 90                             | 00900C45                       | PDSxna                             |                |
| 91                             | 00911E08                       | SDPSnoaxn                          |                |
| 92                             | 009217A9                       | DPSDPoaxx                          |                |
| 93                             | 009301C4                       | SPDaxn                             |                |
| 94                             | 009417AA                       | PSDPSoaxx                          |                |
| 95                             | 009501C9                       | DPSaxn                             |                |
| 96                             | 00960169                       | DPSxx                              |                |
| 97                             | 0097588A                       | PSDPSonoxx                         |                |
| 98                             | 00981888                       | SDPSonoxn                          |                |
| 99                             | 00990066                       | DSxn                               |                |
| 9A                             | 009A0709                       | DPSnax                             |                |
| 9B                             | 009B07A8                       | SDPSoaxn                           |                |
| 9C                             | 009C0704                       | SPDnax                             |                |
| 9D                             | 009D07A6                       | DSPDoaxn                           |                |
| 9E                             | 009E16E6                       | DSPDSaoxx                          |                |
| 9F                             | 009F0345                       | PDSxan                             |                |
| A0                             | 00A000C9                       | DPa                                |                |
| A1                             | 00A11B05                       | PDSPnaoxn                          |                |
| A2                             | 00A20E09                       | DPSnoa                             |                |
| A3                             | 00A30669                       | DPSDxoxn                           |                |
| A4                             | 00A41885                       | PDSPonoxn                          |                |
| A5                             | 00A50065                       | PDxn                               |                |
| A6                             | 00A60706                       | DSPnax                             |                |
| A7                             | 00A707A5                       | PDSPoaxn                           |                |
| A8                             | 00A803A9                       | DPSoa                              |                |
| A9                             | 00A90189                       | DPSoxn                             |                |
| AA                             | 00AA0029                       | D                                  |                |
| AB                             | 00AB0889                       | DPSono                             |                |
| ALTERNA                             | 00AC0744                       | SPDSxax                            |                |
| AD                             | 00AD06E9                       | DPSDaoxn                           |                |
| AE                             | 00AE0B06                       | DSPnao                             |                |
| AF                             | 00AF0229                       | DPno                               |                |
| B0                             | 00B00E05                       | PDSnoa                             |                |
| B1                             | 00B10665                       | PDSPxoxn                           |                |
| B2                             | 00B21974                       | SSPxDSxox                          |                |
| B3                             | 00B30CE8                       | SDPanan                            |                |
| B4                             | 00B4070A                       | PSDnax                             |                |
| B5                             | 00B507A9                       | DPSDoaxn                           |                |
| B6                             | 00B616E9                       | DPSDPaoxx                          |                |
| B7                             | 00B70348                       | SDPxan                             |                |
| B8                             | 00B8074A                       | PSDPxax                            |                |
| B9                             | 00B906E6                       | DSPDaoxn                           |                |
| BA                             | 00BA0B09                       | DPSnao                             |                |
| BB                             | 00BB0226                       | DSno                               | MERGEPAINT     |
| BC                             | 00BC1CE4                       | SPDSanax                           |                |
| BD                             | 00BD0D7D                       | SDxPDxan                           |                |
| BE                             | 00BE0269                       | DPSxo                              |                |
| BF                             | 00BF08C9                       | DPSano                             |                |
| C0                             | 00C000CA                       | PSa                                | MERGECOPY      |
| C1                             | 00C11B04                       | SPDSnaoxn                          |                |
| C2                             | 00C21884                       | SPDSonoxn                          |                |
| C3                             | 00C3006A                       | PSxn                               |                |
| C4                             | 00C40E04                       | SPDnoa                             |                |
| C5                             | 00C50664                       | SPDSxoxn                           |                |
| C6                             | 00C60708                       | SDPnax                             |                |
| C7                             | 00C707AA                       | PSDPoaxn                           |                |
| C8                             | 00C803A8                       | SDPoa                              |                |
| C9                             | 00C90184                       | SPDoxn                             |                |
| CA                             | 00CA0749                       | DPSDxax                            |                |
| CB                             | 00CB06E4                       | SPDSaoxn                           |                |
| CC                             | 00CC0020                       | S                                  | Srccopy        |
| CD                             | 00CD0888                       | SDPono                             |                |
| CE                             | 00CE0B08                       | SDPnao                             |                |
| CF                             | 00CF0224                       | SPno                               |                |
| D0                             | 00D00E0A                       | PSDnoa                             |                |
| D1                             | 00D1066A                       | PSDPxoxn                           |                |
| D2                             | 00D20705                       | PDSnax                             |                |
| D3                             | 00D307A4                       | SPDSoaxn                           |                |
| D4                             | 00D41D78                       | SSPxPDxax                          |                |
| D5                             | 00D50CE9                       | DPSanan                            |                |
| D6                             | 00D616EA                       | PSDPSaoxx                          |                |
| D7                             | 00D70349                       | DPSxan                             |                |
| D8                             | 00D80745                       | PDSPxax                            |                |
| D9                             | 00D906E8                       | SDPSaoxn                           |                |
| DA                             | 00DA1CE9                       | DPSAx                           |                |
| DB                             | 00DB0D75                       | SPxDSxan                           |                |
| DC                             | 00DC0B04                       | SPDnao                             |                |
| DD                             | 00DD0228                       | SDno                               |                |
| DE                             | 00DE0268                       | SDPxo                              |                |
| DF                             | 00DF08C8                       | SDPano                             |                |
| E0                             | 00E003A5                       | PDSoa                              |                |
| E1                             | 00E10185                       | PDSoxn                             |                |
| E2                             | 00E20746                       | DSPDxax                            |                |
| E3                             | 00E306EA                       | PSDPaoxn                           |                |
| E4                             | 00E40748                       | SDPSxax                            |                |
| E5                             | 00E506E5                       | PDSPaoxn                           |                |
| E6                             | 00E61CE8                       | SDPSanax                           |                |
| E7                             | 00E70D79                       | SPxPDxan                           |                |
| E8                             | 00E81D74                       | SSPxDSxax                          |                |
| E9                             | 00E95CE6                       | DSPDSanaxxn                        |                |
| EA                             | 00EA02E9                       | DPSao                              |                |
| EB                             | 00EB0849                       | DPSxno                             |                |
| EC                             | 00EC02E8                       | SDPao                              |                |
| ED                             | 00ED0848                       | SDPxno                             |                |
| EE                             | 00EE0086                       | DSo                                | SRCPAINT       |
| EF                             | 00EF0A08                       | SDPnoo                             |                |
| F0                             | 00F00021                       | P                                  | PATCOPY        |
| F1                             | 00F10885                       | PDSono                             |                |
| F2                             | 00F20B05                       | PDSnao                             |                |
| F3                             | 00F3022A                       | PSno                               |                |
| F4                             | 00F40B0A                       | PSDnao                             |                |
| F5                             | 00F50225                       | PDno                               |                |
| F6                             | 00F60265                       | PDSxo                              |                |
| F7                             | 00F708C5                       | PDSano                             |                |
| F8                             | 00F802E5                       | PDSao                              |                |
| F9                             | 00F90845                       | PDSxno                             |                |
| FA                             | 00FA0089                       | DPo                                |                |
| FB                             | 00FB0A09                       | DPSnoo                             | PATPAINT       |
| FC                             | 00FC008A                       | PSo                                |                |
| FD                             | 00FD0A0A                       | PSDnoo                             |                |
| FE                             | 00FE02A9                       | DPSoo                              |                |
| FF                             | 00FF0062                       | 1                                  | DOCUMENTAÇÃO      |
| 8000                           | 80 milhões                       |                                    | NOMIRRORBITMAP |



 

 

 



