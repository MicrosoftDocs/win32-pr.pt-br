---
title: Wecutil.exe
description: Wecutil.exe é um utilitário coletor de eventos do Windows que permite que um administrador crie e gerencie assinaturas para eventos encaminhados de fontes de eventos remotas que dão suporte ao protocolo WS-Management.
ms.assetid: 93ce25df-f829-43b9-96f2-7f2f291d100e
ms.tgt_platform: multiple
keywords:
- Wecutil.exe
topic_type:
- apiref
api_name:
- Wecutil.exe
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaf6f74007b56cff85c28c4106fd4345c5627d4e
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/10/2021
ms.locfileid: "104298445"
---
# <a name="wecutilexe"></a>Wecutil.exe

Wecutil.exe é um utilitário coletor de eventos do Windows que permite que um administrador crie e gerencie assinaturas para eventos encaminhados de fontes de eventos remotas que dão suporte ao protocolo WS-Management. Comandos, opções e valores de opção não diferenciam maiúsculas de minúsculas para este utilitário.

Se você receber uma mensagem dizendo "o servidor RPC não está disponível" ou "a interface é desconhecida" ao tentar executar wecutil, será necessário iniciar o serviço coletor de eventos do Windows (Wecsvc). Para iniciar o Wecsvc, em um prompt de comandos com privilégios elevados, digite **net start Wecsvc**.

## <a name="list-existing-subscriptions"></a>Listar assinaturas existentes

A sintaxe a seguir é usada para listar assinaturas de evento remoto existentes.

``` syntax
wecutil { es | enum-subscription }
```

Se você usar um script para obter os nomes das assinaturas da saída, será necessário ignorar os caracteres da BOM UTF-8 na primeira linha da saída. O script a seguir mostra um exemplo de como você pode ignorar os caracteres da BOM.

``` syntax
setlocal enabledelayedexpansion

set bomskipped=
for /f %%i in ('wecutil es') do (
    set sub=%%i
    if not defined bomskipped (
        set sub=!sub:~3!
        set bomskipped=yes
    )
    echo !sub!
)
goto :eof

endlocal
```

## <a name="get-subscription-configuration"></a>Obter configuração de assinatura

A sintaxe a seguir é usada para exibir dados de configuração de assinatura de evento remoto.

``` syntax
wecutil { gs | get-subscription } SUBSCRIPTION_ID [/f:VALUE 
[/u:VALUE] ...]
```

## <a name="get-configuration-parameters"></a>Obter parâmetros de configuração

<dl> <dt>

<span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**ID da assinatura \_**
</dt> <dd>

Uma cadeia de caracteres que identifica exclusivamente uma assinatura. Esse identificador é especificado no elemento **SubscriptionId** no arquivo de configuração XML usado para criar a assinatura.

</dd> <dt>

<span id="_f_VALUE"></span><span id="_f_value"></span><span id="_F_VALUE"></span>**/f: * valor***
</dt> <dd>

Um valor que especifica a saída dos dados de configuração da assinatura. O *valor* pode ser "XML" ou "conciso", e o padrão é "conciso". Se *Value* for "XML", a saída será impressa no formato "XML". Se *Value* for "conciso", a saída será impressa em pares de nome-valor.

</dd> <dt>

<span id="_u_VALUE"></span><span id="_u_value"></span><span id="_U_VALUE"></span>**/u: *valor***
</dt> <dd>

Um valor que especifica se a saída está no formato Unicode. O *valor* pode ser "true" ou "false". Se *Value* for "true", a saída estará no formato Unicode e, se *Value* for "false", a saída não estará no formato Unicode.

</dd> </dl>

## <a name="get-subscription-runtime-status"></a>Obter status do tempo de execução da assinatura

A sintaxe a seguir é usada para exibir o status do tempo de execução da assinatura.

``` syntax
wecutil { gr | get-subscriptionruntimestatus } SUBSCRIPTION_ID
 [EVENT_SOURCE [EVENT_SOURCE] ...]
```

## <a name="get-status-parameters"></a>Obter parâmetros de status

<dl> <dt>

<span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**ID da assinatura \_**
</dt> <dd>

Uma cadeia de caracteres que identifica exclusivamente uma assinatura. Esse identificador é especificado no elemento **SubscriptionId** no arquivo de configuração XML usado para criar a assinatura.

</dd> <dt>

<span id="EVENT_SOURCE"></span><span id="event_source"></span>**origem do evento \_**
</dt> <dd>

Um valor que identifica um computador que é uma origem de evento para uma assinatura de evento. Esse valor pode ser o nome de domínio totalmente qualificado para o computador, o nome NetBIOS ou o endereço IP.

</dd> </dl>

## <a name="set-subscription-configuration-information"></a>Definir informações de configuração de assinatura

A sintaxe a seguir é usada para definir os dados de configuração da assinatura alterando os parâmetros de assinatura da linha de comando ou usando um arquivo de configuração XML.

``` syntax
wecutil { ss | set_subscription } SUBSCRIPTION_ID [/e:VALUE] 
[/esa:EVENT_SOURCE [/ese:VALUE] [/aes] [/res] [/un:USERNAME] [/up:PASSWORD]] 
[/d:DESCRIPTION] [/uri:URI] [/cm:CONFIGURATION_MODE] [/ex:DATE_TIME] 
[/q:QUERY] [/dia:DIALECT] [/tn:TRANSPORTNAME] [/tp:TRANSPORTPORT] [/dm:MODE] 
[/dmi:NUMBER] [/dmlt:MS] [/hi:MS] [/cf:FORMAT] [/l:LOCALE] [/ree:[VALUE]] 
[/lf:FILENAME] [/pn:PUBLISHER] [/hn:NAME] [/ct:TYPE] 
[/cun:USERNAME] [/cup:PASSWORD] 
[/ica:THUMBPRINTS] [/as:ALLOWED] [/ds:DENIED] [/adc:SDDL]

wecutil {ss | set_subscription } /c:CONGIG_FILE [/cun:USERNAME] 
[/cup:PASSWORD]
```

### <a name="remarks"></a>Comentários

Quando um nome de usuário ou senha incorretos for especificado no comando **wecutil SS** , nenhum erro será relatado até que você exiba o status de tempo de execução da assinatura usando o comando **wecutil gr** .

## <a name="set-configuration-parameters"></a>Definir parâmetros de configuração

<dl> <dt>

<span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**ID da assinatura \_**
</dt> <dd>

Uma cadeia de caracteres que identifica exclusivamente uma assinatura. Esse identificador é especificado no elemento **SubscriptionId** no arquivo de configuração XML usado para criar a assinatura.

</dd> <dt>

<span id="_c_CONGIG_FILE"></span><span id="_c_congig_file"></span><span id="_C_CONGIG_FILE"></span>**/c: *\_ arquivo CONGIG***
</dt> <dd>

Um valor que especifica o caminho para o arquivo XML que contém informações de configuração de assinatura. O caminho pode ser absoluto ou relativo ao diretório atual. Esse parâmetro só pode ser usado com os parâmetros optional/cus e/Cup, e é mutuamente exclusivo com todos os outros parâmetros.

</dd> <dt>

<span id="_e_VALUE"></span><span id="_e_value"></span><span id="_E_VALUE"></span>**/e: *valor***
</dt> <dd>

Um valor que determina se a assinatura deve ser habilitada ou desabilitada. O valor pode ser true ou false. O valor padrão é true, que habilita a assinatura.

> [!Note]  
> Quando você desabilita uma assinatura iniciada pelo coletor, a origem do evento se torna inativa em vez de desabilitada. Em uma assinatura iniciada pelo coletor, você pode desabilitar uma origem de evento independente da assinatura.

 

</dd> <dt>

<span id="_d_DESCRIPTION"></span><span id="_d_description"></span><span id="_D_DESCRIPTION"></span>**/d: *Descrição***
</dt> <dd>

Um valor que especifica uma descrição para a assinatura de evento.

</dd> <dt>

<span id="_ex_DATE_TIME"></span><span id="_ex_date_time"></span><span id="_EX_DATE_TIME"></span>**/ex: *data e \_ hora***
</dt> <dd>

Um valor que especifica o tempo de expiração da assinatura. *Data de início \_ O tempo* é um valor especificado no formato de data/hora padrão XML ou ISO8601: "aaaa-mm-ddThh: mm: SS \[ . SSS \] \[ Z \] ", em que "T" é o separador de tempo e "Z" indica a hora UTC. Por exemplo, se *data e \_ hora* for "2007-01-12T01:20:00", o tempo de expiração da assinatura será 12 de janeiro de 2007, 01:20.

</dd> <dt>

<span id="_uri_URI"></span><span id="_uri_uri"></span><span id="_URI_URI"></span>**/URI: *URI***
</dt> <dd>

Um valor que especifica o tipo de eventos consumidos pela assinatura. O endereço do computador de origem do evento junto com o URI (Uniform Resource Identifier) identifica exclusivamente a origem dos eventos. A cadeia de caracteres do URI é usada para todos os endereços de origem do evento na assinatura.

</dd> <dt>

<span id="_cm_CONFIGURATION_MODE"></span><span id="_cm_configuration_mode"></span><span id="_CM_CONFIGURATION_MODE"></span>**/cm: *\_ modo de configuração***
</dt> <dd>

Um valor que especifica o modo de configuração da assinatura de evento. *Configuração \_ do O modo* pode ser uma das seguintes cadeias de caracteres: "normal", "Custom", "MinLatency" ou "MinBandwidth". A enumeração do modo de configuração de assinatura do EC define os modos de configuração. [**\_ \_ \_**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_configuration_mode) Os parâmetros/DM,/DMI,/Hi e/dmlt só poderão ser especificados se o modo de configuração for definido como personalizado.

</dd> <dt>

<span id="_q_QUERY"></span><span id="_q_query"></span><span id="_Q_QUERY"></span>**/q: *consulta***
</dt> <dd>

Um valor que especifica a cadeia de caracteres de consulta para a assinatura. O formato dessa cadeia de caracteres pode ser diferente para valores de URI diferentes e se aplica a todas as origens de evento na assinatura.

</dd> <dt>

<span id="_dia_DIALECT"></span><span id="_dia_dialect"></span><span id="_DIA_DIALECT"></span>**/dia: *dialeto***
</dt> <dd>

Um valor que especifica o dialeto que a cadeia de caracteres de consulta usa.

</dd> <dt>

<span id="_cf_FORMAT"></span><span id="_cf_format"></span><span id="_CF_FORMAT"></span>**/CF: *formato***
</dt> <dd>

Um valor que especifica o formato dos eventos retornados. O *formato* pode ser "Events" ou "RenderedText". Quando o valor é "RenderedText", os eventos são retornados com as cadeias de caracteres localizadas (como cadeias de caracteres de descrição do evento) anexadas aos eventos. O valor padrão do *formato* é "RenderedText".

</dd> <dt>

<span id="_l_LOCALE"></span><span id="_l_locale"></span><span id="_L_LOCALE"></span>**/l: *localidade***
</dt> <dd>

Um valor que especifica a localidade para entrega das cadeias de caracteres localizadas no formato de texto renderizado. A *localidade* é um identificador de cultura de idioma/país, por exemplo, "en-US". Esse parâmetro só é válido quando o parâmetro/CF é definido como "RenderedText".

</dd> <dt>

<span id="_ree__VALUE_"></span><span id="_ree__value_"></span><span id="_REE__VALUE_"></span>**/Ree: \[ *valor*\]**
</dt> <dd>

Um valor que especifica quais eventos devem ser entregues para a assinatura. O *valor* pode ser true ou false. Quando o *valor* for true, todos os eventos existentes serão lidos das fontes de evento de assinatura. Quando o *valor* for false, somente os eventos futuros (chegando) serão entregues. O padrão é true quando/Ree é especificado sem um valor, e o padrão é false se/Ree não for especificado.

</dd> <dt>

<span id="_lf_FILENAME"></span><span id="_lf_filename"></span><span id="_LF_FILENAME"></span>**/LF: *filename***
</dt> <dd>

Um valor que especifica o log de eventos local que é usado para armazenar eventos recebidos da assinatura de evento.

</dd> <dt>

<span id="_pn_PUBLISHER"></span><span id="_pn_publisher"></span><span id="_PN_PUBLISHER"></span>**/PN: *Publicador***
</dt> <dd>

Um valor que especifica o nome do editor de eventos (provedor). Ele deve ser um Publicador que possui ou importa o log especificado pelo parâmetro/LF.

</dd> <dt>

<span id="_dm_MODE"></span><span id="_dm_mode"></span><span id="_DM_MODE"></span>**/DM: *modo***
</dt> <dd>

Um valor que especifica o modo de entrega da assinatura. O *modo* pode ser Push ou pull. Essa opção só será válida se o parâmetro/cm for definido como Custom.

</dd> <dt>

<span id="_dmi_NUMBER"></span><span id="_dmi_number"></span><span id="_DMI_NUMBER"></span>**/DMI: *número***
</dt> <dd>

Um valor que especifica o número máximo de itens para entrega em lote na assinatura do evento. Essa opção só será válida se o parâmetro/cm for definido como Custom.

</dd> <dt>

<span id="_dmlt_MS"></span><span id="_dmlt_ms"></span><span id="_DMLT_MS"></span>**/dmlt: *MS***
</dt> <dd>

Um valor que especifica a latência máxima permitida no fornecimento de um lote de eventos. MS é o número de milissegundos permitidos. Esse parâmetro só será válido se o parâmetro/cm for definido como Custom.

</dd> <dt>

<span id="_hi_MS"></span><span id="_hi_ms"></span><span id="_HI_MS"></span>**/Hi: *MS***
</dt> <dd>

Um valor que especifica o intervalo de pulsação para a assinatura. *MS* é o número de milissegundos usados no intervalo. Esse parâmetro só será válido se o parâmetro/cm for definido como Custom.

</dd> <dt>

<span id="_tn_TRANSPORTNAME"></span><span id="_tn_transportname"></span><span id="_TN_TRANSPORTNAME"></span>**/TN: *TRANSportname***
</dt> <dd>

Um valor que especifica o nome do transporte usado para se conectar ao computador de origem do evento remoto.

</dd> <dt>

<span id="_esa_EVENT_SOURCE"></span><span id="_esa_event_source"></span><span id="_ESA_EVENT_SOURCE"></span>**/ESA: *\_ origem do evento***
</dt> <dd>

Um valor que especifica o endereço de um computador de origem do evento. *Evento \_ de SOURCE* é uma cadeia de caracteres que identifica um computador de origem de evento usando o nome de domínio totalmente qualificado para o computador, o nome NetBIOS ou o endereço IP. Esse parâmetro pode ser usado com os parâmetros/ese,/AES,/res ou/un e/up.

</dd> <dt>

<span id="_ese_VALUE"></span><span id="_ese_value"></span><span id="_ESE_VALUE"></span>**/ESE: *valor***
</dt> <dd>

Um valor que determina se uma origem de evento deve ser habilitada ou desabilitada. O *valor* pode ser true ou false. O valor padrão é true, que habilita a origem do evento. Esse parâmetro só será usado se o parâmetro/ESA for usado.

</dd> <dt>

<span id="_aes"></span><span id="_AES"></span>**/aes**
</dt> <dd>

Um valor que adiciona a origem do evento especificada pelo parâmetro/ESA se a origem do evento ainda não faz parte da assinatura do evento. Se o computador especificado pelo parâmetro/ESA já for uma parte da assinatura, será exibido um erro. Esse parâmetro só será permitido se o parâmetro/ESA for usado.

</dd> <dt>

<span id="_res"></span><span id="_RES"></span>**/res**
</dt> <dd>

Um valor que remove a origem do evento especificada pelo parâmetro/ESA se a origem do evento já faz parte da assinatura do evento. Se o computador especificado pelo parâmetro/ESA não fizer parte da assinatura, será exibido um erro. Esse parâmetro só será permitido se o parâmetro/ESA for usado.

</dd> <dt>

<span id="_un_USERNAME"></span><span id="_un_username"></span><span id="_UN_USERNAME"></span>**/un: *nome de usuário***
</dt> <dd>

Um valor que especifica o nome de usuário usado nas credenciais para se conectar à origem do evento especificada no parâmetro/ESA. Esse parâmetro só será permitido se o parâmetro/ESA for usado.

</dd> <dt>

<span id="_up_PASSWORD"></span><span id="_up_password"></span><span id="_UP_PASSWORD"></span>**/up: *senha***
</dt> <dd>

Um valor que especifica a senha para o nome de usuário especificado no parâmetro/un. As credenciais de nome de usuário e senha são usadas para se conectar à origem do evento especificada no parâmetro/ESA. Esse parâmetro só será permitido se o parâmetro/un for usado.

</dd> <dt>

<span id="_tp_TRANSPORTPORT"></span><span id="_tp_transportport"></span><span id="_TP_TRANSPORTPORT"></span>**/TP: *TRANSPORTPORT***
</dt> <dd>

Um valor que especifica o número da porta usado pelo transporte ao se conectar a um computador de origem do evento remoto.

</dd> <dt>

<span id="_hn_NAME"></span><span id="_hn_name"></span><span id="_HN_NAME"></span>**/HN: *nome***
</dt> <dd>

Um valor que especifica o nome DNS do computador local. Esse nome é usado por fontes de eventos remotas para enviar eventos por push e deve ser usado somente para assinaturas push.

</dd> <dt>

<span id="_ct_TYPE"></span><span id="_ct_type"></span><span id="_CT_TYPE"></span>**/CT: *tipo***
</dt> <dd>

Um valor que especifica o tipo de credencial usado para acessar fontes de eventos remotas. O *tipo* pode ser "default", "Negotiate", "Digest", "Basic" ou "LocalMachine". O padrão é "default". Esses valores são definidos na enumeração [**de \_ \_ \_ tipo de credenciais de assinatura do EC**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_credentials_type) .

</dd> <dt>

<span id="_cun_USERNAME"></span><span id="_cun_username"></span><span id="_CUN_USERNAME"></span>**/cun: *nome de usuário***
</dt> <dd>

Um valor que define as credenciais de usuário compartilhadas usadas para fontes de eventos que não têm suas próprias credenciais de usuário.

> [!Note]  
> Se esse parâmetro for usado com a opção/c, as configurações de nome de usuário e senha para origens de eventos individuais do arquivo de configuração serão ignoradas. Se você quiser usar credenciais diferentes para uma origem de evento específica, poderá substituir esse valor especificando os parâmetros/un e/up para uma origem de evento específica na linha de comando de outro comando Set-Subscription.

 

</dd> <dt>

<span id="_cup_PASSWORD"></span><span id="_cup_password"></span><span id="_CUP_PASSWORD"></span>**/Cup: *senha***
</dt> <dd>

Um valor que define a senha do usuário para as credenciais de usuário compartilhado. Quando a *senha* é definida como \* (asterisco), a senha é lida no console do. Essa opção só é válida quando o parâmetro/cun é especificado.

</dd> <dt>

<span id="_ica_THUMBPRINTS"></span><span id="_ica_thumbprints"></span><span id="_ICA_THUMBPRINTS"></span>**/ICA: *impressões digitais***
</dt> <dd>

Um valor que define a lista de impressões no thumb do certificado do emissor, em uma lista separada por vírgulas.

> [!Note]  
> Essa opção é específica apenas para assinaturas iniciadas pelo código-fonte.

 

</dd> <dt>

<span id="_as_ALLOWED"></span><span id="_as_allowed"></span><span id="_AS_ALLOWED"></span>**/as: *permitido***
</dt> <dd>

Um valor que define uma lista separada por vírgulas de cadeia de caracteres que especificam os nomes DNS de computadores que não são de domínio que têm permissão para iniciar assinaturas. Os nomes podem ser especificados usando curingas, como " \* . mydomain.com". Por padrão, essa lista está vazia.

> [!Note]  
> Essa opção é específica apenas para assinaturas iniciadas pelo código-fonte.

 

</dd> <dt>

<span id="_ds_DENIED"></span><span id="_ds_denied"></span><span id="_DS_DENIED"></span>**/DS: *negado***
</dt> <dd>

Um valor que define uma lista separada por vírgulas de cadeias de caracteres que especificam os nomes DNS de computadores que não são de domínio que não têm permissão para iniciar assinaturas. Os nomes podem ser especificados usando curingas, como " \* . mydomain.com". Por padrão, essa lista está vazia.

> [!Note]  
> Essa opção é específica apenas para assinaturas iniciadas pelo código-fonte.

 

</dd> <dt>

<span id="_adc_SDDL"></span><span id="_adc_sddl"></span><span id="_ADC_SDDL"></span>**/ADC: *SDDL***
</dt> <dd>

Um valor que define uma cadeia de caracteres, no formato SDDL, que especifica quais computadores de domínio têm permissão ou não permissão para iniciar assinaturas. O padrão é permitir que todos os computadores de domínio iniciem assinaturas.

> [!Note]  
> Essa opção é específica apenas para assinaturas iniciadas pelo código-fonte.

 

</dd> </dl>

## <a name="create-a-new-subscription"></a>Criar uma nova assinatura

A sintaxe a seguir é usada para criar uma assinatura de evento para eventos em um computador remoto.

``` syntax
wecutil {cs | create-subscription } CONFIGURATION_FILE [/cun:USERNAME]
[/cup:PASSWORD] 
```

### <a name="remarks"></a>Comentários

Quando um nome de usuário ou senha incorretos for especificado no comando **wecutil cs** , nenhum erro será relatado até que você exiba o status de tempo de execução da assinatura usando o comando **wecutil gr** .

## <a name="creation-parameters"></a>Parâmetros de criação

<dl> <dt>

<span id="CONFIGURATION_FILE"></span><span id="configuration_file"></span>**arquivo de configuração \_**
</dt> <dd>

Um valor que especifica o caminho para o arquivo XML que contém informações de configuração de assinatura. O caminho pode ser absoluto ou relativo ao diretório atual.

O XML a seguir é um exemplo de um arquivo de configuração de assinatura que cria uma assinatura iniciada pelo coletor para encaminhar eventos do log de eventos do aplicativo de um computador remoto para o log ForwardedEvents.


```XML
<Subscription xmlns="http://schemas.microsoft.com/2006/03/windows/events/subscription">
    <SubscriptionId>SampleCISubscription</SubscriptionId>
    <SubscriptionType>CollectorInitiated</SubscriptionType>
    <Description>Collector Initiated Subscription Sample</Description>
    <Enabled>true</Enabled>
    <Uri>http://schemas.microsoft.com/wbem/wsman/1/windows/EventLog</Uri>

    <!-- Use Normal (default), Custom, MinLatency, MinBandwidth -->
    <ConfigurationMode>Custom</ConfigurationMode>

    <Delivery Mode="Push">
        <Batching>
            <MaxItems>20</MaxItems>
            <MaxLatencyTime>60000</MaxLatencyTime>
        </Batching>
        <PushSettings>
            <HostName>thisMachine.myDomain.com</HostName>
            <Heartbeat Interval="60000"/>
        </PushSettings>
    </Delivery>

    <Expires>2010-01-01T00:00:00.000Z</Expires>

    <Query>
        <![CDATA[
            <QueryList>
                <Query Path="Application">
                    <Select>*</Select>
                </Query>
            </QueryList>
        ]]>
    </Query>

    <ReadExistingEvents>false</ReadExistingEvents>
    <TransportName>http</TransportName>
    <ContentFormat>RenderedText</ContentFormat>
    <Locale Language="en-US"/>
    <LogFile>ForwardedEvents</LogFile>
    <CredentialsType>Default</CredentialsType>

    <EventSources>
        <EventSource Enabled="true">
            <Address>mySource.myDomain.com</Address>
            <UserName>myUserName</UserName>
        </EventSource>
    </EventSources>
</Subscription>
```



O XML a seguir é um exemplo de um arquivo de configuração de assinatura que cria uma assinatura iniciada de origem para encaminhar eventos do log de eventos do aplicativo de um computador remoto para o log ForwardedEvents.


```XML
<Subscription xmlns="http://schemas.microsoft.com/2006/03/windows/events/subscription">
    <SubscriptionId>SampleSISubscription</SubscriptionId>
    <SubscriptionType>SourceInitiated</SubscriptionType>
    <Description>Source Initiated Subscription Sample</Description>
    <Enabled>true</Enabled>
    <Uri>http://schemas.microsoft.com/wbem/wsman/1/windows/EventLog</Uri>

    <!-- Use Normal (default), Custom, MinLatency, MinBandwidth -->
    <ConfigurationMode>Custom</ConfigurationMode>

    <Delivery Mode="Push">
        <Batching>
            <MaxItems>1</MaxItems>
            <MaxLatencyTime>1000</MaxLatencyTime>
        </Batching>
        <PushSettings>
            <Heartbeat Interval="60000"/>
        </PushSettings>
    </Delivery>

    <Expires>2018-01-01T00:00:00.000Z</Expires>

    <Query>
        <![CDATA[
            <QueryList>
                <Query Path="Application">
                    <Select>Event[System/EventID='999']</Select>
                </Query>
            </QueryList>
        ]]>
    </Query>

    <ReadExistingEvents>true</ReadExistingEvents>
    <TransportName>http</TransportName>
    <ContentFormat>RenderedText</ContentFormat>
    <Locale Language="en-US"/>
    <LogFile>ForwardedEvents</LogFile>
    <AllowedSourceNonDomainComputers></AllowedSourceNonDomainComputers>
    <AllowedSourceDomainComputers>O:NSG:NSD:(A;;GA;;;DC)(A;;GA;;;NS)</AllowedSourceDomainComputers>
</Subscription>
```



> [!Note]  
> Ao criar uma assinatura iniciada pela origem, se **AllowedSourceDomainComputers**, **AllowedSourceNonDomainComputers** / **IssuerCAList**, **AllowedSubjectList** e **DeniedSubjectList** estiverem todos vazios, um padrão será fornecido para **AllowedSourceDomainComputers** -"O:NSG: NSD: (a;; GA;;;D C) (A;; GA;;; NS) ". Esse padrão de SDDL concede membros do grupo de domínio computadores de domínio, bem como o grupo de serviços de rede local (para o encaminhador local), a capacidade de gerar eventos para essa assinatura.

 

</dd> <dt>

<span id="_cun_USERNAME"></span><span id="_cun_username"></span><span id="_CUN_USERNAME"></span>**/cun: *nome de usuário***
</dt> <dd>

Um valor que define as credenciais de usuário compartilhadas usadas para fontes de eventos que não têm suas próprias credenciais de usuário. Esse valor se aplica somente às assinaturas iniciadas pelo coletor.

> [!Note]  
> Se esse parâmetro for especificado, as configurações de nome de usuário e senha para origens de eventos individuais do arquivo de configuração serão ignoradas. Se você quiser usar credenciais diferentes para uma origem de evento específica, poderá substituir esse valor especificando os parâmetros/un e/up para uma origem de evento específica na linha de comando de outro comando Set-Subscription.

 

</dd> <dt>

<span id="_cup_PASSWORD"></span><span id="_cup_password"></span><span id="_CUP_PASSWORD"></span>**/Cup: *senha***
</dt> <dd>

Um valor que define a senha do usuário para as credenciais de usuário compartilhado. Quando a *senha* for definida como " \* " (asterisco), a senha será lida no console do. Essa opção só é válida quando o parâmetro/cun é especificado.

</dd> </dl>

## <a name="delete-a-subscription"></a>Excluir uma assinatura

A sintaxe a seguir é usada para excluir uma assinatura de evento.

``` syntax
wecutil { ds | delete-subscription } SUBSCRIPTION_ID
```

## <a name="deletion-parameters"></a>Parâmetros de exclusão

<dl> <dt>

<span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**ID da assinatura \_**
</dt> <dd>

Uma cadeia de caracteres que identifica exclusivamente uma assinatura. Esse identificador é especificado no elemento **SubscriptionId** no arquivo de configuração XML usado para criar a assinatura. A assinatura identificada neste parâmetro será excluída.

</dd> </dl>

## <a name="retry-a-subscription"></a>Repetir uma assinatura

A sintaxe a seguir é usada para repetir uma assinatura inativa ao tentar reativar todas as fontes de evento ou origens de eventos específicas, estabelecendo uma conexão com cada origem de evento e enviando uma solicitação de assinatura remota para a origem do evento. As fontes de eventos desabilitadas não são repetidas.

``` syntax
wecutil { rs | retry-subscription } SUBSCRIPTION_ID 
[EVENT_SOURCE [EVENT_SOURCE] ...]
```

## <a name="retry-parameters"></a>Parâmetros de repetição

<dl> <dt>

<span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**ID da assinatura \_**
</dt> <dd>

Uma cadeia de caracteres que identifica exclusivamente uma assinatura. Esse identificador é especificado no elemento **SubscriptionId** no arquivo de configuração XML usado para criar a assinatura. A assinatura identificada neste parâmetro será repetida.

</dd> <dt>

<span id="EVENT_SOURCE"></span><span id="event_source"></span>**origem do evento \_**
</dt> <dd>

Um valor que identifica um computador que é uma origem de evento para uma assinatura de evento. Esse valor pode ser o nome de domínio totalmente qualificado para o computador, o nome NetBIOS ou o endereço IP.

</dd> </dl>

## <a name="configure-the-windows-event-collector-service"></a>Configurar o serviço coletor de eventos do Windows

A sintaxe a seguir é usada para configurar o serviço coletor de eventos do Windows para garantir que as assinaturas de evento possam ser criadas e mantidas por meio de reinicializações do computador. Isso inclui o seguinte procedimento:

**Para configurar o serviço coletor de eventos do Windows**

1.  Habilite o canal ForwardedEvents se ele estiver desabilitado.
2.  Atrase o início do serviço coletor de eventos do Windows.
3.  Inicie o serviço coletor de eventos do Windows se ele não estiver em execução.

``` syntax
wecutil { qc | quick-config } /q:VALUE
```

## <a name="configure-event-collector-parameters"></a>Configurar parâmetros do coletor de eventos

<dl> <dt>

<span id="_q_VALUE"></span><span id="_q_value"></span><span id="_Q_VALUE"></span>**/q: *valor***
</dt> <dd>

Um valor que determina se o comando de configuração rápida solicitará confirmação. O valor pode ser true ou false. Se VALUE for true, o comando solicitará a confirmação. O valor padrão é false.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |



 

 





