---
description: A classe CMediaSample define um exemplo de mídia que dá suporte à interface IMediaSample2. O exemplo de mídia contém um ponteiro para um buffer de memória e várias propriedades armazenadas como variáveis de membro protegidas.
ms.assetid: 1e609c7c-3200-4540-904e-7659976df0da
title: Classe CMediaSample (Amfilter. h)
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
ms.openlocfilehash: 72cfe0f86ff6b6643f2f7793822899136a5c6454
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756624"
---
# <a name="cmediasample-class"></a>Classe CMediaSample

![hierarquia de classe CMediaSample](images/wutil03.png)

A `CMediaSample` classe define um exemplo de mídia que dá suporte à interface [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) . O exemplo de mídia contém um ponteiro para um buffer de memória e várias propriedades armazenadas como variáveis de membro protegidas.

Os exemplos de mídia são criados por alocadores, que são derivados da classe [**CBaseAllocator**](cbaseallocator.md) . O `CMediaSample` Construtor recebe um ponteiro para um buffer alocado, junto com o tamanho do buffer. Outras propriedades normalmente são definidas e recuperadas por meio de métodos de interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) .

O ciclo de vida de um exemplo de mídia difere do da maioria dos objetos COM:

-   O alocador contém uma lista de amostras gratuitas. Quando um filtro precisa de um novo exemplo, ele chama o método [**IMemAllocator:: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) do alocador. O alocador recupera um exemplo de sua lista gratuita, incrementa a contagem de referência da amostra e retorna um ponteiro para o exemplo.
-   Depois que o filtro é feito com o exemplo, ele chama o método **IUnknown:: Release** no exemplo. Ao contrário da maioria dos objetos, o exemplo não se exclui quando sua contagem de referência chega a zero. Em vez disso, ele chama o método [**IMemAllocator:: ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) no alocador e o alocador retorna o exemplo para sua lista gratuita.
-   O alocador não destrói amostras até que o método [**IMemAllocator::D ecommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) seja chamado.



| Variáveis de membro protegido                                           | Descrição                                                                                     |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**o \_ dwFlags**](cmediasample-m-dwflags.md)                         | Sinalizadores de propriedade de exemplo.                                                                          |
| [**\_dwTypeSpecificFlags m**](cmediasample-m-dwtypespecificflags.md) | Sinalizadores específicos de tipo.                                                                            |
| [**\_pBuffer m**](cmediasample-m-pbuffer.md)                         | Ponteiro para o buffer de memória que contém os dados de mídia.                                      |
| [**\_lActual m**](cmediasample-m-lactual.md)                         | Comprimento dos dados válidos no buffer, em bytes.                                               |
| [**\_cbBuffer m**](cmediasample-m-cbbuffer.md)                       | Tamanho do buffer, em bytes.                                                                   |
| [**\_pAllocator m**](cmediasample-m-pallocator.md)                   | Ponteiro para o alocador que criou este exemplo.                                              |
| [**\_pNext m**](cmediasample-m-pnext.md)                             | Aponta para o próximo exemplo na lista de exemplos do alocador.                                  |
| [**início do m \_**](cmediasample-m-start.md)                             | Hora de início do exemplo.                                                                              |
| [**\_fim m**](cmediasample-m-end.md)                                 | Hora de término da amostra.                                                                                |
| [**\_MediaStart m**](cmediasample-m-mediastart.md)                   | Hora de início da mídia.                                                                               |
| [**\_MediaEnd m**](cmediasample-m-mediaend.md)                       | Hora de parada da mídia.                                                                                |
| [**\_pMediaType m**](cmediasample-m-pmediatype.md)                   | Ponteiro para o tipo de mídia, se o tipo tiver sido alterado do exemplo anterior no fluxo de dados. |
| [**\_dwStreamId m**](cmediasample-m-dwstreamid.md)                   | Identificador de fluxo.                                                                              |
| Variáveis de membro público                                              | Descrição                                                                                     |
| [**\_cRef m**](cmediasample-m-cref.md)                               | Contagem de referência.                                                                                |
| Métodos públicos                                                       | Descrição                                                                                     |
| [**CMediaSample**](cmediasample-cmediasample.md)                    | Método de construtor.                                                                             |
| [**~ CMediaSample**](cmediasample--cmediasample.md)                 | Método destruidor. VirtuaisLUNs.                                                                     |
| [**Setpointr**](cmediasample-setpointer.md)                        | Define o ponteiro para o buffer de memória.                                                          |
| Métodos IMediaSample                                                 | Descrição                                                                                     |
| [**Getpointr**](cmediasample-getpointer.md)                        | Recupera um ponteiro de leitura/gravação para o buffer.                                                   |
| [**GetSize**](cmediasample-getsize.md)                              | Recupera o tamanho do buffer.                                                               |
| [**GetTime**](cmediasample-gettime.md)                              | Recupera os tempos de transmissão em que este exemplo deve começar e terminar.                        |
| [**SetTime**](cmediasample-settime.md)                              | Define os tempos de transmissão em que este exemplo deve iniciar e concluir.                             |
| [**IsSyncPoint**](cmediasample-issyncpoint.md)                      | Determina se o início do exemplo é um ponto de sincronização.                           |
| [**SetSyncPoint**](cmediasample-setsyncpoint.md)                    | Especifica se o início deste exemplo é um ponto de sincronização.                      |
| [**IsPreroll**](cmediasample-ispreroll.md)                          | Determina se este exemplo é uma amostra de preversão.                                                  |
| [**SetPreroll**](cmediasample-setpreroll.md)                        | Especifica se este exemplo é uma amostra de preversão.                                              |
| [**GetActualDataLength**](cmediasample-getactualdatalength.md)      | Recupera o comprimento dos dados válidos no buffer.                                           |
| [**SetActualDataLength**](cmediasample-setactualdatalength.md)      | Define o comprimento dos dados válidos no buffer.                                                |
| [**GetMediaType**](cmediasample-getmediatype.md)                    | Recupera o tipo de mídia, se o tipo de mídia for diferente do exemplo anterior.                   |
| [**SetMediaType**](cmediasample-setmediatype.md)                    | Define o tipo de mídia para o exemplo.                                                             |
| [**IsDiscontinuity**](cmediasample-isdiscontinuity.md)              | Determina se este exemplo representa uma interrupção no fluxo de dados.                                |
| [**SetDiscontinuity**](cmediasample-setdiscontinuity.md)            | Especifica se este exemplo representa uma interrupção no fluxo de dados.                            |
| [**GetMediaTime**](cmediasample-getmediatime.md)                    | Recupera os horários de mídia para este exemplo.                                                      |
| [**SetMediaTime**](cmediasample-setmediatime.md)                    | Define os horários de mídia para este exemplo.                                                           |
| Métodos IMediaSample2                                                | Descrição                                                                                     |
| [**GetProperties**](cmediasample-getproperties.md)                  | Recupera as propriedades do exemplo.                                                         |
| [**SetProperties**](cmediasample-setproperties.md)                  | Define as propriedades do exemplo.                                                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




