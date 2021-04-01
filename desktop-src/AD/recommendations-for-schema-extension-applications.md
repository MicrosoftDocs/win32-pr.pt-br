---
title: Recomendações para aplicativos de extensão de esquema
description: Este tópico inclui recomendações para aplicativos de extensão de esquema.
ms.assetid: 615e927e-a113-4557-b354-55a208a649eb
ms.tgt_platform: multiple
keywords:
- Recomendações para AD de aplicativos de extensão de esquema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2393211eb910ce4bc490667398da7f38d212ddcf
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104084438"
---
# <a name="recommendations-for-schema-extension-applications"></a>Recomendações para aplicativos de extensão de esquema

Além dos pré-requisitos, as seguintes práticas recomendadas são recomendadas para aplicativos de extensão de esquema:

-   Localize o mestre de esquema. Associe-se ao esquema no controlador de domínio que é o mestre de esquema. Evite alterar desnecessariamente a função de mestre de esquema entre os DCs. Para associar ao contêiner de esquema no mestre de esquema. Para obter mais informações, consulte [pré-requisitos para instalar uma extensão de esquema](prerequisites-for-installing-a-schema-extension.md).
-   Antes de executar qualquer ação, verifique a propriedade **allowedChildClassesEffective** do contêiner de esquema para verificar se você pode criar atributos e/ou classes. Se **attributeSchema** e **classSchema** não forem valores nessa propriedade, você não terá direitos suficientes para adicionar atributos ou classes ao esquema. Para obter mais informações, consulte [código de exemplo para verificar se há direitos para criar objetos de esquema](example-code-for-checking-for-rights-to-create-schema-objects.md).
-   Verifique se a atualização de esquema permitida está definida corretamente no registro do mestre de esquema. Para criar ou definir esse valor, restaure-o para seu estado original como parte da rotina de limpeza do seu aplicativo. Para obter mais informações sobre como verificar e definir esse valor, consulte [habilitando alterações de esquema no mestre de esquema](enabling-schema-changes-at-the-schema-master.md).
-   Antes de adicionar atributos ou classes, certifique-se de que eles ainda não existem. Se eles existirem, verifique se eles são os mesmos atributos ou classes que você está adicionando, e não um atributo ou uma classe criada por alguém com sintaxe e propriedades diferentes que são incompatíveis com seus atributos ou classes.

    Para atributos, consulte **CN**, **AttributeID**, **governsID**, **lDAPDisplayName** e **schemaIDGUID** para garantir que eles ainda não estejam sendo usados. Se você adicionar um conjunto de atributos vinculados (um link para frente, um link regressivo), verifique se os **LinkId** s já não estão sendo usados. Consulta para **governsID** porque o identificador de objeto (OID) deve ser exclusivo entre atributos e classes.

    Para classes, consulte para **CN**, **governsID**, **AttributeID**, **lDAPDisplayName** e **schemaIDGUID** para garantir que eles ainda não estejam sendo usados. Consulta para **AttributeID** porque o OID deve ser exclusivo entre classes e atributos.

    Para obter mais informações sobre como verificar se há colisões de nomenclatura, consulte [código de exemplo para detectar colisões de nomenclatura de esquema](example-code-for-detecting-schema-naming-collisions.md).

    Se existirem atributos ou classes que entram em conflito com seus novos atributos ou classes, seu aplicativo não deverá aplicar as alterações de esquema.

-   Se essa colisão existir, seu aplicativo não deverá aplicar as alterações de esquema. O administrador do esquema pode precisar resolver a colisão e executar o aplicativo novamente. Como alternativa, um **lDAPDisplayName** diferente poderia ser usado; no entanto, todos os aplicativos que usam o atributo ou o objeto devem estar cientes dessa alteração. Para ajudar a evitar colisões de OID, obtenha um OID de uma autoridade de registro de nome ISO.
-   Se seu aplicativo depende de atributos ou classes que ele adicionou, atualize o cache de esquema antes de adicionar os novos atributos ou classes que dependem desses atributos ou classes. Lembre-se de que o atributo operacional **schemaUpdateNow** é síncrono. Ou seja, a chamada de método [**IADs::P UT**](/windows/desktop/api/iads/nf-iads-iads-put) será bloqueada até que o cache de esquema seja atualizado. Quando a chamada retorna, o cache de esquema foi atualizado e os novos atributos e/ou classes são acessíveis.

    Para obter mais informações sobre como atualizar o cache de esquema, consulte [código de exemplo para atualizar o cache de esquema](example-code-for-updating-the-schema-cache.md).

 

 