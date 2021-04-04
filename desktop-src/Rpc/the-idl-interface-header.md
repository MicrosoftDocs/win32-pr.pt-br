---
title: O cabeçalho da interface IDL
description: O cabeçalho da interface IDL especifica informações sobre a interface como um todo. Ao contrário do ACF, o cabeçalho da interface contém atributos que são independentes de plataforma.
ms.assetid: 667e5228-3ea7-4910-90b9-999e6fd705e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8abce6204fdc09ed74a63a85e9366125dbef8e35
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084864"
---
# <a name="the-idl-interface-header"></a>O cabeçalho da interface IDL

O cabeçalho da interface IDL especifica informações sobre a interface como um todo. Ao contrário do ACF, o cabeçalho da interface contém atributos que são independentes de plataforma.

Os atributos no cabeçalho da interface são globais para toda a interface. Ou seja, eles se aplicam à interface e a todas as suas partes. Esses atributos são colocados entre colchetes no início da definição da interface. Um exemplo é mostrado na seguinte definição de interface:

``` syntax
[
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface INTERFACENAME
{

}
```

Observe que o cabeçalho da interface contém os **\[** atributos [**UUID**](/windows/desktop/Midl/uuid) **\]** e **\[** [**version**](/windows/desktop/Midl/version) **\]** . Como eles representam o UUID e o número de versão da interface, respectivamente, eles são atributos de toda a interface.

O corpo da interface também pode conter atributos. No entanto, eles não são aplicáveis à interface inteira. Eles se referem a itens específicos na interface, como parâmetros de procedimento remoto.

Para obter uma discussão completa sobre os atributos de cabeçalho IDL, consulte a [referência de linguagem MIDL](/windows/desktop/Midl/midl-language-reference).

 

 