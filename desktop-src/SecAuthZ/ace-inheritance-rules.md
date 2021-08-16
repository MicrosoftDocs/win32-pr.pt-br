---
description: O sistema propaga as ACEs (entradas de controle de acesso) herdáveis para objetos filho de acordo com um conjunto de regras de herança.
ms.assetid: 08f76aaa-8379-4ba8-9735-7568001bcd53
title: Regras de herança de ACE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba77e5d9fcbef9125108e8f0be76cd5b7c79a2f99ba524c81f3fd1da84336f04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785357"
---
# <a name="ace-inheritance-rules"></a>Regras de herança de ACE

O sistema propaga as ACEs ( [*entradas de controle de acesso*](/windows/desktop/SecGloss/a-gly) ) herdáveis para objetos filho de acordo com um conjunto de regras de herança. O sistema coloca ACEs herdadas na DACL ( [*lista de controle de acesso discricionário*](/windows/desktop/SecGloss/d-gly) ) do filho de acordo com a [ordem preferida das ACEs em uma DACL](order-of-aces-in-a-dacl.md). O sistema define o \_ sinalizador Ace herdado em todas as ACEs herdadas.

As ACEs herdadas por objetos filho de contêiner e não recipiente diferem, dependendo das combinações de sinalizadores de herança. Essas regras de herança funcionam da mesma para as DACLs e as SACLs ( [*listas de controle de acesso do sistema*](/windows/desktop/SecGloss/s-gly) ).



| Sinalizador de ACE pai                                  | Efeito na ACL filho                                                                                                                                                                                                                      |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Herdar \_ somente ACE de objeto                        | Objetos filho não contêineres: herdados como uma ACE efetiva. Objetos filho do contêiner: os contêineres herdam uma ACE somente de herança, a menos que o \_ sinalizador de bit de ACE de herança não propagar \_ \_ também seja definido.<br/>                                       |
| \_Herdar \_ somente ACE de contêiner                     | Objetos filho não contêineres: nenhum efeito sobre o objeto filho. Objetos filho do contêiner: o objeto filho herda uma ACE efetiva. A ACE herdada é herdável, a menos que o \_ sinalizador de bit de ACE de herança não propagar \_ \_ também seja definido.<br/> |
| \_Herdar Ace \_ e ACE de objeto \_ \_ herdado | Objetos filho não contêineres: herdados como uma ACE efetiva. Objetos filho do contêiner: o objeto filho herda uma ACE efetiva. A ACE herdada é herdável, a menos que o \_ sinalizador de bit de ACE de herança não propagar \_ \_ também seja definido.<br/> |
| Nenhum sinalizador de herança definido                         | Nenhum efeito no contêiner filho ou objetos não recipiente.                                                                                                                                                                                    |



 

Se uma ACE herdada for uma ACE efetiva para o objeto filho, o sistema mapeará todos os direitos genéricos para os direitos específicos do objeto filho. Da mesma forma, o sistema mapeia [*identificadores de segurança*](/windows/desktop/SecGloss/s-gly) (SIDs) genéricos, como \_ o proprietário do criador, para o Sid apropriado. Se uma ACE herdada for uma ACE somente de herança, todos os direitos genéricos ou SIDs genéricos permanecerão inalterados para que possam ser mapeados adequadamente quando a ACE for herdada pela próxima geração de objetos filho.

Para um caso em que um objeto de contêiner herda uma ACE que seja eficaz no contêiner e herdável por seus descendentes, o contêiner pode herdar duas ACEs. Isso ocorrerá se a ACE herdável contiver informações genéricas. O contêiner herda uma ACE somente herdada que contém as informações genéricas e uma ACE somente efetiva em que as informações genéricas foram mapeadas.

Uma [Ace específica de objeto](object-specific-aces.md) tem um membro **InheritedObjectType** que pode conter um GUID para identificar o tipo de objeto que pode herdar a Ace.

Se o GUID **InheritedObjectType** não for especificado, as regras de herança para uma ACE específica do objeto serão as mesmas para uma ACE padrão.

Se o GUID **InheritedObjectType** for especificado, a Ace será herdável por objetos que correspondem ao GUID se o objeto \_ herdar \_ Ace estiver definido e por contêineres que correspondam ao GUID se o contêiner \_ herdar \_ Ace estiver definido. Observe que atualmente somente os objetos DS dão suporte a ACEs específicas de objeto, e o DS trata todos os tipos de objeto como contêineres.

 

