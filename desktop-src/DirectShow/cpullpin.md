---
description: A classe CPullPin dá suporte a pinos de entrada que e pull de dados por meio da interface IAsyncReader.
ms.assetid: 33a6c342-3896-41f8-b32d-01db3eed003e
title: Classe CPullPin (Pullpin.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d70217fa60afdae3f588f98ecbe61a728ace6ec0b0d78859f55cd241cbc00e1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119330837"
---
# <a name="cpullpin-class"></a>Classe CPullPin

![Hierarquia de classes cpullpin](images/pulpin01.png)

A `CPullPin` classe fornece suporte para pinos de entrada que e pull de dados por meio da interface [**IAsyncReader.**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) Use essa classe se você estiver implementando um filtro que usa o modelo de pull para solicitar dados do filtro upstream. Para obter mais informações, consulte Data Flow no Filtro Graph e Modelo de Pull.

Essa classe não deriva de **CBasePin** nem implementa a interface [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) e alguns dos nomes de método estão em conflito com **IPin,** portanto, ele é melhor usado como um objeto auxiliar dentro de seu pin. Para usar essa classe, faça o seguinte:

1.  Derive uma classe auxiliar de `CPullPin` e derive uma classe de pino de entrada de **CBasePin.** Declare uma instância do objeto `CPullPin` como uma variável de membro da classe pin.
2.  Substitua o [**método CBasePin::CheckConnect**](cbasepin-checkconnect.md) para chamar [**CPullPin::Conexão**](cpullpin-connect.md). Esse método consulta o outro pin para **IAsyncReader.**
3.  Substitua o [**método CBasePin::BreakConnect**](cbasepin-breakconnect.md) para [**chamar CPullPin::D isconnect.**](cpullpin-disconnect.md)
4.  Substitua o [**método CBasePin::Active**](cbasepin-active.md) para chamar [**CPullPin::Active.**](cpullpin-active.md) Esse método inicia um thread de trabalho que recebe amostras do filtro upstream. Quando os pinos se conectam, você pode especificar se deseja que o thread de trabalho faça solicitações de leitura assíncronas ou síncronas.
5.  Substitua o [**método CBasePin::Inactive**](cbasepin-inactive.md) para chamar [**CPullPin::Inactive.**](cpullpin-inactive.md) Esse método desliga o thread de trabalho.
6.  Implemente o método [**CPullPin::Receive virtual puro**](cpullpin-receive.md) para processar amostras de entrada e entregar downstream.
7.  Para definir as posições stop e start ou para buscar o fluxo, chame o [**método CPullPin::Seek.**](cpullpin-seek.md) Esse método pausa o thread de trabalho e libera o grafo de filtro.
8.  Implemente os métodos [**CPullPin::EndOfStream**](cpullpin-endofstream.md), [**CPullPin::BeginFlush**](cpullpin-beginflush.md)e [**CPullPin::EndFlush**](cpullpin-endflush.md) puros, conforme descrito nos comentários desses métodos.
9.  Implemente o método [**CPullPin::OnError**](cpullpin-onerror.md) virtual puro para tratar erros de streaming.



| Variáveis de membro público                             | Description                                                                           |
|-----------------------------------------------------|---------------------------------------------------------------------------------------|
| [**m \_ pAlloc**](cpullpin-m-palloc.md)              | Ponteiro para a **interface IMemAllocator** do alocador de memória.                   |
| Métodos públicos                                      | Description                                                                           |
| [**Ativo**](cpullpin-active.md)                   | Cria um thread de trabalho que recebe dados do pino de saída.                          |
| [**AlignDown**](cpullpin-aligndown.md)             | Trunca um valor para um limite de alinhamento especificado.                                  |
| [**AlignUp**](cpullpin-alignup.md)                 | Eleva um valor até um limite de alinhamento especificado.                                  |
| [**Conectar**](cpullpin-connect.md)                 | Conclui uma conexão com o pino de saída.                                             |
| [**Cpullpin**](cpullpin-cpullpin.md)               | Método do construtor.                                                                   |
| [**~CPullPin**](cpullpin--cpullpin.md)             | Método destruidor. Virtual.                                                           |
| [**DecideAllocator**](cpullpin-decideallocator.md) | Negocia um alocador com o pino de saída. Virtual.                                 |
| [**Desconectar**](cpullpin-disconnect.md)           | Desembra a conexão com o pino de saída.                                             |
| [**Duração**](cpullpin-duration.md)               | Recupera a duração do fluxo.                                                 |
| [**Getreader**](cpullpin-getreader.md)             | Retorna um ponteiro para a interface [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) do pino de saída. |
| [**Inativo**](cpullpin-inactive.md)               | Desliga o thread de trabalho que recebe dados do pino de saída.                     |
| [**Seek**](cpullpin-seek.md)                       | Define as posições de início e parada do fluxo.                                      |
| Métodos virtuais puros                                | Description                                                                           |
| [**Beginflush**](cpullpin-beginflush.md)           | Informa o filtro de propriedade para liberar os filtros downstream.                            |
| [**Endflush**](cpullpin-endflush.md)               | Informa o filtro de propriedade para encerrar uma operação de liberação.                                   |
| [**Endofstream**](cpullpin-endofstream.md)         | Chamado depois que o objeto entrega o último exemplo.                                     |
| [**Onerror**](cpullpin-onerror.md)                 | Chamado se ocorrer um erro durante o streaming.                                           |
| [**Receber**](cpullpin-receive.md)                 | Chamado quando o objeto recebe um exemplo de mídia do pino de saída.                   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Pullpin.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



 

 




