---
description: Os reconhecedores de texto dividem uma amostra de tinta em segmentos e convertem os segmentos de tinta em texto.
ms.assetid: 9fbdde0e-5312-48ec-9273-ded6703b99a9
title: Reconhecedores de texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f2a579681fbd06c6b5dd27e5388f2c797e6be50433e11490fb5fe204d1c65d6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119842816"
---
# <a name="text-recognizers"></a>Reconhecedores de texto

Os reconhecedores de texto dividem uma amostra de tinta em segmentos e convertem os segmentos de tinta em texto. Isso é útil para reconhecer a manuscrito. Também é útil em cenários de escrita complexos, como reconhecer glifos Kanji individuais e oferecer aos usuários o preenchimento automático de um caractere enquanto eles o escrevem.

Um reconhecedor de texto retorna uma cadeia de caracteres Unicode para cada segmento de reconhecimento de tinta. Acompanhar a cadeia de caracteres é o nível de confiança que o reconhecedor atribui ao resultado e um mapeamento do resultado de volta para a tinta original. Esse mapeamento mostra qual segmento na tinta original corresponde à cadeia de caracteres de código Unicode. A cadeia de caracteres que representa a saída do reconhecedor de texto é sempre representada na ordem linear, em vez de na ordem espacial ou ordem cronológica na qual os segmentos eram entrada.

A tabela a seguir lista os idiomas com suporte pelos reconhecedores de manuscrito da Microsoft e as versões Windows em que esses idiomas foram introduzidos pela primeira vez. Observe que alguns reconhecedores de idioma podem não estar disponíveis em determinada versão do Windows e precisarão ser baixados separadamente. Os reconhecedores de terceiros também podem estar disponíveis para idiomas adicionais, mas não necessariamente são endossados pela Microsoft.



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
| Holandês (Países Baixos e Canadá)            |                              |                                   | X             |           |
| Português (Brasil e Português/Neutro) |                              |                                   | X             |           |
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



 

 

 



