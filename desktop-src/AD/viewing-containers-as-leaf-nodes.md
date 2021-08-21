---
title: Exibindo contêineres como nós folha
description: Qualquer objeto no Active Directory Domain Services pode ser um contêiner de outros objetos.
ms.assetid: 38300ca5-745a-4640-9723-6052a9843f45
ms.tgt_platform: multiple
keywords:
- Exibindo contêineres como nós folha
- contêineres do AD , exibindo como nós folha
- folha do AD , exibindo contêineres como nós folha
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33713f70e1b84ded536a928f8489f4fd41461bd4e37de46a84036bc6370327db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118182249"
---
# <a name="viewing-containers-as-leaf-nodes"></a>Exibindo contêineres como nós folha

Qualquer objeto no Active Directory Domain Services pode ser um contêiner de outros objetos. Isso pode desorganar a interface do usuário, portanto, é possível declarar que um objeto de uma classe específica seja exibido apenas como uma folha na interface do usuário. O **atributo treatAsLeaf** é um atributo especificador de exibição de valor único que determina se os objetos dessa classe só devem ser exibidos como objetos folha. Esse atributo é um valor booliana que, se **TRUE,** indica que os objetos da classe só devem ser exibidos como elementos folha. Se **FALSE**, indica que os objetos da classe podem ser exibidos como um contêiner ou uma folha. Assim como todos os atributos do especificador de exibição, o atributo **treatAsLeaf** é definido por localidade, de modo que esse atributo possa ser localizado conforme necessário. Por exemplo, o especificador de exibição **User-Display** para a localidade em inglês (0409) tem o atributo **treatAsLeaf** definido como **TRUE** por padrão. Isso faz com que a interface do usuário exibe todos **os objetos User** como objetos folha.

**Para definir o valor do **atributo treatAsLeaf****

1.  A bind ao atributo de exibição desejado na localidade desejada. Para obter mais informações e um exemplo de código, consulte [DisplaySpecifiers Container](displayspecifiers-container.md).
2.  Use o [**método IADs::P ut**](/windows/desktop/api/iads/nf-iads-iads-put) para definir o **atributo treatAsLeaf** como **TRUE** ou **FALSE.**
3.  Para fazer commit das alterações no diretório, chame o [**método IADs::SetInfo.**](/windows/desktop/api/iads/nf-iads-iads-setinfo)

 

 