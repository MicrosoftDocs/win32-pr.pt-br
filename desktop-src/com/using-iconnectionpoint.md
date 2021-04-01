---
title: Usando IConnectionPoint
description: Usando IConnectionPoint
ms.assetid: afd50b84-1fd6-47ad-a3ef-e8b4a725b72b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe7aa758ec1bd40233b1cc41a6c375ed296fc167
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104008391"
---
# <a name="using-iconnectionpoint"></a>Usando IConnectionPoint

Quando o cliente tem um ponteiro para um ponto de conexão, ele pode executar as seguintes operações, conforme expresso por meio de [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint):

-   Primeiro, [**IConnectionPoint:: GetConnectionInterface**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-getconnectioninterface) recupera a interface de saída IID suportada pelo ponto de conexão. Quando usado em conjunto com [**IEnumConnectionPoints**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnectionpoints), esse método permite que o cliente examine a IIDs de todas as interfaces de saída com suporte no objeto conectável.
-   Em segundo lugar, um cliente pode navegar do ponto de conexão de volta para a interface [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) do objeto de conexão por meio do método [**IConnectionPoint:: GetConnectionPointContainer**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-getconnectionpointcontainer) .
-   Em terceiro lugar, os métodos mais interessantes para o cliente são [**IConnectionPoint:: Advise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise) e [**IConnectionPoint:: Unadvise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-unadvise). Quando um cliente deseja conectar seu próprio objeto de coletor ao objeto que pôde ser conectado, o cliente passa o ponteiro [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) do coletor (ou qualquer outro ponteiro de interface no mesmo objeto) para **aconselhar**. O ponto de conexão consulta o coletor para a interface de saída específica esperada. Se essa interface estiver disponível no coletor, o ponto de conexão armazenará o ponteiro de interface. A partir desse ponto até que **Unadvise** seja chamado, o objeto conectável fará chamadas para o coletor por meio dessa interface quando ocorrerem eventos. Para desconectar o coletor do ponto de conexão, o cliente passa uma chave retornada de **Advise** para o método **Unadvise** . **Unadvise** deve chamar [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) na interface do coletor.
-   Por fim, um cliente pode solicitar a um ponto de conexão para enumerar todas as conexões a ele que existem por meio de [**IConnectionPoint:: EnumConnections**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-enumconnections). Esse método cria um objeto enumerador (com uma contagem de referência separada) retornando um ponteiro [**IEnumConnections**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnections) para ele. O cliente deve chamar [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) quando o enumerador não for mais necessário. Além disso, o enumerador retorna uma série de estruturas [**CONNECTDATA**](/windows/win32/api/ocidl/ns-ocidl-connectdata) , uma para cada conexão. Cada estrutura descreve uma conexão usando o ponteiro [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) do coletor, bem como a chave de conexão retornada originalmente de [**Advise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise). Quando concluídos com esses ponteiros de interface do coletor, o cliente deve chamar **Release** em cada ponteiro retornado em uma estrutura **CONNECTDATA** .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interfaces de objeto conectáveis](connectable-object-interfaces.md)
</dt> </dl>

 

 