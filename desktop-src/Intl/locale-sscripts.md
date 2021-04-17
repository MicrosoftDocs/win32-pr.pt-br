---
description: SSCRIPTS de localidade \_
ms.assetid: d15c501a-b77b-4446-bee6-6dbbd714b4e0
title: LOCALE_SSCRIPTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bb79f78626e7afb54229d8e0619e26d94250f86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770390"
---
# <a name="locale_sscripts"></a>SSCRIPTS de localidade \_

**Windows Vista e posterior:** Uma cadeia de caracteres que representa uma lista de scripts, usando a notação de 4 caracteres usada no [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html). Cada nome de script consiste em quatro caracteres latinos e a lista é organizada em ordem alfabética com cada nome, incluindo o último, seguido por um ponto-e-vírgula.

[**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) ou [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) podem ser chamados com *LCTYPE* definido como localidade \_ SSCRIPTS como parte de uma estratégia para atenuar problemas de segurança relacionados a IDNs (nomes de domínio internacionalizados). Aqui estão alguns exemplos de valores:



| Locale                  | Nome da localidade/idioma | Valor                                                                                                  |
|-------------------------|----------------------|--------------------------------------------------------------------------------------------------------|
| Inglês (Estados Unidos) | pt-BR                | Latn                                                                                                  |
| Híndi (Índia)           | hi-IN                | DESVPADPA                                                                                                  |
| Japonês (Japão)        | ja-JP                | **Windows 7 e posterior:** Hani; Hira; Jpan; Kana<br/> **Windows Vista:** Hani; Hira; Kana<br/> |



 

Um valor de script composto não inclui o script latino, a menos que seja uma parte essencial do sistema de escrita usado para a localidade específica. Os caracteres latinos são geralmente usados no contexto de localidades para os quais não são nativos, por exemplo, para um nome comercial estrangeiro. No exemplo acima para Hindi na Índia, o único valor de script é "DESVPADA" (para "Devanágari"), embora os caracteres latinos também possam aparecer em texto em Híndi. A função [VerifyScripts](/windows/desktop/api/Winnls/nf-winnls-verifyscripts) tem um sinalizador especial para resolver esse caso.

 

 




