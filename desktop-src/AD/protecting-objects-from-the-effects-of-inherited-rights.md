---
title: Protegendo objetos contra os efeitos de direitos herdados
description: Conforme discutido no tópico Herança e delegação de administração, as ACEs podem ser definidas em um objeto de contêiner, como uma organizationalUnit, domainDNS, contêiner e assim por diante, e propagadas para objetos filho com base nos sinalizadores ACE definidos nessas ACEs.
ms.assetid: 3da000dd-3a32-4294-a636-ad077e618db2
ms.tgt_platform: multiple
keywords:
- Protegendo objetos contra os efeitos do AD de direitos herdados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dcc1067fcfe0d57e2e7aca837b97d73f18b55a41a4f1347ac36224b987918aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185011"
---
# <a name="protecting-objects-from-the-effects-of-inherited-rights"></a>Protegendo objetos contra os efeitos de direitos herdados

Conforme discutido no tópico Herança e delegação de [administração,](inheritance-and-delegation-of-administration.md)as ACEs podem ser definidas em um objeto de contêiner, como **uma organizationalUnit,** **domainDNS,** **contêiner** e assim por diante, e propagadas para objetos filho com base nos sinalizadores ACE definidos nessas ACEs.

Se você tiver um objeto seguro ou um objeto cujos ACEs deseja controlar explicitamente, como uma UO privada ou um usuário especial, poderá impedir que acEs são propagadas para o objeto por seu contêiner pai ou seus antecessores de contêiner pai.

Use a [**propriedade IADsSecurityDescriptor.Control**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) para controlar se AS DACLs e SACLs são herdadas pelo objeto de seu contêiner pai.

A [**propriedade IADsSecurityDescriptor.Control**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) pode ser usada para proteger um objeto contra os efeitos de ACEs herdadas. Os sinalizadores a seguir forçam o controle de acesso a ser definido explicitamente no objeto e impedem que um usuário modifique o controle de acesso para o objeto definindo ACEs herdáveis no contêiner pai do objeto ou os antecessores do contêiner pai.



| Sinalizador                               | Descrição                                                                                                                                                                     |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_ES DACL \_ PROTEGIDO**<br/> | Impede que ACEs definidos na DACL do contêiner pai e quaisquer objetos acima do contêiner pai na hierarquia de diretórios, seja aplicado à DACL de objeto.<br/> |
| **\_ES SACL \_ PROTEGIDO**<br/> | Impede que ACEs definidos no SACL do contêiner pai e quaisquer objetos acima do contêiner pai na hierarquia de diretórios, seja aplicado ao objeto SACL.<br/> |



 

Esteja ciente de que o **sinalizador \_ ES DACL \_ PRESENT** deve estar presente para definir **ES \_ DACL \_ PROTECTED** e **ES \_ SACL \_ PRESENT** deve estar presente para definir **ES \_ SACL \_ PROTECTED**.

 

