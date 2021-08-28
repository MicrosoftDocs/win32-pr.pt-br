---
description: A classe CBasePin é uma classe abstrata que implementa um pin genérico.
ms.assetid: 23b9a0e2-24fe-4ff9-b2bb-97630c237de9
title: Classe CBasePin (Amfilter.h)
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
ms.openlocfilehash: 55f697d6ff1a2bd3ebac77a77d8ba98321f29d09a75181b52e8ef08b03eed682
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056187"
---
# <a name="cbasepin-class"></a>Classe CBasePin

![Hierarquia de classes cbasepin](images/filter02.png)

A `CBasePin` classe é uma classe abstrata que implementa um pino genérico.

Os tópicos a seguir descrevem como usar essa classe:

-   [Processo de conexão do CBasePin](cbasepin-connection-process.md)
-   [Notificando o CBasePin sobre alterações de estado do filtro](notifying-cbasepin-of-filter-state-changes.md)
-   [Derivando de CBasePin](deriving-from-cbasepin.md)



| Variáveis de membro protegidas                                               | Descrição                                                                                                |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**m \_ pName**](cbasepin-m-pname.md)                                     | Nome do pino.                                                                                                  |
| [**m \_ Conectado**](cbasepin-m-connected.md)                             | Ponteiro para o pino que está conectado a esse pino.                                                          |
| [**m \_ dir**](cbasepin-m-dir.md)                                         | Direção do pino.                                                                                      |
| [**m \_ pLock**](cbasepin-m-plock.md)                                     | Ponteiro para um objeto de seção crítico.                                                                      |
| [**m \_ bRunTimeError**](cbasepin-m-bruntimeerror.md)                     | Sinalizador que indica se ocorreu um erro em tempo de executar.                                                 |
| [**m \_ bCanReconnectWhenActive**](cbasepin-m-bcanreconnectwhenactive.md) | Sinalizador que indica se o pino dá suporte à reconexão dinâmica.                                         |
| [**m \_ bTryMyTypesFirst**](cbasepin-m-btrymytypesfirst.md)               | Sinalizador que indica se o pino tenta seus próprios tipos de mídia preferenciais antes daqueles do pino de recebimento. |
| [**m \_ pFilter**](cbasepin-m-pfilter.md)                                 | Ponteiro para o filtro que criou o pino.                                                                |
| [**m \_ pQSink**](cbasepin-m-pqsink.md)                                   | Ponteiro para o objeto que lida com mensagens de qualidade.                                                       |
| [**m \_ TypeVersion**](cbasepin-m-typeversion.md)                         | Versão atual do conjunto de tipos de mídia preferenciais.                                                       |
| [**m \_ mt**](cbasepin-m-mt.md)                                           | Tipo de mídia para a conexão de pino atual.                                                                 |
| [**m \_ tStart**](cbasepin-m-tstart.md)                                   | Hora de início do segmento.                                                                                        |
| [**m \_ tStop**](cbasepin-m-tstop.md)                                     | Hora de parada do segmento.                                                                                         |
| [**m \_ dRate**](cbasepin-m-drate.md)                                     | Taxa de segmento.                                                                                              |
| Métodos Protegidos                                                        | Descrição                                                                                                |
| [**DisplayPinInfo**](cbasepin-displaypininfo.md)                        | Rastreamentos de uma conexão de pino durante a depuração.                                                                  |
| [**DisplayTypeInfo**](cbasepin-displaytypeinfo.md)                      | Exibe informações de tipo de mídia durante a depuração.                                                          |
| [**AttemptConnection**](cbasepin-attemptconnection.md)                  | Conecta-se a outro pin usando um tipo de mídia especificado.                                                      |
| [**Trymediatypes**](cbasepin-trymediatypes.md)                          | Dada uma lista de tipos de mídia, tenta concluir uma conexão usando um desses tipos.                      |
| [**Agreemediatype**](cbasepin-agreemediatype.md)                        | Pesquisa um tipo de mídia para fazer uma conexão de pino.                                                        |
| [**DisconnectInternal**](cbasepin-disconnectinternal.md)                | Interrompe a conexão de pino atual.                                                                         |
| Métodos públicos                                                           | Descrição                                                                                                |
| [**Cbasepin**](cbasepin-cbasepin.md)                                    | Método do construtor.                                                                                        |
| [**~ CBasePin**](cbasepin--cbasepin.md)                                 | Método destruidor. Virtual.                                                                                |
| [**Isconnected**](cbasepin-isconnected.md)                              | Determina se o pino está conectado a outro pino.                                                    |
| [**GetConnected**](cbasepin-getconnected.md)                            | Recupera o pino que está conectado a esse pino.                                                           |
| [**IsStopped**](cbasepin-isstopped.md)                                  | Determina se o filtro que contém esse pino é interrompido.                                              |
| [**GetMediaTypeVersion**](cbasepin-getmediatypeversion.md)              | Recupera um número de versão para o conjunto de tipos de mídia preferenciais. Virtual.                                  |
| [**IncrementTypeVersion**](cbasepin-incrementtypeversion.md)            | Incrementa o número de versão no conjunto de tipos de mídia preferenciais.                                         |
| [**Ativo**](cbasepin-active.md)                                        | Notifica o pino de que o filtro agora está ativo. Virtual.                                                   |
| [**Inativo**](cbasepin-inactive.md)                                    | Notifica o pino de que o filtro não está mais ativo. Virtual.                                             |
| [**Executar**](cbasepin-run.md)                                              | Notifica o pino de que o filtro agora está em execução. Virtual.                                                  |
| [**Setmediatype**](cbasepin-setmediatype.md)                            | Define o tipo de mídia para a conexão. Virtual.                                                           |
| [**Checkconnect**](cbasepin-checkconnect.md)                            | Determina se uma conexão de pino é adequada. Virtual.                                                  |
| [**Breakconnect**](cbasepin-breakconnect.md)                            | Libera o pino de uma conexão. Virtual.                                                               |
| [**Completeconnect**](cbasepin-completeconnect.md)                      | Conclui uma conexão com outro pin. Virtual.                                                            |
| [**Getmediatype**](cbasepin-getmediatype.md)                            | Recupera um tipo de mídia preferencial, por valor de índice. Virtual.                                                 |
| [**CurrentStopTime**](cbasepin-currentstoptime.md)                      | Recupera o tempo de parada do segmento.                                                                           |
| [**CurrentStartTime**](cbasepin-currentstarttime.md)                    | Recupera a hora de início do segmento.                                                                          |
| [**Taxa de Atual**](cbasepin-currentrate.md)                              | Recupera a taxa de segmento.                                                                                |
| [**Nome**](cbasepin-name.md)                                            | Recupera o identificador do PIN.                                                                              |
| [**SetReconnectWhenActive**](cbasepin-setreconnectwhenactive.md)        | Especifica se o PIN dá suporte a reconexões dinâmicas.                                                  |
| [**CanReconnectWhenActive**](cbasepin-canreconnectwhenactive.md)        | Consulta se o PIN dá suporte a reconexões dinâmicas.                                                    |
| Métodos virtuais puros                                                     | Descrição                                                                                                |
| [**CheckMediaType**](cbasepin-checkmediatype.md)                        | Determina se o PIN aceita um tipo de mídia específico.                                                       |
| Métodos IPin                                                             | Descrição                                                                                                |
| [**Conectar**](cbasepin-connect.md)                                      | Conecta o PIN a outro PIN.                                                                           |
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
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




