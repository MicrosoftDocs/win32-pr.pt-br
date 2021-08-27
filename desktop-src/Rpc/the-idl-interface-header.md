---
title: O header da interface IDL
description: O header da interface IDL especifica informações sobre a interface como um todo. Ao contrário do ACF, o header da interface contém atributos que são independentes de plataforma.
ms.assetid: 667e5228-3ea7-4910-90b9-999e6fd705e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33c176078c370819331405b070ffa832384584a944b65fae771b9a2044a178e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924265"
---
# <a name="the-idl-interface-header"></a>O header da interface IDL

O header da interface IDL especifica informações sobre a interface como um todo. Ao contrário do ACF, o header da interface contém atributos que são independentes de plataforma.

Os atributos no header da interface são globais para toda a interface. Ou seja, eles se aplicam à interface e a todas as suas partes. Esses atributos são incluídos entre colchetes no início da definição da interface. Um exemplo é mostrado na seguinte definição de interface:

``` syntax
[
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface INTERFACENAME
{

}
```

Observe que o header da interface contém os **\[** [**atributos uuid**](/windows/desktop/Midl/uuid) **\]** e **\[** [**version.**](/windows/desktop/Midl/version) **\]** Como eles representam o UUID e o número de versão da interface, respectivamente, eles são atributos de toda a interface.

O corpo da interface também pode conter atributos. No entanto, eles não são aplicáveis a toda a interface. Eles se referem a itens específicos na interface, como parâmetros de procedimento remoto.

Para uma discussão completa sobre os atributos de header IDL, consulte a [Referência de linguagem MIDL](/windows/desktop/Midl/midl-language-reference).

 

 