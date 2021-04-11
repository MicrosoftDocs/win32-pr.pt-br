---
title: Exibindo contêineres como nós folha
description: Qualquer objeto no Active Directory Domain Services pode ser um contêiner de outros objetos.
ms.assetid: 38300ca5-745a-4640-9723-6052a9843f45
ms.tgt_platform: multiple
keywords:
- Exibindo contêineres como nós folha
- contêineres AD, exibindo como nós folha
- ANÚNCIO folha, exibindo contêineres como nós folha
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1631526ed78132829a7576960a997b13cc232b5f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104293881"
---
# <a name="viewing-containers-as-leaf-nodes"></a>Exibindo contêineres como nós folha

Qualquer objeto no Active Directory Domain Services pode ser um contêiner de outros objetos. Isso pode obstruir a interface do usuário, portanto, é possível declarar que um objeto de uma classe específica só seja exibido como uma folha na interface do usuário. O atributo **treatAsLeaf** é um atributo de especificador de exibição com valor único que determina se os objetos dessa classe devem ser exibidos apenas como objetos folha. Esse atributo é um valor booliano que, se **verdadeiro**, indica que os objetos da classe só devem ser exibidos como elementos folha. Se **for false**, indicará que os objetos da classe podem ser exibidos como um contêiner ou uma folha. Como todos os atributos de especificador de exibição, o atributo **treatAsLeaf** é definido em uma base por localidade, portanto, esse atributo pode ser localizado conforme necessário. Por exemplo, a **exibição de usuário** para o especificador de exibição do idioma inglês (0409) tem o atributo **TreatAsLeaf** definido como **true** por padrão. Isso faz com que a interface do usuário exiba todos os objetos de **usuário** como objetos folha.

**Para definir o valor do atributo **treatAsLeaf****

1.  Associe-se ao atributo de exibição desejado na localidade desejada. Para obter mais informações e um exemplo de código, consulte [contêiner DisplaySpecifiers](displayspecifiers-container.md).
2.  Use o método [**IADs::P UT**](/windows/desktop/api/iads/nf-iads-iads-put) para definir o atributo **treatAsLeaf** como **true** ou **false**.
3.  Para confirmar as alterações no diretório, chame o método [**IADs:: setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) .

 

 