---
description: '\_SSCRIPTS DE LOCALIDADE'
ms.assetid: d15c501a-b77b-4446-bee6-6dbbd714b4e0
title: LOCALE_SSCRIPTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aede4d6d1843fd32bdd17ae3a275a364c3a2d4f0bd282302f49d7b4a3b0dd1ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105846"
---
# <a name="locale_sscripts"></a>\_SSCRIPTS DE LOCALIDADE

**Windows Vista e posterior:** Uma cadeia de caracteres que representa uma lista de scripts, usando a notação de 4 caracteres usada no [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html). Cada nome de script consiste em quatro caracteres latinos e a lista é organizada em ordem alfabética com cada nome, incluindo o último, seguido por um ponto e vírgula.

[**GetLocaleInfo ou**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) pode ser chamado com *LCType* definido como LOCALE SSCRIPTS como parte de uma estratégia para atenuar problemas de segurança relacionados a IDNs (Nomes de Domínio \_ Internacionalizados). Aqui estão alguns valores de exemplo:



| Local                  | Nome da localidade/idioma | Valor                                                                                                  |
|-------------------------|----------------------|--------------------------------------------------------------------------------------------------------|
| Inglês (Estados Unidos) | pt-BR                | Latn;                                                                                                  |
| Híndi (Índia)           | hi-IN                | Deva;                                                                                                  |
| Japonês (Japão)        | ja-JP                | **Windows 7 e posterior:** Hani; Hira; Jpan; Kana;<br/> **Windows Vista:** Hani; Hira; Kana;<br/> |



 

Um valor de script composto não inclui o script latino, a menos que ele seja uma parte essencial do sistema de escrita usado para a localidade específica. Caracteres latinos geralmente são usados no contexto de localidades para as quais não são nativos, por exemplo, para um nome comercial externo. No exemplo acima para Híndi na Índia, o único valor de script é "Deva" (para "Devanagari"), embora os caracteres latinos também possam aparecer em texto híndi. A [função VerifyScripts](/windows/desktop/api/Winnls/nf-winnls-verifyscripts) tem um sinalizador especial para resolver esse caso.

 

 




