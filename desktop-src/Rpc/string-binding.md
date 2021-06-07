---
title: Associação de cadeia de caracteres
description: A associação de cadeia de caracteres é uma cadeia de caracteres sem assinatura composta por cadeias de caracteres que representam o objeto de associação UUID, a sequência de protocolo RPC, o endereço de rede e as opções de ponto de extremidade e ponto de extremidade.
ms.assetid: 5e55ddd0-d71c-42ef-90cc-dd1f0b9ed305
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b3f925c03c85be3c47ab174a85f31e72e40d828
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386975"
---
# <a name="string-binding"></a>Associação de cadeia de caracteres

A associação de cadeia de caracteres é uma cadeia de caracteres sem assinatura composta por cadeias de caracteres que representam o objeto de associação UUID, a sequência de protocolo RPC, o endereço de rede e as opções de ponto de extremidade e ponto de extremidade.

*ObjectUUID* @ *ProtocolSequence:**NetworkAddress* \[ *Endpoint*,*Option*\]

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="ObjectUUID"></span><span id="objectuuid"></span><span id="OBJECTUUID"></span>*ObjectUUID*
</dt> <dd>

[UUID](/windows/desktop/Midl/uuid) do objeto operado pela chamada de procedimento remoto. No servidor, a biblioteca em tempo de executar RPC mapeia o tipo de objeto para um vetor de ponto de entrada do gerenciador (uma matriz de ponteiros de função) para invocar a rotina de gerenciador correta. Para uma discussão sobre como mapear UUIDs de objeto para vetores de ponto de entrada do gerenciador, consulte [Registrando interfaces](registering-interfaces.md).

</dd> <dt>

<span id="ProtocolSequence"></span><span id="protocolsequence"></span><span id="PROTOCOLSEQUENCE"></span>*ProtocolSequence*
</dt> <dd>

Cadeia de caracteres que representa uma combinação válida de um protocolo RPC (como ncacn), um protocolo de transporte (como TCP) e um protocolo de rede (como IP). O Microsoft RPC dá suporte aos seguintes protocolos especificados em [Constantes de Sequência de Protocolo](protocol-sequence-constants.md).

</dd> <dt>

<span id="NetworkAddress"></span><span id="networkaddress"></span><span id="NETWORKADDRESS"></span>*Networkaddress*
</dt> <dd>

Endereço de rede do sistema para receber chamadas de procedimento remoto.

> [!Note]  
> As seguintes sequências de protocolo não têm suporte a partir do Windows XP:

 

-   [ncacn \_ nb \_ tcp](/windows/desktop/Midl/ncacn-nb-tcp)
-   [ncacn \_ nb \_ nb](/windows/desktop/Midl/ncacn-nb-nb)
-   [ncacn \_ nb \_ ipx](/windows/desktop/Midl/ncacn-nb-ipx)
-   [ncacn \_ dnet \_ nsp](/windows/desktop/Midl/ncacn-dnet-nsp)
-   [ncacn \_ vns \_ spp](/windows/desktop/Midl/ncacn-vns-spp)
-   [ncadg \_ mq](/windows/desktop/Midl/ncadg-mq)
-   [ncadg \_ ipx](/windows/desktop/Midl/ncadg-ipx)

O formato e o conteúdo do endereço de rede dependem da sequência de protocolo especificada da seguinte forma.



| Sequência de protocolo                       | Endereços de rede                                                                                                                                  | Exemplos                                               |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [ncacn \_ nb \_ tcp](/windows/desktop/Midl/ncacn-nb-tcp)     | Nome do computador                                                                                                                                    | Myserver                                               |
| [ncacn \_ nb \_ ipx](/windows/desktop/Midl/ncacn-nb-ipx)     | Nome do computador                                                                                                                                    | Myserver                                               |
| [ncacn \_ nb \_ nb](/windows/desktop/Midl/ncacn-nb-nb)       | Nome do computador                                                                                                                                    | Myserver                                               |
| [ncacn \_ ip \_ tcp](/windows/desktop/Midl/ncacn-ip-tcp)     | Endereço de Internet de quatro octetos ou nome do host. Se a pilha de rede IPv6 estiver instalada, o IPv6 terá suporte total e um endereço IPv6 também será aceito. | 128.10.2.30 anynode.microsoft.com                      |
| [ncacn \_ np](/windows/desktop/Midl/ncacn-np)              | Nome do servidor (as duas invasões duplas à frente são opcionais)                                                                                            | myserver \\ \\ myotherserver                             |
| [ncacn \_ spx](/windows/desktop/Midl/ncacn-spx)            | Endereço da Internet IPX ou nome do servidor                                                                                                             | ~0000000108002B30612C myserver                         |
| [ncacn \_ dnet \_ nsp](/windows/desktop/Midl/ncacn-dnet-nsp) | Sintaxe de área e nó                                                                                                                             | 4.120                                                  |
| [ncacn \_ em \_ dsp](/windows/desktop/Midl/ncacn-at-dsp)     | Nome do computador, opcionalmente seguido por @ e o nome da zona do AppleTalk. O padrão é @ \* , a zona do cliente, se nenhuma zona for fornecida                     | servername@zonename Servername                         |
| [ncacn \_ vns \_ spp](/windows/desktop/Midl/ncacn-vns-spp)   | Nome do servidor StreetTalk do formulário item@group@organization                                                                                       | printserver@sdkdocs@microsoft                          |
| [ncadg \_ mq](/windows/desktop/Midl/ncadg-mq)              | Nome do servidor                                                                                                                                      | Myserver                                               |
| [ncacn \_ http](/windows/desktop/Midl/ncacn-http)          | Endereço da Internet (nome amigável ou de quatro octetos ou nome do servidor local)                                                                       | 128.10.2.30 somesvr@anywhere.com mylocalsvr<br/> |
| [ncadg \_ ip \_ udp](/windows/desktop/Midl/ncadg-ip-udp)     | Endereço da Internet de quatro octetos ou nome do host                                                                                                        | 128.10.2.30 anynode.microsoft.com                      |
| [ncadg \_ ipx](/windows/desktop/Midl/ncadg-ipx)            | Endereço da Internet IPX ou nome do servidor                                                                                                             | ~0000000108002B30612C myserver                         |
| [ncalrpc](/windows/desktop/Midl/ncalrpc)                 | Nome do computador                                                                                                                                     | thismachine                                            |



 

O campo de endereço de rede é opcional. Quando você não especifica um endereço de rede, a associação de cadeia de caracteres refere-se ao host local. É possível especificar o nome do computador local quando você usa a sequência de protocolo **ncalrpc,** no entanto, fazer isso é completamente desnecessário.

</dd> <dt>

<span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>*Extremidade*
</dt> <dd>

Ponto de extremidade ou endereço do processo para receber chamadas de procedimento remoto. Um ponto de extremidade pode ser precedido pela **palavra-chave endpoint=**. Especificar o ponto de extremidade será opcional se o servidor tiver registrado suas vinculações com o mapeado de ponto de extremidade. Consulte [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister).

O formato e o conteúdo de um ponto de extremidade dependem da sequência de protocolo especificada, conforme mostrado na tabela ponto de extremidade/opção a seguir.

</dd> <dt>

<span id="Option"></span><span id="option"></span><span id="OPTION"></span>*Opção*
</dt> <dd>

Opções específicas do protocolo. O campo de opção não é obrigatório. Cada opção é especificada por um par {name, value} que usa o valor da opção *de nome de* sintaxe = *.* As opções são definidas para cada sequência de protocolo, conforme mostrado na tabela Ponto de Extremidade/Opção a seguir.



| Sequência de protocolo                       | Ponto de extremidade                                                                                           | Exemplos             | Nome da opção                                            |
|-----------------------------------------|----------------------------------------------------------------------------------------------------|----------------------|--------------------------------------------------------|
| [ncacn \_ nb \_ tcp](/windows/desktop/Midl/ncacn-nb-tcp)     | Inteiro entre 1 e 254. Muitos valores entre 0 e 32 são reservados pela Microsoft.                 | 100                  | Nenhum                                                   |
| [ncacn \_ nb \_ ipx](/windows/desktop/Midl/ncacn-nb-ipx)     | (como acima)                                                                                         | (como acima)           | Nenhum                                                   |
| [ncacn \_ nb \_ nb](/windows/desktop/Midl/ncacn-nb-nb)       | (como acima)                                                                                         | (como acima)           | Nenhum                                                   |
| [ncacn \_ ip \_ tcp](/windows/desktop/Midl/ncacn-ip-tcp)     | Número da porta da Internet.                                                                              | 1025                 | Nenhum                                                   |
| [ncacn \_ np](/windows/desktop/Midl/ncacn-np)              | Pipe nomeado. O nome deve começar com \\ \\ "pipe".                                                       | \\\\pipe \\ \\ pipename | Segurança                                               |
| [ncacn \_ spx](/windows/desktop/Midl/ncacn-spx)            | Inteiro entre 1 e 65535.                                                                       | 5.000                 | Nenhum                                                   |
| [ncacn \_ dnet \_ nsp](/windows/desktop/Midl/ncacn-dnet-nsp) | Número do objeto IV da fase DECnet (deve ser precedido pelo \# caractere) ou nome do objeto.              | mailserver \# 17      | Nenhum                                                   |
| [ncacn \_ em \_ dsp](/windows/desktop/Midl/ncacn-at-dsp)     | Uma cadeia de caracteres, com até 22 bytes de comprimento.                                                           | myservicesendpoint   | Nenhum                                                   |
| [ncacn \_ vns \_ spp](/windows/desktop/Midl/ncacn-vns-spp)   | Número da porta vines SPP entre 250 e 511.                                                         | 500                  | Nenhum                                                   |
| [ncadg \_ mq](/windows/desktop/Midl/ncadg-mq)              | Inteiro entre 1 e 65535.                                                                       | 5.000                 | Nenhum                                                   |
| [ncacn \_ http](/windows/desktop/Midl/ncacn-http)          | Número da porta da Internet.                                                                              | 2215                 | Nomes de servidor proxy HTTP e RPC, opção HttpConnection |
| [ncadg \_ ip \_ udp](/windows/desktop/Midl/ncadg-ip-udp)     | Número da porta da Internet.                                                                              | 1025                 | Nenhum                                                   |
| [ncadg \_ ipx](/windows/desktop/Midl/ncadg-ipx)            | Inteiro entre 1 e 65535.                                                                       | 5.000                 | Nenhum                                                   |
| [ncalrpc](/windows/desktop/Midl/ncalrpc)                 | Cadeia de caracteres que especifica o nome do aplicativo ou do serviço. A cadeia de caracteres não pode incluir caracteres de faixa invertida. | minha \_ impressora          | Segurança                                               |



 

O **nome da opção HttpConnectionOption,** com suporte para a sequência de protocolo http ncacn, recebe o valor a \_ seguir.



| Nome da opção       | Valor            |
|-------------------|------------------|
| HttpConnectOption | **UseHttpProxy** |



 

O **HttpConnectionOption** permite direcionar o comportamento do RPC ao fazer conexões HTTP. O **valor UseHttpProxy** instrui o RPC a rotear seu tráfego por meio do proxy Http o tempo todo, incluindo quando o cliente tem as Opções da Internet definidas no Internet Explorer para Ignorar o servidor proxy para endereços locais.  Essa opção direciona o cliente a se conectar com força ao proxy RPC por meio do proxy Http. Isso acelera o tempo para estabelecer uma conexão, pois ignora qualquer atraso na pesquisa do servidor RPC diretamente antes de usar o proxy HTTP.

Se essa **opção HttpConnectionOption** for usada e Internet Explorer no cliente não estiver configurada para usar esse proxy Http, as conexões poderão falhar com **RPC \_ S INVALID \_ NETWORK \_ \_ OPTIONS**.

``` syntax
HttpConnectOption=UseHttpProxy
```

Para obter mais informações sobre **o HttpConnectionOption,** consulte [Usando HTTP como um transporte RPC.](using-http-as-an-rpc-transport.md)

O **nome da** opção Segurança, com suporte para as sequências de protocolo ncalrpc, ncacn \_ np, ncadg ip udp e \_ \_ ncadg ipx, assume os seguintes valores de \_ opção.



| Nome da opção  | Valor de opção                                                                               |
|--------------|--------------------------------------------------------------------------------------------|
| **Segurança** | {identificação \| de \| representação anônima} {estático \| dinâmico} {**true** \| **false**} |



 

Se o nome da opção de segurança for especificado, uma entrada de cada um dos conjuntos de valores de opção de segurança também deverá ser fornecida. Os valores de opção devem ser separados por um caractere de espaço único. Por exemplo, os seguintes *campos Opção* são válidos:

``` syntax
Security=identification dynamic true
Security=impersonation static true
```

Os valores da opção de segurança têm os seguintes significados.



| Valor da opção de segurança | Descrição                                                                                                                                                                                                                                                                                                                                              |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Anônima             | O cliente é anônimo ao servidor.                                                                                                                                                                                                                                                                                                                   |
| Dinâmico               | As alterações na identidade de segurança do cliente são vistas pelo servidor quando o servidor usa a segurança de transporte. Esse é o modo padrão para segurança de nível de transporte LRPC (ncalrpc) e para segurança de nível de transporte de pipe nomeado local (ncacn \_ np).                                                                                                             |
| **Falso**             | Effective = **FALSE**; todas as configurações de privilégios de token, incluindo aquelas definidas como OFF, são incluídas no token no servidor e podem ser habilitadas pelo servidor. Os privilégios são relevantes apenas para chamadas RPC do mesmo computador.                                                                                                                                     |
| **Identificação**    | O servidor tem informações sobre o cliente, mas não pode representar.                                                                                                                                                                                                                                                                                      |
| **Representação**     | O servidor pode agir em nome do cliente dentro do sistema local (a segurança no nível do transporte não dá suporte à delegação).                                                                                                                                                                                                                               |
| **Estático**            | As alterações na identidade de segurança do cliente não são vistas pelo servidor quando o servidor usa a segurança de transporte. Esse é o único modo disponível para segurança de nível de transporte de pipe nomeado remoto (ncacn \_ np). A identidade do chamador é salva durante a primeira chamada de procedimento remoto nesse alçamento de associação, não no momento em que o alça de associação é criado. |
| **True**              | Effective = **TRUE**; Somente as configurações de privilégios de token definidas como ON são incluídas no token no servidor. Os privilégios definidos como OFF não poderão ser ligado pelo servidor se essa opção for usada. Os privilégios são relevantes apenas para chamadas RPC do mesmo computador.                                                                                                         |



 

Para obter mais informações sobre opções de segurança, [Segurança](security.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

O espaço em branco não é permitido em vinculações de cadeia de caracteres, exceto quando exigido pela *sintaxe Option.* As configurações padrão para os *campos NetworkAddress,* *Ponto* de Extremidade e *Opção* variam de acordo com o valor do membro *ProtocolSequence.*

Para todos os campos de associação de cadeia de caracteres, um único caractere de faixa invertida ( \\ ) é interpretado como um caractere de escape. Para especificar um único caractere de faixa invertida literal, você deve fornecer dois caracteres de faixa invertida ( \\ \\ ).

Uma associação de cadeia de caracteres contém a representação de caractere de um alça de associação e, ocasionalmente, partes de um alça de associação. As vinculações de cadeia de caracteres são convenientes para representar partes de um alça de associação, mas não podem ser usadas para fazer chamadas de procedimento remoto. Eles devem primeiro ser convertidos em um alçamento de associação chamando [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding).

Além disso, uma associação de cadeia de caracteres não contém todas as informações de um alça de associação. Por exemplo, as informações de autenticação, se alguma, associadas a um alça de associação não são convertida na associação de cadeia de caracteres retornada chamando [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding).

Durante o desenvolvimento de um aplicativo distribuído, os servidores podem comunicar suas informações de associação aos clientes usando vinculações de cadeia de caracteres para estabelecer uma relação cliente-servidor sem usar o banco de dados endpoint-map ou o banco de dados name-service. Para estabelecer essa relação, use a função [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding) para converter um ou mais alças de associação de um vetor de alça de associação em uma associação de cadeia de caracteres e forneça a associação de cadeia de caracteres ao cliente.

## <a name="examples"></a>Exemplos

A seguir estão exemplos de vinculações de cadeia de caracteres válidas. Nesses exemplos, *obj-uuid* é usado para conveniência para representar um UUID válido no formato de cadeia de caracteres. Em vez de mostrar o UUID 308FB580-1EB2-11CA-923B-08002B1075A7, os exemplos mostram *obj-uuid*.

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

 

