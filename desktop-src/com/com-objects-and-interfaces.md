---
title: Objetos e interfaces COM
description: Objetos e interfaces COM
ms.assetid: a3b78086-0f02-4b3f-a856-46bfcf4457f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d0a663b5d6e5966422927e37f1501924bf8ec8921210c9d38765153dc0d80fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119501546"
---
# <a name="com-objects-and-interfaces"></a>Objetos e interfaces COM

COM é uma tecnologia que permite que os objetos interajam entre os limites do processo e do computador tão facilmente quanto em um único processo. COM permite isso especificando que a única maneira de manipular os dados associados a um objeto é por meio de uma *interface* no objeto . Quando esse termo é usado nesta documentação, ele se refere a uma implementação no código de uma interface compatível com binário COM associada a um objeto .

O COM usa a *interface* de palavra em um sentido diferente do que normalmente é usado na Visual C++ programação. Uma interface C++ refere-se a todas as funções que uma classe dá suporte e que os clientes de um objeto podem chamar para interagir com ela. Uma interface COM refere-se a um grupo predefinido de funções relacionadas que uma classe COM implementa, mas uma interface específica não representa necessariamente todas as funções que a classe dá suporte.

Consultar um objeto que implementa uma interface significa que o objeto usa código que implementa cada método da interface e fornece ponteiros em conformidade com COM para essas funções para *a* biblioteca COM. O COM disponibiliza essas funções para qualquer cliente que peça um ponteiro para a interface, independentemente de o cliente estar dentro ou fora do processo que implementa essas funções.

Para obter mais informações, consulte estes tópicos:

-   [Interfaces e implementações de interface](interfaces-and-interface-implementations.md)
-   [Ponteiros de interface e interfaces](interface-pointers-and-interfaces.md)
-   [Herança de interface e IUnknown](iunknown-and-interface-inheritance.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interfaces](interfaces.md)
</dt> </dl>

 

 




