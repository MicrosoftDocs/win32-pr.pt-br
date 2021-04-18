---
title: Usando IConnectionPointContainer
description: Usando IConnectionPointContainer
ms.assetid: a87afb25-4d45-4ce2-9b27-840da5107bce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4d0b7c691e1ba6a8445af56978b43a2ccbf33e7
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "105771338"
---
# <a name="using-iconnectionpointcontainer"></a>Usando IConnectionPointContainer

Um objeto conectável implementa [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) (e a expõe por meio de [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q))) para indicar a existência de interfaces de saída. Para cada interface de saída, o objeto conectável gerencia um subobjeto de ponto de conexão que, por sua vez, implementa [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint). O objeto conectável, portanto, contém os pontos de conexão, portanto, a nomenclatura de **IConnectionPointContainer** e **IConnectionPoint**.

Por meio do [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer), um cliente pode executar duas operações. Primeiro, se o cliente já tiver o IID para uma interface de saída que ele suporta, ele poderá localizar o ponto de conexão correspondente para o IID usando [**IConnectionPointContainer:: FindConnectionPoint**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint). O cliente não pode consultar o ponto de conexão diretamente devido à relação contêiner/contido entre o objeto conectável e seus pontos de conexão independentes. Basicamente, **FindConnectionPoint** é o [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) para interfaces de saída quando o IID é conhecido pelo cliente.

Em segundo lugar, o cliente pode enumerar todos os pontos de conexão no objeto de conexão por meio de [**IConnectionPointContainer:: EnumConnectionPoints**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpointcontainer-enumconnectionpoints). Esse método retorna um ponteiro de interface [**IEnumConnectionPoints**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnectionpoints) para um objeto enumerador separado. Por meio de [**IEnumConnectionPoints:: Next**](/windows/desktop/api/ocidl/nf-ocidl-ienumconnectionpoints-next), o cliente pode obter ponteiros de interface [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) para cada ponto de conexão.

Depois que o cliente obtém a interface [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) , ele deve chamar [**IConnectionPoint:: GetConnectionInterface**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-getconnectioninterface) para determinar o IID da interface de saída compatível com cada ponto de conexão. Se o cliente já der suporte a essa interface de saída, ele poderá estabelecer uma conexão. Caso contrário, ele ainda pode ser capaz de dar suporte à interface de saída usando informações da biblioteca de tipos do objeto que pode ser conectado para fornecer suporte em tempo de execução. Essa técnica requer que o objeto conectável dê suporte à interface [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) . (Consulte [usando IProvideClassInfo](using-iprovideclassinfo.md).)

Como o enumerador é um objeto separado, o cliente deve chamar **IEnumConnectionPoints:: Release** quando o enumerador não for mais necessário. Além disso, cada ponto de conexão é um objeto com uma contagem de referência separada do objeto de conexão que o contém. Portanto, o cliente também deve chamar IConnectionPoint:: Release para cada ponto de conexão acessado por meio do enumerador ou por meio de [**FindConnectionPoint**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interfaces de objeto conectáveis](connectable-object-interfaces.md)
</dt> </dl>

 

 




