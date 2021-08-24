---
title: RAS_PORT_0 estrutura (Rassapi.h)
description: A estrutura RAS \_ PORT \_ 0 contém informações que descrevem uma porta RAS.
ms.assetid: 750fc705-0770-427b-b7d6-7876b8b9118a
keywords:
- ras RAS_PORT_0 estrutura de RAS_PORT_0
- PRAS_PORT_0 RAS do ponteiro de estrutura
topic_type:
- apiref
api_name:
- RAS_PORT_0
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67891ccd65aaa56fc41dd077ae46bd4bf61f816cdc02afeb65964886cbaf9562
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119673126"
---
# <a name="ras_port_0-structure"></a>Estrutura RAS \_ PORT \_ 0

\[Esta versão da estrutura **RAS \_ PORT \_ 0** não tem suporte desde Windows Vista. Em vez disso, [**use a PORTA RAS \_ \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) mais nova definida em mprapi.h.\]

A **estrutura RAS PORT \_ \_ 0** contém informações que descrevem uma porta RAS.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _RAS_PORT_0 {
  WCHAR wszPortName[RASSAPI_MAX_PORT_NAME];
  WCHAR wszDeviceType[RASSAPI_MAX_DEVICETYPE_NAME];
  WCHAR wszDeviceName[RASSAPI_MAX_DEVICE_NAME];
  WCHAR wszMediaName[RASSAPI_MAX_MEDIA_NAME];
  DWORD reserved;
  DWORD Flags;
  WCHAR wszUserName[UNLEN + 1];
  WCHAR wszComputer[NETBIOS_NAME_LEN];
  DWORD dwStartSessionTime;
  WCHAR wszLogonDomain[DNLEN + 1];
  BOOL  fAdvancedServer;
} RAS_PORT_0, *PRAS_PORT_0;
```



## <a name="members"></a>Membros

<dl> <dt>

**wszPortName**
</dt> <dd>

Uma cadeia de caracteres Unicode terminada em nulo que especifica o nome da porta, como "COM1".

</dd> <dt>

**wszDeviceType**
</dt> <dd>

Uma cadeia de caracteres Unicode terminada em nulo que especifica o tipo do dispositivo no qual a conexão foi feita, como Modem ou ISDN. A lista de tipos de dispositivo que podem ser especificados neste membro inclui todos os tipos de dispositivo instalados no servidor, incluindo dispositivos de terceiros.

</dd> <dt>

**wszDeviceName**
</dt> <dd>

Uma cadeia de caracteres Unicode terminada em nulo que especifica o nome do dispositivo no qual a conexão foi feita, como "Andy 9600" ou "PCIMACISDN1".

</dd> <dt>

**wszMediaName**
</dt> <dd>

Especifica uma cadeia de caracteres Unicode terminada em nulo que especifica o nome da mídia usada para a conexão, como *rasser* ou *rastapi.*

</dd> <dt>

**Reservados**
</dt> <dd>

Reservado.

</dd> <dt>

**Sinalizadores**
</dt> <dd>

Especifica um conjunto de sinalizadores de bits que especificam a natureza da conexão feita nessa porta. Esse membro pode ser uma combinação dos sinalizadores a seguir.



| Valor                                                                                                                                                                        | Significado                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GATEWAY_ACTIVE"></span><span id="gateway_active"></span><dl> <dt>**GATEWAY \_ ATIVO**</dt> </dl>             | Se esse sinalizador estiver definido, o gateway NetBIOS será ativo no servidor.<br/>                                                                                                                                                                                                                                                                                                               |
| <span id="MESSENGER_PRESENT"></span><span id="messenger_present"></span><dl> <dt>**MESSENGER \_ PRESENTE**</dt> </dl>    | Se esse sinalizador estiver definido, o serviço messenger será executado no cliente remoto.<br/>                                                                                                                                                                                                                                                                                                     |
| <span id="PORT_MULTILINKED"></span><span id="port_multilinked"></span><dl> <dt>**PORTA \_ MULTILINKED**</dt> </dl>       | Se esse sinalizador for definido, a porta será multilinkada com outras portas. Use essas informações para exibir o status da conexão como uma porta multilink. <br/> Para uma porta multilink, a estrutura [**RAS \_ PORT \_ STATISTICS**](ras-port-statistics-str.md) contém dois conjuntos de estatísticas: um para a porta sozinho e outro para as portas combinadas na conexão multilink.<br/> |
| <span id="PPP_CLIENT"></span><span id="ppp_client"></span><dl> <dt>**CLIENTE \_ PPP**</dt> </dl>                         | Se esse sinalizador estiver definido, o cliente remoto será conectado usando PPP. Se esse sinalizador não estiver definido, o cliente remoto será conectado usando o protocolo AMB.<br/>                                                                                                                                                                                                                                        |
| <span id="REMOTE_LISTEN"></span><span id="remote_listen"></span><dl> <dt>**REMOTE \_ LISTEN**</dt> </dl>                | Se esse sinalizador for definido, o parâmetro RemoteListen do gateway NetBIOS será definido como 1 no servidor.<br/>                                                                                                                                                                                                                                                                               |
| <span id="USER_AUTHENTICATED"></span><span id="user_authenticated"></span><dl> <dt>**AUTENTICADO \_ PELO USUÁRIO**</dt> </dl> | Se esse sinalizador estiver definido, um cliente remoto será conectado ao servidor e o usuário será autenticado. Verifique esse sinalizador para garantir que um cliente esteja realmente conectado a uma porta.<br/>                                                                                                                                                                                                   |



 

Se os sinalizadores MESSENGER PRESENT, GATEWAY ACTIVE e REMOTE LISTEN estão definidos, use o serviço messenger para enviar uma mensagem administrativa \_ \_ para o cliente \_ remoto. Se MESSENGER PRESENT e REMOTE LISTEN estão definidos, mas o GATEWAY ACTIVE não está, envie mensagens para o cliente somente do servidor RAS ao qual \_ \_ o cliente está \_ conectado.

</dd> <dt>

**wszUserName**
</dt> <dd>

Uma cadeia de caracteres Unicode terminada em nulo que especifica o nome do usuário remoto conectado a essa porta.

</dd> <dt>

**wszComputer**
</dt> <dd>

Uma cadeia de caracteres Unicode terminada em nulo que especifica o nome do computador cliente remoto.

</dd> <dt>

**dwStartSessionTime**
</dt> <dd>

Especifica a hora, em segundos a partir de 1º de janeiro de 1970, em que o cliente se conectou ao servidor RAS nessa porta. Use as funções de tempo padrão para formatar esse valor para exibição.

</dd> <dt>

**wszLogonDomain**
</dt> <dd>

Especifica uma cadeia de caracteres Unicode terminada em nulo que especifica o nome do domínio no qual o usuário remoto foi autenticado. Essa cadeia de caracteres é apenas o nome de domínio, sem nenhum \\ \\ prefixo ".

</dd> <dt>

**fAdvancedServer**
</dt> <dd>

Especifica um sinalizador que não é zero se o servidor RAS associado a essa porta for um servidor avançado, como o Windows 2000 Advanced Server. Use essas informações para determinar o nome do servidor que tem o banco de dados da conta de usuário. Se o servidor RAS for um servidor avançado, obter o nome do servidor de conta de usuário concatenando o prefixo " " para o nome retornado no \\ \\ **membro wszLogonDomain.** Isso porque, para um servidor avançado, o nome de domínio de logon local é o mesmo que o nome do servidor. Se o servidor RAS for uma estação de trabalho, use a [**função RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) para obter o nome do servidor de conta de usuário.

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

[**PORTA RAS \_ \_ 1**](ras-port-1-str.md)
</dt> <dt>

[**ESTATÍSTICAS \_ DE \_ PORTA RAS**](ras-port-statistics-str.md)
</dt> <dt>

[**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md)
</dt> <dt>

[**RasAdminPortEnum**](rasadminportenum.md)
</dt> </dl>

 

 





