---
title: Nomeando atributos e classes
description: Este tópico inclui diretrizes para nomear atributos e classes.
ms.assetid: ccbc2859-332f-4ded-9125-5bf507cad960
ms.tgt_platform: multiple
keywords:
- Nomeando atributos e classes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80bfd2614033e12f68ba2727cc7aec689c16071e
ms.sourcegitcommit: 02e6e0b58720bf6b77797dd7a9ddc11c95f42b33
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/21/2020
ms.locfileid: "105752988"
---
# <a name="naming-attributes-and-classes"></a>Nomeando atributos e classes

Este tópico inclui diretrizes para nomear atributos e classes.

Para criar uma nova classe ou atributo, siga as seguintes regras de nomenclatura:

-   Use o mesmo nome para as propriedades **CN** e **lDAPDisplayName** de um novo objeto **attributeSchema** ou **classSchema** .
-   Identifique a empresa com um prefixo em minúsculas na primeira seção do nome. Esse prefixo pode ser um nome DNS, acrônimo ou outra cadeia de caracteres que identifica exclusivamente a empresa. O prefixo garante que todos os atributos e classes de uma empresa específica sejam exibidos consecutivamente ao navegar no esquema.
-   Se você estiver desenvolvendo uma extensão de esquema como um fornecedor de software independente, adicione uma abreviação do nome do produto do prefixo. Isso adiciona distinção entre vários produtos que contêm extensões de esquema LDAP.
-   Use um hífen como o próximo caractere após o prefixo.
-   Especifique um nome de atributo ou classe que seja exclusivo dentro dos atributos da empresa após o hífen. Essa parte do nome comum deve ser descritiva. Não use nomes de ilógico que não sejam de sentido para desenvolvedores e visualizadores do esquema.

Por exemplo, se a empresa fictícia Fabrikam estendeu o esquema adicionando um atributo para armazenar um identificador de correio de voz, o **CN** e o **lDAPDisplayName** do novo atributo poderiam ser "fabrikam-postalid".

Se o **lDAPDisplayName** de um atributo ou classe não for especificado, o sistema usará o **CN** para gerar um. No entanto, o algoritmo do sistema para gerar o nome pode resultar em colisões de nome ou nomes que são difíceis de ler. Para evitar esses problemas, é recomendável que um **lDAPDisplayName** seja explicitamente especificado para todos os atributos e classes.

Para fins de desenvolvimento e teste, pode ser desejável acrescentar um sufixo de versão ao **CN** e ao **lDAPDisplayName**, por exemplo, "fabrikam-correio de voz-001". Em um ambiente de desenvolvimento/teste distribuído, um sufixo de versão permite que os desenvolvedores executem várias versões de seu software simultaneamente. Após a conclusão do teste, renomeie o atributo ou a classe para remover o sufixo.

Não é possível excluir versões expiradas de extensões de esquema, mas é possível desabilitá-las e renomeá-las com nomes obscuros. Para obter mais informações, consulte [desabilitando classes e atributos existentes](disabling-existing-classes-and-attributes.md).

 

 




