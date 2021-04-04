---
title: Definindo um novo atributo
description: Este tópico mostra como definir um novo atributo ao estender o esquema de Active Directory.
ms.assetid: b8ac69ba-3b75-4e55-bf80-dabf2e80288a
ms.tgt_platform: multiple
keywords:
- Definindo um novo atributo de AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9da1a0a003d92fe09f27043098cb1abc4387b81e
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104084453"
---
# <a name="defining-a-new-attribute"></a>Definindo um novo atributo

Este tópico mostra como definir um novo atributo ao estender o esquema de Active Directory.

Considere o seguinte ao definir um novo atributo:

-   Use atributos existentes quando possível.
-   Sempre use a propriedade **CN** ("nome comum") como o atributo de nomenclatura (nome distinto relativo). Esse é o padrão para a maioria das classes, incluindo aquelas derivadas diretamente da parte superior. A propriedade **CN** é uma propriedade indexada e tornará a pesquisa de objetos pelo nome mais eficiente.
-   Grandes atributos de vários valores são caros de armazenar e recuperar e devem ser evitados. Active Directory Domain Services implementar uma extensão LDAP para habilitar a leitura incremental de propriedades grandes com vários valores, mas nem todos os clientes LDAP reconhecerão essa extensão.
-   Lembre-se de que os atributos são simples, ou seja, não há subestrutura implícita para um atributo. Todos os atributos em uma determinada classe devem estar relacionados diretamente a instâncias dessa classe.

## <a name="creating-a-new-attribute"></a>Criando um novo atributo

Para criar um novo atributo:

-   Escolha um nome para o atributo. O nome estará contido nos atributos **CN** e **lDAPDisplayName** . Para obter mais informações sobre como compor um nome para um novo atributo, consulte [nomenclatura de atributos e classes](naming-attributes-and-classes.md).
-   Obtenha um OID (identificador de objeto) para o atributo. Para obter mais informações, consulte [obtendo um identificador de objeto raiz](obtaining-an-object-identifier.md).
-   Escolha uma sintaxe para o atributo. A sintaxe é determinada pela combinação dos atributos **oMSyntax** e **oMObjectClass** . Para obter mais informações, consulte [escolhendo uma sintaxe](choosing-a-syntax.md).
-   Decida se o atributo é único ou com vários valores. O atributo **isSingleValued** determina se o atributo é único ou com vários valores.
-   Decida se o atributo deve ser indexado por padrão. Para obter mais informações, consulte [atributos indexados](indexed-attributes.md).
-   Decida se o atributo deve estar no catálogo global por padrão. Para obter mais informações, consulte [atributos incluídos no catálogo global](attributes-included-in-the-global-catalog.md).
-   Se o atributo for um inteiro ou uma cadeia de caracteres, decida se um limite de intervalo é necessário. Os atributos **RangeLower** e **rangeUpper** são usados para especificar o limite de intervalo.
-   Se o atributo for de valor DN, decida se o atributo deve ser vinculado a outro atributo. Nesse caso, o atributo [**LinkId**](/windows/desktop/ADSchema/a-linkid) deve ser definido adequadamente em cada atributo; um atributo deve ser um vínculo progressivo, o outro, um link regressivo. Para obter mais informações sobre atributos vinculados, consulte [atributos vinculados](linked-attributes.md).
-   Crie um novo objeto **attributeSchema** no contêiner de esquema e defina os atributos apropriados para o objeto. Há um grande número de atributos que podem ser definidos para um objeto **attributeSchema** , mas os atributos listados na tabela a seguir são essenciais para a definição de um novo atributo. Os valores desses atributos são determinados pelas etapas anteriores. Para obter mais informações sobre esses atributos, consulte [características dos atributos](characteristics-of-attributes.md).

    | Atributo                                    | Comentário                                              |
    |----------------------------------------------|------------------------------------------------------|
    | **cn**<br/>                            | Obrigatórios.<br/>                                 |
    | **lDAPDisplayName**<br/>               | Obrigatórios.<br/>                                 |
    | **adminDisplayName**<br/>              | Obrigatórios.<br/>                                 |
    | **attributeSyntax**<br/>               | Obrigatórios.<br/>                                 |
    | **oMSyntax**<br/>                      | Obrigatórios.<br/>                                 |
    | **oMObjectClass**<br/>                 | Obrigatórios.<br/>                                 |
    | **schemaIDGUID**<br/>                  | Obrigatórios.<br/>                                 |
    | **attributeID**<br/>                   | Obrigatórios.<br/>                                 |
    | **isSingleValued**<br/>                | Obrigatórios.<br/>                                 |
    | **searchFlags**<br/>                   | Obrigatórios.<br/>                                 |
    | **isMemberOfPartialAttributeSet**<br/> | Obrigatórios.<br/>                                 |
    | **rangeLower**<br/>                    | Opcional.<br/>                                 |
    | **rangeUpper**<br/>                    | Opcional.<br/>                                 |
    | **linkID**<br/>                        | Opcional. Obrigatório para atributos vinculados.<br/> |
    | **descrição**<br/>                   | Opcional.<br/>                                 |

    

     

-   Confirme o novo objeto **attributeSchema** para o contêiner de esquema.
-   Atualize o cache de esquema, se necessário. Para obter mais informações, consulte [atualizando o cache de esquema](updating-the-schema-cache.md).

 

