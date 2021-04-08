---
description: O subsistema Posix deve ser capaz de converter qualquer SID (identificador de segurança) que encontra em um valor de 32 bits, chamado de ID POSIX.
ms.assetid: cd6c89ef-c3f1-47fe-8183-320b5d24b0dd
title: Mapeando identificadores POSIX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dabb944b543fba65942eb89d526590a5aff2c26c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829647"
---
# <a name="mapping-posix-identifiers"></a>Mapeando identificadores POSIX

O subsistema Posix deve ser capaz de converter qualquer Sid ( [*identificador de segurança*](/windows/desktop/SecGloss/s-gly) ) que encontra em um valor de 32 bits, chamado de *ID POSIX*. Além disso, ele deve ser capaz de categorizar a ID como uma ID de usuário ou uma ID de grupo. Para entender como esse mapeamento é realizado, vamos primeiro examinar os SIDs que devem ser mapeados.

Os SIDs têm dois componentes, o SID do domínio e a ID relativa da conta no domínio. Por exemplo, no SID S-1-518364-21-43-8, o último número, 8, é a ID relativa da conta (RID) e S-1-518364-21-43 é o SID do domínio.

As informações de domínio são armazenadas em objetos [**TrustedDomain**](trusteddomain-object.md) . Parte das informações armazenadas em um objeto **TrustedDomain** é um deslocamento de ID POSIX a ser usado para SIDs dentro desse domínio. Por exemplo, suponha que um **TrustedDomain** seja definido da seguinte maneira:

``` syntax
    Name:    NtPgm
    Sid:    S-1-518364-21-43
    Posix Offset:    0x130000
```

As IDs POSIX para contas nesse domínio seriam geradas adicionando 0x130000 à ID relativa da conta. Portanto, a ID POSIX correspondente ao SID S-1-518364-21-43-8 seria 0x130008.

Nem todas as traduções de ID POSIX usam um objeto [**TrustedDomain**](trusteddomain-object.md) . A tabela a seguir mostra os SIDs que são mapeados usando valores de deslocamento conhecidos.



| Fonte                                              | Deslocamento de ID POSIX |
|-----------------------------------------------------|-----------------|
| SIDs do domínio interno                       | 0x20000         |
| SIDs do domínio da conta                        | 0x30000         |
| SIDs do domínio primário (somente em estações de trabalho) | 0x40000         |



 

E, finalmente, um outro conjunto de SIDs, SIDs de logon, requer processamento especial. Esses valores são atribuídos pelo processo de logon do Windows para cada sessão de logon e têm a forma S-1-5-5-X-Y, em que X e Y são tratados como um único \_ inteiro grande que é incrementado para cada sessão de logon. Esses SIDs são mapeados para a ID POSIX constante 0xFFF. Para mapear a ID do POSIX 0xFFF, você pode converter qualquer [*identificador de logon*](/windows/desktop/SecGloss/l-gly) que melhor atenda à situação, ou você pode usar S-1-5-5-0-0 por padrão. (Por exemplo, se um usuário POSIX aplicar proteção a um objeto e especificar FFFx, será melhor substituir o identificador de logon desse usuário do que apenas atribuir S-1-5-5-0-0.)

 

 
