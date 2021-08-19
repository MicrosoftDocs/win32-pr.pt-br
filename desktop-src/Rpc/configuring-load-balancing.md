---
title: Configurando o balanceamento de carga
description: Configurando o balanceamento de carga
ms.assetid: c78ffde1-1811-4065-941f-c24692eb144c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3560359bd5ad064dc270e0840845674b97b093af66796dc92f31f7a15170f467
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118931689"
---
# <a name="configuring-load-balancing"></a>Configurando o balanceamento de carga

Cada computador proxy RPC que deve atuar como um serviço LBS (Servidor de Balanceamento de Carga) deve ser configurado como um serviço LBS com conhecimento dos servidores no farm de servidores. Opcionalmente, o recurso padrão pode ser definido e a segurança do Proxy para chamadas LBS e LBS para LBS RPC pode ser definida. Essas configurações são definidas por um conjunto de **Chaves** do Registro Necessárias e Chaves opcionais do **Registro,** conforme descrito abaixo.

## <a name="required-registry-keys"></a>Chaves necessárias do Registro

Várias chaves e valores do Registro são necessários para configurar um servidor LBS. Se alguma chave estiver ausente ou for inserida com erro, um evento Windows será registrado. Consulte a descrição de cada chave e valor para obter informações sobre o evento registrado.

Para configurar o farm de servidores, uma chave do Registro deve ser criada **HKLM \\ SOFTWARE \\ Microsoft \\ \\ RpcProxy** chamada **LBSConfiguration**. Na chave **LBSConfiguration,** uma chave é criada para cada recurso no farm de servidores. O nome da chave é a representação de cadeia de caracteres do GUID para o recurso. Pelo menos uma chave de recurso deve existir e esse recurso é idêntico ao [**UUID**](./rpcdce/ns-rpcdce-uuid.md) definido por clientes no handle de associação, [**RPC \_ BINDING \_ HANDLE**](rpc-binding-handle.md), quando eles criam a associação RPC/HTTP (para obter mais informações, consulte [**RpcBindingSetObject**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetobject)). Em cada chave UUID de recurso, deve haver um valor DWORD chamado **ConfigurationType** que descreve a configuração usada. Também deve existir um **REG \_ SZ de** identificadores de servidor delimitados por ponto e vírgula chamado **ServerFarm**. Os servidores identificados na chave **ServerFarm** são os servidores que são membros do farm de servidores de balanceamento de carga.

Veja a seguir um detalhamento dos valores e chaves do Registro necessários:

**HKLM \\ SOFTWARE \\ Microsoft \\ Rpc \\ RpcProxy \\ LBSConfiguration**

Chave do Registro. A **chave LBSConfiguration** é a chave do Registro que contém a configuração do LBS. Isso inclui os [**UUIDs**](./rpcdce/ns-rpcdce-uuid.md) de recurso que devem ter balanceamento de carga, o tipo de configuração para cada recurso e os servidores nos farms de servidores que participam do balanceamento de carga. Se essa chave estiver ausente ou inválida, o LBS não será considerado configurado e o serviço LBS não será executado.

\-

**HKLM \\ SOFTWARE \\ Microsoft \\ \\ Rpc RpcProxy \\ LBSConfiguration \\ XXXXXXXX-XXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXXXXXXXX**

Chave do Registro. A **chave UUID de** recurso identifica o UUID do recurso a ser balanceado de carga. Esse UUID de recurso é o mesmo que [**o UUID**](./rpcdce/ns-rpcdce-uuid.md) definido pelos clientes no alça de associação, [**RPC \_ BINDING \_ HANDLE.**](rpc-binding-handle.md) Deve haver pelo menos um UUID de recurso para balancear a carga, pode haver vários UUIDs de recurso. Pode haver apenas um farm de servidores e todos os pontos de extremidade devem estar em todos os servidores no farm de servidores. Se essa chave não puder ser analisado para um UUID válido, o evento **RPCPROXY \_ EVENTLOG \_ LB INVALID KEY \_ \_ (0xC0000006)** será registrado no Log de Eventos Windows.

\-

**HKLM \\ SOFTWARE \\ Microsoft \\ \\ Rpc RpcProxy \\ LBSConfiguration \\ XXXXXXXX-XXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX \\ ConfigurationType**

DWORD. O **ConfigurationType** DWORD é armazenado sob a **chave UUID do** recurso. O único valor permitido é 1. Se esse valor for diferente de 1, o evento **RPCPROXY \_ EVENTLOG \_ LB UNKNOWN \_ \_ CFG TYPE \_ (0xC0000007)** será registrado no Log de Eventos Windows.

\-

**HKLM \\ SOFTWARE \\ Microsoft \\ \\ RpcProxy \\ LBSConfiguration \\ XXXXXXXX-XXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX \\ ServerFarm**

REG \_ SZ. O **valor do Registro ServerFarm** contém uma lista delimitada por ponto e vírgula de identificadores de servidor. O formato para os identificadores de servidor é:

"ServerID1,ServerPort1,LBSPort1, \[ LBSPort2, ... LBSPortN \] ;"

Vários identificadores de servidor devem ser listados na chave do Registro **ServerFarm.** Eles devem ser delimitados por um ponto e vírgula. Os campos que fazem parte do identificador do servidor são descritos na tabela a seguir. Se esse campo não puder ser analisado corretamente, o evento **RPCPROXY \_ EVENTLOG \_ LB BAD \_ \_ CONFIG ENTRY \_ (0xC0000008)** será registrado no Log de Eventos Windows.



| Campo identificador | Requisito | Descrição                                                                                                                                                                                                                                                                        |
|------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ServerID         | Obrigatório    | Um nome de rede resolvível para o servidor. Pode ser um nome DNS, um nome netbios ou um endereço IP.                                                                                                                                                                                |
| ServerPort       | Opcional    | Se especificado, a porta na qual o servidor escuta conexões RPC/HTTP. Se não for especificado, o mapeado Ponto de extremidade no computador do servidor será usado para encontrar a porta do servidor.                                                                                                         |
| LBSPort          | Opcional    | Se especificado, a porta na qual o servidor escuta LBS. Para usar essa chave, as interfaces LBS devem ser definidas como um ponto de extremidade estático usando um comando netsh RPC firewall. Consulte [Práticas recomendadas de balanceamento de](load-balancing-best-practices.md) carga para ver exemplos do comando netsh. |



 

## <a name="optional-registry-keys"></a>Chaves opcionais do Registro

Há três valores opcionais do Registro para configurar um servidor LBS. As chaves controlam principalmente o nível de segurança para chamadas de e para o serviço LBS e também controlam o UUID de recurso padrão a ser usado. Veja a seguir valores opcionais:

Veja a seguir um detalhamento dos valores e chaves do Registro necessários:

**HKLM \\ SOFTWARE \\ Microsoft \\ Rpc \\ RpcProxy \\ LBSConfiguration \\ NoSecurity**

DWORD. Quando o **NoSecurity** DWORD não está presente ou definido como 0, as chamadas não seguras de entrada para o serviço LBS são rejeitadas. Quando presente e não 0, as chamadas não seguras de entrada para o serviço LBS não são rejeitadas. Essa chave é lida uma vez na inicialização do serviço LBS.

\-

**HKLM \\ SOFTWARE \\ Microsoft \\ Rpc \\ RpcProxy \\ LBSConfiguration \\ AssumeResourceUUID**

DWORD. Quando **AssumeResourceUUID** DWORD não está presente, nenhuma alteração no serviço LBS ocorre. Quando presente, ele deve ser definido com um [**UUID válido.**](./rpcdce/ns-rpcdce-uuid.md) Esse **UUID será** usado como o UUID do recurso para todas as conexões que não especificam um UUID de recurso. Isso geralmente é usado em casos em que os clientes não especificam um UUID de recurso quando criam a associação RPC/HTTP, mas um administrador deseja balancear a carga do tráfego RPC/HTTP para um farm de servidores. Se essa chave não puder ser analisado para um UUID, um erro RPC interno será apresentado, gerando INFORMAÇÕES DE ERRO ESTENDIDO RPC se ela estiver habilitada. [**\_ \_ \_**](/windows/win32/api/rpcasync/ns-rpcasync-rpc_extended_error_info)

\-

**HKLM \\ Software \\ Microsoft \\ Rpc \\ RPCHTTPLBSServer \\ NoSecurity**

DWORD. Quando o **NoSecurity** DWORD não for apresentado ou definido como 0, todas as chamadas de saída feitas aos serviços lbS terão segurança. Se estiver presente e não estiver definido como 0, todas as chamadas de saída feitas aos serviços lbS não terão segurança. Verifique se essa configuração corresponde **à configuração HKLM \\ SOFTWARE Microsoft \\ \\ \\ RpcProxy \\ LBSConfiguration \\ NoSecurity.**

 

 