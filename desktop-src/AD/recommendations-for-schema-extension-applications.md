---
title: Recomendações aplicativos de extensão de esquema
description: Este tópico inclui recomendações para aplicativos de extensão de esquema.
ms.assetid: 615e927e-a113-4557-b354-55a208a649eb
ms.tgt_platform: multiple
keywords:
- Recomendações para o AD de Aplicativos de Extensão de Esquema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c0a01e68fbe9751b778caa2404d02afb1ddd7704457c9cf0aedcc914387ab5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025264"
---
# <a name="recommendations-for-schema-extension-applications"></a>Recomendações aplicativos de extensão de esquema

Além dos pré-requisitos, as seguintes práticas recomendadas são recomendadas para aplicativos de extensão de esquema:

-   Encontre o mestre de esquema. A bind ao esquema no DC que é o mestre de esquema. Evite alterar desnecessariamente a função mestra de esquema entre os DCs. Para se vincular ao contêiner de esquema no mestre de esquema. Para obter mais informações, consulte [Prerequisites for Installing a Schema Extension](prerequisites-for-installing-a-schema-extension.md).
-   Antes de executar qualquer ação, verifique a **propriedade allowedChildClassesEffective** do contêiner de esquema para verificar se você pode criar atributos e/ou classes. Se **attributeSchema** e **classSchema** não são valores nessa propriedade, você não tem direitos suficientes para adicionar atributos ou classes ao esquema. Para obter mais informações, consulte [Código de exemplo para verificar se há direitos para criar objetos de esquema](example-code-for-checking-for-rights-to-create-schema-objects.md).
-   Verifique se a Atualização de Esquema Permitida está definida adequadamente no registro do mestre de esquema. Para criar ou definir esse valor, restaure-o para seu estado original como parte da rotina de limpeza do aplicativo. Para obter mais informações sobre como verificar e definir esse valor, consulte [Habilitando](enabling-schema-changes-at-the-schema-master.md)alterações de esquema no Mestre de Esquema.
-   Antes de adicionar atributos ou classes, certifique-se de que eles ainda não existem. Se eles existirem, verifique se são os mesmos atributos ou classes que você está adicionando e não um atributo ou classe criado por alguém com sintaxe e propriedades diferentes incompatíveis com seus atributos ou classes.

    Para atributos, consulte **cn**, **attributeID**, **governsID**, **lDAPDisplayName** e **schemaIDGUID** para garantir que eles ainda não sejam usados. Se você adicionar um conjunto de atributos vinculados (um link para frente, um link de retorno), verifique se os **linkIDs** ainda não foram usados. Consulte **governsID porque** o OID (identificador de objeto) deve ser exclusivo entre atributos e classes.

    Para classes, consulte **cn**, **governsID,** **attributeID**, **lDAPDisplayName** e **schemaIDGUID** para garantir que eles ainda não sejam usados. Consulte **attributeID porque** o OID deve ser exclusivo entre classes e atributos.

    Para obter mais informações sobre como verificar se há colisões de nomeação, consulte Código de [exemplo para detectar colisões](example-code-for-detecting-schema-naming-collisions.md)de nomeação de esquema .

    Se existirem atributos ou classes que estão em conflito com seus novos atributos ou classes, seu aplicativo não deverá aplicar as alterações de esquema.

-   Se essa colisão existir, seu aplicativo não deverá aplicar as alterações de esquema. O administrador do esquema pode precisar resolver a colisão e, em seguida, executar o aplicativo novamente. Como alternativa, um **lDAPDisplayName diferente** pode ser usado; no entanto, todos os aplicativos que usam o atributo ou o objeto devem estar cientes dessa alteração. Para ajudar a evitar colisões OID, obtenha um OID de uma autoridade de registro de nome ISO.
-   Se o aplicativo for dependente de atributos ou classes que ele adicionou, atualize o cache de esquema antes de adicionar os novos atributos ou classes que dependem desses atributos ou classes. Esteja ciente de que o **atributo operacional schemaUpdateNow** é síncrono. Ou seja, a [**chamada de método IADs::P ut**](/windows/desktop/api/iads/nf-iads-iads-put) será bloqueado até que o cache de esquema seja atualizado. Quando a chamada retorna, o cache de esquema foi atualizado e os novos atributos e/ou classes estão acessíveis.

    Para obter mais informações sobre como atualizar o cache de esquema, consulte [Código de exemplo para atualizar o cache de esquema.](example-code-for-updating-the-schema-cache.md)

 

 