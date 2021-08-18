---
title: Nomeando atributos e classes
description: Este tópico inclui diretrizes para nomear atributos e classes.
ms.assetid: ccbc2859-332f-4ded-9125-5bf507cad960
ms.tgt_platform: multiple
keywords:
- Nomeando atributos e classes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e042decaf7d3dd15606ea7e138d9e6315d4200f2a641c10381951f2657a5aafe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185991"
---
# <a name="naming-attributes-and-classes"></a>Nomeando atributos e classes

Este tópico inclui diretrizes para nomear atributos e classes.

Para criar uma nova classe ou atributo, adera às seguintes regras de nomen entre:

-   Use o mesmo nome para as propriedades **cn** e **lDAPDisplayName** de um novo **objeto attributeSchema** **ou classSchema.**
-   Identifique a empresa com um prefixo de caso inferior na primeira seção do nome. Esse prefixo pode ser um nome DNS, acrônimo ou outra cadeia de caracteres que identifica exclusivamente a empresa. O prefixo garante que todos os atributos e classes de uma empresa específica sejam exibidos consecutivamente ao navegar pelo esquema.
-   Se você estiver desenvolvendo uma extensão de esquema como um fornecedor de software independente, adicione uma abreviação do nome do produto do prefixo. Isso adiciona distinção entre vários produtos que contêm extensões de esquema LDAP.
-   Use um hífen como o próximo caractere após o prefixo.
-   Especifique um atributo ou nome de classe exclusivo nos atributos da empresa após o hífen. Essa parte do nome comum deve ser descritiva. Não use nomes lógicos sem sentido para desenvolvedores e visualizadores do esquema.

Por exemplo, se a empresa fictícia Fabrikam estendeu o esquema adicionando um atributo para armazenar um identificador de email de voz, **cn** e **lDAPDisplayName** do novo atributo poderão ser "fabrikam-VoiceMailID".

Se **o lDAPDisplayName** de um atributo ou classe não for especificado, o sistema usará **o cn** para gerar um. No entanto, o algoritmo do sistema para gerar o nome pode resultar em colisões de nomes ou nomes difíceis de ler. Para evitar esses problemas, é recomendável que **um lDAPDisplayName** seja especificado explicitamente para todos os atributos e classes.

Para fins de desenvolvimento e teste, pode ser desejável anexar um sufixo de versão ao **cn** e **lDAPDisplayName,** por exemplo, "fabrikam-VoiceMailID-001". Em um ambiente de desenvolvimento/teste distribuído, um sufixo de versão permite que os desenvolvedores executem várias versões de seu software simultaneamente. Após a conclusão do teste, renomeie o atributo ou a classe para remover o sufixo.

Não é possível excluir versões antigas de extensões de esquema, mas é possível desabilitá-las e renomeá-las com nomes obscurecidos. Para obter mais informações, [consulte Desabilitando classes e atributos existentes.](disabling-existing-classes-and-attributes.md)

 

 




