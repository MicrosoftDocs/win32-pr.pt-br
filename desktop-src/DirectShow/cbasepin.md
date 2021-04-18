---
description: A classe CBasePin é uma classe abstrata que implementa um PIN genérico.
ms.assetid: 23b9a0e2-24fe-4ff9-b2bb-97630c237de9
title: Classe CBasePin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3ba7b3a85b512b2ad8d6e85aa38627a2abc68c21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753353"
---
# <a name="cbasepin-class"></a>Classe CBasePin

![hierarquia de classe CBasePin](images/filter02.png)

A `CBasePin` classe é uma classe abstrata que implementa um PIN genérico.

Os tópicos a seguir descrevem como usar essa classe:

-   [Processo de conexão do CBasePin](cbasepin-connection-process.md)
-   [Notificando CBasePin de alterações de estado de filtro](notifying-cbasepin-of-filter-state-changes.md)
-   [Derivando de CBasePin](deriving-from-cbasepin.md)



| Variáveis de membro protegido                                               | Descrição                                                                                                |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**\_pname m**](cbasepin-m-pname.md)                                     | Nome do PIN.                                                                                                  |
| [**m \_ conectado**](cbasepin-m-connected.md)                             | Ponteiro para o PIN que está conectado a este pin.                                                          |
| [**Dir. de m \_**](cbasepin-m-dir.md)                                         | Direção do PIN.                                                                                      |
| [**\_pLock m**](cbasepin-m-plock.md)                                     | Ponteiro para um objeto de seção crítica.                                                                      |
| [**\_bRunTimeError m**](cbasepin-m-bruntimeerror.md)                     | Sinalizador que indica se ocorreu um erro em tempo de execução.                                                 |
| [**\_bCanReconnectWhenActive m**](cbasepin-m-bcanreconnectwhenactive.md) | Sinalizador que indica se o PIN dá suporte à reconexão dinâmica.                                         |
| [**\_bTryMyTypesFirst m**](cbasepin-m-btrymytypesfirst.md)               | Sinalizador que indica se o PIN tenta seus próprios tipos de mídia preferenciais antes daqueles do PIN de recebimento. |
| [**\_pFilter m**](cbasepin-m-pfilter.md)                                 | Ponteiro para o filtro que criou o PIN.                                                                |
| [**\_pQSink m**](cbasepin-m-pqsink.md)                                   | Ponteiro para o objeto que manipula as mensagens de qualidade.                                                       |
| [**\_TypeVersion m**](cbasepin-m-typeversion.md)                         | Versão atual do conjunto de tipos de mídia preferenciais.                                                       |
| [**m \_ MT**](cbasepin-m-mt.md)                                           | Tipo de mídia para a conexão do PIN atual.                                                                 |
| [**\_tStart m**](cbasepin-m-tstart.md)                                   | Hora de início do segmento.                                                                                        |
| [**\_tStop m**](cbasepin-m-tstop.md)                                     | Hora de parada do segmento.                                                                                         |
| [**\_drate m**](cbasepin-m-drate.md)                                     | Taxa de segmento.                                                                                              |
| Métodos Protegidos                                                        | Descrição                                                                                                |
| [**DisplayPinInfo**](cbasepin-displaypininfo.md)                        | Rastreia uma conexão de PIN durante a depuração.                                                                  |
| [**DisplayTypeInfo**](cbasepin-displaytypeinfo.md)                      | Exibe informações de tipo de mídia durante a depuração.                                                          |
| [**AttemptConnection**](cbasepin-attemptconnection.md)                  | Conecta-se a outro PIN usando um tipo de mídia especificado.                                                      |
| [**TryMediaTypes**](cbasepin-trymediatypes.md)                          | Dada uma lista de tipos de mídia, o tenta concluir uma conexão usando um desses tipos.                      |
| [**AgreeMediaType**](cbasepin-agreemediatype.md)                        | Procura um tipo de mídia para fazer uma conexão de PIN.                                                        |
| [**DisconnectInternal**](cbasepin-disconnectinternal.md)                | Interrompe a conexão do PIN atual.                                                                         |
| Métodos públicos                                                           | Descrição                                                                                                |
| [**CBasePin**](cbasepin-cbasepin.md)                                    | Método de construtor.                                                                                        |
| [**~ CBasePin**](cbasepin--cbasepin.md)                                 | Método destruidor. VirtuaisLUNs.                                                                                |
| [**IsConnected**](cbasepin-isconnected.md)                              | Determina se o PIN está conectado a outro PIN.                                                    |
| [**GetConnected**](cbasepin-getconnected.md)                            | Recupera o PIN que está conectado a este pin.                                                           |
| [**IsStopped**](cbasepin-isstopped.md)                                  | Determina se o filtro que contém este pin é interrompido.                                              |
| [**GetMediaTypeVersion**](cbasepin-getmediatypeversion.md)              | Recupera um número de versão para o conjunto de tipos de mídia preferenciais. VirtuaisLUNs.                                  |
| [**IncrementTypeVersion**](cbasepin-incrementtypeversion.md)            | Incrementa o número de versão no conjunto de tipos de mídia preferenciais.                                         |
| [**Activo**](cbasepin-active.md)                                        | Notifica o PIN de que o filtro está ativo agora. VirtuaisLUNs.                                                   |
| [**Inativo**](cbasepin-inactive.md)                                    | Notifica o PIN de que o filtro não está mais ativo. VirtuaisLUNs.                                             |
| [**Executar**](cbasepin-run.md)                                              | Notifica o PIN de que o filtro agora está em execução. VirtuaisLUNs.                                                  |
| [**SetMediaType**](cbasepin-setmediatype.md)                            | Define o tipo de mídia para a conexão. VirtuaisLUNs.                                                           |
| [**CheckConnect**](cbasepin-checkconnect.md)                            | Determina se uma conexão de PIN é adequada. VirtuaisLUNs.                                                  |
| [**BreakConnect**](cbasepin-breakconnect.md)                            | Libera o PIN de uma conexão. VirtuaisLUNs.                                                               |
| [**CompleteConnect**](cbasepin-completeconnect.md)                      | Conclui uma conexão com outro PIN. VirtuaisLUNs.                                                            |
| [**GetMediaType**](cbasepin-getmediatype.md)                            | Recupera um tipo de mídia preferencial, por valor de índice. VirtuaisLUNs.                                                 |
| [**CurrentStopTime**](cbasepin-currentstoptime.md)                      | Recupera a hora de parada do segmento.                                                                           |
| [**CurrentStartTime**](cbasepin-currentstarttime.md)                    | Recupera a hora de início do segmento.                                                                          |
| [**CurrentRate**](cbasepin-currentrate.md)                              | Recupera a taxa de segmento.                                                                                |
| [**Nome**](cbasepin-name.md)                                            | Recupera o identificador do PIN.                                                                              |
| [**SetReconnectWhenActive**](cbasepin-setreconnectwhenactive.md)        | Especifica se o PIN dá suporte a reconexões dinâmicas.                                                  |
| [**CanReconnectWhenActive**](cbasepin-canreconnectwhenactive.md)        | Consulta se o PIN dá suporte a reconexões dinâmicas.                                                    |
| Métodos virtuais puros                                                     | Descrição                                                                                                |
| [**CheckMediaType**](cbasepin-checkmediatype.md)                        | Determina se o PIN aceita um tipo de mídia específico.                                                       |
| Métodos IPin                                                             | Descrição                                                                                                |
| [**Connect**](cbasepin-connect.md)                                      | Conecta o PIN a outro PIN.                                                                           |
| [**ReceiveConnection**](cbasepin-receiveconnection.md)                  | Aceita uma conexão de outro PIN.                                                                     |
| [**Desconectar**](cbasepin-disconnect.md)                                | Interrompe a conexão do PIN atual.                                                                         |
| [**Conectado a**](cbasepin-connectedto.md)                              | Recupera o PIN conectado a este pin.                                                                   |
| [**ConnectionMediaType**](cbasepin-connectionmediatype.md)              | Recupera o tipo de mídia para a conexão do PIN atual, se houver.                                           |
| [**QueryPinInfo**](cbasepin-querypininfo.md)                            | Recupera informações sobre o PIN.                                                                       |
| [**QueryDirection**](cbasepin-querydirection.md)                        | Recupera a direção do PIN (entrada ou saída).                                                      |
| [**QueryId**](cbasepin-queryid.md)                                      | Recupera o identificador do PIN.                                                                              |
| [**QueryAccept**](cbasepin-queryaccept.md)                              | Determina se o PIN aceita um tipo de mídia especificado.                                                 |
| [**EnumMediaTypes**](cbasepin-enummediatypes.md)                        | Enumera os tipos de mídia preferenciais do PIN.                                                                |
| [**QueryInternalConnections**](cbasepin-queryinternalconnections.md)    | Recupera os PINs que estão conectados internamente a esse PIN (dentro do filtro).                          |
| [**EndOfStream**](cbasepin-endofstream.md)                              | Notifica o PIN de que nenhum dado adicional é esperado.                                                      |
| [**NewSegment**](cbasepin-newsegment.md)                                | Notifica o PIN que as amostras de mídia recebidas após essa chamada são agrupadas como um segmento.                     |
| Métodos IQualityControl                                                  | Descrição                                                                                                |
| [**Notificar**](cbasepin-notify.md)                                        | Notifica o PIN de que uma alteração de qualidade é solicitada.                                                       |
| [**SetSink**](cbasepin-setsink.md)                                      | Define um Gerenciador de qualidade externo.                                                                          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




