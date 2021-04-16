---
title: Propriedades e atributos ADSI
description: Os atributos são, às vezes, chamados de propriedades. Isso pode causar confusão. Esta documentação usa as definições a seguir para propriedades e atributos.
ms.assetid: 8e391d36-5a8d-4960-805a-0caf281cab80
ms.tgt_platform: multiple
keywords:
- ADSI de propriedades e atributos ADSI
- ADSI ADSI, usando, acessando e manipulando dados, propriedades e atributos
- ADSI de propriedades
- ADSI de atributos
- Propriedades ADSI, definidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10c7b1dca9882f53b7fa746121ed431ace7f9af7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105750341"
---
# <a name="adsi-properties-and-attributes"></a>Propriedades e atributos ADSI

Os atributos são, às vezes, chamados de propriedades. Isso pode causar confusão. Esta documentação usa as definições a seguir para propriedades e atributos.

As propriedades são valores nomeados associados a um objeto de programação. Por exemplo, a interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) expõe propriedades como [**Class**](iads-property-methods.md) e **Name**.

Os atributos são os dados associados a objetos em um serviço de diretório. Por exemplo, um objeto de usuário terá um atributo chamado **CN** , que contém uma cadeia de caracteres que é o nome distinto comum ou relativo do objeto. Os atributos são acessíveis por meio de métodos de interface ADSI, como [**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) e [**IADs. put**](/windows/desktop/api/Iads/nf-iads-iads-put).

Para obter mais informações sobre propriedades e atributos ADSI, consulte:

-   [O cache de atributo ADSI](the-adsi-attribute-cache.md)
-   [Atributos únicos versus múltiplos valores](single-vs--multiple-value-attributes.md)
-   [Active Directory atributos operacionais](active-directory-operational-attributes.md)

 

 




