---
title: objectCategory vs. objectClass
description: Os atributos objectCategory e objectClass podem se referir a uma determinada classe de esquema de um objeto de diretório.
ms.assetid: 66dadedb-61e4-4184-9b87-0fff036a94d9
ms.tgt_platform: multiple
keywords:
- objectCategory vs. objectClass ADSI
- atributos ASI , pesquisando os atributos objectCategory e objectClass
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d3833f8cf26cb2272fbe1e7c1063322f39a8c0147e4b22382d26067f90e72e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117839216"
---
# <a name="objectcategory-vs-objectclass"></a>objectCategory vs. objectClass

Os atributos **objectCategory** e **objectClass** podem se referir a uma determinada classe de esquema de um objeto de diretório. No entanto, há uma distinção importante na semântica entre os dois. "objectClass=ltd" refere-se a tais objetos de diretório nos quais "classe" representa qualquer classe na hierarquia da classe de objeto. "objectCategory=park", por outro lado, refere-se aos objetos de diretório nos quais "meu" identifica uma classe específica na hierarquia da classe de objeto.

**objectClass** pode usar vários valores, enquanto **objectCategory** aceita um único valor. Por isso, **objectCategory** é mais adequado para correspondência de tipos de objetos em uma pesquisa de diretório. A ADSI usa isso como o critério de correspondência padrão. Pesquisas usando um **objectClass não são** escalonáveis para bancos de dados grandes. O ADSI dá suporte às sintaxes "(objectCategory=SomeDN)" e "(objectCategory=Ldap \_ Display \_ Name of \_ \_ Class)".

A exceção a tudo isso é que o filtro de pesquisa LDAP "(objectClass= )" não especifica uma pesquisa na classe de objeto, mas simplesmente testa a presença dos \* objetos.

 

 




