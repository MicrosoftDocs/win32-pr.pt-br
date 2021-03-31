---
title: Decidindo o que encontrar
description: Antes de Pesquisar um diretório, considere como sua pesquisa será executada com base em sua abordagem. Os dados e as propriedades a serem retornados afetam o local em que você se associa para iniciar uma pesquisa, a profundidade de sua pesquisa, o filtro de consulta e o desempenho da pesquisa.
ms.assetid: 788fa12c-9086-4d8b-bd2e-e96a494a26ad
ms.tgt_platform: multiple
keywords:
- critérios de pesquisa Active Directory
- decidindo o que encontrar Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 818b0f9be56830a836453c5e52ceadd52928a522
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004940"
---
# <a name="deciding-what-to-find"></a>Decidindo o que encontrar

Antes de Pesquisar um diretório, considere como sua pesquisa será executada com base em sua abordagem. Os dados e as propriedades a serem retornados afetam o local em que você se associa para iniciar uma pesquisa, a profundidade de sua pesquisa, o filtro de consulta e o desempenho da pesquisa.

Por exemplo, se você quiser pesquisar todos os objetos de usuário com o sobrenome Smith:



| Área                       | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Onde Pesquisar            | Um contêiner específico ou uma UO (unidade organizacional) em um domínio, um domínio específico, uma árvore de domínio específica ou toda a floresta. Se você Pesquisar objetos dentro de um contêiner ou domínio específico, a consulta de pesquisa terá um desempenho melhor com a associação direta a esse contêiner ou domínio em vez de executar uma pesquisa de subárvore em uma árvore de domínio.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Tipo de pesquisa             | Se você verificar a existência de ou recuperar as propriedades de um objeto específico que tem um DN (nome distinto) que você já conhece, deverá executar uma pesquisa básica, que pesquisa somente o objeto ao qual você está vinculado.<br/> Se você souber que um objeto é um descendente direto de um contêiner específico, vincule a esse contêiner e faça uma pesquisa de nível único (objetos **attributeSchema** e **classSchema** no contêiner de esquema e objetos estendidos à direita no contêiner de direitos estendidos são bons exemplos).<br/> Se você não souber exatamente onde está o objeto, ou se quiser pesquisar o objeto ao qual você está vinculado e todos os objetos filho abaixo dele na hierarquia de diretório, execute uma pesquisa de subárvore.<br/>                                                       |
| Usar índices sempre que possível | Por fim, se você procurar uma classe específica de objeto, o filtro de consulta deverá ter expressões que avaliem as propriedades definidas para essa classe.<br/> Para pesquisar objetos de grupo, inclua a expressão (objectCategory = Group) no filtro. Para procurar objetos de usuário, especifique (& (objectClass = user) (objectCategory = Person)), pois a classe Computer deriva da classe User, portanto (objectClass = user) retornaria usuários e computadores e também porque os objetos Contact e User têm uma **objectCategory** de Person, portanto (objectCategory = Person) retornaria usuários e contatos.<br/> Para obter mais informações, consulte [classe de objeto e categoria de objeto](object-class-and-object-category.md) e [atributos indexados](indexed-attributes.md).<br/> |



 

 

 





