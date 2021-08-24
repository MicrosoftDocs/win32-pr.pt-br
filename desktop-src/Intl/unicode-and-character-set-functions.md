---
description: As funções a seguir são usadas com conjuntos de caracteres.
ms.assetid: 1799f5da-1391-4b6e-ac13-718017a77557
title: Funções Unicode e conjunto de caracteres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd26edd8931b1a63887816ca07698d779bd0d4d3decceb3b53faf5d499605612
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811706"
---
# <a name="unicode-and-character-set-functions"></a>Funções Unicode e conjunto de caracteres

As funções a seguir são usadas com conjuntos de caracteres.



| Função                                                       | Descrição                                                                                                           |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**GetTextCharset**](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharset)                       | Recupera um identificador de conjunto de caracteres para a fonte selecionada atualmente em um contexto de dispositivo especificado.         |
| [**GetTextCharsetInfo**](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharsetinfo)               | Recupera informações sobre o conjunto de caracteres da fonte atualmente selecionada em um contexto de dispositivo especificado. |
| [**IsDBCSLeadByte**](/windows/desktop/api/Winnls/nf-winnls-isdbcsleadbyte)                       | Determina se um caractere especificado é um byte principal para o padrão do sistema Windows página de código ANSI (CP \_ ACP).           |
| [**IsDBCSLeadByteEx**](/windows/desktop/api/Winnls/nf-winnls-isdbcsleadbyteex)                   | Determina se um caractere especificado é potencialmente um byte de lead.                                                       |
| [**IsTextUnicode**](/windows/desktop/api/Winbase/nf-winbase-istextunicode)                         | Determina se é provável que um buffer contenha uma forma de texto Unicode.                                                   |
| [**Multibytetowidechar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar)             | Mapas cadeia de caracteres em uma cadeia de caracteres UTF-16 (caractere largo).                                                          |
| [**TranslateCharsetInfo**](/windows/desktop/api/Wingdi/nf-wingdi-translatecharsetinfo)           | Converte informações do conjunto de caracteres e define todos os membros de uma estrutura de destino para valores apropriados.           |
| [**Widechartomultibyte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte)             | Mapas uma cadeia de caracteres UTF-16 (caractere largo) para uma nova cadeia de caracteres.                                                      |
| [**BytesToUnicode**](/previous-versions/dd317724(v=vs.85))                       | Não use.                                                                                                           |
| [**NlsDllCodePageTranslation**](/windows/desktop/api/Gb18030/nf-gb18030-nlsdllcodepagetranslation) | Não use.                                                                                                           |
| [**UnicodeToBytes**](/previous-versions/windows/desktop/legacy/dd374082(v=vs.85))                       | Não use.                                                                                                           |



 

 

 
