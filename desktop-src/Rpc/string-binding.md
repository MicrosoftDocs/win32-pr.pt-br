---
title: Associação de cadeia de caracteres
description: A associação de cadeia de caracteres é uma cadeia de caracteres não assinada composta de cadeias que representam o UUID do objeto de associação, a sequência do Protocolo RPC, o endereço de rede e as opções ponto de extremidade e ponto de extremidade.
ms.assetid: 5e55ddd0-d71c-42ef-90cc-dd1f0b9ed305
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5d804fe614185b054b8041e13069e900501342a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366496"
---
# <a name="string-binding"></a>Associação de cadeia de caracteres

A associação de cadeia de caracteres é uma cadeia de caracteres não assinada composta de cadeias que representam o UUID do objeto de associação, a sequência do Protocolo RPC, o endereço de rede e as opções ponto de extremidade e ponto de extremidade.

*OBJECTuuid* @ *ProtocolSequence*: \[ *ponto de extremidade* networkaddress,*opção*\]

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="ObjectUUID"></span><span id="objectuuid"></span><span id="OBJECTUUID"></span>*Objectuuid*
</dt> <dd>

[UUID](/windows/desktop/Midl/uuid) do objeto operado pela chamada de procedimento remoto. No servidor, a biblioteca de tempo de execução RPC mapeia o tipo de objeto para um vetor de ponto de entrada de gerente (uma matriz de ponteiros de função) para invocar a rotina do Gerenciador correta. Para obter uma discussão sobre como mapear UUIDs de objeto para os vetores de ponto de entrada do Gerenciador, consulte [registrando interfaces](registering-interfaces.md).

</dd> <dt>

<span id="ProtocolSequence"></span><span id="protocolsequence"></span><span id="PROTOCOLSEQUENCE"></span>*ProtocolSequence*
</dt> <dd>

Cadeia de caracteres que representa uma combinação válida de um protocolo RPC (como ncacn), um protocolo de transporte (como TCP) e um protocolo de rede (como IP). O Microsoft RPC dá suporte aos seguintes protocolos especificados nas [constantes de sequência de protocolo](protocol-sequence-constants.md).

</dd> <dt>

<span id="NetworkAddress"></span><span id="networkaddress"></span><span id="NETWORKADDRESS"></span>*NetworkAddress*
</dt> <dd>

Endereço de rede do sistema para receber chamadas de procedimento remoto.

> [!Note]  
> As seguintes sequências de protocolo não são suportadas a partir do Windows XP:

 

-   [ncacn \_ NB \_ TCP](/windows/desktop/Midl/ncacn-nb-tcp)
-   [ncacn \_ NB NB \_](/windows/desktop/Midl/ncacn-nb-nb)
-   [IPX do ncacn \_ NB \_](/windows/desktop/Midl/ncacn-nb-ipx)
-   [ncacn \_ dnet \_ NSP](/windows/desktop/Midl/ncacn-dnet-nsp)
-   [ncacn \_ VNS \_ spp](/windows/desktop/Midl/ncacn-vns-spp)
-   [ncadg \_ MQ](/windows/desktop/Midl/ncadg-mq)
-   [ncadg \_ IPX](/windows/desktop/Midl/ncadg-ipx)

O formato e o conteúdo do endereço de rede dependem da sequência de protocolo especificada da seguinte maneira.



| Sequência de protocolos                       | Endereços de rede                                                                                                                                  | Exemplos                                               |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [ncacn \_ NB \_ TCP](/windows/desktop/Midl/ncacn-nb-tcp)     | Nome do computador                                                                                                                                    | meuservidor                                               |
| [IPX do ncacn \_ NB \_](/windows/desktop/Midl/ncacn-nb-ipx)     | Nome do computador                                                                                                                                    | meuservidor                                               |
| [ncacn \_ NB NB \_](/windows/desktop/Midl/ncacn-nb-nb)       | Nome do computador                                                                                                                                    | meuservidor                                               |
| [\_TCP IP \_ ncacn](/windows/desktop/Midl/ncacn-ip-tcp)     | Endereço de Internet de quatro octetos ou nome do host. Se a pilha de rede IPv6 estiver instalada, o IPv6 terá suporte total e um endereço IPv6 também será aceito. | 128.10.2.30 anynode.microsoft.com                      |
| [ncacn \_ NP](/windows/desktop/Midl/ncacn-np)              | Nome do servidor (barras invertidas duplas à esquerda são opcionais)                                                                                            | meuservidor \\ \\ myotherserver                             |
| [ncacn \_ SPX](/windows/desktop/Midl/ncacn-spx)            | Endereço IPX da Internet ou nome do servidor                                                                                                             | ~ 0000000108002B30612C meuservidor                         |
| [ncacn \_ dnet \_ NSP](/windows/desktop/Midl/ncacn-dnet-nsp) | Sintaxe de área e nó                                                                                                                             | 4,120                                                  |
| [ncacn \_ no \_ DSP](/windows/desktop/Midl/ncacn-at-dsp)     | Nome do computador, opcionalmente seguido por @ e o nome da zona AppleTalk. O padrão é @ \* , a zona do cliente, se nenhuma zona for fornecida                     | servername@zonename ServerName                         |
| [ncacn \_ VNS \_ spp](/windows/desktop/Midl/ncacn-vns-spp)   | Nome do Servidor StreetTalk do formulário item@group@organization                                                                                       | printserver@sdkdocs@microsoft                          |
| [ncadg \_ MQ](/windows/desktop/Midl/ncadg-mq)              | Nome do servidor                                                                                                                                      | meuservidor                                               |
| [\_http ncacn](/windows/desktop/Midl/ncacn-http)          | Endereço da Internet (com quatro octetos ou nome amigável ou nome do servidor local                                                                       | 128.10.2.30 somesvr@anywhere.com mylocalsvr<br/> |
| [\_UDP IP \_ ncadg](/windows/desktop/Midl/ncadg-ip-udp)     | Endereço de Internet de quatro octetos ou nome do host                                                                                                        | 128.10.2.30 anynode.microsoft.com                      |
| [ncadg \_ IPX](/windows/desktop/Midl/ncadg-ipx)            | Endereço IPX da Internet ou nome do servidor                                                                                                             | ~ 0000000108002B30612C meuservidor                         |
| [ncalrpc](/windows/desktop/Midl/ncalrpc)                 | Nome do computador                                                                                                                                     | thismachine                                            |



 

O campo de endereço de rede é opcional. Quando você não especifica um endereço de rede, a associação de cadeia de caracteres refere-se ao host local. É possível especificar o nome do computador local ao usar a sequência de protocolo **Ncalrpc** . no entanto, fazer isso é completamente desnecessário.

</dd> <dt>

<span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>*Extremidade*
</dt> <dd>

Ponto de extremidade ou endereço do processo para receber chamadas de procedimento remoto. Um ponto de extremidade pode ser precedido pela palavra-chave **Endpoint =**. A especificação do ponto de extremidade será opcional se o servidor tiver registrado suas associações com o mapeador de ponto de extremidade. Consulte [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister).

O formato e o conteúdo de um ponto de extremidade dependem da sequência de protocolo especificada, conforme mostrado na tabela ponto de extremidade/opção a seguir.

</dd> <dt>

<span id="Option"></span><span id="option"></span><span id="OPTION"></span>*Option*
</dt> <dd>

Opções específicas de protocolo. O campo de opção não é obrigatório. Cada opção é especificada por um par {Name, Value} que usa o valor de opção de *nome da opção* de sintaxe = . As opções são definidas para cada sequência de protocolo, conforme mostrado na tabela ponto de extremidade/opção a seguir.



| Sequência de protocolos                       | Ponto de extremidade                                                                                           | Exemplos             | Nome da opção                                            |
|-----------------------------------------|----------------------------------------------------------------------------------------------------|----------------------|--------------------------------------------------------|
| [ncacn \_ NB \_ TCP](/windows/desktop/Midl/ncacn-nb-tcp)     | Inteiro entre 1 e 254. Muitos valores entre 0 e 32 são reservados pela Microsoft.                 | 100                  | Nenhum                                                   |
| [IPX do ncacn \_ NB \_](/windows/desktop/Midl/ncacn-nb-ipx)     | (como acima)                                                                                         | (como acima)           | Nenhum                                                   |
| [ncacn \_ NB NB \_](/windows/desktop/Midl/ncacn-nb-nb)       | (como acima)                                                                                         | (como acima)           | Nenhum                                                   |
| [\_TCP IP \_ ncacn](/windows/desktop/Midl/ncacn-ip-tcp)     | Número da porta da Internet.                                                                              | 1025                 | Nenhum                                                   |
| [ncacn \_ NP](/windows/desktop/Midl/ncacn-np)              | Pipe nomeado. O nome deve começar com " \\ \\ pipe".                                                       | \\\\\\ \\ pipeName do pipe | Segurança                                               |
| [ncacn \_ SPX](/windows/desktop/Midl/ncacn-spx)            | Inteiro entre 1 e 65535.                                                                       | 5.000                 | Nenhum                                                   |
| [ncacn \_ dnet \_ NSP](/windows/desktop/Midl/ncacn-dnet-nsp) | O número de objeto da fase IV do DECnet (deve ser precedido pelo \# caractere) ou o nome do objeto.              | MailServer \# 17      | Nenhum                                                   |
| [ncacn \_ no \_ DSP](/windows/desktop/Midl/ncacn-at-dsp)     | Uma cadeia de caracteres, até 22 bytes de comprimento.                                                           | myservicesendpoint   | Nenhum                                                   |
| [ncacn \_ VNS \_ spp](/windows/desktop/Midl/ncacn-vns-spp)   | Número da porta Vines SPP entre 250 e 511.                                                         | 500                  | Nenhum                                                   |
| [ncadg \_ MQ](/windows/desktop/Midl/ncadg-mq)              | Inteiro entre 1 e 65535.                                                                       | 5.000                 | Nenhum                                                   |
| [\_http ncacn](/windows/desktop/Midl/ncacn-http)          | Número da porta da Internet.                                                                              | 2215                 | Nomes de servidor proxy HTTP e RPC, opção HttpConnection |
| [\_UDP IP \_ ncadg](/windows/desktop/Midl/ncadg-ip-udp)     | Número da porta da Internet.                                                                              | 1025                 | Nenhum                                                   |
| [ncadg \_ IPX](/windows/desktop/Midl/ncadg-ipx)            | Inteiro entre 1 e 65535.                                                                       | 5.000                 | Nenhum                                                   |
| [ncalrpc](/windows/desktop/Midl/ncalrpc)                 | Cadeia de caracteres que especifica o nome do aplicativo ou do serviço. A cadeia de caracteres não pode incluir caracteres de barra invertida. | minha \_ impressora          | Segurança                                               |



 

O nome da opção **HttpConnectionOption** , com suporte para a \_ sequência de protocolo http ncacn, usa o seguinte valor.



| Nome da opção       | Valor            |
|-------------------|------------------|
| HttpConnectOption | **UseHttpProxy** |



 

O **HttpConnectionOption** permite direcionar o comportamento de RPC s ao fazer conexões http. O valor **UseHttpProxy** INSTRUI o RPC a rotear seu tráfego por meio do proxy http em todos os momentos, incluindo quando o cliente tem as opções de Internet definidas no Internet Explorer para ignorar o servidor proxy para endereços locais.  Essa opção direciona o cliente para se conectar de modo forçado ao proxy RPC por meio do proxy http. Isso acelera o tempo para estabelecer uma conexão, já que ignora qualquer atraso na pesquisa do servidor RPC diretamente antes de usar o proxy HTTP.

Se essa opção **HttpConnectionOption** for usada e o Internet Explorer no cliente não estiver configurado para usar esse proxy http, as conexões poderão falhar **com \_ Opções de \_ \_ rede \_ RPC S inválidas**.

``` syntax
HttpConnectOption=UseHttpProxy
```

Para obter mais informações sobre o **HttpConnectionOption**, consulte [usando http como um transporte RPC](using-http-as-an-rpc-transport.md).

O nome da opção de **segurança** , com suporte para as \_ sequências de protocolo Ncalrpc, ncacn NP, ncadg \_ IP \_ UDP e ncadg \_ IPX, usa os seguintes valores de opção.



| Nome da opção  | Valor de opção                                                                               |
|--------------|--------------------------------------------------------------------------------------------|
| **Segurança** | {identificação \| de \| representação anônima} { \| static dinâmico}**{true** \| **false**} |



 

Se o nome da opção de segurança for especificado, uma entrada de cada um dos conjuntos de valores de opção de segurança também deverá ser fornecida. Os valores de opção devem ser separados por um caractere de espaço único. Por exemplo, os seguintes campos de *opção* são válidos:

``` syntax
Security=identification dynamic true
Security=impersonation static true
```

Os valores da opção de segurança têm os seguintes significados.



| Valor da opção de segurança | Descrição                                                                                                                                                                                                                                                                                                                                              |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Anônima             | O cliente é anônimo ao servidor.                                                                                                                                                                                                                                                                                                                   |
| Dinâmico               | As alterações na identidade do Client Security são vistas pelo servidor quando o servidor usa a segurança de transporte. Este é o modo padrão para segurança de nível de transporte do LRPC (Ncalrpc) e para segurança de nível de transporte ncacn NP (pipe nomeado local \_ ).                                                                                                             |
| **Falso**             | Efetivo = **falso**; todas as configurações de privilégios de token, incluindo aquelas definidas como OFF, são incluídas no token no servidor e podem ser habilitadas pelo servidor. Os privilégios são relevantes apenas para chamadas RPC de mesmo computador.                                                                                                                                     |
| **Identificação**    | O servidor tem informações sobre o cliente, mas não pode representar.                                                                                                                                                                                                                                                                                      |
| **Representação**     | O servidor pode agir em nome do cliente no sistema local (a segurança em nível de transporte não oferece suporte à delegação).                                                                                                                                                                                                                               |
| **Estático**            | As alterações na identidade do Client Security não são vistas pelo servidor quando o servidor usa a segurança de transporte. Esse é o único modo disponível para segurança de nível de transporte do pipe nomeado remoto (ncacn \_ NP). A identidade do chamador é salva durante a primeira chamada de procedimento remoto nesse identificador de ligação, não no momento em que o identificador de associação é criado. |
| **True**              | Efetivo = **verdadeiro**; somente as configurações de privilégios de token definidas como ON são incluídas no token no servidor. Os privilégios definidos como desativado não poderão ser ativados pelo servidor se essa opção for usada. Os privilégios são relevantes apenas para chamadas RPC de mesmo computador.                                                                                                         |



 

Para obter mais informações sobre opções de segurança, [segurança](security.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

O espaço em branco não é permitido em associações de cadeias de caracteres, exceto quando exigido pela sintaxe da *opção* . As configurações padrão para os campos *networkaddress*, *ponto de extremidade* e *opção* variam de acordo com o valor do membro *ProtocolSequence* .

Para todos os campos de ligação de cadeia de caracteres, um caractere de barra invertida simples ( \) é interpretado como um caractere de escape. Para especificar um caractere de barra invertida literal único, você deve fornecer dois caracteres de barra invertida ( \\ \) .

Uma associação de cadeia de caracteres contém a representação de caracteres de um identificador de associação e, ocasionalmente, partes de um identificador de associação. Associações de cadeia de caracteres são convenientes para representar partes de um identificador de associação, mas não podem ser usadas para fazer chamadas de procedimento remotas. Eles devem primeiro ser convertidos em um identificador de ligação chamando [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding).

Além disso, uma associação de cadeia de caracteres não contém todas as informações de um identificador de associação. Por exemplo, as informações de autenticação, se houver, associadas a um identificador de associação não são convertidas na associação de cadeia de caracteres retornada pela chamada de [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding).

Durante o desenvolvimento de um aplicativo distribuído, os servidores podem comunicar suas informações de associação com os clientes usando associações de cadeia de caracteres para estabelecer uma relação de cliente-servidor sem usar o banco de dados do mapa de ponto de extremidade ou o banco de dados de serviço de nome. Para estabelecer essa relação, use a função [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding) para converter um ou mais identificadores de associação de um vetor de identificador de associação para uma associação de cadeia de caracteres e forneça a associação de cadeia de caracteres ao cliente.

## <a name="examples"></a>Exemplos

Veja a seguir exemplos de associações de cadeia de caracteres válidas. Nestes exemplos, *obj-UUID* é usado para conveniência para representar um UUID válido no formato de cadeia de caracteres. Em vez de mostrar o UUID 308FB580-1EB2-11CA-923B-08002B1075A7, os exemplos mostram *obj-UUID*.

``` syntax
obj-uuid@ncadg_mq:mymqserver
obj-uuid@ncacn_http:major7.microsoft.com[2225]
obj_uuid@ncacn_http:major7.microsoft.com[,HttpProxy=proxysvr:80,
    RpcProxy=websvr1.microsoft.com:80]
obj_uuid@ncacn_http:major7.microsoft.com[,HttpProxy=proxysvr:80,
    RpcProxy=websvr1.microsoft.com:80,HttpConnectOption=UseHttpProxy]
obj-uuid@ncacn_ip_tcp:16.20.16.27[2001]
obj-uuid@ncacn_ip_tcp:16.20.16.27[endpoint=2001]
obj-uuid@ncacn_nb_nb:
obj-uuid@ncacn_nb_nb:[100]
obj-uuid@ncacn_np:
obj-uuid@ncacn_np:[\\pipe\\p3,Security=impersonation static true]
obj-uuid@ncacn_np:\\\\marketing[\\pipe\\p2\\p3\\p4]
obj-uuid@ncacn_np:\\\\marketing[endpoint=\\pipe\\p2\\p3\\p4]
obj-uuid@ncacn_np:\\\\sales
obj-uuid@ncacn_np:\\\\sales[\\pipe\\p1,Security=identification dynamic true]
obj-uuid@ncalrpc:
obj-uuid@ncalrpc:[object1_name_demonstrating_that_these_can_be_lengthy]
obj-uuid@ncalrpc:[object2_name,Security=anonymous static true]
obj-uuid@ncacn_vns_spp:server@group@org[500]
obj-uuid@ncacn_dnet_nsp:took[elf_server]
obj-uuid@ncacn_dnet_nsp:took[endpoint=elf_server]
obj-uuid@ncadg_ip_udp:128.10.2.30
obj-uuid@ncadg_ip_udp:maryos.microsoft.com[1025]
obj-uuid@ncadg_ipx: ~0000000108002B30612C[5000]
obj-uuid@ncadg_ipx:printserver
obj-uuid@ncacn_spx:annaw[4390]
obj-uuid@ncacn_spx:~0000000108002B30612C
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding)
</dt> <dt>

[**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding)
</dt> <dt>

[**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister)
</dt> <dt>

[Usando HTTP como um transporte RPC](using-http-as-an-rpc-transport.md)
</dt> </dl>

 

