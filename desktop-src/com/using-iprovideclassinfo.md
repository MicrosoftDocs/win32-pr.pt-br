---
title: Usando IProvideClassInfo
description: Usando IProvideClassInfo
ms.assetid: 16541aab-474f-4ae5-a6b6-fb2fea6d38ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c589e86596bf3e6719d3db8589570cfe347150c077e6bad19373693c18ee1ce0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118550570"
---
# <a name="using-iprovideclassinfo"></a>Usando IProvideClassInfo

Um objeto conectável pode oferecer as interfaces [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) e [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2) para que seus clientes possam examinar facilmente suas informações de tipo. Esse recurso é importante ao lidar com interfaces de saída, que, por definição, são definidos por um objeto, mas implementados por um cliente em seu próprio objeto Sink. Em alguns casos, uma interface de saída é conhecida em tempo de compilação tanto para o objeto connectável quanto para o objeto Sink; Esse é o caso com [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink).

Em outros casos, no entanto, somente o objeto conectável sabe suas definições de interface de saída no momento da compilação. Nesses casos, o cliente deve obter as informações de tipo da interface de saída para que ela possa fornecer dinamicamente um coletor com suporte aos pontos de entrada certos, da seguinte maneira:

1.  O cliente enumera os pontos de conexão e, em seguida, para obter o IIDs de interfaces de saída com suporte do objeto connectável, chama [**IConnectionPoint:: GetConnectionInterface**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-getconnectioninterface) para cada ponto de conexão.
2.  O cliente consulta o objeto que pôde ser conectado para uma das interfaces [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) .
3.  O cliente chama métodos nas interfaces [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) para obter as informações de tipo para a interface de saída.
4.  O cliente cria um objeto de coletor que dá suporte à interface de saída.
5.  O processo continua e o cliente chama [**IConnectionPoint:: Advise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise) para conectar seu coletor ao ponto de conexão.

Nas informações de tipo, a [**origem**](/windows/desktop/Midl/source) do atributo marca uma [**interface**](/windows/desktop/Midl/interface) ou [**dispinterface**](/windows/desktop/Midl/dispinterface) listada em uma [**coclass**](/windows/desktop/Midl/coclass) como uma interface de saída. Aqueles listados sem esse atributo são considerados interfaces de entrada.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interfaces de objeto conectáveis](connectable-object-interfaces.md)
</dt> <dt>

[Fornecendo informações de classe](providing-class-information.md)
</dt> </dl>

 

 