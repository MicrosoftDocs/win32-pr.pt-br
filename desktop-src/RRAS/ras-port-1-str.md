---
title: RAS_PORT_1 estrutura (Rassapi.h)
description: A estrutura RAS \_ PORT \_ 1 contém informações sobre uma porta RAS.
ms.assetid: f226ef16-feb4-41e0-ba60-ddb2f0acd305
keywords:
- ras RAS_PORT_1 estrutura de RAS_PORT_1
- PRAS_PORT_1 RAS do ponteiro de estrutura
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
ms.openlocfilehash: 5c73677b10743434bb9548c8d6add95100c4cf017d25bb44d7436e2f68b9ca4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119673106"
---
# <a name="ras_port_1-structure"></a>Estrutura RAS \_ PORT \_ 1

\[Esta versão da estrutura **RAS \_ PORT \_ 1** não tem suporte desde o Windows Vista. Em vez disso, [**use a PORTA RAS \_ \_ 1**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_1) mais nova definida em mprapi.h.\]

A **estrutura RAS PORT \_ \_ 1** contém informações sobre uma porta RAS.

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

Especifica uma [**estrutura RAS PORT \_ \_ 0**](ras-port-0-str.md) que contém informações sobre a porta, como o nome da porta, o nome do usuário remoto conectado à porta e assim por diante.

</dd> <dt>

**LineCondition**
</dt> <dd>

Especifica o estado da porta. Esse membro pode ser um dos valores a seguir.



| Valor                                                                                                                                                                                            | Significado                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RAS_PORT_NON_OPERATIONAL"></span><span id="ras_port_non_operational"></span><dl> <dt>**PORTA RAS \_ \_ NÃO \_ OPERACIONAL**</dt> </dl> | A porta não está operacional. Verifique o log de eventos em busca de erros relatados pelo servidor.<br/>                                                                         |
| <span id="RAS_PORT_DISCONNECTED"></span><span id="ras_port_disconnected"></span><dl> <dt>**PORTA RAS \_ \_ DESCONECTADA**</dt> </dl>           | No momento, a porta está desconectada.<br/>                                                                                                                         |
| <span id="RAS_PORT_CALLING_BACK"></span><span id="ras_port_calling_back"></span><dl> <dt>**RETORNO DE \_ CHAMADA \_ DE PORTA \_ RAS**</dt> </dl>          | O servidor RAS está chamando de volta o cliente RAS.<br/>                                                                                                              |
| <span id="RAS_PORT_LISTENING"></span><span id="ras_port_listening"></span><dl> <dt>**RAS \_ PORT \_ LISTENING**</dt> </dl>                    | A porta está aguardando um cliente chamar.<br/>                                                                                                                |
| <span id="RAS_PORT_AUTHENTICATING"></span><span id="ras_port_authenticating"></span><dl> <dt>**AUTENTICAÇÃO \_ DE PORTA RAS \_**</dt> </dl>     | O servidor está no processo de autenticação do cliente remoto.<br/>                                                                                           |
| <span id="RAS_PORT_AUTHENTICATED"></span><span id="ras_port_authenticated"></span><dl> <dt>**PORTA RAS \_ \_ AUTENTICADA**</dt> </dl>        | O cliente remoto agora está autenticado.<br/>                                                                                                                     |
| <span id="RAS_PORT_INITIALIZING"></span><span id="ras_port_initializing"></span><dl> <dt>**INICIALIZAÇÃO DE PORTA RAS \_ \_**</dt> </dl>           | O dispositivo anexado à porta está sendo inicializado. O estado da porta será altere para RAS \_ PORT LISTENING quando a \_ inicialização for concluída.<br/> |



 

</dd> <dt>

**HardwareCondition**
</dt> <dd>

Especifica um dos valores a seguir para indicar o estado do dispositivo anexado à porta.



| Valor                                                                                                                                                                                                  | Significado                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="RAS_MODEM_OPERATIONAL"></span><span id="ras_modem_operational"></span><dl> <dt>**RAS \_ MODEM \_ OPERACIONAL**</dt> </dl>                 | O modem anexado a essa porta está operacional e está pronto para receber chamadas de cliente.<br/> |
| <span id="RAS_MODEM_HARDWARE_FAILURE"></span><span id="ras_modem_hardware_failure"></span><dl> <dt>**FALHA DE \_ HARDWARE DO MODEM \_ \_ RAS**</dt> </dl> | O modem anexado a essa porta tem um problema de hardware.<br/>                              |



 

</dd> <dt>

**LineSpeed**
</dt> <dd>

Especifica a velocidade, em bits por segundo, com a qual o computador pode se comunicar com a porta.

</dd> <dt>

**NumStatistics**
</dt> <dd>

Esse membro não é usado. As funções de administração ras, como [**a função RasAdminPortGetInfo,**](rasadminportgetinfo.md) usam a estrutura [**RAS PORT \_ \_ STATISTICS**](ras-port-statistics-str.md) para retornar estatísticas de porta.

</dd> <dt>

**NumMediaParms**
</dt> <dd>

Especifica o número de parâmetros específicos de mídia para essa porta. Para mídia serial, esse normalmente é o número de valores que aparecem no arquivo SERIAL.INI dados.

</dd> <dt>

**SizeMediaParms**
</dt> <dd>

Especifica o tamanho, em bytes, do buffer necessário para todos os parâmetros específicos da mídia. A [**função RasAdminPortGetInfo**](rasadminportgetinfo.md) retorna um buffer que contém uma matriz de estruturas [**RAS \_ PARAMETERS**](ras-parameters-str.md) com os parâmetros de mídia e os valores para a porta.

</dd> <dt>

**ProjResult**
</dt> <dd>

Uma [**estrutura RAS PPP PROJECTION \_ \_ \_ RESULT**](ras-ppp-projection-result-str.md) que especifica as informações de projeção DE PPP para essa porta. Essa estrutura fornece informações para cada protocolo negociado quando um cliente RAS se conecta a um servidor.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Fim do suporte ao cliente<br/>    | Windows XP<br/>                                                                |
| Fim do suporte ao servidor<br/>    | Windows Server 2003<br/>                                                       |
| Cabeçalho<br/>                   | <dl> <dt>Rassapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral do RAS (Serviço de Acesso Remoto)](about-remote-access-service.md)
</dt> <dt>

[Estruturas de administração de servidor RAS](ras-server-administration-structures.md)
</dt> <dt>

[**PARÂMETROS \_ RAS**](ras-parameters-str.md)
</dt> <dt>

[**PORTA RAS \_ \_ 0**](ras-port-0-str.md)
</dt> <dt>

[**ESTATÍSTICAS \_ DE \_ PORTA RAS**](ras-port-statistics-str.md)
</dt> <dt>

[**RESULTADO DA \_ \_ PROJEÇÃO RAS \_ PPP**](ras-ppp-projection-result-str.md)
</dt> <dt>

[**RasAdminAcceptNewConnection**](rasadminacceptnewconnection.md)
</dt> <dt>

[**RasAdminConnectionConnectupNotification**](rasadminconnectionhangupnotification.md)
</dt> <dt>

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)
</dt> </dl>

 

 





