---
title: Usando o IConnectionPoint
description: Usando o IConnectionPoint
ms.assetid: afd50b84-1fd6-47ad-a3ef-e8b4a725b72b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d2449be5f1711457807666e9e2068d13defd8437bedee93402f7b974d5298d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129418"
---
# <a name="using-iconnectionpoint"></a>Usando o IConnectionPoint

Quando o cliente tem um ponteiro para um ponto de conexão, ele pode executar as seguintes operações, conforme expresso por [**meio de IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint):

-   Primeiro, [**IConnectionPoint::GetConnectionInterface**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-getconnectioninterface) recupera a IID da interface de saída com suporte pelo ponto de conexão. Quando usado em conjunto com [**IEnumConnectionPoints**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnectionpoints), esse método permite que o cliente examine os IIDs de todas as interfaces de saída com suporte no objeto conectável.
-   Em segundo lugar, um cliente pode navegar do ponto de conexão de volta para a interface [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) do objeto conectável por meio do método [**IConnectionPoint::GetConnectionPointContainer.**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-getconnectionpointcontainer)
-   Em terceiro lugar, os métodos mais interessantes para o cliente [**são IConnectionPoint::Advise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise) e [**IConnectionPoint::Unadvise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-unadvise). Quando um cliente deseja conectar seu próprio objeto de sink ao objeto conectável, o cliente passa o ponteiro [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) do sink (ou qualquer outro ponteiro de interface no mesmo objeto) para **Avisar**. O ponto de conexão consulta o sink para a interface de saída específica esperada. Se essa interface estiver disponível no sink, o ponto de conexão armazenará o ponteiro da interface. Deste ponto até que **Unadvise** seja chamado, o objeto conectável fará chamadas ao sink por meio dessa interface quando ocorrerem eventos. Para desconectar o sink do ponto de conexão, o cliente passa uma chave retornada de **Advise** para o **método Unadvise.** **Unadvise deve** chamar [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) na interface do sink.
-   Por fim, um cliente pode solicitar que um ponto de conexão enumere todas as conexões a ele que existem por meio de [**IConnectionPoint::EnumConnections**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-enumconnections). Esse método cria um objeto enumerador (com uma contagem de referência separada) retornando um [**ponteiro IEnumConnections**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnections) para ele. O cliente deve chamar [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) quando o enumerador não for mais necessário. Além disso, o enumerador retorna uma série de estruturas [**CONNECTDATA,**](/windows/win32/api/ocidl/ns-ocidl-connectdata) uma para cada conexão. Cada estrutura descreve uma conexão usando o ponteiro [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) do sink, bem como a chave de conexão originalmente retornada de [**Aconselhar**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise). Quando terminar com esses ponteiros de interface do sink, o cliente deverá chamar **Release** em cada ponteiro retornado em uma **estrutura CONNECTDATA.**

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interfaces de objeto conectáveis](connectable-object-interfaces.md)
</dt> </dl>

 

 