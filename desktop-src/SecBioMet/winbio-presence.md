---
title: Estrutura de WINBIO_PRESENCE (WinBio \_ Types. h)
description: Contém informações sobre a presença de um indivíduo cuja presença está sendo monitorada.
ms.assetid: 810D452E-DDFA-4AB2-AEFB-0C170C0C18D4
keywords:
- API de Windows Biometric Framework de estrutura de WINBIO_PRESENCE
- Ponteiro de estrutura de PWINBIO_PRESENCE Windows Biometric Framework API
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
ms.openlocfilehash: 8a4a917f09f419ce8dd5eb59c9c277293261bffa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085611"
---
# <a name="winbio_presence-structure"></a>\_Estrutura de presença WINBIO

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

**Subfator**
</dt> <dd>

O qualificador de subfator biométrico para o fator biométrico usado para monitorar a presença do indivíduo.

</dd> <dt>

**Status**
</dt> <dd>

O status do procedimento de identificação para o indivíduo.

</dd> <dt>

**RejectDetail**
</dt> <dd>

Informações adicionais sobre a falha ao reconhecer um indivíduo, incluindo comentários que explica como corrigir a falha.

</dd> <dt>

**Identidade**
</dt> <dd>

A identidade do indivíduo cuja presença está sendo monitorada, uma vez que essa pessoa foi identificada.

</dd> <dt>

**TrackingId**
</dt> <dd>

Um inteiro que é gerado pelo adaptador e identifica exclusivamente o indivíduo. O identificador de rastreamento que o adaptador atribui a um indivíduo específico é garantido como constante, desde que essa pessoa permaneça no quadro da câmera.

</dd> <dt>

**Ticket**
</dt> <dd>

Reservado. Defina como 0 pelo adaptador.

</dd> <dt>

**Propriedades**
</dt> <dd>

Informações específicas do fator sobre a posição de um indivíduo.

</dd> </dl>

## <a name="remarks"></a>Comentários

A função [**EngineAdapterIdentifyAll**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_all_fn) cria uma matriz de estruturas de **\_ presença WINBIO** e envia essa matriz para o serviço biométrico. O serviço biométrico usa a matriz para atualizar seu modelo interno de seres humanos perto do computador.

Dependendo dos resultados dessa atualização, o serviço biométrico pode gerar uma estrutura de [**\_ \_ resultados assíncrona WINBIO**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) para a função [**WinBioMonitorPresence**](/windows/desktop/api/winbio/nf-winbio-winbiomonitorpresence) para qualquer cliente com monitores de presença ativos. O **\_ resultado assíncrono WINBIO \_ .** O membro de operação da estrutura contém a **\_ presença do \_ Monitor \_ de operação WINBIO** e o **\_ resultado assíncrono WINBIO \_ . Parameters. MonitorPresence. Altertype** membro fornece informações adicionais sobre o estado do indivíduo.

Quando um indivíduo que o adaptador de mecanismo associa a um determinado identificador de controle é exibido no fluxo de entrada pela primeira vez, o serviço biométrico gera uma estrutura [**de \_ \_ resultado assíncrono WINBIO**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) do lado do cliente em que o **\_ resultado assíncrono WINBIO \_ . Parameters. MonitorPresence. Altertype** membro é **WINBIO a chegada do \_ \_ tipo \_ de alteração**. Essa estrutura é enviada para a função de retorno de chamada do aplicativo ou para a fila de mensagens do aplicativo antes de qualquer outra estrutura de **\_ \_ resultados assíncronas WINBIO** em que o **\_ resultado assíncrono WINBIO \_ Parameters. MonitorPresence. PresenceArray** inclui uma estrutura de **\_ presença WINBIO** com o mesmo valor para a **presença de WINBIO \_ . TrackingID**.

As seguintes combinações de valores na matriz de estruturas **de \_ presença WINBIO** que o **\_ resultado assíncrono WINBIO \_ . O membro Parameters. MonitorPresence. PresenceArray** indica tipos específicos de alterações no estado de um indivíduo.

-   Quando um indivíduo está visível no quadro da câmera, mas o mecanismo ainda está tentando identificar o indivíduo, os membros da estrutura de **\_ presença WINBIO** têm os valores na tabela a seguir.

    

    | Membro            | Valor                                                    |
    |-------------------|----------------------------------------------------------|
    | **TrackingId**    | Um inteiro que identifica o indivíduo para o mecanismo. |
    | **Status**        | **S \_ OK**                                                |
    | **Identidade. tipo** | **\_tipo de ID WINBIO \_ \_ NULL**                               |

    

     

    Nesse caso, o serviço biométrico estende o tempo de expiração para o indivíduo e não gera uma estrutura de [**\_ \_ resultado assíncrono WINBIO**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) do lado do cliente para o identificador de rastreamento em que o **\_ resultado assíncrono WINBIO \_ . Parameters. MonitorPresence. Altertype** membro é **WINBIO \_ tipo de alteração \_ \_ Recognize**.

    A primeira vez que uma estrutura de [**\_ \_ resultado assíncrono WINBIO**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) inclui a estrutura de **\_ presença WINBIO** onde o membro de **status** é **S \_ OK** e o membro **Identity. Type** é **WINBIO \_ tipo de ID \_ \_ NULL** depois que uma ou mais estruturas de **\_ \_ resultado assíncrono WINBIO** incluíam uma estrutura de **\_ presença WINBIO** com um membro de **status** de **WINBIO \_ E a \_ \_ captura incorreta**, o monitor de presença gera uma única estrutura de **\_ \_ resultado assíncrono de WINBIO** para **\_ \_ Parameters. MonitorPresence. Altertype** membro é **WINBIO \_ alterar \_ tipo \_ Track**. Essa estrutura de **\_ \_ resultado assíncrona WINBIO** em que o **\_ resultado assíncrono WINBIO \_ . Parameters. MonitorPresence. Altertype** é **WINBIO o \_ tipo de alteração \_ \_ Track** informa ao cliente que o problema que causou o **WINBIO E erro de \_ \_ \_ captura inadequada** foi resolvido. Para obter mais informações sobre as circunstâncias em que uma estrutura de **\_ presença WINBIO** tem membro de **status** de **WINBIO \_ E \_ \_ captura incorreta**, consulte a descrição sobre como o adaptador do mecanismo fornece comentários ao usuário para corrigir falhas de reconhecimento posteriormente nesses comentários.

-   Quando um indivíduo está visível no quadro da câmera, mas o mecanismo ainda está tentando identificar o indivíduo e deseja fornecer comentários ao usuário sobre como corrigir uma falha de reconhecimento, os membros da estrutura de **\_ presença WINBIO** têm os valores na tabela a seguir.

    

    | Membro                                                                                                      | Valor                                                                         |
    |-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
    | **TrackingId**                                                                                              | Um inteiro que identifica o indivíduo para o mecanismo.                      |
    | **Status**                                                                                                  | **\_captura WINBIO E \_ inadequada \_**                                                   |
    | **Identidade. tipo**                                                                                           | **\_tipo de ID WINBIO \_ \_ NULL**                                                    |
    | **Properties. FacialFeatures. BoundingBox**, se o valor de **factor** for **WINBIO \_ tipo \_ facial \_ Features** | O local da face do indivíduo dentro do quadro da câmera.           |
    | **Properties. íris. BoundingBox**, se o valor de **factor** for **WINBIO do \_ tipo \_ íris**                       | O local da íris ou íris do indivíduo dentro do quadro da câmera. |

    

     

    Nesse caso, o serviço biométrico estende o tempo de expiração para o indivíduo e gera uma estrutura [**de \_ \_ resultado assíncrona WINBIO**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) para o identificador de rastreamento em que o **\_ resultado assíncrono WINBIO \_ . Parameters. MonitorPresence. Altertype** membro é **WINBIO \_ alterar \_ tipo \_ Track**.

-   Quando um indivíduo está visível no quadro da câmera e o adaptador do mecanismo determina a identidade do indivíduo, os membros da estrutura de **\_ presença WINBIO** têm os valores na tabela a seguir.

    

    | Membro                        | Valor                                                    |
    |-------------------------------|----------------------------------------------------------|
    | **TrackingId**                | Um inteiro que identifica o indivíduo para o mecanismo. |
    | **Status**                    | **S \_ OK**                                                |
    | **Identidade. tipo**             | **\_SID do \_ tipo de ID de WINBIO \_**                                |
    | **Identity. Value. AccountId** | O SID (identificador de segurança) do indivíduo.         |

    

     

    Nesse caso, o serviço biométrico associa o identificador de rastreamento ao SID do indivíduo e gera uma estrutura de [**\_ \_ resultado assíncrono WINBIO**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) do lado do cliente para o identificador de rastreamento em que o **\_ resultado assíncrono WINBIO \_ . Parameters. MonitorPresence. Altertype** membro é **WINBIO \_ tipo de alteração \_ \_ Recognize**. O serviço biométrico não gera estruturas de **\_ \_ resultados assíncronos** adicionais do lado do cliente para o identificador de rastreamento, a menos que a pessoa deixe o quadro da câmera.

-   Quando um indivíduo está visível no quadro da câmera, mas o adaptador do mecanismo determina que o indivíduo não está registrado, os membros da estrutura de **\_ presença WINBIO** têm os valores na tabela a seguir.

    

    | Membro            | Valor                                                    |
    |-------------------|----------------------------------------------------------|
    | **TrackingId**    | Um inteiro que identifica o indivíduo para o mecanismo. |
    | **Status**        | **WINBIO \_ E \_ \_ ID desconhecida**                               |
    | **Identidade. tipo** | **\_tipo de ID WINBIO \_ \_ NULL**                               |

    

     

    Nesse caso, o serviço biométrico associa o identificador de rastreamento do indivíduo a uma identidade de desconhecido e gera uma estrutura de [**\_ \_ resultado assíncrono WINBIO**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) do lado do cliente para o identificador de rastreamento em que o **\_ resultado assíncrono WINBIO \_ . Parameters. MonitorPresence. Altertype** membro é **WINBIO \_ tipo de alteração \_ \_ Recognize**. O serviço biométrico não gera estruturas de **\_ \_ resultados assíncronos** adicionais do lado do cliente para o identificador de rastreamento, a menos que a pessoa deixe o quadro da câmera.

Quando um indivíduo que o adaptador do mecanismo associa a um determinado identificador de controle deixa o quadro da câmera e para de aparecer nos valores retornados pela função [**EngineAdapterIdentifyAll**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_all_fn) , o identificador de rastreamento eventualmente expira. Quando o identificador de rastreamento expira, o serviço biométrico gera uma estrutura de [**\_ \_ resultado assíncrono WINBIO**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) no lado do cliente em que o **\_ resultado assíncrono WINBIO \_ . Parameters. MonitorPresence. Altertype** é **WINBIO a parte do \_ \_ tipo \_ de alteração**. O adaptador do mecanismo pode impedir que o serviço biométrico gere essa estrutura com o valor da **parte do \_ tipo de alteração \_ \_ WINBIO** , incluindo uma estrutura de **\_ presença WINBIO** na matriz que **EngineAdapterIdentifyAll** retorna, onde a **\_ presença WINBIO.** O membro de status é **S \_ OK** e a **presença de WINBIO \_ . O membro Identity. Type** é **WINBIO \_ ID \_ Type \_ NULL** conforme descrito anteriormente nesses comentários. Essa ação estende a hora de expiração do identificador de rastreamento sem causar nenhuma atividade do cliente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                                                                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2016\]<br/>                                                                                                                     |
| parâmetro<br/>                   | <dl> <dt>WinBio \_ Types. h (inclui WinBio. h para aplicativos cliente ou WinBio \_ Adapters. h para adaptadores)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_resultado assíncrono do WINBIO \_**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result)
</dt> <dt>

[**WinBioMonitorPresence**](/windows/desktop/api/winbio/nf-winbio-winbiomonitorpresence)
</dt> <dt>

[**EngineAdapterIdentifyAll**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_all_fn)
</dt> </dl>

 

 





