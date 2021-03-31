---
title: QueryInterface navegando em um objeto
description: QueryInterface navegando em um objeto
ms.assetid: 7dec015f-7609-40eb-a71e-f6e9c9b9f8ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dbd44d200bf0a992f47bc375d0782bdadacf6a3
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "104293705"
---
# <a name="queryinterface-navigating-in-an-object"></a>QueryInterface: navegando em um objeto

Depois que você tiver um ponteiro inicial para uma interface em um objeto, COM terá um mecanismo muito simples para descobrir se o objeto dá suporte a outra interface específica e, em caso afirmativo, obter um ponteiro para ele. (Para obter informações sobre como obter um ponteiro inicial para uma interface em um objeto, consulte [obtendo um ponteiro para um objeto](getting-a-pointer-to-an-object.md).) Esse mecanismo é o método [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) da interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) . Se o objeto der suporte à interface solicitada, o método deverá retornar um ponteiro para essa interface. Isso permite que um objeto navegue livremente pelas interfaces às quais um objeto dá suporte. **QueryInterface** separa a solicitação "você dá suporte a um determinado contrato?" do uso de alto desempenho desse contrato, depois que as negociações tiverem sido bem-sucedidas.

Quando um cliente recebe inicialmente o acesso a um objeto, esse cliente receberá, no mínimo, um ponteiro de interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) (a interface mais fundamental) por meio do qual ele pode controlar o tempo de vida do objeto — informando ao objeto quando ele é feito usando o objeto — e invocar [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)). O cliente é programado para perguntar a cada objeto que ele gerencia para executar algumas operações, mas a interface **IUnknown** não tem funções para essas operações. Em vez disso, essas operações são expressas por meio de outras interfaces. O cliente é, portanto, programado para negociar com objetos para essas interfaces. Especificamente, o cliente chamará **QueryInterface** para solicitar um objeto para uma interface por meio da qual o cliente pode invocar as operações desejadas.

Como o objeto implementa [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), ele tem a capacidade de aceitar ou rejeitar a solicitação. Se o objeto aceitar a solicitação do cliente, **QueryInterface** retornará um novo ponteiro para a interface solicitada para o cliente. Através desse ponteiro de interface, o cliente tem acesso aos métodos dessa interface. Se, por outro lado, o objeto rejeitar a solicitação do cliente, **QueryInterface** retornará um ponteiro nulo — um erro — e o cliente não terá nenhum ponteiro por meio do qual chamar as funções desejadas. Nesse caso, o cliente deve lidar normalmente com essa possibilidade. Por exemplo, suponha que um cliente tenha um ponteiro para a interface A em um objeto e solicite as interfaces B e C. suponha também que o objeto dá suporte à interface B, mas não dá suporte à interface C. O resultado é que o objeto retorna um ponteiro para B e relata que não há suporte para C.

Um ponto importante é que quando um objeto rejeita uma chamada para [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), é impossível para o cliente solicitar que o objeto execute as operações expressas por meio da interface solicitada. Um cliente deve ter um ponteiro de interface para invocar métodos nessa interface. Se o objeto se recusar a fornecer o ponteiro solicitado, o cliente deverá estar preparado para fazer isso sem, não fazendo o que pretendia fazer com esse objeto ou tentando fazer fallback em outra interface, talvez menos eficiente,. Esse recurso da funcionalidade COM funciona bem em comparação com outros sistemas orientados a objeto, nos quais você não pode saber se uma função funcionará até que você chame essa função, e mesmo assim, a falha de manipulação é incerta. **QueryInterface** fornece uma maneira confiável e consistente de saber se um objeto dá suporte a uma interface antes de tentar chamar seus métodos.

O método [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) também fornece uma maneira robusta e confiável para que um objeto indique que ele não dá suporte a um determinado contrato. Ou seja, se em uma chamada para **QueryInterface** , alguém solicitará um objeto "antigo" se ele der suporte a uma interface "nova" (uma, por exemplo, que foi inventado após o objeto antigo ter sido enviado), o objeto antigo será confiável, sem causar uma falha, responder "não". A tecnologia que dá suporte a esse é o algoritmo pelo qual IIDs são alocados. Embora isso possa parecer um ponto pequeno, é extremamente importante para a arquitetura geral do sistema, e a capacidade de consultar elementos herdados sobre a nova funcionalidade é, surpreendentemente, um recurso que não está presente na maioria das outras arquiteturas de objeto.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando e implementando IUnknown](using-and-implementing-iunknown.md)
</dt> </dl>

 

 




