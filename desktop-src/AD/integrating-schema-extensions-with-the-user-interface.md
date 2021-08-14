---
title: Integrando extensões de esquema com o Interface do Usuário
description: As ferramentas de administração do Active Directory Domain Services usam uma arquitetura comum para conectar a interface do usuário administrativo ao esquema de diretório.
ms.assetid: 62cf9f9d-7091-4cff-9995-5934dfa3e97e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c23d951ec51d7453ee92cf90ddcb28ddb8219d3056b1edb96d16bf15494fe956
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187205"
---
# <a name="integrating-schema-extensions-with-the-user-interface"></a>Integrando extensões de esquema com o Interface do Usuário

As ferramentas de administração do Active Directory Domain Services usam uma arquitetura comum para conectar a interface do usuário administrativo ao esquema de diretório. A peça central dessa arquitetura é a **classe de objeto displaySpecifier.** Especificadores de exibição e seu uso são descritos em detalhes em [Estendendo](extending-the-user-interface-for-directory-objects.md)o Interface do Usuário para objetos de diretório .

Ao criar uma nova classe com a subclasse de uma classe existente, você pode aproveitar a interface do usuário existente para a superclasse copiando o especificador de exibição da superclasse. Uma maneira fácil de copiar o especificador de exibição de uma classe é exportá-lo para um arquivo LDIF usando LDIFDE, editar o Nome diferenciado e CN e, em seguida, importar o arquivo LDIF modificado. Se a subclasse tiver atributos adicionais, você precisará fornecer páginas de propriedades adicionais para dar suporte à edição. Se a subclasse tiver propriedades adicionais que precisam ter, você precisará fornecer páginas de extensão da Caixa de Diálogo de Criação, pois a interface do usuário fornecida pela superclasse não tem como criar esses novos atributos.

 

 




