---
title: Mapeamento de interface do usuário de objeto de computador
description: As tabelas a seguir listam os elementos das folhas de propriedades de objeto de computador no snap-in Active Directory usuários e computadores.
ms.assetid: e2a7a42d-e854-43fc-a36b-f3031c1685a7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de2a2b3ed4ec8cbf3c1af59e024fc5e04bc68ae8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103640428"
---
# <a name="computer-object-user-interface-mapping"></a>Mapeamento de interface do usuário de objeto de computador

As tabelas a seguir listam os elementos das folhas de propriedades de objeto de computador no snap-in Active Directory usuários e computadores.

## <a name="general-property-sheet"></a>Folha de propriedades geral

A tabela a seguir lista os rótulos de interface do usuário da folha de propriedades **geral** .



| Rótulo da interface do usuário                         | Active Directory Domain Services atributo | Comentários                                         |
|----------------------------------|--------------------------------------------|--------------------------------------------------|
| Nome do computador (anterior ao Windows 2000) | sAMAccountName                             |                                                  |
| Nome DNS                         | dNSHostName                                |                                                  |
| Função                             | userAccountControl                         | Alterna um bit no bitmask userAccountControl. |
| Descrição                      | descrição                                |                                                  |
| Confiar no computador para delegação    | userAccountControl                         | Alterna um bit no bitmask userAccountControl. |



 

## <a name="location-property-sheet"></a>Folha de propriedades de localização

A tabela a seguir lista os rótulos de interface do usuário da folha de propriedades **local** .



| Rótulo da interface do usuário | Active Directory Domain Services atributo |
|----------|--------------------------------------------|
| Localização | local                                   |



 

## <a name="member-of-property-sheet"></a>Membro da folha de propriedades

A tabela a seguir lista os rótulos de interface de usuário do **membro da folha de** Propriedades.



| Rótulo da interface do usuário          | Active Directory Domain Services atributo | Comentários                                                                                                                                                                   |
|-------------------|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Membro de         | memberOf                                   | Inclui todos os grupos na lista de interface do usuário, exceto o grupo primário, que é representado no anúncio por meio do atributo [**primaryGroupId**](/windows/desktop/ADSchema/a-primarygroupid) . |
| Definir grupo primário | primaryGroupID                             | LDAP: vinculado a [**primaryGroupToken**](/windows/desktop/ADSchema/a-primarygrouptoken) do grupo primário.                                                                                  |



 

## <a name="operating-system-property-sheet"></a>Folha de propriedades do sistema operacional

A tabela a seguir lista os rótulos de interface do usuário da folha de propriedades do **sistema operacional** .



| Rótulo da interface do usuário     | Active Directory Domain Services atributo |
|--------------|--------------------------------------------|
| Name         | operatingSystem                            |
| Versão      | operatingSystemVersion                     |
| Service Pack | operatingSystemServicePack                 |



 

 

 