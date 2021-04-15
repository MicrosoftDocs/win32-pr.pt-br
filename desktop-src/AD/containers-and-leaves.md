---
title: Contêineres e folhas
description: Active Directory Domain Services conter uma hierarquia de objetos na qual cada instância de objeto, exceto a raiz da hierarquia de diretórios, está contida em algum outro objeto.
ms.assetid: ef17e84c-6c7f-4ebe-a904-fead6c27518d
ms.tgt_platform: multiple
keywords:
- contêineres e folhas de Active Directory
- Active Directory folha
- Active Directory de contêiner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f9039e4619ea0bd50d20c3bd425b6a8536a1034
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104453947"
---
# <a name="containers-and-leaves"></a>Contêineres e folhas

Active Directory Domain Services conter uma hierarquia de objetos na qual cada instância de objeto, exceto a raiz da hierarquia de diretórios, está contida em algum outro objeto. A estrutura dessa hierarquia é mais flexível do que um sistema de arquivos de diretórios e arquivos. Em vez disso, as regras, no [esquema de Active Directory](active-directory-schema.md), determinam quais classes de objeto podem conter instâncias das quais outras classes de objeto. Por exemplo, a definição de esquema padrão da classe de objeto [**User**](/windows/desktop/ADSchema/c-user) inclui as classes de objeto de [**contêiner**](/windows/desktop/ADSchema/c-container) e de [**unidade organizacional**](/windows/desktop/ADSchema/c-organizationalunit) como superiores possíveis; ou seja, possíveis objetos pai ou contêineres de uma instância de objeto de **usuário** . Isso significa que um objeto **de unidade organizacional** pode conter um objeto de **usuário** , mas um objeto de **usuário** não pode conter outro objeto de **usuário** , a menos que a definição de esquema da classe de **usuário** seja alterada.

Exceto para objetos de esquema, ou seja, os objetos [**classSchema**](/windows/desktop/ADSchema/c-classschema) ou [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) que definem as classes e os atributos que podem existir em uma floresta de servidor, qualquer objeto em Active Directory Domain Services pode ser um contêiner. Especificamente, qualquer classe de objeto que aparece no atributo [**possSuperior**](/windows/desktop/ADSchema/a-posssuperiors) ou [**systemPossSuperiors**](/windows/desktop/ADSchema/a-systemposssuperiors) de uma definição de classe de objeto é potencialmente um contêiner. Para obter mais informações sobre contêineres de uma classe de objeto predefinida, consulte [referência de Active Directory Domain Services](active-directory-domain-services-reference.md). Você pode associar programaticamente ao esquema abstrato e usar os métodos [**IADsClass:: get \_ contenção**](/windows/desktop/api/iads/nn-iads-iadsclass) ou [**IADsClass:: get \_ PossibleSuperiors**](/windows/desktop/api/iads/nn-iads-iadsclass) para obter as classes que uma determinada classe pode conter ou que estão contidas. Para obter mais informações, consulte [lendo o esquema abstrato](reading-the-abstract-schema.md). Você também pode ler o atributo [**PossibleInferiors**](/windows/desktop/ADSchema/a-possibleinferiors) de qualquer instância de objeto para determinar as classes de objeto que o objeto pode conter. Lembre-se de que **PossibleInferiors** é um atributo construído, o que significa que ele é calculado a partir dos valores de  / **systemPossSuperiors** de possSuperior das outras definições de classe e não está realmente armazenado no diretório.

Lembre-se de que o esquema de Active Directory define uma classe de [**contêiner**](/windows/desktop/ADSchema/c-container) . Conforme discutido anteriormente, um objeto não precisa ser uma instância da classe de **contêiner** para ser um contêiner. Há também uma classe [**folha**](/windows/desktop/ADSchema/c-leaf) e, embora as subclasses dessa classe normalmente não sejam contêineres, não há nenhum motivo para não poderem ser.

Por fim, você pode definir um sinalizador no especificador de exibição associado a uma classe de objeto para indicar que as interfaces de usuário devem sempre exibir instâncias da classe como folhas, e não contêineres. Isso ajuda a impedir que a interface do usuário seja obstruída por muitos contêineres. Para obter mais informações, consulte [exibindo contêineres como nós folha](viewing-containers-as-leaf-nodes.md).

 

 