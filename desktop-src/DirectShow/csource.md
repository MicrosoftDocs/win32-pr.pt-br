---
description: A classe CSource é uma classe base para implementar filtros de origem. Um filtro derivado de CSource contém um ou mais Pins de saída derivados da classe CSourceStream. Cada pino de saída cria um thread de trabalho que envia amostras de mídia por push downstream.
ms.assetid: 25bd0334-4ad1-48ed-93f9-b36c13a280a3
title: Classe CSource (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6708ce38c826aae9ccb40d077972d267a20d5e22b4f67157000c4a62e92afa1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687506"
---
# <a name="csource-class"></a>Classe CSource

![hierarquia de classe CSource](images/source01.png)

A classe **CSource** é uma classe base para implementar filtros de origem. Um filtro derivado de **CSource** contém um ou mais Pins de saída derivados da classe [**CSourceStream**](csourcestream.md) . Cada pino de saída cria um thread de trabalho que envia amostras de mídia por push downstream.

> [!Note]  
> A classe **CSource** foi projetada para dar suporte ao modelo de push para o fluxo de dados. Essa classe não é recomendada para a criação de filtros de leitor de arquivo. Os leitores de arquivo devem dar suporte ao modelo de pull, por meio da interface [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) . para obter mais informações, consulte [Data Flow para os desenvolvedores de filtro](data-flow-for-filter-developers.md).

 



| Variáveis de membro protegido                     | Descrição                                                  |
|------------------------------------------------|--------------------------------------------------------------|
| [**\_iPins m**](csource-m-ipins.md)            | Número de Pins no filtro.                                |
| [**\_paStreams m**](csource-m-pastreams.md)    | Matriz de Pins.                                               |
| [**\_cStateLock m**](csource-m-cstatelock.md)  | Objeto de seção crítica que protege o estado do filtro.      |
| Métodos públicos                                 | Descrição                                                  |
| [**CSource**](csource-csource.md)             | Método de construtor.                                          |
| [**~ CSource**](csource--csource.md)           | Método destruidor.                                           |
| [**GetPinCount**](csource-getpincount.md)     | Recupera o número de Pins no filtro.                  |
| [**GetPin**](csource-getpin.md)               | Recupera um PIN.                                             |
| [**pStateLock**](csource--pstatelock.md)      | Recupera um ponteiro para o objeto de seção crítica do filtro. |
| [**AddPin**](csource-addpin.md)               | Adiciona um novo pino de saída ao filtro.                         |
| [**RemovePin**](csource-removepin.md)         | Remove um PIN especificado do filtro.                     |
| [**FindPinNumber**](csource-findpinnumber.md) | Recupera o número de um PIN especificado no filtro.       |
| Métodos IBaseFilter                            | Descrição                                                  |
| [**FindPin**](csource-findpin.md)             | Recupera o PIN com o identificador especificado.             |



 

## <a name="remarks"></a>Comentários

Para implementar um PIN de saída, faça o seguinte:

-   Derive uma classe de [**CSourceStream**](csourcestream.md).
-   Substitua o método [**CSourceStream:: GetMediaType**](csourcestream-getmediatype.md) e, possivelmente, o método [**CSourceStream:: CheckMediaType**](csourcestream-checkmediatype.md) , que valida os tipos de mídia para o PIN.
-   Implemente o método [**CBaseOutputPin::D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md) , que retorna os requisitos de buffer do PIN.
-   Implemente o método [**CSourceStream:: FillBuffer**](csourcestream-fillbuffer.md) , que preenche um buffer de exemplo de mídia com dados.

Para implementar o filtro, faça o seguinte:

-   Derive uma classe de **CSource**.
-   No construtor, crie um ou mais Pins de saída derivados de [**CSourceStream**](csourcestream.md). Os PINs se adicionam automaticamente ao filtro em seus métodos de construtor e se removem em seus métodos destruidores.

Para sincronizar o estado do filtro entre vários threads, chame o método [**CSource::P stateLock**](csource--pstatelock.md) . Esse método retorna um ponteiro para a seção crítica de estado de filtro. Use a classe [**CAutoLock**](cautolock.md) para manter a seção crítica. De um PIN, você pode acessar **pStateLock** da variável de membro [**CBasePin:: m \_ pFilter**](cbasepin-m-pfilter.md) do PIN, da seguinte maneira:


```
CAutoLock lock(m_pFilter->pStateLock());
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Source. h (incluir Fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Gravando filtros de origem](writing-source-filters.md)
</dt> </dl>

 

 




