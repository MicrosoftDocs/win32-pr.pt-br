---
title: Interfaces de objeto conectáveis
description: Interfaces de objeto conectáveis
ms.assetid: 136fb7bd-7a38-4051-b47b-3d08f1dbee79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dc2d747d7aabe25788c34d80bddb8ca1466e9c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103823014"
---
# <a name="connectable-object-interfaces"></a>Interfaces de objeto conectáveis

O suporte para objetos conectáveis requer suporte para quatro interfaces:

-   [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) no objeto conectável
-   [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) no objeto de ponto de conexão
-   [**IEnumConnectionPoints**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnectionpoints) em um objeto enumerador
-   [**IEnumConnections**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnections) em um objeto enumerador

Os dois últimos são definidos como enumeradores padrão para os tipos **IConnectionPoint \*** e [**CONNECTDATA**](/windows/win32/api/ocidl/ns-ocidl-connectdata).

Além disso, o objeto conectável pode, opcionalmente, dar suporte a [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) e [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2) para fornecer informações suficientes para um cliente para que o cliente possa fornecer suporte para a interface de saída em tempo de execução.

Por fim, o cliente deve fornecer um objeto Sink que implementa a interface de saída, que é uma interface COM personalizada definida pelo objeto que pode ser conectado.

Para mais informações, consulte os seguintes tópicos:

-   [Usando IConnectionPointContainer](using-iconnectionpointcontainer.md)
-   [Usando IConnectionPoint](using-iconnectionpoint.md)
-   [Usando IProvideClassInfo](using-iprovideclassinfo.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Arquitetura de objetos conectáveis](architecture-of-connectable-objects.md)
</dt> </dl>

 

 




