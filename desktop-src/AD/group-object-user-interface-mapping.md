---
title: Mapeamento de Interface do Usuário objeto de grupo
description: Este tópico descreve as folhas de propriedades do objeto Group Usuários e Computadores do Active Directory snap-in. Geral Property SheetMember de Property SheetMembers Property SheetManaged by Property Sheet
ms.assetid: c0cd73f0-f09f-4645-966d-6149888ce482
ms.tgt_platform: multiple
keywords:
- AD de mapeamento Interface do Usuário objeto de grupo
- Interface do Usuário mapeamento, AD de objeto de grupo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 308b3bafc24f8b8419b23c351d981f4f01961885cd535ac2d24b96cd62e17633
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188960"
---
# <a name="group-object-user-interface-mapping"></a>Mapeamento de Interface do Usuário objeto de grupo

Este tópico descreve as folhas de propriedades do objeto Group Usuários e Computadores do Active Directory snap-in.

-   [Folha de propriedades geral](#general-property-sheet)
-   [Membro da folha de propriedades](#member-of-property-sheet)
-   [Folha de propriedades members](#members-property-sheet)
-   [Folha de propriedades gerenciada por](#managed-by-property-sheet)

## <a name="general-property-sheet"></a>Folha de propriedades geral

A tabela a seguir mostra os rótulos de interface do usuário da **folha de propriedades** Geral.



| Rótulo da interface do usuário                      | Atributo em Active Directory Domain Services     |
|-------------------------------|---------------------------------------------------|
| Nome do grupo (pré-Windows 2000) | [**Sam-Account-Name**](/windows/desktop/ADSchema/a-samaccountname) |
| Descrição                   | [**Descrição**](/windows/desktop/ADSchema/a-description)         |
| Email                        | [**Endereços de email**](/windows/desktop/ADSchema/a-mail)           |
| Escopo do Grupo                   | [**Tipo de grupo**](/windows/desktop/ADSchema/a-grouptype)            |
| Tipo de Grupo                    | [**Tipo de grupo**](/windows/desktop/ADSchema/a-grouptype)            |
| Observações                         | [**Comentário**](/windows/desktop/ADSchema/a-info)                    |



 

## <a name="member-of-property-sheet"></a>Membro da folha de propriedades

A tabela a seguir mostra os rótulos de interface do usuário **da folha de propriedades Membro** de .



| Rótulo da interface do usuário  | Atributo em Active Directory Domain Services | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-----------|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Membro de | [**Is-Member-of-DL**](/windows/desktop/ADSchema/a-memberof)    | Contém os nomes diferenciados dos grupos aos quais esse grupo pertence. O atributo membro de cada um dos grupos nesta lista contém o nome diferenciado desse objeto de grupo. A interface do usuário não modifica diretamente o [**atributo Is-Member-Of-DL.**](/windows/desktop/ADSchema/a-memberof) Ele modifica o [**atributo Member**](/windows/desktop/ADSchema/a-member) no objeto de grupo do qual esse objeto se tornou membro. O servidor do Active Directory mantém o **atributo Is-Member-Of-DL.**<br/> |



 

## <a name="members-property-sheet"></a>Folha de propriedades members

A tabela a seguir mostra os rótulos de interface do usuário da **folha de propriedades** Membros.



| Rótulo da interface do usuário | Atributo em Active Directory Domain Services | Descrição                                                           |
|----------|-----------------------------------------------|-----------------------------------------------------------------------|
| Membros  | [**Membro**](/windows/desktop/ADSchema/a-member)               | Contém os nomes diferenciados dos membros desse objeto de grupo. |



 

## <a name="managed-by-property-sheet"></a>Folha de propriedades gerenciada por

A tabela a seguir mostra os rótulos de interface do usuário da **folha de propriedades Gerenciado** por.



| Rótulo da interface do usuário                           | Atributo em Active Directory Domain Services                                                                                   |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Nome                               | [**Gerenciado por**](/windows/desktop/ADSchema/a-managedby)                                                                                          |
| O Gerente pode atualizar a lista de associação | Nenhum. Uma ACE com a permissão "Permitir – Gravar Membros" é adicionada à conta identificada pelo **Nome**.                        |
| Office                             | O [**atributo Physical-Delivery-Office-Name**](/windows/desktop/ADSchema/a-physicaldeliveryofficename) da conta identificada pelo **Nome**. |
| Street                             | O [**atributo Street-Address**](/windows/desktop/ADSchema/a-street) da conta identificada pelo **Nome**.                                    |
| City                               | O [**atributo Locality-Name**](/windows/desktop/ADSchema/a-l) da conta identificada pelo **Nome**.                                          |
| Estado/Província                     | O [**atributo State-Or-Province-Name**](/windows/desktop/ADSchema/a-st) da conta identificada pelo **Nome**.                                |
| País/região                     | O [**atributo Country-Name**](/windows/desktop/ADSchema/a-c) da conta identificada pelo **Nome**.                                           |
| Número de telefone                   | O [**atributo Número de**](/windows/desktop/ADSchema/a-telephonenumber) Telefone da conta identificada pelo **Nome**.                         |
| Número de fax                         | O [**atributo Facsimile-Telephone-Number**](/windows/desktop/ADSchema/a-facsimiletelephonenumber) da conta identificada pelo **Nome**.      |



 

 

