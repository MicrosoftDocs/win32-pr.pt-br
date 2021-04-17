---
title: Mapeando sintaxe de Active Directory para sintaxe ADSI
description: A tabela a seguir mapeia as sintaxes de Active Directory para suas sintaxes ADSI correspondentes.
ms.assetid: ffb40eff-e137-4d6a-81e7-24d2cbbdbfbf
ms.tgt_platform: multiple
keywords:
- atributos ADSI, mapeando Active Directory sintaxe para sintaxe ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6ba332a39a5d2452925f1a8f1cc8c8ca766ca10
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105754417"
---
# <a name="mapping-active-directory-syntax-to-adsi-syntax"></a>Mapeando sintaxe de Active Directory para sintaxe ADSI

A tabela a seguir mapeia as sintaxes de Active Directory para suas sintaxes ADSI correspondentes.



| ID da sintaxe do atributo | Tipo de sintaxe Active Directory             | Tipo de sintaxe ADSI equivalente                                         |
|---------------------|------------------------------------------|---------------------------------------------------------------------|
| 2.5.5.1<br/>  | Cadeia de caracteres DN<br/>                     | Cadeia de caracteres DN<br/>                                                |
| 2.5.5.2<br/>  | ID de objeto<br/>                     | Cadeia de caracteres CaseIgnore<br/>                                        |
| 2.5.5.3<br/>  | Cadeia de caracteres diferencia maiúsculas de minúscula<br/>         | Cadeia de caracteres CaseExact<br/>                                         |
| 2.5.5.4<br/>  | Cadeia de caracteres ignorada de caso<br/>           | Cadeia de caracteres CaseIgnore<br/>                                        |
| 2.5.5.5<br/>  | Imprimir cadeia de caracteres de caso<br/>             | Cadeia de caracteres imprimível<br/>                                         |
| 2.5.5.6<br/>  | Cadeia de caracteres numérica<br/>                | Cadeia de caracteres numérica<br/>                                           |
| 2.5.5.7<br/>  | **Ou** Nome DNWithOctetString<br/> | Sem suporte<br/>                                            |
| 2.5.5.8<br/>  | Booliano<br/>                       | Booliano<br/>                                                  |
| 2.5.5.9<br/>  | Integer<br/>                       | Integer<br/>                                                  |
| 2.5.5.10<br/> | Cadeia de caracteres de octeto<br/>                  | Cadeia de caracteres de octeto<br/>                                             |
| 2.5.5.11<br/> | Hora<br/>                          | Hora UTC<br/>                                                 |
| 2.5.5.12<br/> | Unicode<br/>                       | Cadeia de caracteres de Ignorar maiúsculas<br/>                                       |
| 2.5.5.13<br/> | Endereço<br/>                       | Sem suporte<br/>                                            |
| 2.5.5.14<br/> | Distname-Address<br/>              |                                                                     |
| 2.5.5.15<br/> | Descritor de segurança NT<br/>        | [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)<br/> |
| 2.5.5.16<br/> | Inteiro grande<br/>                 | [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger)<br/>             |
| 2.5.5.17<br/> | SID<br/>                           | Cadeia de caracteres de octeto<br/>                                             |



 

 

 





