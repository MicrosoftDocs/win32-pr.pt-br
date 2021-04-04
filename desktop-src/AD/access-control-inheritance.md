---
title: Herança de controle de acesso
description: As ACEs (entradas de controle de acesso) em uma ACL (lista de controle de acesso) de objeto podem pertencer a uma ACL efetiva ou herdar a ACL.
ms.assetid: 2530eef5-7804-4b27-8756-d97be1cea116
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aec7514ab8cae8b07121d84e579ccb8492b67c45
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104084424"
---
# <a name="access-control-inheritance"></a>Herança de controle de acesso

As ACEs (entradas de controle de acesso) em uma ACL (lista de controle de acesso) de objeto podem pertencer a uma das duas categorias:

-   ACL efetiva: as ACEs nesta categoria se aplicam ao objeto.
-   Herdar ACL: as ACEs nessa categoria são herdadas por objetos criados no contêiner.

Cada ACE na DACL pode pertencer a uma ou mais categorias. As categorias para onde uma ACE pertence são determinadas pelos sinalizadores de controle de herança definidos na ACE.

Três sinalizadores de controle de herança podem ser definidos na propriedade [**AceFlags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) de uma ACE.



| Sinalizador                                          | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_ACE de \_ herança de ACEFLAG ADS \_**                | Esse sinalizador indica que a ACE faz parte da ACL de herança e que os objetos filho herdam os sinalizadores de controle de herança dessa ACE.                                                                                                                                                                                                                                                                                                                         |
| **ADS \_ ACEFLAG \_ não \_ propagar \_ a \_ Ace INHERIT** | Esse sinalizador indica que a ACE faz parte da ACL de herança, mas que nenhum sinalizador de controle de herança é propagado para objetos filho diretos (descendentes diretos) e a ACE é eficaz nos objetos filho diretos.                                                                                                                                                                                                                                          |
| **os anúncios \_ ACEFLAG \_ herdam \_ apenas \_ Ace**          | Esse sinalizador indica que a ACE não faz parte da ACL efetiva. Se esse sinalizador não for definido, a ACE faz parte da ACL efetiva. Esse sinalizador é útil para definir permissões herdáveis por subobjetos, mas não afetam a acessibilidade do contêiner. Por exemplo, se uma ACE se destinar a ser herdada por objetos de usuário em uma unidade organizacional, é provável que ela não deva ser imposta para acesso à própria unidade organizacional.<br/> |



 

O **ADS \_ ACEFLAG \_ não \_ propagar \_ herdar \_ Ace** e **anúncios \_ ACEFLAG \_ herdarão \_ somente sinalizadores \_ Ace** serão significativos somente se o **ADS \_ ACEFLAG \_ herdar \_ Ace** estiver presente. Isso ocorre porque o sinalizador de **\_ \_ \_ Ace ACEFLAG de herança do ADS** adiciona o comportamento de herança a uma ACE herdável, mas não define o tipo de herança. O **ADS \_ ACEFLAG \_ não \_ propagar \_ herdar \_ Ace** e **anúncios \_ ACEFLAG \_ herdam \_ apenas sinalizadores \_ Ace** definem um tipo específico de comportamento de herança.

É importante lembrar que o sistema também define os sinalizadores a seguir com base no tipo e no estado da ACE.



| Sinalizador                                    | Descrição                                           |
|-----------------------------------------|-------------------------------------------------------|
| **\_ \_ Ace herdado do ADS ACEFLAG \_**        | Esse sinalizador indica que a ACE foi herdada.       |
| **\_sinalizadores de \_ \_ herança válidos \_ do ADS ACEFLAG** | Esse sinalizador indica que os sinalizadores de herança são válidos. |



 

A tabela a seguir lista os efeitos das diferentes combinações de sinalizador para a propriedade [**AceFlags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) de uma ACE.



| Sinalizador                                                                                                                    | Efeito no objeto que contém a ACE                     | Efeito em objetos filho diretos                                                      | Efeito em objetos abaixo dos filhos diretos               |
|-------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|-------------------------------------------------------------------------------------|-------------------------------------------------------|
| Nenhum sinalizador definido.                                                                                                           | ACE efetivo: ACE aplica-se ao objeto.               | ACE não é herdado.                                                               | ACE não é herdado.                                 |
| **\_ACE de \_ herança de ACEFLAG ADS \_**                                                                                          | ACE efetivo                                           | ACE é herdado. ACE é uma ACE efetiva.<br/>                               | ACE é herdado. ACE é uma ACE efetiva.<br/> |
| **Anúncios \_ do ACEFLAG \_ herdar \_** os anúncios da ACE \| **\_ ACEFLAG \_ herdar \_ somente \_ Ace**                                                  | Não é uma ACE efetiva: ACE não se aplica ao objeto. | ACE é herdado. ACE é uma ACE efetiva.<br/>                               | ACE é herdado. ACE é uma ACE efetiva.<br/> |
| **Anúncios \_ do ACEFLAG \_ herdar \_ Ace** \| **ADS \_ ACEFLAG \_ não \_ propagar \_ herdar \_ Ace**                                         | ACE efetivo                                           | ACE é herdado, mas sem sinalizadores de herança. ACE é uma ACE efetiva<br/>  | ACE não é herdado.                                 |
| **Anúncios \_ do ACEFLAG \_ herdar \_** os anúncios da ACE \| **\_ ACEFLAG \_ herdar \_ somente \_** os anúncios da ACE \| **\_ ACEFLAG \_ não \_ propagar a \_ \_ Ace INHERIT** | Não é uma ACE efetiva.                                   | ACE é herdado, mas sem sinalizadores de herança. ACE é uma ACE efetiva.<br/> | ACE não é herdado.                                 |



 

 

