---
description: As funções a seguir são usadas com conjuntos de caracteres.
ms.assetid: 1799f5da-1391-4b6e-ac13-718017a77557
title: Funções de conjunto de caracteres e Unicode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6996139d8a9bb426c21a460ac2bcb1358e6c8e7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011563"
---
# <a name="unicode-and-character-set-functions"></a>Funções de conjunto de caracteres e Unicode

As funções a seguir são usadas com conjuntos de caracteres.



| Função                                                       | Descrição                                                                                                           |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**GetTextCharset**](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharset)                       | Recupera um identificador de conjunto de caracteres para a fonte selecionada no momento em um contexto de dispositivo especificado.         |
| [**GetTextCharsetInfo**](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharsetinfo)               | Recupera informações sobre o conjunto de caracteres da fonte selecionada no momento em um contexto de dispositivo especificado. |
| [**IsDBCSLeadByte**](/windows/desktop/api/Winnls/nf-winnls-isdbcsleadbyte)                       | Determina se um caractere especificado é um byte de Lead para a página de código ANSI padrão do sistema (CP \_ ACP).           |
| [**IsDBCSLeadByteEx**](/windows/desktop/api/Winnls/nf-winnls-isdbcsleadbyteex)                   | Determina se um caractere especificado é potencialmente um byte de Lead.                                                       |
| [**IsTextUnicode**](/windows/desktop/api/Winbase/nf-winbase-istextunicode)                         | Determina se é provável que um buffer contenha uma forma de texto Unicode.                                                   |
| [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar)             | Mapeia uma cadeia de caracteres para uma cadeia de caracteres UTF-16 (caracteres largos).                                                          |
| [**TranslateCharsetInfo**](/windows/desktop/api/Wingdi/nf-wingdi-translatecharsetinfo)           | Traduz informações de conjunto de caracteres e define todos os membros de uma estrutura de destino com os valores apropriados.           |
| [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte)             | Mapeia uma cadeia de caracteres UTF-16 (caracteres largos) para uma nova cadeia de caracteres.                                                      |
| [**BytesToUnicode**](/previous-versions/dd317724(v=vs.85))                       | Não use.                                                                                                           |
| [**NlsDllCodePageTranslation**](/windows/desktop/api/Gb18030/nf-gb18030-nlsdllcodepagetranslation) | Não use.                                                                                                           |
| [**UnicodeToBytes**](/previous-versions/windows/desktop/legacy/dd374082(v=vs.85))                       | Não use.                                                                                                           |



 

 

 
