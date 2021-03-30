---
title: Objetos e interfaces COM
description: Objetos e interfaces COM
ms.assetid: a3b78086-0f02-4b3f-a856-46bfcf4457f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a8c2b74f2b9741e41e7fe23226041f4c225bd85
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634997"
---
# <a name="com-objects-and-interfaces"></a>Objetos e interfaces COM

O COM é uma tecnologia que permite que os objetos interajam entre os limites do processo e do computador tão facilmente quanto em um único processo. COM habilita isso especificando que a única maneira de manipular os dados associados a um objeto é por meio de uma *interface* no objeto. Quando este termo é usado nesta documentação, ele se refere a uma implementação no código de uma interface compatível com binário com, que está associada a um objeto.

O COM usa a *interface* do Word de forma diferente da que normalmente é usada em Visual C++ programação. Uma interface C++ refere-se a todas as funções às quais uma classe dá suporte e que os clientes de um objeto podem chamar para interagir com ela. Uma interface COM refere-se a um grupo predefinido de funções relacionadas que uma classe COM implementa, mas uma interface específica não representa necessariamente todas as funções às quais a classe dá suporte.

Fazer referência a um objeto que *implementa* uma interface significa que o objeto usa código que implementa cada método da interface e fornece ponteiros compatíveis com binários com para essas funções para a biblioteca com. COM, o COM torna essas funções disponíveis para qualquer cliente que solicite um ponteiro para a interface, se o cliente está dentro ou fora do processo que implementa essas funções.

Para mais informações, consulte os seguintes tópicos:

-   [Interfaces e implementações de interface](interfaces-and-interface-implementations.md)
-   [Ponteiros de interface e interfaces](interface-pointers-and-interfaces.md)
-   [IUnknown e herança de interface](iunknown-and-interface-inheritance.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interfaces](interfaces.md)
</dt> </dl>

 

 




