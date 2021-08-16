---
description: A classe CPullPin fornece suporte para Pins de entrada que efetuam pull de dados por meio da interface IAsyncReader.
ms.assetid: 33a6c342-3896-41f8-b32d-01db3eed003e
title: Classe CPullPin (Pullpin. h)
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

![hierarquia de classe CPullPin](images/pulpin01.png)

A `CPullPin` classe fornece suporte para Pins de entrada que efetuam pull de dados por meio da interface [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) . Use essa classe se você estiver implementando um filtro que usa o modelo de pull para solicitar dados do filtro upstream. para obter mais informações, consulte Data Flow no filtro Graph e o modelo de Pull.

Essa classe não deriva de **CBasePin** ou implementa a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) , e alguns dos nomes de método conflitam com **IPin**, portanto, ele é melhor usado como um objeto auxiliar dentro do seu PIN. Para usar essa classe, faça o seguinte:

1.  Derive uma classe auxiliar de `CPullPin` e derive uma classe de pino de entrada de **CBasePin**. Declare uma instância do `CPullPin` objeto como uma variável de membro da classe PIN.
2.  substitua o método [**CBasePin:: CheckConnect**](cbasepin-checkconnect.md) para chamar [**CPullPin:: Conexão**](cpullpin-connect.md). Esse método consulta o outro PIN para **IAsyncReader**.
3.  Substitua o método [**CBasePin:: BreakConnect**](cbasepin-breakconnect.md) para chamar [**CPullPin::D isconnect**](cpullpin-disconnect.md).
4.  Substitua o método [**CBasePin:: active**](cbasepin-active.md) para chamar [**CPullPin:: active**](cpullpin-active.md). Esse método inicia um thread de trabalho que extrai amostras do filtro upstream. Quando os PINs se conectam, você pode especificar se deseja que o thread de trabalho faça solicitações de leitura assíncronas ou síncronas.
5.  Substitua o método [**CBasePin:: Inactive**](cbasepin-inactive.md) para chamar [**CPullPin:: Inactive**](cpullpin-inactive.md). Esse método desliga o thread de trabalho.
6.  Implemente o método puramente virtual [**CPullPin:: Receive**](cpullpin-receive.md) para processar amostras de entrada e entregá-las downstream.
7.  Para definir as posições de parar e iniciar ou para buscar o fluxo, chame o método [**CPullPin:: Seek**](cpullpin-seek.md) . Esse método pausa o thread de trabalho e libera o gráfico de filtro.
8.  Implemente os métodos puros [**CPullPin:: EndOfStream**](cpullpin-endofstream.md), [**CPullPin:: BeginFlush**](cpullpin-beginflush.md)e [**CPullPin:: EndFlush**](cpullpin-endflush.md) , conforme descrito nos comentários para esses métodos.
9.  Implemente o método puramente virtual [**CPullPin:: OnError**](cpullpin-onerror.md) para lidar com erros de streaming.



| Variáveis de membro público                             | Descrição                                                                           |
|-----------------------------------------------------|---------------------------------------------------------------------------------------|
| [**\_pAlloc m**](cpullpin-m-palloc.md)              | Ponteiro para a interface **IMemAllocator** do alocador de memória.                   |
| Métodos públicos                                      | Descrição                                                                           |
| [**Ativo**](cpullpin-active.md)                   | Cria um thread de trabalho que extrai dados do pino de saída.                          |
| [**AlignDown**](cpullpin-aligndown.md)             | Trunca um valor para um limite de alinhamento especificado.                                  |
| [**AlignUp**](cpullpin-alignup.md)                 | Arredonda um valor até um limite de alinhamento especificado.                                  |
| [**Conectar**](cpullpin-connect.md)                 | Conclui uma conexão com o pino de saída.                                             |
| [**CPullPin**](cpullpin-cpullpin.md)               | Método de construtor.                                                                   |
| [**~ CPullPin**](cpullpin--cpullpin.md)             | Método destruidor. VirtuaisLUNs.                                                           |
| [**DecideAllocator**](cpullpin-decideallocator.md) | Negocia um alocador com o pino de saída. VirtuaisLUNs.                                 |
| [**Desconectar**](cpullpin-disconnect.md)           | Beaks a conexão com o pino de saída.                                             |
| [**Permanência**](cpullpin-duration.md)               | Recupera a duração do fluxo.                                                 |
| [**GetReader**](cpullpin-getreader.md)             | Retorna um ponteiro para a interface [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) do pino de saída. |
| [**Inativo**](cpullpin-inactive.md)               | Desliga o thread de trabalho que efetua pull dos dados do pino de saída.                     |
| [**Seek**](cpullpin-seek.md)                       | Define as posições de início e de término do fluxo.                                      |
| Métodos virtuais puros                                | Descrição                                                                           |
| [**BeginFlush**](cpullpin-beginflush.md)           | Informa o filtro proprietário para liberar os filtros downstream.                            |
| [**EndFlush**](cpullpin-endflush.md)               | Informa o filtro proprietário para finalizar uma operação de liberação.                                   |
| [**EndOfStream**](cpullpin-endofstream.md)         | Chamado depois que o objeto entrega a última amostra.                                     |
| [**OnError**](cpullpin-onerror.md)                 | Chamado se ocorrer um erro durante o streaming.                                           |
| [**Recebe**](cpullpin-receive.md)                 | Chamado quando o objeto recebe um exemplo de mídia do pino de saída.                   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Pullpin. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




