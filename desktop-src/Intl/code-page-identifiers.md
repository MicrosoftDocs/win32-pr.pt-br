---
description: A tabela a seguir define os identificadores de página de código disponíveis.
ms.assetid: 5d6fc86a-f205-4d14-bb7c-ecd71682e0fe
title: Identificadores de página de código
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35fb0482247313e8d61d61d7d3178906536ab9e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090263"
---
# <a name="code-page-identifiers"></a>Identificadores de página de código

A tabela a seguir define os identificadores de página de código disponíveis.

> [!Note]  
> As páginas de código ANSI podem ser diferentes em computadores diferentes ou podem ser alteradas para um único computador, levando à corrupção de dados. Para os resultados mais consistentes, os aplicativos devem usar Unicode, como UTF-8 ou UTF-16, em vez de uma página de código específica.

 



| Identificador | Nome do .NET               | Informações adicionais                                                                              |
|------------|-------------------------|-----------------------------------------------------------------------------------------------------|
| 037        | IBM037                  | US-Canada IBM EBCDIC                                                                                |
| 437        | IBM437                  | Estados Unidos OEM                                                                                   |
| 500        | IBM500                  | IBM EBCDIC internacional                                                                            |
| 708        | ASMO-708                | Árabe (ASMO 708)                                                                                   |
| 709        |                         | Árabe (ASMO-449 +, BCON v4)                                                                         |
| 710        |                         | Árabe-árabe transparente                                                                         |
| 720        | DOS – 720                 | Árabe (ASMO transparente); Árabe (DOS)                                                             |
| 737        | ibm737                  | OEM grego (anteriormente 437G); Grego (DOS)                                                              |
| 775        | ibm775                  | Báltico OEM; Báltico (DOS)                                                                            |
| 850        | ibm850                  | OEM multilíngue latino 1; Europeu Ocidental (DOS)                                                    |
| 852        | ibm852                  | OEM latino 2; Europa Central (DOS)                                                                 |
| 855        | IBM855                  | OEM cirílico (essencialmente, russo)                                                                    |
| 857        | ibm857                  | OEM Turco; Turco (DOS)                                                                          |
| 858        | IBM00858                | Símbolo de euro multilíngue latino 1 +                                                              |
| 860        | IBM860                  | Português do OEM; Português (DOS)                                                                    |
| 861        | ibm861                  | OEM Islandês; Islandês (DOS)                                                                      |
| 862        | DOS – 862                 | OEM Hebraico; Hebraico (DOS)                                                                            |
| 863        | IBM863                  | OEM francês canadense; Francês canadense (DOS)                                                          |
| 864        | IBM864                  | OEM árabe; Árabe (864)                                                                            |
| 865        | IBM865                  | Nórdico OEM; Nórdico (DOS)                                                                            |
| 866        | cp866                   | OEM russo; Cirílico (DOS)                                                                         |
| 869        | ibm869                  | Grego moderno do OEM; Grego, moderno (DOS)                                                               |
| 870        | IBM870                  | IBM EBCDIC multilíngue/ROECE (latino 2); IBM EBCDIC latino multilíngue 2                            |
| 874        | Windows-874             | Tailandês (Windows)                                                         |
| 875        | cp875                   | IBM EBCDIC grego moderno                                                                             |
| 932        | SHIFT \_ JIS              | ANSI/OEM japonês; Japonês (Shift-JIS)                                                             |
| 936        | GB2312                  | Chinês simplificado para ANSI/OEM (PRC, Cingapura); Chinês simplificado (GB2312)                           |
| 949        | KS \_ c \_ 5601-1987        | ANSI/OEM coreano (código Hangul unificado)                                                               |
| 950        | Big5                    | Chinês tradicional ANSI/OEM (Taiwan; Rae de Hong Kong, PRC); Chinês tradicional (Big5)               |
| 1026       | IBM1026                 | IBM EBCDIC Turco (latino 5)                                                                        |
| 1047       | IBM01047                | IBM EBCDIC Latin 1/sistema aberto                                                                      |
| 1140       | IBM01140                | IBM EBCDIC US-Canada (037 + símbolo de euro); IBM EBCDIC (EUA-Canadá-Euro)                               |
| 1141       | IBM01141                | IBM EBCDIC Alemanha (20273 + símbolo de euro); IBM EBCDIC (Alemanha-euro)                                 |
| 1142       | IBM01142                | IBM EBCDIC Denmark-Norway (20277 + símbolo de euro); IBM EBCDIC (Dinamarca-Noruega-euro)                   |
| 1143       | IBM01143                | IBM EBCDIC Finland-Sweden (20278 + símbolo de euro); IBM EBCDIC (Finlândia-Suécia-euro)                   |
| 1144       | IBM01144                | IBM EBCDIC Itália (20280 + símbolo de euro); IBM EBCDIC (Itália-Euro)                                     |
| 1145       | IBM01145                | IBM EBCDIC latino America-Spain (20284 + símbolo de euro); IBM EBCDIC (Espanha-Euro)                       |
| 1146       | IBM01146                | IBM EBCDIC Reino Unido (20285 + símbolo de euro); IBM EBCDIC (Reino Unido-euro)                               |
| 1147       | IBM01147                | IBM EBCDIC França (20297 + símbolo de euro); IBM EBCDIC (França-euro)                                   |
| 1148       | IBM01148                | IBM EBCDIC internacional (500 + símbolo de euro); IBM EBCDIC (internacional-euro)                       |
| 1149       | IBM01149                | IBM EBCDIC Islandês (20871 + símbolo de euro); IBM EBCDIC (Islandês-euro)                             |
| 1200       | UTF-16                  | Unicode UTF-16, little endian ordem de byte (BMP de ISO 10646); disponível somente para aplicativos gerenciados |
| 1201       | unicodeFFFE             | Unicode UTF-16, big endian ordem de byte; disponível somente para aplicativos gerenciados                       |
| 1250       | Windows-1250            | Europa Central ANSI; Europa Central (Windows)                                                   |
| 1251       | Windows-1251            | ANSI cirílico; Cirílico (Windows)                                                                   |
| 1252       | Windows-1252            | ANSI latino 1; Europeu Ocidental (Windows)                                                            |
| 1253       | Windows-1253            | ANSI grego; Grego (Windows)                                                                         |
| 1254       | Windows-1254            | ANSI Turco; Turco (Windows)                                                                     |
| 1255       | Windows-1255            | ANSI Hebraico; Hebraico (Windows)                                                                       |
| 1256       | Windows-1256            | ANSI árabe; Árabe (Windows)                                                                       |
| 1257       | Windows-1257            | Báltico ANSI; Báltico (Windows)                                                                       |
| 1258       | Windows-1258            | ANSI/OEM vietnamita; Vietnamita (Windows)                                                           |
| 1361       | Johab                   | Coreano (Johab)                                                                                      |
| 10000      | </c0>               | MAC Romano; Europeu Ocidental (Mac)                                                                   |
| 10001      | x-Mac-japonês          | Japonês (Mac)                                                                                      |
| 10002      | x-Mac-chinesetrad       | MAC tradicional chinês (Big5); Chinês tradicional (Mac)                                           |
| 10003      | x-Mac-coreano            | Coreano (Mac)                                                                                        |
| 10004      | x-Mac-árabe            | Árabe (Mac)                                                                                        |
| 10005      | x-Mac-Hebraico            | Hebraico (Mac)                                                                                        |
| 10006      | x-Mac-grego             | Grego (Mac)                                                                                         |
| 10007      | x-Mac-cirílico          | Cirílico (Mac)                                                                                      |
| 10008      | x-Mac-chinesesimp       | MAC simplificado em Chinês (GB 2312); Chinês simplificado (Mac)                                          |
| 10010      | x-Mac-romeno          | Romeno (Mac)                                                                                      |
| 10017      | x-Mac-ucraniano         | Ucraniano (Mac)                                                                                     |
| 10021      | x-Mac-tailandês              | Tailandês (Mac)                                                                                          |
| 10029      | x-Mac-CE                | MAC latino 2; Europa Central (Mac)                                                                 |
| 10079      | x-Mac-Islandês         | Islandês (Mac)                                                                                     |
| 10081      | x-Mac-Turco           | Turco (Mac)                                                                                       |
| 10082      | x-Mac-Croata          | Croata (Mac)                                                                                      |
| 12000      | UTF-32                  | Unicode UTF-32, little endian ordem de byte; disponível somente para aplicativos gerenciados                    |
| 12001      | UTF-32BE                | Unicode UTF-32, big endian ordem de byte; disponível somente para aplicativos gerenciados                       |
| 20000      | x-chinês \_ CNS          | CNS Taiwan; Chinês tradicional (CNS)                                                               |
| 20001      | x-cp20001               | TCA de Taiwan                                                                                          |
| 20002      | x \_ chinês-eTEN         | Eten Taiwan; Chinês tradicional (eTEN)                                                             |
| 20003      | x-cp20003               | IBM5550 Taiwan                                                                                      |
| 20004      | x-cp20004               | TELETEXT Taiwan                                                                                     |
| 20005      | x-cp20005               | Wang Taiwan                                                                                         |
| 20105      | x-IA5                   | IA5 (IRV International alfabeto no. 5, 7 bits); Europeu Ocidental (IA5)                               |
| 20106      | x-IA5-alemão            | IA5 alemão (7 bits)                                                                                  |
| 20107      | x-IA5-Sueco           | IA5 sueco (7 bits)                                                                                 |
| 20108      | x-IA5-norueguês         | IA5 norueguês (7 bits)                                                                               |
| 20127      | US-ASCII                | US-ASCII (7 bits)                                                                                    |
| 20261      | x-cp20261               | T. 61                                                                                                |
| 20269      | x-cp20269               | ISO 6937 Acento sem Espaçamento                                                                         |
| 20273      | IBM273                  | IBM EBCDIC Alemanha                                                                                  |
| 20277      | IBM277                  | Denmark-Norway IBM EBCDIC                                                                           |
| 20278      | IBM278                  | Finland-Sweden IBM EBCDIC                                                                           |
| 20280      | IBM280                  | IBM EBCDIC Itália                                                                                    |
| 20284      | IBM284                  | America-Spain IBM EBCDIC latino                                                                      |
| 20285      | IBM285                  | IBM EBCDIC Reino Unido                                                                           |
| 20290      | IBM290                  | IBM EBCDIC japonês katakana estendido                                                               |
| 20297      | IBM297                  | IBM EBCDIC França                                                                                   |
| 20420      | IBM420                  | IBM EBCDIC árabe                                                                                   |
| 20423      | IBM423                  | IBM EBCDIC grego                                                                                    |
| 20424      | IBM424                  | IBM EBCDIC Hebraico                                                                                   |
| 20833      | x-EBCDIC-KoreanExtended | IBM EBCDIC coreano estendido                                                                          |
| 20838      | IBM-tailandês                | IBM EBCDIC tailandês                                                                                     |
| 20866      | KOI8-r                  | Russo (KOI8-R); Cirílico (KOI8-R)                                                                 |
| 20871      | IBM871                  | IBM EBCDIC Islandês                                                                                |
| 20880      | IBM880                  | IBM EBCDIC Cirílico Russo                                                                         |
| 20905      | IBM905                  | IBM EBCDIC Turco                                                                                  |
| 20924      | IBM00924                | IBM EBCDIC latino 1/sistema aberto (1047 + símbolo de euro)                                                 |
| 20932      | EUC-JP                  | Japonês (JIS 0208-1990 e 0212-1990)                                                              |
| 20936      | x-cp20936               | Chinês simplificado (GB2312); Chinês simplificado (GB2312-80)                                         |
| 20949      | x-cp20949               | Wansung coreano                                                                                      |
| 21025      | cp1025                  | Serbian-Bulgarian IBM EBCDIC cirílico                                                               |
| 21027      |                         | preterido                                                                                        |
| 21866      | KOI8-u                  | Ucraniano (KOI8-U); Cirílico (KOI8-U)                                                               |
| 28591      | ISO-8859-1              | ISO 8859-1 latino 1; Europeu Ocidental (ISO)                                                          |
| 28592      | ISO-8859-2              | ISO 8859-2 Europa Central; Europa Central (ISO)                                                 |
| 28593      | ISO-8859-3              | ISO 8859-3 latino 3                                                                                  |
| 28594      | ISO-8859-4              | Báltico ISO 8859-4                                                                                   |
| 28595      | ISO-8859-5              | ISO 8859-5 Cirílico                                                                                 |
| 28596      | ISO-8859-6              | ISO 8859-6 Árabe                                                                                   |
| 28597      | ISO-8859-7              | ISO 8859-7 Grego                                                                                    |
| 28598      | ISO-8859-8              | ISO 8859-8 Hebraico; Hebraico (ISO-Visual)                                                              |
| 28599      | ISO-8859-9              | ISO 8859-9 Turco                                                                                  |
| 28603      | ISO-8859-13             | ISO 8859-13 estoniano                                                                                |
| 28605      | ISO-8859-15             | ISO 8859-15 latino 9                                                                                 |
| 29001      | x-Europa                | Europa 3                                                                                            |
| 38598      | ISO-8859-8-i            | ISO 8859-8 Hebraico; Hebraico (ISO-lógico)                                                             |
| 50220      | ISO-2022-JP             | ISO 2022 japonês sem Katakana de meia-largura; Japonês (JIS)                                        |
| 50221      | csISO2022JP             | ISO 2022 japonês com Katakana de meia-largura; Japonês (JIS-permitir kana de 1 byte)                         |
| 50222      | ISO-2022-JP             | ISO 2022 japonês JIS X 0201-1989; Japonês (JIS-permitir kana de 1 byte-SO/SI)                         |
| 50225      | ISO-2022-KR             | ISO 2022 coreano                                                                                     |
| 50227      | x-cp50227               | ISO 2022 chinês simplificado; Chinês simplificado (ISO 2022)                                          |
| 50229      |                         | ISO 2022 chinês tradicional                                                                        |
| 50930      |                         | EBCDIC japonês (katakana) estendido                                                                 |
| 50931      |                         | EBCDIC US-Canada e japonês                                                                       |
| 50933      |                         | EBCDIC coreano estendido e coreano                                                                   |
| 50935      |                         | EBCDIC chinês simplificado e chinês simplificado                                           |
| 50936      |                         | EBCDIC chinês simplificado                                                                           |
| 50937      |                         | EBCDIC US-Canada e chinês tradicional                                                            |
| 50939      |                         | EBCDIC japonês (latino) estendido e japonês                                                       |
| 51932      | EUC-JP                  | Japonês EUC                                                                                        |
| 51936      | EUC-CN                  | Chinês simplificado-EUC; Chinês simplificado (EUC)                                                    |
| 51949      | EUC-Kr                  | Coreano EUC                                                                                          |
| 51950      |                         | Chinês tradicional de EUC                                                                             |
| 52936      | Hz-GB-2312              | HZ-GB2312 chinês simplificado; Chinês simplificado (HZ)                                               |
| 54936      | GB18030                 | **Windows XP e posterior:** Chinês simplificado GB18030 (4 bytes); Chinês simplificado (GB18030)         |
| 57002      | x-ISCII-de              | ISCII Devanágari                                                                                    |
| 57003      | x-ISCII-ser              | ISCII Bengali                                                                                        |
| 57004      | x-ISCII-ta              | ISCII tâmil                                                                                         |
| 57005      | x-ISCII-te              | ISCII télugo                                                                                        |
| 57006      | x-ISCII-as              | ISCII Assamês                                                                                      |
| 57007      | x-ISCII-ou              | ISCII odia                                                                                          |
| 57008      | x-ISCII-Ka              | ISCII Kannada                                                                                       |
| 57009      | x-ISCII-ma              | ISCII malaiala                                                                                     |
| 57010      | x-ISCII-Gu              | ISCII Guzerate                                                                                      |
| 57011      | x-ISCII-PA              | ISCII Punjabi                                                                                       |
| 65000      | UTF-7                   | Unicode (UTF-7)                                                                                     |
| 65001      | utf-8                   | Unicode (UTF-8)                                                                                     |



 

 

 



