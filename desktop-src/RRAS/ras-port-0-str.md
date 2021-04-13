---
title: Estrutura de RAS_PORT_0 (Rassapi. h)
description: A \_ estrutura da porta 0 do RAS \_ contém informações que descrevem uma porta RAS.
ms.assetid: 750fc705-0770-427b-b7d6-7876b8b9118a
keywords:
- RAS da estrutura de RAS_PORT_0
- RAS de ponteiro de estrutura de PRAS_PORT_0
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
ms.openlocfilehash: 80d66725415d86aea44138f23fb3748e3187820f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499409"
---
# <a name="ras_port_0-structure"></a>Estrutura da porta do RAS \_ \_ 0

\[Não há suporte para esta versão da estrutura de **\_ porta \_ 0 do RAS** a partir do Windows Vista. Em vez disso, use a [**porta do RAS \_ \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) mais recente definida em mprapi. h.\]

A estrutura da **\_ porta \_ 0 do RAS** contém informações que descrevem uma porta RAS.

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

Uma cadeia de caracteres Unicode terminada em nulo que especifica o tipo do dispositivo no qual a conexão foi feita, como modem ou ISDN. A lista de tipos de dispositivos que podem ser especificados nesse membro inclui todos os tipos de dispositivos instalados no servidor, incluindo dispositivos de terceiros.

</dd> <dt>

**wszDeviceName**
</dt> <dd>

Uma cadeia de caracteres Unicode terminada em nulo que especifica o nome do dispositivo no qual a conexão foi feita, como "Hayes 9600" ou "PCIMACISDN1".

</dd> <dt>

**wszMediaName**
</dt> <dd>

Especifica uma cadeia de caracteres Unicode terminada em nulo que especifica o nome da mídia usada para a conexão, como *rasser* ou *RASTAPI*.

</dd> <dt>

**reservado**
</dt> <dd>

Reservado.

</dd> <dt>

**Sinalizadores**
</dt> <dd>

Especifica um conjunto de sinalizadores de bits que especificam a natureza da conexão feita nessa porta. Esse membro pode ser uma combinação dos sinalizadores a seguir.



| Valor                                                                                                                                                                        | Significado                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GATEWAY_ACTIVE"></span><span id="gateway_active"></span><dl> <dt>**GATEWAY \_ ativo**</dt> </dl>             | Se esse sinalizador for definido, o gateway NetBIOS estará ativo no servidor.<br/>                                                                                                                                                                                                                                                                                                               |
| <span id="MESSENGER_PRESENT"></span><span id="messenger_present"></span><dl> <dt>**MESSENGER \_ presente**</dt> </dl>    | Se esse sinalizador for definido, o serviço de mensageiro será executado no cliente remoto.<br/>                                                                                                                                                                                                                                                                                                     |
| <span id="PORT_MULTILINKED"></span><span id="port_multilinked"></span><dl> <dt>**PORTA \_ MULTIlink**</dt> </dl>       | Se esse sinalizador for definido, a porta será vinculada com outras portas. Use essas informações para exibir o status da conexão como uma porta com conexões múltiplas. <br/> Para uma porta com múltiplas conexões, a estrutura de [**\_ \_ Estatísticas de porta de Ras**](ras-port-statistics-str.md) contém dois conjuntos de estatísticas: um para a porta sozinha e outro para as portas combinadas na conexão de vínculos múltiplos.<br/> |
| <span id="PPP_CLIENT"></span><span id="ppp_client"></span><dl> <dt>**\_cliente PPP**</dt> </dl>                         | Se esse sinalizador estiver definido, o cliente remoto conectado usando o PPP. Se esse sinalizador não for definido, o cliente remoto será conectado usando o protocolo AMB.<br/>                                                                                                                                                                                                                                        |
| <span id="REMOTE_LISTEN"></span><span id="remote_listen"></span><dl> <dt>**\_escuta remota**</dt> </dl>                | Se esse sinalizador for definido, o parâmetro RemoteListen do gateway NetBIOS será definido como 1 no servidor.<br/>                                                                                                                                                                                                                                                                               |
| <span id="USER_AUTHENTICATED"></span><span id="user_authenticated"></span><dl> <dt>**USUÁRIO \_ autenticado**</dt> </dl> | Se esse sinalizador for definido, um cliente remoto será conectado ao servidor e o usuário foi autenticado. Marque esse sinalizador para garantir que um cliente esteja realmente conectado a uma porta.<br/>                                                                                                                                                                                                   |



 

Se o MESSENGER \_ presente, o gateway \_ ativo e os \_ sinalizadores de escuta remota estiverem definidos, use o serviço mensageiro para enviar uma mensagem administrativa ao cliente remoto. Se \_ o Messenger presente e a \_ escuta remota estiverem definidos, mas o gateway \_ ativo não estiver, envie mensagens para o cliente somente do servidor RAS ao qual o cliente está conectado.

</dd> <dt>

**wszUserName**
</dt> <dd>

Uma cadeia de caracteres Unicode terminada em nulo que especifica o nome do usuário remoto conectado a esta porta.

</dd> <dt>

**wszComputer**
</dt> <dd>

Uma cadeia de caracteres Unicode terminada em nulo que especifica o nome do computador cliente remoto.

</dd> <dt>

**dwStartSessionTime**
</dt> <dd>

Especifica o tempo, em segundos, de 1º de janeiro de 1970, que o cliente conectou ao servidor RAS nesta porta. Use as funções de hora padrão para formatar esse valor para exibição.

</dd> <dt>

**wszLogonDomain**
</dt> <dd>

Especifica uma cadeia de caracteres Unicode terminada em nulo que especifica o nome do domínio no qual o usuário remoto foi autenticado. Essa cadeia de caracteres é apenas o nome de domínio, sem o \\ \\ prefixo "".

</dd> <dt>

**fAdvancedServer**
</dt> <dd>

Especifica um sinalizador que será diferente de zero se o servidor RAS associado a essa porta for um servidor avançado, como o Windows 2000 Advanced Server. Use essas informações para determinar o nome do servidor que tem o banco de dados da conta de usuário. Se o servidor RAS for um servidor avançado, obtenha o nome do servidor de conta de usuário concatenando o prefixo " \\ \\ " para o nome retornado no membro **wszLogonDomain** . Isso ocorre porque, para um servidor avançado, o nome de domínio de logon local é o mesmo que o nome do servidor. Se o servidor RAS for uma estação de trabalho, use a função [**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) para obter o nome do servidor de conta de usuário.

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

[**\_Porta RAS \_ 1**](ras-port-1-str.md)
</dt> <dt>

[**\_Estatísticas de porta RAS \_**](ras-port-statistics-str.md)
</dt> <dt>

[**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md)
</dt> <dt>

[**RasAdminPortEnum**](rasadminportenum.md)
</dt> </dl>

 

 





