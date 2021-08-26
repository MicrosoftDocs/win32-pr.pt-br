---
description: A classe CMediaSample define um exemplo de mídia que dá suporte à interface IMediaSample2. O exemplo de mídia contém um ponteiro para um buffer de memória e várias propriedades armazenadas como variáveis de membro protegidas.
ms.assetid: 1e609c7c-3200-4540-904e-7659976df0da
title: Classe CMediaSample (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7b0b27c8878a2841eeecb3bc1ae24bdcc43d056c57a881596179f5d2bd990fcd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084486"
---
# <a name="cmediasample-class"></a>Classe CMediaSample

![Hierarquia de classes cmediasample](images/wutil03.png)

A `CMediaSample` classe define um exemplo de mídia que dá suporte à interface [**IMediaSample2.**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) O exemplo de mídia contém um ponteiro para um buffer de memória e várias propriedades armazenadas como variáveis de membro protegidas.

Os exemplos de mídia são criados por alocadores, que são derivados da [**classe CBaseAllocator.**](cbaseallocator.md) O `CMediaSample` construtor recebe um ponteiro para um buffer alocado, juntamente com o tamanho do buffer. Outras propriedades normalmente são definidas e recuperadas por meio de métodos de interface [**IMediaSample.**](/windows/desktop/api/Strmif/nn-strmif-imediasample)

O ciclo de vida de um exemplo de mídia é diferente da maioria dos objetos COM:

-   O alocador contém uma lista de exemplos gratuitos. Quando um filtro precisa de um novo exemplo, ele chama o método [**IMemAllocator::GetBuffer do**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) alocador. O alocador recupera um exemplo de sua lista livre, incrementa a contagem de referência da amostra e retorna um ponteiro para a amostra.
-   Depois que o filtro é feito com o exemplo, ele chama o **método IUnknown::Release** no exemplo. Ao contrário da maioria dos objetos, o exemplo não se exclui quando sua contagem de referência atinge zero. Em vez disso, ele chama o método [**IMemAllocator::ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) no alocador e o alocador retorna o exemplo para sua lista livre.
-   O alocador não destrói amostras até que o [**método IMemAllocator::D ecommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) seja chamado.



| Variáveis de membro protegidas                                           | Descrição                                                                                     |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**m \_ dwFlags**](cmediasample-m-dwflags.md)                         | Sinalizadores de propriedade de exemplo.                                                                          |
| [**m \_ dwTypeSpecificFlags**](cmediasample-m-dwtypespecificflags.md) | Sinalizadores específicos do tipo.                                                                            |
| [**m \_ pBuffer**](cmediasample-m-pbuffer.md)                         | Ponteiro para o buffer de memória que contém os dados de mídia.                                      |
| [**m \_ lActual**](cmediasample-m-lactual.md)                         | Comprimento dos dados válidos no buffer, em bytes.                                               |
| [**m \_ cbBuffer**](cmediasample-m-cbbuffer.md)                       | Tamanho do buffer, em bytes.                                                                   |
| [**m \_ pAllocator**](cmediasample-m-pallocator.md)                   | Ponteiro para o alocador que criou este exemplo.                                              |
| [**m \_ pNext**](cmediasample-m-pnext.md)                             | Ponteiro para o próximo exemplo na lista de amostras do alocador.                                  |
| [**m \_ Iniciar**](cmediasample-m-start.md)                             | Hora de início de exemplo.                                                                              |
| [**m \_ End**](cmediasample-m-end.md)                                 | Hora de término de exemplo.                                                                                |
| [**m \_ MediaStart**](cmediasample-m-mediastart.md)                   | Hora de início da mídia.                                                                               |
| [**m \_ MediaEnd**](cmediasample-m-mediaend.md)                       | Hora de parada da mídia.                                                                                |
| [**m \_ pMediaType**](cmediasample-m-pmediatype.md)                   | Ponteiro para o tipo de mídia, se o tipo tiver sido alterado do exemplo anterior no fluxo de dados. |
| [**m \_ dwStreamId**](cmediasample-m-dwstreamid.md)                   | Identificador de fluxo.                                                                              |
| Variáveis de membro público                                              | Descrição                                                                                     |
| [**m \_ cRef**](cmediasample-m-cref.md)                               | Contagem de referência.                                                                                |
| Métodos públicos                                                       | Descrição                                                                                     |
| [**Cmediasample**](cmediasample-cmediasample.md)                    | Método do construtor.                                                                             |
| [**~ CMediaSample**](cmediasample--cmediasample.md)                 | Método destruidor. Virtual.                                                                     |
| [**SetPointer**](cmediasample-setpointer.md)                        | Define o ponteiro para o buffer de memória.                                                          |
| Métodos IMediaSample                                                 | Descrição                                                                                     |
| [**GetPointer**](cmediasample-getpointer.md)                        | Recupera um ponteiro de leitura/gravação para o buffer.                                                   |
| [**Getsize**](cmediasample-getsize.md)                              | Recupera o tamanho do buffer.                                                               |
| [**Gettime**](cmediasample-gettime.md)                              | Recupera os horários de fluxo nos quais este exemplo deve começar e concluir.                        |
| [**Settime**](cmediasample-settime.md)                              | Define os horários de fluxo nos quais este exemplo deve iniciar e concluir.                             |
| [**IsSyncPoint**](cmediasample-issyncpoint.md)                      | Determina se o início do exemplo é um ponto de sincronização.                           |
| [**SetSyncPoint**](cmediasample-setsyncpoint.md)                    | Especifica se o início deste exemplo é um ponto de sincronização.                      |
| [**IsPreroll**](cmediasample-ispreroll.md)                          | Determina se este exemplo é um exemplo de pré-roll.                                                  |
| [**SetPreroll**](cmediasample-setpreroll.md)                        | Especifica se este exemplo é um exemplo de pré-roll.                                              |
| [**GetActualDataLength**](cmediasample-getactualdatalength.md)      | Recupera o comprimento dos dados válidos no buffer.                                           |
| [**SetActualDataLength**](cmediasample-setactualdatalength.md)      | Define o comprimento dos dados válidos no buffer.                                                |
| [**Getmediatype**](cmediasample-getmediatype.md)                    | Recupera o tipo de mídia, se o tipo de mídia for diferente do exemplo anterior.                   |
| [**Setmediatype**](cmediasample-setmediatype.md)                    | Define o tipo de mídia para o exemplo.                                                             |
| [**IsDiscontinuity**](cmediasample-isdiscontinuity.md)              | Determina se este exemplo representa uma quebra no fluxo de dados.                                |
| [**SetDiscontinuity**](cmediasample-setdiscontinuity.md)            | Especifica se este exemplo representa uma quebra no fluxo de dados.                            |
| [**GetMediaTime**](cmediasample-getmediatime.md)                    | Recupera os tempos de mídia para este exemplo.                                                      |
| [**SetMediaTime**](cmediasample-setmediatime.md)                    | Define os tempos de mídia para este exemplo.                                                           |
| Métodos IMediaSample2                                                | Descrição                                                                                     |
| [**GetProperties**](cmediasample-getproperties.md)                  | Recupera as propriedades do exemplo.                                                         |
| [**SetProperties**](cmediasample-setproperties.md)                  | Define as propriedades do exemplo.                                                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




