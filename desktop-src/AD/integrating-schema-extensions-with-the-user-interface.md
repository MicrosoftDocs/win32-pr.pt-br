---
title: Integrando extensões de esquema com a interface do usuário
description: As ferramentas de administração do Active Directory Domain Services usam uma arquitetura comum para conectar a interface do usuário administrativo ao esquema de diretório.
ms.assetid: 62cf9f9d-7091-4cff-9995-5934dfa3e97e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 446c3b5150d66357206bd1eb139a391d2408ee9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105749125"
---
# <a name="integrating-schema-extensions-with-the-user-interface"></a>Integrando extensões de esquema com a interface do usuário

As ferramentas de administração do Active Directory Domain Services usam uma arquitetura comum para conectar a interface do usuário administrativo ao esquema de diretório. O ponto central dessa arquitetura é a classe de objeto **displaySpecifier** . Os especificadores de exibição e seu uso são descritos em detalhes na [extensão da interface do usuário para objetos de diretório](extending-the-user-interface-for-directory-objects.md).

Ao criar uma nova classe por meio da subclasse de uma classe existente, você pode aproveitar a interface do usuário existente para a superclasse copiando o especificador de exibição da superclasse. Uma maneira fácil de copiar o especificador de exibição para uma classe é exportá-lo para um arquivo LDIF usando LDIFDE, editar o nome e CN distintos e, em seguida, importar o arquivo LDIF modificado. Se a subclasse tiver atributos adicionais, será necessário fornecer páginas de propriedades adicionais para dar suporte à edição. Se a subclasse tiver propriedades adicionais necessárias, você precisará fornecer páginas de extensão da caixa de diálogo de criação, pois a interface do usuário fornecida pela superclasse não tem como criar esses novos atributos.

 

 




