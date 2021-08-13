---
title: WINBIO_PRESENCE estrutura (Tipos \_ Winbio.h)
description: Contém informações sobre a presença de um indivíduo cuja presença está sendo monitorada.
ms.assetid: 810D452E-DDFA-4AB2-AEFB-0C170C0C18D4
keywords:
- WINBIO_PRESENCE estrutura Windows API do Biometric Framework
- PWINBIO_PRESENCE ponteiro de estrutura Windows API do Biometric Framework
topic_type:
- apiref
api_name:
- WINBIO_PRESENCE
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2671faaee7bc277f9389d7c993e4d511dac03db459755b40bf3f659ff5256a56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909574"
---
# <a name="winbio_presence-structure"></a>Estrutura WINBIO \_ PRESENCE

Contém informações sobre a presença de um indivíduo cuja presença está sendo monitorada.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _WINBIO_PRESENCE {
  WINBIO_BIOMETRIC_TYPE      Factor;
  WINBIO_BIOMETRIC_SUBTYPE   SubFactor;
  HRESULT                    Status;
  WINBIO_REJECT_DETAIL       RejectDetail;
  WINBIO_IDENTITY            Identity;
  ULONGLONG                  TrackingId;
  WINBIO_PROTECTION_TICKET   Ticket;
  WINBIO_PRESENCE_PROPERTIES Properties;
} WINBIO_PRESENCE, *PWINBIO_PRESENCE;
```



## <a name="members"></a>Membros

<dl> <dt>

**Fator**
</dt> <dd>

O fator biométrico usado para monitorar a presença do indivíduo.

</dd> <dt>

**Subfactor**
</dt> <dd>

O qualificador biométrico do subfator para o fator biométrico usado para monitorar a presença do indivíduo.

</dd> <dt>

**Status**
</dt> <dd>

O status do procedimento de identificação para o indivíduo.

</dd> <dt>

**RejectDetail**
</dt> <dd>

Informações adicionais sobre a falha ao reconhecer um indivíduo, incluindo comentários que explicam como corrigir a falha.

</dd> <dt>

**Identidade**
</dt> <dd>

A identidade do indivíduo cuja presença está sendo monitorada, depois que esse indivíduo tiver sido identificado.

</dd> <dt>

**TrackingId**
</dt> <dd>

Um inteiro que é gerado pelo adaptador e identifica exclusivamente o indivíduo. O identificador de rastreamento que o adaptador atribui a um indivíduo específico tem a garantia de ser constante, desde que essa pessoa permaneça no quadro da câmera.

</dd> <dt>

**Ticket**
</dt> <dd>

Reservado. Definido como 0 pelo adaptador.

</dd> <dt>

**Propriedades**
</dt> <dd>

Informações específicas do fator sobre a posição de um indivíduo.

</dd> </dl>

## <a name="remarks"></a>Comentários

A [**função EngineAdapterIdentifyAll**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_all_fn) cria uma matriz de estruturas **\_ WINBIO PRESENCE** e envia essa matriz para o serviço biométrico. O serviço biométrico usa a matriz para atualizar seu modelo interno de humanos próximo ao computador.

Dependendo dos resultados dessa atualização, o serviço biométrico pode gerar uma estrutura [**WINBIO \_ ASYNC \_ RESULT**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) para a [**função WinBioMonitorPresence**](/windows/desktop/api/winbio/nf-winbio-winbiomonitorpresence) para clientes com monitores de presença ativos. O **RESULTADO \_ ASSÍNCRONO \_ DO WINBIO. O** membro de operação da estrutura contém **WINBIO \_ OPERATION MONITOR \_ \_ PRESENCE** e **o WINBIO \_ ASYNC \_ RESULT. O membro Parameters.MonitorPresence.ChangeType** fornece informações adicionais sobre o estado do indivíduo.

Quando um indivíduo associado pelo adaptador de mecanismo a um identificador de rastreamento específico aparece no fluxo de entrada pela primeira vez, o serviço biométrico gera uma estrutura [**WINBIO \_ ASYNC \_ RESULT**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) do lado do cliente em que o **WINBIO \_ ASYNC \_ RESULT. O membro Parameters.MonitorPresence.ChangeType** é **WINBIO \_ CHANGE TYPE \_ \_ ARRIVAL.** Essa estrutura é enviada à função de retorno de chamada do aplicativo ou à fila de mensagens do aplicativo antes de qualquer outra estrutura **WINBIO \_ ASYNC \_ RESULT** em que **o WINBIO \_ ASYNC \_ RESULT. Parameters.MonitorPresence.PresenceArray** inclui uma estrutura **WINBIO \_ PRESENCE** com o mesmo valor para **WINBIO \_ PRESENCE. TrackingId**.

As seguintes combinações de valores na matriz de estruturas **WINBIO \_ PRESENCE** que o **\_ WINBIO ASYNC \_ RESULT. O membro Parameters.MonitorPresence.PresenceArray** indica tipos específicos de alterações no estado de um indivíduo.

-   Quando um indivíduo está visível no quadro da câmera, mas o mecanismo ainda está tentando identificar o indivíduo, os membros da estrutura **WINBIO \_ PRESENCE** têm os valores na tabela a seguir.

    

    | Membro            | Valor                                                    |
    |-------------------|----------------------------------------------------------|
    | **TrackingId**    | Um inteiro que identifica o indivíduo para o mecanismo. |
    | **Status**        | **S \_ OK**                                                |
    | **Identity.Type** | **TIPO \_ DE ID \_ WINBIO \_ NULL**                               |

    

     

    Nesse caso, o serviço biométrico estende o tempo de expiração para o indivíduo e não gera uma estrutura [**WINBIO \_ ASYNC \_ RESULT**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) do lado do cliente para o identificador de acompanhamento em que o **WINBIO \_ ASYNC \_ RESULT. O membro Parameters.MonitorPresence.ChangeType** é **WINBIO \_ CHANGE TYPE \_ \_ RECOGNIZE.**

    Na primeira vez que uma estrutura [**WINBIO \_ ASYNC \_ RESULT**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) inclui **a** estrutura WINBIO PRESENCE em que o membro **Status** é **S \_ OK** e o membro **Identity.Type** é **WINBIO \_ ID \_ TYPE \_ NULL** depois que uma ou mais estruturas **WINBIO \_ ASYNC \_ RESULT** incluíram uma estrutura **WINBIO \_ PRESENCE** com um membro status de WINBIO E BAD **\_** CAPTURE , o monitor de presença gera uma única estrutura **\_ WINBIO ASYNC \_ RESULT** para o identificador de acompanhamento em que o RESULTADO ASYNC **\_ \_ \_** **\_ WINBIO. \_ O membro Parameters.MonitorPresence.ChangeType** é **WINBIO \_ CHANGE TYPE \_ \_ TRACK.** Essa **estrutura WINBIO \_ ASYNC \_ RESULT** em que **o \_ WINBIO ASYNC \_ RESULT. O membro Parameters.MonitorPresence.ChangeType** é **WINBIO \_ CHANGE TYPE \_ \_ TRACK** informa ao cliente que o problema que causou o erro **WINBIO E BAD \_ \_ \_ CAPTURE** foi resolvido. Para obter mais informações sobre as circunstâncias em que uma estrutura **WINBIO \_ PRESENCE** tem o Membro de **Status** de **WINBIO \_ E BAD \_ \_ CAPTURE**, consulte a descrição sobre como o adaptador de mecanismo fornece comentários para o usuário corrigir falhas de reconhecimento posteriormente nesses Comentários.

-   Quando um indivíduo está visível no quadro da câmera, mas o mecanismo ainda está tentando identificar o indivíduo e deseja fornecer comentários ao usuário sobre como corrigir uma falha de reconhecimento, os membros da estrutura **WINBIO \_ PRESENCE** têm os valores na tabela a seguir.

    

    | Membro                                                                                                      | Valor                                                                         |
    |-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
    | **TrackingId**                                                                                              | Um inteiro que identifica o indivíduo para o mecanismo.                      |
    | **Status**                                                                                                  | **WINBIO \_ E \_ CAPTURA \_ RUIM**                                                   |
    | **Identity.Type**                                                                                           | **TIPO \_ DE ID \_ WINBIO \_ NULL**                                                    |
    | **Properties.FacialFeatures.BoundingBox**, se o valor de **Factor** for **WINBIO \_ TYPE FACIAL \_ \_ FEATURES** | O local do rosto do indivíduo dentro do quadro da câmera.           |
    | **Properties.Iris.BoundingBox**, se o valor de **Factor** for **WINBIO \_ TYPE \_ IRIS**                       | O local da íris ou íris do indivíduo dentro do quadro da câmera. |

    

     

    Nesse caso, o serviço biométrico estende o tempo de expiração para o indivíduo e gera uma estrutura [**WINBIO \_ ASYNC \_ RESULT**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) para o identificador de rastreamento em que o **WINBIO \_ ASYNC \_ RESULT. O membro Parameters.MonitorPresence.ChangeType** é **WINBIO \_ CHANGE TYPE \_ \_ TRACK.**

-   Quando um indivíduo está visível no quadro da câmera e o adaptador do mecanismo determina a identidade do indivíduo, os membros da estrutura **WINBIO \_ PRESENCE** têm os valores na tabela a seguir.

    

    | Membro                        | Valor                                                    |
    |-------------------------------|----------------------------------------------------------|
    | **TrackingId**                | Um inteiro que identifica o indivíduo para o mecanismo. |
    | **Status**                    | **S \_ OK**                                                |
    | **Identity.Type**             | **SID DE \_ TIPO DE ID \_ \_ DO WINBIO**                                |
    | **Identity.Value.AccountSid** | O SID (identificador de segurança) do indivíduo.         |

    

     

    Nesse caso, o serviço biométrico associa o identificador de acompanhamento ao SID para o indivíduo e gera uma estrutura [**WINBIO \_ ASYNC \_ RESULT**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) do lado do cliente para o identificador de acompanhamento em que o **RESULTADO \_ ASYNC \_ WINBIO. O membro Parameters.MonitorPresence.ChangeType** é **WINBIO \_ CHANGE TYPE \_ \_ RECOGNIZE.** O serviço biométrico não gera estruturas **adicionais WINBIO \_ ASYNC \_ RESULT** do lado do cliente para o identificador de rastreamento, a menos que o indivíduo saia do quadro da câmera.

-   Quando um indivíduo está visível no quadro da câmera, mas o adaptador do mecanismo determina com certeza que o indivíduo não está inscrito, os membros da estrutura **WINBIO \_ PRESENCE** têm os valores na tabela a seguir.

    

    | Membro            | Valor                                                    |
    |-------------------|----------------------------------------------------------|
    | **TrackingId**    | Um inteiro que identifica o indivíduo para o mecanismo. |
    | **Status**        | **WINBIO \_ E \_ \_ ID DESCONHECIDA**                               |
    | **Identity.Type** | **TIPO \_ DE ID \_ WINBIO \_ NULL**                               |

    

     

    Nesse caso, o serviço biométrico associa o identificador de acompanhamento do indivíduo a uma identidade DE UNKNOWN e gera uma estrutura [**WINBIO \_ ASYNC \_ RESULT**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) do lado do cliente para o identificador de acompanhamento em que o **RESULTADO \_ ASYNC \_ WINBIO. O membro Parameters.MonitorPresence.ChangeType** é **WINBIO \_ CHANGE TYPE \_ \_ RECOGNIZE.** O serviço biométrico não gera estruturas **adicionais WINBIO \_ ASYNC \_ RESULT** do lado do cliente para o identificador de rastreamento, a menos que o indivíduo saia do quadro da câmera.

Quando um indivíduo associado pelo adaptador de mecanismo a um identificador de acompanhamento específico deixa o quadro da câmera e para de aparecer nos valores que a função [**EngineAdapterIdentifyAll**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_all_fn) retorna, o identificador de acompanhamento eventualmente expira. Quando o identificador de rastreamento expira, o serviço biométrico gera uma estrutura [**WINBIO \_ ASYNC \_ RESULT**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) do lado do cliente em que o **WINBIO \_ ASYNC \_ RESULT. O membro Parameters.MonitorPresence.ChangeType** é **WINBIO \_ CHANGE TYPE \_ \_ DEPART.** O adaptador do mecanismo pode impedir que o serviço biométrico gere essa estrutura com o valor **DEPART WINBIO \_ CHANGE \_ TYPE \_** incluindo uma estrutura **WINBIO \_ PRESENCE** na matriz retornada por **EngineAdapterIdentifyAll,** em que a **WINBIO PRESENCE \_ retorna. O** membro de status **é S \_ OK** e **WINBIO \_ PRESENCE. O membro Identity.Type** é **WINBIO \_ ID \_ TYPE \_ NULL,** conforme descrito anteriormente nestes Comentários. Essa ação estende o tempo de expiração para o identificador de rastreamento sem causar nenhuma atividade do lado do cliente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 10 somente aplicativos da área de trabalho\]<br/>                                                                                                                              |
| Servidor mínimo com suporte<br/> | \[Windows Server 2016 somente aplicativos da área de trabalho\]<br/>                                                                                                                     |
| parâmetro<br/>                   | <dl> <dt>Winbio \_ types.h (inclua Winbio.h para aplicativos cliente ou \_ adaptadores Winbio.h para adaptadores)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**RESULTADO \_ ASSÍNCRONO DO \_ WINBIO**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result)
</dt> <dt>

[**WinBioMonitorPresence**](/windows/desktop/api/winbio/nf-winbio-winbiomonitorpresence)
</dt> <dt>

[**EngineAdapterIdentifyAll**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_all_fn)
</dt> </dl>

 

 





