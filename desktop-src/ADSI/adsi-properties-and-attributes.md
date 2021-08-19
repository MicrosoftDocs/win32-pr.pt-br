---
title: Propriedades e atributos ADSI
description: Às vezes, os atributos são chamados de propriedades. Isso pode causar confusão. Esta documentação usa as definições a seguir para propriedades e atributos.
ms.assetid: 8e391d36-5a8d-4960-805a-0caf281cab80
ms.tgt_platform: multiple
keywords:
- Propriedades e atributos ADSI ADSI
- ADSI ADSI , usando, acessando e manipulando dados, propriedades e atributos
- ADSI de propriedades
- ADSI de atributos
- propriedades ADSI , definidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b05637cada9a62cee129e9645385233b4700cbf2762b9446ba9a871d1897d440
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082790"
---
# <a name="adsi-properties-and-attributes"></a>Propriedades e atributos ADSI

Às vezes, os atributos são chamados de propriedades. Isso pode causar confusão. Esta documentação usa as definições a seguir para propriedades e atributos.

As propriedades são valores nomeados associados a um objeto de programação. Por exemplo, a interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) expõe propriedades como [**Classe**](iads-property-methods.md) e **Nome**.

Atributos são os dados associados a objetos em um serviço de diretório. Por exemplo, um objeto de usuário terá um atributo chamado **cn** que contém uma cadeia de caracteres que é o nome diferenciado comum ou relativo do objeto. Os atributos são acessíveis por meio de métodos de interface [**ADSI, como IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) e [**IADs.Put.**](/windows/desktop/api/Iads/nf-iads-iads-put)

Para obter mais informações sobre propriedades e atributos ADSI, consulte:

-   [O cache de atributo ADSI](the-adsi-attribute-cache.md)
-   [Atributos de valor único vs. múltiplo](single-vs--multiple-value-attributes.md)
-   [Atributos operacionais do Active Directory](active-directory-operational-attributes.md)

 

 




