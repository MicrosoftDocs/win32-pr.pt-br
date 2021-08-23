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

Um objeto conectável pode oferecer as interfaces [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) e [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2) para que seus clientes possam examinar facilmente suas informações de tipo. Essa funcionalidade é importante ao lidar com interfaces de saída, que, por definição, são definidas por um objeto, mas implementadas por um cliente em seu próprio objeto de sink. Em alguns casos, uma interface de saída é conhecida no tempo de compilação para o objeto conectável e o objeto de sink; esse é o caso de [**IPropertyNotifySink.**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink)

Em outros casos, no entanto, somente o objeto conectável conhece suas definições de interface de saída no tempo de compilação. Nesses casos, o cliente deve obter as informações de tipo para a interface de saída para que ele possa fornecer dinamicamente um sink que dê suporte aos pontos de entrada certos, da seguinte maneira:

1.  O cliente enumera os pontos de conexão e, em seguida, para obter os IIDs de interfaces de saída com suporte pelo objeto conectável, chama [**IConnectionPoint::GetConnectionInterface**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-getconnectioninterface) para cada ponto de conexão.
2.  O cliente consulta o objeto conectável para uma das interfaces [**IProvideClassInfo.**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo)
3.  O cliente chama métodos nas interfaces [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) para obter as informações de tipo para a interface de saída.
4.  O cliente cria um objeto de sink que dá suporte à interface de saída.
5.  O processo continua e o cliente chama [**IConnectionPoint::Advise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise) para conectar seu sink ao ponto de conexão.

Nas informações de tipo, a origem [**do**](/windows/desktop/Midl/source) atributo marca uma [**interface**](/windows/desktop/Midl/interface) ou [**dispinterface**](/windows/desktop/Midl/dispinterface) listada em uma [**coclasse**](/windows/desktop/Midl/coclass) como uma interface de saída. Aqueles listados sem esse atributo são considerados interfaces de entrada.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interfaces de objeto conectáveis](connectable-object-interfaces.md)
</dt> <dt>

[Fornecendo informações de classe](providing-class-information.md)
</dt> </dl>

 

 