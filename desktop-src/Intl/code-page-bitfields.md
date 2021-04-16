---
description: A página de código bitfields é usada nas estruturas FONTSIGNATURE e LOCALESIGNATURE. Observe que todas as localidades não oferecem suporte a páginas de código.
ms.assetid: 830b1a88-cb0c-4719-b857-4cc2cd67dd5d
title: Página de código bitfields
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08f9df44ac14d935a026a10ab1e71eb7378840de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758326"
---
# <a name="code-page-bitfields"></a>Página de código bitfields

A página de código bitfields é usada nas estruturas [**fontSignature**](/windows/win32/api/wingdi/ns-wingdi-fontsignature) e [**LOCALESIGNATURE**](/windows/win32/api/wingdi/ns-wingdi-localesignature) .

> [!Note]  
> Todas as localidades não oferecem suporte a páginas de código. O bitfields descrito neste tópico não se aplica a localidades Unicode. Para determinar os scripts com suporte para uma localidade, seu aplicativo pode usar a localidade constante do identificador de localidade [ \_ SSCRIPTS](locale-sscripts.md) com [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex).

 

> [!Note]  
> A presença de um pouco em um campo de página de código não significa necessariamente que todas as cadeias de caracteres de uma localidade possam ser codificadas nessa página de código sem perda. Para preservar os dados sem perda, é recomendável usar Unicode UTF-8 ou UTF-16.

 



| bit          | Página de código | Descrição                                           |
|--------------|-----------|-------------------------------------------------------|
| ANSI         |           |                                                       |
| 0            | 1252      | Latino 1                                               |
| 1            | 1250      | Latino 2: Europa Central                               |
| 2            | 1251      | Cirílico                                              |
| 3            | 1253      | Grego                                                 |
| 4            | 1254      | Turco                                               |
| 5            | 1255      | Hebraico                                                |
| 6            | 1256      | Árabe                                                |
| 7            | 1257      | Báltico                                                |
| 8            | 1258      | Vietnamita                                            |
| 9 - 15       |           | Reservado para ANSI                                     |
| ANSI e OEM |           |                                                       |
| 16           | 874       | Tailandês                                                  |
| 17           | 932       | Japonês, Shift-JIS                                   |
| 18           | 936       | Chinês simplificado (PRC, Cingapura)                   |
| 19           | 949       | Código Hangul unificado coreano (código Hangul TongHabHyung) |
| 20           | 950       | Chinês tradicional (Taiwan; Rae de Hong Kong, PRC)      |
| 21           | 1361      | Coreano (Johab)                                        |
| 22 - 29      |           | Reservado para ANSI e OEM alternativos                   |
| 30 - 31      |           | Reservado pelo sistema.                                   |
| OEM          |           |                                                       |
| 32-46      |           | Reservado para OEM                                      |
| 47           | 1258      | Vietnamita                                            |
| 48           | 869       | Grego moderno                                          |
| 49           | 866       | Russo                                               |
| 50           | 865       | Nórdico                                                |
| 51           | 864       | Árabe                                                |
| 52           | 863       | Francês do Canadá                                       |
| 53           | 862       |                                                       |
| 54           | 861       | Islandês                                             |
| 55           | 860       | Português                                            |
| 56           | 857       | Turco                                               |
| 57           | 855       | Cirílico essencialmente russo                           |
| 58           | 852       | Latino 2                                               |
| 59           | 775       | Báltico                                                |
| 60           | 737       | Ipsum anteriormente 437G                                  |
| 61           | 708; 720  | Árabe ASMO 708                                      |
| 62           | 850       | Multilíngue latino 1                                  |
| 63           | 437       | EUA                                                    |



 

 

 



