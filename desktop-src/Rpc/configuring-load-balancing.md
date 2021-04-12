---
title: Configurando o balanceamento de carga
description: Configurando o balanceamento de carga
ms.assetid: c78ffde1-1811-4065-941f-c24692eb144c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b82dbfc23e491d53a6687b50aa77b23878ce52ec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294428"
---
# <a name="configuring-load-balancing"></a>Configurando o balanceamento de carga

Cada computador de proxy RPC que deve atuar como um serviço de servidor de balanceamento de carga (LBS) precisa ser configurado como um serviço de LBS com conhecimento dos servidores no farm de servidores. Opcionalmente, o recurso padrão pode ser definido e a segurança do proxy para LBS e LBS a lbs chamadas RPC pode ser definida. Essas configurações são definidas por um conjunto de **chaves de Registro necessárias** e **chaves de registro opcionais** , conforme descrito abaixo.

## <a name="required-registry-keys"></a>Chaves do Registro necessárias

Várias chaves e valores do registro são necessários para configurar um servidor LBS. Se alguma chave estiver ausente ou for inserida com erro, um evento do Windows será registrado. Consulte a descrição de cada chave e valor para obter informações sobre o log de eventos.

Para configurar o farm de servidores, uma chave do registro deve ser criada **HKLM \\ software \\ Microsoft \\ RPC \\ RpcProxy** chamado **LBSConfiguration**. Na chave **LBSConfiguration** , uma chave é criada para cada recurso no farm de servidores. O nome da chave é a representação da cadeia de caracteres do GUID do recurso. Pelo menos uma chave de recurso deve existir e esse recurso é idêntico ao [**UUID**](./rpcdce/ns-rpcdce-uuid.md) definido pelos clientes no identificador de associação, [**identificador de \_ Associação \_ RPC**](rpc-binding-handle.md), quando eles criam a associação RPC/http (para obter mais informações, consulte [**RpcBindingSetObject**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetobject)). Em cada chave UUID do recurso, deve existir um valor DWORD chamado **ConfigurationType** que descreve a configuração usada. Também deve existir um **\_ sz do reg** de identificadores de servidor delimitados por ponto e vírgula chamado **ServerFarm**. Os servidores identificados na chave do **ServerFarm** são os servidores que são membros do farm de servidores de balanceamento de carga.

Veja a seguir uma análise detalhada das chaves e valores de registro necessários:

**HKLM \\ software \\ Microsoft \\ RPC \\ RpcProxy \\ LBSConfiguration**

Chave do registro. A chave **LBSConfiguration** é a chave do registro que contém a configuração de lbs. Isso inclui os [**UUIDs**](./rpcdce/ns-rpcdce-uuid.md) de recurso que devem ter a carga balanceada, o tipo de configuração para cada recurso e os servidores nos farms de servidores que participam do balanceamento de carga. Se essa chave estiver ausente ou for inválida, LBS não será considerado configurado e o serviço LBS não será executado.

\-

**HKLM \\ software \\ Microsoft \\ RPC \\ RPCPROXY \\ LBSCONFIGURATION \\ xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx**

Chave do registro. A chave do **UUID de recurso** identifica o UUID de recurso a ser balanceado de carga. Esse UUID de recurso é igual ao [**UUID**](./rpcdce/ns-rpcdce-uuid.md) que os clientes definem no identificador de associação [**, \_ \_ identificador de associação RPC**](rpc-binding-handle.md). Deve haver pelo menos um UUID de recurso para balancear a carga, pode haver vários UUIDs de recurso. Pode haver apenas um farm de servidores e todos os pontos de extremidade devem estar em todos os servidores no farm de servidores. Se essa chave não puder ser analisada como um UUID válido, a **\_ chave inválida do evento RPCPROXY EventLog \_ lb \_ \_ (0xc0000006)** será registrada no log de eventos do Windows.

\-

**HKLM \\ software \\ Microsoft \\ RPC \\ RPCPROXY \\ LBSCONFIGURATION \\ xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx \\ ConfigurationType**

DWORD. O **ConfigurationType** DWORD é armazenado sob a chave **UUID do recurso** . O único valor permitido é 1. Se esse valor for algo diferente de 1, o tipo de cfg do evento **RPCPROXY \_ \_ do log de eventos \_ \_ \_ (0xC0000007) desconhecido** do

\-

**HKLM \\ software \\ Microsoft \\ RPC \\ RPCPROXY \\ LBSCONFIGURATION \\ xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx \\ ServerFarm**

REG \_ sz. O valor do registro do **ServerFarm** contém uma lista de delimitated de ponto-e-vírgula de identificadores de servidor. O formato para os identificadores de servidor é:

"ServerID1, ServerPort1, LBSPort1, \[ LBSPort2,... LBSPortN \] ; "

Vários identificadores de servidor devem ser listados na chave do registro do **ServerFarm** . Eles devem ser delimitados por ponto e vírgula. Os campos que fazem parte do identificador do servidor são descritos na tabela a seguir. Se esse campo não puder ser analisado corretamente, o evento **RPCPROXY \_ EventLog lb de \_ \_ configuração incorreta \_ \_ (0xC0000008)** será registrado no log de eventos do Windows.



| Campo de identificador | Requisito | Descrição                                                                                                                                                                                                                                                                        |
|------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ServerID         | Obrigatório    | Um nome de rede que possa ser resolvido para o servidor. Pode ser um nome DNS, um nome NetBIOS ou um endereço IP.                                                                                                                                                                                |
| ServerPort       | Opcional    | Se especificado, a porta na qual o servidor escuta conexões RPC/HTTP. Se não for especificado, o mapeador de ponto final na máquina do servidor será usado para localizar a porta do servidor.                                                                                                         |
| LBSPort          | Opcional    | Se especificado, a porta na qual o servidor escuta por LBS. Para usar essa chave, as interfaces LBS devem ser definidas como um ponto de extremidade estático usando um comando netsh RPC firewall. Consulte [práticas recomendadas de balanceamento de carga](load-balancing-best-practices.md) para obter exemplos do comando netsh. |



 

## <a name="optional-registry-keys"></a>Chaves do registro opcionais

Há três valores de registro opcionais para configurar um servidor LBS. As chaves controlam principalmente o nível de segurança para chamadas de e para o serviço LBS e também controlam o UUID de recurso padrão a ser usado. Estes são os valores opcionais:

Veja a seguir uma análise detalhada das chaves e valores de registro necessários:

**HKLM \\ software \\ Microsoft \\ RPC \\ RpcProxy \\ LBSConfiguration \\ NoSecurity**

DWORD. Quando o DWORD **NoSecurity** não está presente ou definido como 0, as chamadas não seguras de entrada para o serviço lbs são rejeitadas. Quando presente e não 0, as chamadas não seguras de entrada para o serviço LBS não são rejeitadas. Essa chave é lida uma vez na inicialização do serviço LBS.

\-

**HKLM \\ software \\ Microsoft \\ RPC \\ RpcProxy \\ LBSConfiguration \\ AssumeResourceUUID**

DWORD. Quando o **AssumeResourceUUID** DWORD não está presente, nenhuma alteração no serviço lbs ocorre. Quando presente, ele deve ser definido com um [**UUID**](./rpcdce/ns-rpcdce-uuid.md)válido. Esse **UUID** será usado como UUID de recurso para todas as conexões que não especificam um UUID de recurso. Isso é normalmente usado nos casos em que os clientes não especificam um UUID de recurso quando criam a associação RPC/HTTP, mas um administrador deseja balancear a carga do tráfego RPC/HTTP para um farm de servidores. Se essa chave não puder ser analisada para um UUID, um erro interno de RPC será reparado, gerando [**\_ \_ \_ informações de erro estendido RPC**](/windows/win32/api/rpcasync/ns-rpcasync-rpc_extended_error_info) se ele estiver habilitado.

\-

**HKLM \\ software \\ Microsoft \\ RPC \\ RPCHTTPLBSServer \\ NoSecurity**

DWORD. Quando o DWORD **NoSecurity** não é apresentado ou definido como 0, todas as chamadas de saída feitas para os serviços de lbs terão segurança. Se presente e não for definido como 0, todas as chamadas de saída feitas para os serviços de LBS não terão segurança. Verifique se essa configuração corresponde à configuração do **HKLM \\ software \\ Microsoft \\ RPC \\ RpcProxy \\ LBSConfiguration \\ NoSecurity** .

 

 