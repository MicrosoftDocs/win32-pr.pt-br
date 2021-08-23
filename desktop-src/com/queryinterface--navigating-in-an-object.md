---
title: QueryInterface Navegando em um objeto
description: QueryInterface Navegando em um objeto
ms.assetid: 7dec015f-7609-40eb-a71e-f6e9c9b9f8ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdbb25f76f87b43f6fc4fc4d3a1a3eb65c19960942769818a83f176fc62f72c9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119611066"
---
# <a name="queryinterface-navigating-in-an-object"></a>QueryInterface: navegando em um objeto

Depois que você tiver um ponteiro inicial para uma interface em um objeto , o COM terá um mecanismo muito simples para descobrir se o objeto dá suporte a outra interface específica e, se for o caso, obter um ponteiro para ele. (Para obter informações sobre como obter um ponteiro inicial para uma interface em um objeto, consulte [Getting a Pointer to an Object](getting-a-pointer-to-an-object.md).) Esse mecanismo é o [**método QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) da interface [**IUnknown.**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) Se o objeto dá suporte à interface solicitada, o método deve retornar um ponteiro para essa interface. Isso permite que um objeto navegue livremente pelas interfaces às que um objeto dá suporte. **QueryInterface** separa a solicitação "Você dá suporte a um determinado contrato?" do uso de alto desempenho desse contrato depois que as negociações foram bem-sucedidas.

Quando um cliente inicialmente obtém acesso a um objeto, esse cliente receberá, no mínimo, um ponteiro de interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) (a interface mais fundamental) por meio do qual ele pode controlar o tempo de vida do objeto , dizendo ao objeto quando terminar de usar o objeto e [**invocando QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)). O cliente é programado para solicitar que cada objeto que ele gerencia execute algumas operações, mas a interface **IUnknown** não tem funções para essas operações. Em vez disso, essas operações são expressas por meio de outras interfaces. Portanto, o cliente é programado para negociar com objetos para essas interfaces. Especificamente, o cliente chamará **QueryInterface** para solicitar a um objeto uma interface por meio da qual o cliente pode invocar as operações desejadas.

Como o objeto implementa [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), ele tem a capacidade de aceitar ou rejeitar a solicitação. Se o objeto aceitar a solicitação do cliente, **QueryInterface** retornará um novo ponteiro para a interface solicitada para o cliente. Por meio desse ponteiro de interface, o cliente tem acesso aos métodos dessa interface. Se, por outro lado, o objeto rejeitar a solicitação do cliente, **QueryInterface** retornar um ponteiro nulo – um erro – e o cliente não tiver nenhum ponteiro por meio do qual chamar as funções desejadas. Nesse caso, o cliente deve lidar normalmente com essa possibilidade. Por exemplo, suponha que um cliente tenha um ponteiro para a interface A em um objeto e peça as interfaces B e C. Suponha também que o objeto dá suporte à interface B, mas não dá suporte à interface C. O resultado é que o objeto retorna um ponteiro para B e informa que não há suporte para C.

Um ponto importante é que, quando um objeto rejeita uma chamada para [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), é impossível para o cliente solicitar que o objeto execute as operações expressas por meio da interface solicitada. Um cliente deve ter um ponteiro de interface para invocar métodos nessa interface. Se o objeto se recusar a fornecer o ponteiro solicitado, o cliente deverá estar preparado para fazer sem, não fazendo o que ele pretendia fazer com esse objeto ou tentando fazer fall back em outra interface, talvez menos poderosa. Esse recurso da funcionalidade COM funciona bem em comparação com outros sistemas orientados a objeto nos quais você não pode saber se uma função funcionará até que você chame essa função e, mesmo assim, lidar com falhas não é seguro. **QueryInterface fornece** uma maneira confiável e consistente de saber se um objeto dá suporte a uma interface antes de tentar chamar seus métodos.

O [**método QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) também fornece uma maneira robusta e confiável para um objeto indicar que ele não dá suporte a um determinado contrato. Ou seja, se em uma chamada para **QueryInterface** perguntar a um objeto "antigo" se ele dá suporte a uma interface "nova" (uma, por exemplo, que foi desfeita depois que o objeto antigo foi enviado), o objeto antigo será confiável, sem causar uma falha, responder "não". A tecnologia que dá suporte a isso é o algoritmo pelo qual os IIDs são alocados. Embora isso possa parecer um ponto pequeno, é extremamente importante para a arquitetura geral do sistema e a capacidade de perguntar sobre os elementos herdados sobre a nova funcionalidade é, surpreendentemente, um recurso não presente na maioria das outras arquiteturas de objeto.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando e implementando IUnknown](using-and-implementing-iunknown.md)
</dt> </dl>

 

 




