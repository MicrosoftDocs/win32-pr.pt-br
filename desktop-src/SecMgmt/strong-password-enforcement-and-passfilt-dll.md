---
description: Lista os requisitos impostos por ferramentas de administração do sistema de senha forte.
ms.assetid: a84f83b2-181b-4f65-82bd-bc7f0689aad3
title: Imposição de senha forte e Passfilt.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63b7be524511d52048e06ae83ab110384c3bf5c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501540"
---
# <a name="strong-password-enforcement-and-passfiltdll"></a>Imposição de senha forte e Passfilt.dll

A imposição de senha forte pode ser habilitada usando as ferramentas de administração do sistema. Se a política de administração do sistema estiver habilitada, as senhas deverão atender aos seguintes requisitos mínimos quando forem criadas ou alteradas:

-   As senhas não podem conter o valor samAccountName (nome da conta) do usuário ou o displayName inteiro (valor de nome completo). Ambas as verificações não diferenciam maiúsculas de minúsculas.
-   O samAccountName é verificado em sua totalidade apenas para determinar se ele faz parte da senha. Se samAccountName tiver menos de três caracteres, essa verificação será ignorada.
-   O displayName é analisado para delimitadores: vírgulas, pontos, traços ou hifens, sublinhados, espaços, sinais de libra e tabulações. Se qualquer um desses delimitadores for encontrado, o displayName será dividido e todas as seções analisadas (tokens) serão confirmadas para não serem incluídas na senha. Os tokens com menos de três caracteres são ignorados e as subcadeias dos tokens não são verificadas. Por exemplo, o nome "Erin M. Hagens" é dividido em três tokens: "Erin", "M" e "Hagens". Como o segundo token é apenas um caractere, ele é ignorado. Portanto, esse usuário não poderia ter uma senha que incluisse "Erin" ou "Hagens" como uma subcadeia de caracteres em qualquer lugar da senha.
-   As senhas devem conter caracteres de três das cinco categorias a seguir.



| Categorias de caractere                                                                                                                                                      | Exemplos                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| Letras maiúsculas de idiomas europeus (A a Z, com marcas diacrítico, caracteres gregos e cirílico)<br/>                                                     | A, B, C, Z<br/>                |
| Letras minúsculas de idiomas europeus (a a z, Sharp-s, com marcas de sinais diacríticos, caracteres gregos e cirílico)<br/>                                            | a, b, c, z<br/>                |
| 10 dígitos base (0 a 9)<br/>                                                                                                                                   | 0, 1, 2, 9<br/>                |
| Caracteres não alfanuméricos (caracteres especiais)<br/>                                                                                                               | $,!,%, ^, () {} \[ \] ;: <>?<br/> |
| Qualquer caractere Unicode que é Categorizado como um caractere alfabético, mas não é maiúsculo ou minúsculo. Isso inclui caracteres Unicode de idiomas asiáticos.<br/> |                                        |



 

**Para habilitar a imposição de senha forte**

1.  No console de administração, localize **política de segurança local**.
2.  Selecione **política de conta** e selecione **política de senha**.
3.  Habilite a configuração as **senhas devem atender aos requisitos de complexidade** .

> [!Note]  
> Um determinado caractere pode satisfazer apenas uma categoria. A função [GetStringTypeW](/windows/win32/api/stringapiset/nf-stringapiset-getstringtypew) é usada para testar se cada caractere na senha é maiúsculo, minúsculo ou alfanumérico.

 

 

