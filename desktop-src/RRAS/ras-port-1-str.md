---
title: Estrutura de RAS_PORT_1 (Rassapi. h)
description: A \_ estrutura da porta 1 do RAS \_ contém informações sobre uma porta RAS.
ms.assetid: f226ef16-feb4-41e0-ba60-ddb2f0acd305
keywords:
- RAS da estrutura de RAS_PORT_1
- RAS de ponteiro de estrutura de PRAS_PORT_1
topic_type:
- apiref
api_name:
- RAS_PORT_1
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d73fe450e5ea5f8ceee48436dbbe05570d0d818a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105752426"
---
# <a name="ras_port_1-structure"></a>Estrutura da porta do RAS \_ \_ 1

\[Não há suporte para esta versão da estrutura da **porta do RAS \_ \_ 1** no Windows Vista. Em vez disso, use a [**\_ porta \_ 1 do RAS**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_1) mais recente definida em mprapi. h.\]

A estrutura da **\_ porta \_ 1 do RAS** contém informações sobre uma porta RAS.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _RAS_PORT_1 {
  RAS_PORT_0                rasport0;
  DWORD                     LineCondition;
  DWORD                     HardwareCondition;
  DWORD                     LineSpeed;
  WORD                      NumStatistics;
  WORD                      NumMediaParms;
  DWORD                     SizeMediaParms;
  RAS_PPP_PROJECTION_RESULT ProjResult;
} RAS_PORT_1, *PRAS_PORT_1;
```



## <a name="members"></a>Membros

<dl> <dt>

**rasport0**
</dt> <dd>

Especifica uma estrutura de [**\_ porta \_ 0 RAS**](ras-port-0-str.md) que contém informações sobre a porta, como o nome da porta, o nome do usuário remoto conectado à porta e assim por diante.

</dd> <dt>

**LineCondition**
</dt> <dd>

Especifica o estado da porta. Esse membro pode ser um dos valores a seguir.



| Valor                                                                                                                                                                                            | Significado                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RAS_PORT_NON_OPERATIONAL"></span><span id="ras_port_non_operational"></span><dl> <dt>**\_porta RAS \_ não \_ operacional**</dt> </dl> | A porta não está operacional. Verifique se há erros relatados pelo servidor no log de eventos.<br/>                                                                         |
| <span id="RAS_PORT_DISCONNECTED"></span><span id="ras_port_disconnected"></span><dl> <dt>**\_porta RAS \_ desconectada**</dt> </dl>           | A porta está desconectada no momento.<br/>                                                                                                                         |
| <span id="RAS_PORT_CALLING_BACK"></span><span id="ras_port_calling_back"></span><dl> <dt>**\_retorno de \_ chamada da porta RAS \_**</dt> </dl>          | O servidor RAS está chamando novamente o cliente RAS.<br/>                                                                                                              |
| <span id="RAS_PORT_LISTENING"></span><span id="ras_port_listening"></span><dl> <dt>**\_escuta de porta RAS \_**</dt> </dl>                    | A porta está aguardando um cliente chamar.<br/>                                                                                                                |
| <span id="RAS_PORT_AUTHENTICATING"></span><span id="ras_port_authenticating"></span><dl> <dt>**\_autenticação de porta RAS \_**</dt> </dl>     | O servidor está no processo de autenticação do cliente remoto.<br/>                                                                                           |
| <span id="RAS_PORT_AUTHENTICATED"></span><span id="ras_port_authenticated"></span><dl> <dt>**\_porta RAS \_ autenticada**</dt> </dl>        | O cliente remoto agora está autenticado.<br/>                                                                                                                     |
| <span id="RAS_PORT_INITIALIZING"></span><span id="ras_port_initializing"></span><dl> <dt>**\_inicialização de porta RAS \_**</dt> </dl>           | O dispositivo conectado à porta está sendo inicializado. O estado da porta será alterado para escuta da \_ porta RAS \_ quando a inicialização for concluída.<br/> |



 

</dd> <dt>

**HardwareCondition**
</dt> <dd>

Especifica um dos valores a seguir para indicar o estado do dispositivo conectado à porta.



| Valor                                                                                                                                                                                                  | Significado                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="RAS_MODEM_OPERATIONAL"></span><span id="ras_modem_operational"></span><dl> <dt>**\_modem \_ operacional do RAS**</dt> </dl>                 | O modem anexado a esta porta está funcionando e está pronto para receber chamadas de cliente.<br/> |
| <span id="RAS_MODEM_HARDWARE_FAILURE"></span><span id="ras_modem_hardware_failure"></span><dl> <dt>**\_falha de \_ hardware do modem RAS \_**</dt> </dl> | O modem anexado a essa porta tem um problema de hardware.<br/>                              |



 

</dd> <dt>

**LineSpeed**
</dt> <dd>

Especifica a velocidade, em bits por segundo, com a qual o computador pode se comunicar com a porta.

</dd> <dt>

**NumStatistics**
</dt> <dd>

Este membro não é usado. As funções de administração de RAS, como a função [**RasAdminPortGetInfo**](rasadminportgetinfo.md) , usam a estrutura de [**Estatísticas de \_ porta \_ de Ras**](ras-port-statistics-str.md) para retornar estatísticas de porta.

</dd> <dt>

**NumMediaParms**
</dt> <dd>

Especifica o número de parâmetros específicos de mídia para esta porta. Para mídia serial, normalmente é o número de valores que aparecem no arquivo de SERIAL.INI.

</dd> <dt>

**SizeMediaParms**
</dt> <dd>

Especifica o tamanho, em bytes, do buffer necessário para todos os parâmetros específicos de mídia. A função [**RasAdminPortGetInfo**](rasadminportgetinfo.md) retorna um buffer que contém uma matriz de estruturas de [**\_ parâmetros de Ras**](ras-parameters-str.md) com os parâmetros de mídia e os valores da porta.

</dd> <dt>

**ProjResult**
</dt> <dd>

Uma estrutura de [**\_ \_ \_ resultados de projeção de Ras PPP**](ras-ppp-projection-result-str.md) que especifica as informações de projeção PPP para esta porta. Essa estrutura fornece informações para cada protocolo negociado quando um cliente RAS se conecta a um servidor.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Fim do suporte do cliente<br/>    | Windows XP<br/>                                                                |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                                                       |
| parâmetro<br/>                   | <dl> <dt>Rassapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral do serviço de acesso remoto (RAS)](about-remote-access-service.md)
</dt> <dt>

[Estruturas de administração do servidor RAS](ras-server-administration-structures.md)
</dt> <dt>

[**parâmetros de RAS \_**](ras-parameters-str.md)
</dt> <dt>

[**\_Porta RAS \_ 0**](ras-port-0-str.md)
</dt> <dt>

[**\_Estatísticas de porta RAS \_**](ras-port-statistics-str.md)
</dt> <dt>

[**\_resultado da \_ projeção do RAS PPP \_**](ras-ppp-projection-result-str.md)
</dt> <dt>

[**RasAdminAcceptNewConnection**](rasadminacceptnewconnection.md)
</dt> <dt>

[**RasAdminConnectionHangupNotification**](rasadminconnectionhangupnotification.md)
</dt> <dt>

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)
</dt> </dl>

 

 





