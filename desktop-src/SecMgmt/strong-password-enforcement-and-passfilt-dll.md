---
description: Lista os requisitos imposto pelas ferramentas de administração de sistema de senha forte.
ms.assetid: a84f83b2-181b-4f65-82bd-bc7f0689aad3
title: Imposição de senha forte e Passfilt.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c3e34e77b15ca9797240ce5647aa58decf3efa05f04cd431b3d723b148bf406
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004890"
---
# <a name="strong-password-enforcement-and-passfiltdll"></a>Imposição de senha forte e Passfilt.dll

A imposição de senha forte pode ser habilitada usando as ferramentas de administração do sistema. Se a política de administração do sistema estiver habilitada, as senhas deverão atender aos seguintes requisitos mínimos quando elas são criadas ou alteradas:

-   As senhas podem não conter o valor samAccountName (Nome da Conta) do usuário ou displayName inteiro (valor de Nome Completo). Ambas as verificações não são sensíveis a minúsculas.
-   O samAccountName é verificado em sua totalidade apenas para determinar se ele faz parte da senha. Se o samAccountName tiver menos de três caracteres, essa verificação será ignorada.
-   O displayName é analisado para delimitadores: vírgulas, pontos, traços ou hifens, sublinhados, espaços, sinais de quilo de peso e guias. Se algum desses delimitadores for encontrado, displayName será dividido e todas as seções analisados (tokens) serão confirmadas como não incluídas na senha. Tokens com menos de três caracteres são ignorados e as substrings dos tokens não são verificadas. Por exemplo, o nome "Aaron M. Ltds" é dividido em três tokens: "Aaron", "M" e "Aarons". Como o segundo token tem apenas um caractere de comprimento, ele é ignorado. Portanto, esse usuário não pôde ter uma senha que incluía "meu" ou "até mesmo", como uma substring em qualquer lugar na senha.
-   As senhas devem conter caracteres de três das cinco categorias a seguir.



| Categorias de caractere                                                                                                                                                      | Exemplos                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| Letras maiúsculas de idiomas europeus (A a Z, com marcas diacríticas, caracteres gregos e cirílicos)<br/>                                                     | A, B, C, Z<br/>                |
| Letras minúsculas de idiomas europeus (a a z, sharp-s, com marcas diacríticas, caracteres gregos e cirílicos)<br/>                                            | a, b, c, z<br/>                |
| 10 dígitos base (0 a 9)<br/>                                                                                                                                   | 0, 1, 2, 9<br/>                |
| Caracteres não alfanuméricos (caracteres especiais)<br/>                                                                                                               | $,!,%,^,() {} \[ \] ;:<>?<br/> |
| Qualquer caractere Unicode categorizado como um caractere alfabético, mas não está em letras maiúsculas ou minúsculas. Isso inclui caracteres Unicode de idiomas asiáticos.<br/> |                                        |



 

**Para habilitar a imposição de senha forte**

1.  No console de administração, localize **Política de Segurança Local.**
2.  Selecione **Política de Conta** e, em seguida, selecione Política de **Senha**.
3.  Habilitar **a configuração Senhas deve atender aos requisitos de** complexidade.

> [!Note]  
> Um determinado caractere pode satisfazer apenas uma categoria. A [função GetStringTypeW](/windows/win32/api/stringapiset/nf-stringapiset-getstringtypew) é usada para testar se cada caractere na senha é maiúscula, minúscula ou alfanumérica.

 

 

