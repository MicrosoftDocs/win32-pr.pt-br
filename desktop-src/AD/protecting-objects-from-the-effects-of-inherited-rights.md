---
title: Protegendo objetos dos efeitos de direitos herdados
description: Conforme discutido no tópico herança e delegação de administração, as ACEs podem ser definidas em um objeto de contêiner, como um organizationalUnit, domainDNS, contêiner e assim por diante, e propagadas para objetos filho com base nos sinalizadores de ACE definidos nessas ACEs.
ms.assetid: 3da000dd-3a32-4294-a636-ad077e618db2
ms.tgt_platform: multiple
keywords:
- Protegendo objetos dos efeitos de AD de direitos herdados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78e49991cd8a479e05b024c6ea2538783a843025
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104007301"
---
# <a name="protecting-objects-from-the-effects-of-inherited-rights"></a>Protegendo objetos dos efeitos de direitos herdados

Conforme discutido no tópico [herança e delegação de administração](inheritance-and-delegation-of-administration.md), as ACEs podem ser definidas em um objeto de contêiner, como um **OrganizationalUnit**, **domainDns**, **contêiner** e assim por diante, e propagadas para objetos filho com base nos sinalizadores de Ace definidos nessas ACEs.

Se você tiver um objeto seguro ou um objeto cujas ACEs você deseja controlar explicitamente, como uma OU particular ou um usuário especial, poderá impedir que as ACEs sejam propagadas para o objeto pelo seu contêiner pai ou por seus predecessores do contêiner pai.

Use a propriedade [**IADsSecurityDescriptor. Control**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) para controlar se as DACLs e SACLs são herdadas pelo objeto do seu contêiner pai.

A propriedade [**IADsSecurityDescriptor. Control**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) pode ser usada para proteger um objeto dos efeitos de ACEs herdadas. Os sinalizadores a seguir forçam o controle de acesso a ser definido explicitamente no objeto e impedem que um usuário modifique o controle de acesso ao objeto definindo ACEs herdáveis no contêiner pai do objeto ou seus predecessores do contêiner pai.



| Sinalizador                               | Descrição                                                                                                                                                                     |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **DACL de SE \_ \_ protegida**<br/> | Impede que as ACEs definidas na DACL do contêiner pai e quaisquer objetos acima do contêiner pai na hierarquia de diretório sejam aplicados ao objeto DACL.<br/> |
| **\_SACL \_ protegida**<br/> | Impede que as ACEs definidas na SACL do contêiner pai e quaisquer objetos acima do contêiner pai na hierarquia de diretório sejam aplicados à SACL do objeto.<br/> |



 

Lembre-se de que o sinalizador **se a \_ DACL \_ presente** deve estar presente para definir **se a \_ DACL \_ protegida** e **se a \_ SACL \_ presente** deve estar presente para definir **se a SACL está \_ \_ protegida**.

 

