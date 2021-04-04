---
title: Mapeamento de interface de usuário de objeto de grupo
description: Este tópico descreve as folhas de propriedades de objeto de grupo no snap-in Active Directory usuários e computadores. Propriedade geral SheetMember da propriedade SheetMembers de propriedade SheetManaged por folha de propriedades
ms.assetid: c0cd73f0-f09f-4645-966d-6149888ce482
ms.tgt_platform: multiple
keywords:
- AD de mapeamento de interface do usuário de objeto de grupo
- Mapeamento de interface do usuário, grupo de objetos de grupos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe2277c24f621f8e32f46b9e9571d0d0d4de9cfc
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104007309"
---
# <a name="group-object-user-interface-mapping"></a>Mapeamento de interface de usuário de objeto de grupo

Este tópico descreve as folhas de propriedades de objeto de grupo no snap-in Active Directory usuários e computadores.

-   [Folha de propriedades geral](#general-property-sheet)
-   [Membro da folha de propriedades](#member-of-property-sheet)
-   [Folha de propriedades de membros](#members-property-sheet)
-   [Gerenciado por folha de propriedades](#managed-by-property-sheet)

## <a name="general-property-sheet"></a>Folha de propriedades geral

A tabela a seguir mostra os rótulos de interface do usuário da folha de propriedades **geral** .



| Rótulo da interface do usuário                      | Atributo no Active Directory Domain Services     |
|-------------------------------|---------------------------------------------------|
| Nome do grupo (anterior ao Windows 2000) | [**SAM-Account-Name**](/windows/desktop/ADSchema/a-samaccountname) |
| Descrição                   | [**Descrição**](/windows/desktop/ADSchema/a-description)         |
| Email                        | [**Email-endereços**](/windows/desktop/ADSchema/a-mail)           |
| Escopo do Grupo                   | [**Tipo de grupo**](/windows/desktop/ADSchema/a-grouptype)            |
| Tipo de Grupo                    | [**Tipo de grupo**](/windows/desktop/ADSchema/a-grouptype)            |
| Observações                         | [**Comentário**](/windows/desktop/ADSchema/a-info)                    |



 

## <a name="member-of-property-sheet"></a>Membro da folha de propriedades

A tabela a seguir mostra os rótulos de interface do usuário do **membro da folha de** Propriedades.



| Rótulo da interface do usuário  | Atributo no Active Directory Domain Services | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-----------|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Membro de | [**Is-member-of-DL**](/windows/desktop/ADSchema/a-memberof)    | Contém os nomes distintos dos grupos aos quais esse grupo pertence. O atributo de membro de cada um dos grupos nessa lista contém o nome distinto desse objeto de grupo. A interface do usuário não modifica diretamente o atributo [**is-member-of-DL**](/windows/desktop/ADSchema/a-memberof) . Ele modifica o atributo de [**membro**](/windows/desktop/ADSchema/a-member) no objeto de grupo do qual esse objeto se tornou membro. O servidor de Active Directory mantém o atributo **is-member-of-DL** .<br/> |



 

## <a name="members-property-sheet"></a>Folha de propriedades de membros

A tabela a seguir mostra os rótulos de interface do usuário da folha de propriedades **Membros** .



| Rótulo da interface do usuário | Atributo no Active Directory Domain Services | Descrição                                                           |
|----------|-----------------------------------------------|-----------------------------------------------------------------------|
| Membros  | [**Membro**](/windows/desktop/ADSchema/a-member)               | Contém os nomes distintos dos membros deste objeto de grupo. |



 

## <a name="managed-by-property-sheet"></a>Gerenciado por folha de propriedades

A tabela a seguir mostra os rótulos de interface do usuário da folha de propriedades **gerenciada por** .



| Rótulo da interface do usuário                           | Atributo no Active Directory Domain Services                                                                                   |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Nome                               | [**Gerenciado por**](/windows/desktop/ADSchema/a-managedby)                                                                                          |
| O gerente pode atualizar a lista de membros | Nenhum. Uma ACE com a permissão "Allow-Write Members" é adicionada à conta identificada pelo **nome**.                        |
| Office                             | O atributo [**físico-Delivery-Office-Name**](/windows/desktop/ADSchema/a-physicaldeliveryofficename) da conta identificada por **nome**. |
| Street                             | O atributo de [**endereço de rua**](/windows/desktop/ADSchema/a-street) da conta identificada por **nome**.                                    |
| City                               | O atributo de [**nome de localidade**](/windows/desktop/ADSchema/a-l) da conta identificada por **nome**.                                          |
| Estado/Província                     | O atributo [**State-ou-província-Name**](/windows/desktop/ADSchema/a-st) da conta identificada por **nome**.                                |
| País/Região                     | O atributo [**Country-Name**](/windows/desktop/ADSchema/a-c) da conta identificada por **nome**.                                           |
| Número de telefone                   | O atributo de [**número de telefone**](/windows/desktop/ADSchema/a-telephonenumber) da conta identificada por **nome**.                         |
| Número de fax                         | O atributo [**fax-Phone-Number**](/windows/desktop/ADSchema/a-facsimiletelephonenumber) da conta identificada por **nome**.      |



 

 

