---
description: Os reconhecedores de texto dividem um exemplo de tinta em segmentos e convertem os segmentos de tinta em texto.
ms.assetid: 9fbdde0e-5312-48ec-9273-ded6703b99a9
title: Reconhecedores de texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8372af61d45bb1cc8bcd8377202149073c3decc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663159"
---
# <a name="text-recognizers"></a>Reconhecedores de texto

Os reconhecedores de texto dividem um exemplo de tinta em segmentos e convertem os segmentos de tinta em texto. Isso é útil para reconhecer manuscritos. Ele também é útil em cenários de escrita complexos, como reconhecer glifos kanji individuais e oferecer aos usuários a conclusão automática de um caractere enquanto eles estão gravando.

Um reconhecedor de texto retorna uma cadeia de caracteres Unicode para cada segmento de reconhecimento de tinta. O acompanhamento da cadeia de caracteres é o nível de confiança que o reconhecedor atribui ao resultado e um mapeamento do resultado para a tinta original. Esse mapeamento mostra qual segmento na tinta original corresponde à cadeia de caracteres de código Unicode. A cadeia de caracteres que representa a saída do reconhecedor de texto sempre é representada na ordem linear, em vez de na ordem espacial ou na ordem cronológica em que os segmentos eram inseridos.

A tabela a seguir lista os idiomas com suporte nos reconhecedores de manuscrito da Microsoft e as versões do Windows nas quais esses idiomas foram introduzidos pela primeira vez. Observe que alguns reconhecedores de idioma podem não estar disponíveis em determinadas versões do Windows e precisarão ser baixados separadamente. Os reconhecedores de terceiros também podem estar disponíveis para idiomas adicionais, mas não são necessariamente endossados pela Microsoft.



| Idioma                                   | Windows XP Tablet PC Edition | Windows XP Tablet PC Edition 2005 | Windows Vista | Windows 7 |
|--------------------------------------------|------------------------------|-----------------------------------|---------------|-----------|
| Chinês (simplificado e tradicional)       | X                            |                                   |               |           |
| Inglês (EUA, Reino Unido, Canadá e Austrália)    | X                            |                                   |               |           |
| Francês                                     | X                            |                                   |               |           |
| Alemão                                     | X                            |                                   |               |           |
| Japonês                                   | X                            |                                   |               |           |
| Coreano                                     | X                            |                                   |               |           |
| Espanhol                                    | X                            |                                   |               |           |
| Italiano                                    |                              | X                                 |               |           |
| Holandês (Países Baixos e Bélgica)            |                              |                                   | X             |           |
| Português (Brasil e Português/neutro) |                              |                                   | X             |           |
| Catalão                                    |                              |                                   |               | X         |
| Croata                                   |                              |                                   |               | X         |
| Tcheco                                      |                              |                                   |               | X         |
| Dinamarquês                                     |                              |                                   |               | X         |
| Finlandês                                    |                              |                                   |               | X         |
| Alemão (Suíça)                       |                              |                                   |               | X         |
| Norueguês (Bokmal e Nynorsk)             |                              |                                   |               | X         |
| Polonês                                     |                              |                                   |               | X         |
| Português (Portugal)                      |                              |                                   |               | X         |
| Romeno                                   |                              |                                   |               | X         |
| Russo                                    |                              |                                   |               | X         |
| Sérvio (cirílico e latino)               |                              |                                   |               | X         |
| Espanhol (Argentina e México)             |                              |                                   |               | X         |
| Sueco                                    |                              |                                   |               | X         |



 

 

 



