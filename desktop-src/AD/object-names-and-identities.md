---
title: Nomes de objetos e identidades
description: Um objeto no Active Directory Domain Services tem várias identidades, incluindo as seguintes.
ms.assetid: ad8bc74d-45a8-4df3-bfb8-35dd376b9c0b
ms.tgt_platform: multiple
keywords:
- nomes de objetos e identidades Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a803b4cc068a3ee0f9e2a75f61ff239c1d971bf3
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104453914"
---
# <a name="object-names-and-identities"></a>Nomes de objetos e identidades

Um objeto no Active Directory Domain Services tem várias identidades, incluindo as seguintes.

## <a name="relative-distinguished-name"></a>Nome distinto relativo

O nome distinto relativo é o nome definido pelo atributo de nomenclatura de um objeto. O atributo **rDnAttID** de um objeto **classSchema** identifica o atributo de nomenclatura para instâncias da classe. A maioria das classes de objeto usa o atributo **CN** (nome comum) como o atributo de nomenclatura. O nome distinto relativo de um objeto deve ser exclusivo no contêiner em que o objeto reside. Pode haver muitas instâncias de objeto com o mesmo nome distinto relativo, mas duas podem estar no mesmo contêiner. Para obter mais informações sobre o atributo **rDnAttID** e objetos **ClassSchema** , consulte [características das classes de objeto](characteristics-of-object-classes.md).

## <a name="distinguished-name"></a>Nome Distinto

O [*nome distinto*](/previous-versions/windows/desktop/legacy/ms681901(v=vs.85)) é o nome atual do objeto e está contido no atributo **distinguishedName** do objeto. O nome distinto é uma cadeia de caracteres que inclui o local do objeto e é formado pela concatenação do nome distinto relativo do objeto e de cada um de seus ancestrais até a raiz. Por exemplo, o nome distinto do contêiner usuários no domínio Fabrikam.com seria "CN = Users, DC = Fabrikam, DC = com". Nomes distintos são exclusivos em uma floresta. O nome distinto de um objeto é alterado quando o objeto é movido ou renomeado.

## <a name="object-guid"></a>GUID do objeto

O GUID do objeto é um identificador global exclusivo atribuído por Active Directory Domain Services quando a instância do objeto é criada. O GUID do objeto está contido no atributo **objectGUID** do objeto. Um GUID é um número de 128 bits com garantia de ser exclusivo em espaço e tempo. Os GUIDs de objeto nunca são alterados, portanto, se um objeto for renomeado ou movido em qualquer lugar na floresta da empresa, o GUID do objeto permanecerá o mesmo. Os aplicativos que salvam referências a objetos no Active Directory Domain Services devem usar o GUID do objeto para garantir que a referência do objeto sobreviver a uma renomeação do objeto. O nome distinto de um objeto pode ser alterado, mas o GUID do objeto não será.

## <a name="other-identities"></a>Outras identidades

As instâncias de objeto podem ter muitos outros atributos e os atributos podem ser usados para identificação por aplicativos. Por exemplo, os objetos de entidade de segurança (instâncias das classes de objeto **usuário**, **computador** e **grupo** ) têm os atributos **userPrincipalName**, **sAMAccountName** e **objectSid** . Esses atributos são "nomes" muito importantes para o Windows 2000, mas eles não fazem parte da identidade do objeto da perspectiva do diretório.

 

 