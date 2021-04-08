---
title: objectCategory versus objectClass
description: Os atributos objectCategory e objectClass podem se referir a uma determinada classe de esquema de um objeto de diretório.
ms.assetid: 66dadedb-61e4-4184-9b87-0fff036a94d9
ms.tgt_platform: multiple
keywords:
- ADSI de objectCategory versus objectClass
- atributos ASI, pesquisando atributos objectCategory e objectClass
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbbb8c5fe737b7c81193a75cdae6b772db64e69c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004865"
---
# <a name="objectcategory-vs-objectclass"></a>objectCategory versus objectClass

Os atributos **objectCategory** e **objectClass** podem se referir a uma determinada classe de esquema de um objeto de diretório. No entanto, há uma distinção importante na semântica entre os dois. "objectClass = Joy" refere-se a esses objetos de diretório nos quais "Joy" representa qualquer classe na hierarquia de classes de objeto. "objectCategory = Joy", por outro lado, refere-se aos objetos de diretório nos quais "Joy" identifica uma classe específica na hierarquia de classes de objeto.

o **objectClass** pode assumir vários valores, enquanto **objectCategory** usa um único valor. Por isso, **objectCategory** é mais adequado para a correspondência de tipos de objetos em uma pesquisa de diretório. A ADSI usa isso como o critério de correspondência padrão. Pesquisas usando um **objectClass** não são escalonáveis para bancos de dados grandes. A ADSI dá suporte a sintaxes "(objectCategory = SomeDN)" e "(objectCategory = \_ \_ nome de exibição LDAP \_ de \_ classe)".

A exceção a tudo isso é que o filtro de pesquisa LDAP "(objectClass = \* )" não especifica uma pesquisa na classe de objeto, mas meramente testa a presença dos objetos.

 

 




