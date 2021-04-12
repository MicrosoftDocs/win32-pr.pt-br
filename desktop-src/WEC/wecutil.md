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
# <a name="wecutilexe"></a><span data-ttu-id="a97c9-104">Wecutil.exe</span><span class="sxs-lookup"><span data-stu-id="a97c9-104">Wecutil.exe</span></span>

<span data-ttu-id="a97c9-105">Wecutil.exe é um utilitário coletor de eventos do Windows que permite que um administrador crie e gerencie assinaturas para eventos encaminhados de fontes de eventos remotas que dão suporte ao protocolo WS-Management.</span><span class="sxs-lookup"><span data-stu-id="a97c9-105">Wecutil.exe is a Windows Event Collector utility that enables an administrator to create and manage subscriptions to events forwarded from remote event sources that support the WS-Management protocol.</span></span> <span data-ttu-id="a97c9-106">Comandos, opções e valores de opção não diferenciam maiúsculas de minúsculas para este utilitário.</span><span class="sxs-lookup"><span data-stu-id="a97c9-106">Commands, options, and option values are case-insensitive for this utility.</span></span>

<span data-ttu-id="a97c9-107">Se você receber uma mensagem dizendo "o servidor RPC não está disponível" ou "a interface é desconhecida" ao tentar executar wecutil, será necessário iniciar o serviço coletor de eventos do Windows (Wecsvc).</span><span class="sxs-lookup"><span data-stu-id="a97c9-107">If you receive a message that says "The RPC server is unavailable" or "The interface is unknown" when you try to run wecutil, then you need to start the Windows Event Collector service (wecsvc).</span></span> <span data-ttu-id="a97c9-108">Para iniciar o Wecsvc, em um prompt de comandos com privilégios elevados, digite **net start Wecsvc**.</span><span class="sxs-lookup"><span data-stu-id="a97c9-108">To start wecsvc, at an elevated command prompt type **net start wecsvc**.</span></span>

## <a name="list-existing-subscriptions"></a><span data-ttu-id="a97c9-109">Listar assinaturas existentes</span><span class="sxs-lookup"><span data-stu-id="a97c9-109">List existing subscriptions</span></span>

<span data-ttu-id="a97c9-110">A sintaxe a seguir é usada para listar assinaturas de evento remoto existentes.</span><span class="sxs-lookup"><span data-stu-id="a97c9-110">The following syntax is used to list existing remote event subscriptions.</span></span>

``` syntax
wecutil { es | enum-subscription }
```

<span data-ttu-id="a97c9-111">Se você usar um script para obter os nomes das assinaturas da saída, será necessário ignorar os caracteres da BOM UTF-8 na primeira linha da saída.</span><span class="sxs-lookup"><span data-stu-id="a97c9-111">If you use a script to get the names of the subscriptions from the output, you will need to bypass the UTF-8 BOM characters in the first line of the output.</span></span> <span data-ttu-id="a97c9-112">O script a seguir mostra um exemplo de como você pode ignorar os caracteres da BOM.</span><span class="sxs-lookup"><span data-stu-id="a97c9-112">The following script shows an example of how you might skip the BOM characters.</span></span>

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

## <a name="get-subscription-configuration"></a><span data-ttu-id="a97c9-113">Obter configuração de assinatura</span><span class="sxs-lookup"><span data-stu-id="a97c9-113">Get subscription configuration</span></span>

<span data-ttu-id="a97c9-114">A sintaxe a seguir é usada para exibir dados de configuração de assinatura de evento remoto.</span><span class="sxs-lookup"><span data-stu-id="a97c9-114">The following syntax is used to display remote event subscription configuration data.</span></span>

``` syntax
wecutil { gs | get-subscription } SUBSCRIPTION_ID [/f:VALUE 
[/u:VALUE] ...]
```

## <a name="get-configuration-parameters"></a><span data-ttu-id="a97c9-115">Obter parâmetros de configuração</span><span class="sxs-lookup"><span data-stu-id="a97c9-115">Get Configuration Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a97c9-116"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**ID da assinatura \_**</span><span class="sxs-lookup"><span data-stu-id="a97c9-116"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**SUBSCRIPTION\_ID**</span></span>
</dt> <dd>

<span data-ttu-id="a97c9-117">Uma cadeia de caracteres que identifica exclusivamente uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="a97c9-117">A string that uniquely identifies a subscription.</span></span> <span data-ttu-id="a97c9-118">Esse identificador é especificado no elemento **SubscriptionId** no arquivo de configuração XML usado para criar a assinatura.</span><span class="sxs-lookup"><span data-stu-id="a97c9-118">This identifier is specified in the **SubscriptionId** element in the XML configuration file used to create the subscription.</span></span>

</dd> <dt>

<span data-ttu-id="a97c9-119"><span id="_f_VALUE"></span><span id="_f_value"></span><span id="_F_VALUE"></span>**/f: \* valor**\*</span><span class="sxs-lookup"><span data-stu-id="a97c9-119"><span id="_f_VALUE"></span><span id="_f_value"></span><span id="_F_VALUE"></span>**/f:\*VALUE**\*</span></span>
</dt> <dd>

<span data-ttu-id="a97c9-120">Um valor que especifica a saída dos dados de configuração da assinatura.</span><span class="sxs-lookup"><span data-stu-id="a97c9-120">A value that specifies the output of the subscription configuration data.</span></span> <span data-ttu-id="a97c9-121">O *valor* pode ser "XML" ou "conciso", e o padrão é "conciso".</span><span class="sxs-lookup"><span data-stu-id="a97c9-121">*VALUE* can be "XML" or "Terse", and the default is "Terse".</span></span> <span data-ttu-id="a97c9-122">Se *Value* for "XML", a saída será impressa no formato "XML".</span><span class="sxs-lookup"><span data-stu-id="a97c9-122">If *VALUE* is "XML", then the output is printed in "XML" format.</span></span> <span data-ttu-id="a97c9-123">Se *Value* for "conciso", a saída será impressa em pares de nome-valor.</span><span class="sxs-lookup"><span data-stu-id="a97c9-123">If *VALUE* is "Terse", then the output is printed in name-value pairs.</span></span>

</dd> <dt>

<span data-ttu-id="a97c9-124"><span id="_u_VALUE"></span><span id="_u_value"></span><span id="_U_VALUE"></span>**/u: *valor***</span><span class="sxs-lookup"><span data-stu-id="a97c9-124"><span id="_u_VALUE"></span><span id="_u_value"></span><span id="_U_VALUE"></span>**/u: *VALUE***</span></span>
</dt> <dd>

<span data-ttu-id="a97c9-125">Um valor que especifica se a saída está no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="a97c9-125">A value that specifies whether the output is in Unicode format.</span></span> <span data-ttu-id="a97c9-126">O *valor* pode ser "true" ou "false".</span><span class="sxs-lookup"><span data-stu-id="a97c9-126">*VALUE* can be "true" or "false".</span></span> <span data-ttu-id="a97c9-127">Se *Value* for "true", a saída estará no formato Unicode e, se *Value* for "false", a saída não estará no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="a97c9-127">If *VALUE* is "true", then the output is in Unicode format, and if *VALUE* is "false", then the output is not in Unicode format.</span></span>

</dd> </dl>

## <a name="get-subscription-runtime-status"></a><span data-ttu-id="a97c9-128">Obter status do tempo de execução da assinatura</span><span class="sxs-lookup"><span data-stu-id="a97c9-128">Get subscription runtime status</span></span>

<span data-ttu-id="a97c9-129">A sintaxe a seguir é usada para exibir o status do tempo de execução da assinatura.</span><span class="sxs-lookup"><span data-stu-id="a97c9-129">The following syntax is used to display the subscription runtime status.</span></span>

``` syntax
wecutil { gr | get-subscriptionruntimestatus } SUBSCRIPTION_ID
 [EVENT_SOURCE [EVENT_SOURCE] ...]
```

## <a name="get-status-parameters"></a><span data-ttu-id="a97c9-130">Obter parâmetros de status</span><span class="sxs-lookup"><span data-stu-id="a97c9-130">Get Status Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a97c9-131"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**ID da assinatura \_**</span><span class="sxs-lookup"><span data-stu-id="a97c9-131"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**SUBSCRIPTION\_ID**</span></span>
</dt> <dd>

<span data-ttu-id="a97c9-132">Uma cadeia de caracteres que identifica exclusivamente uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="a97c9-132">A string that uniquely identifies a subscription.</span></span> <span data-ttu-id="a97c9-133">Esse identificador é especificado no elemento **SubscriptionId** no arquivo de configuração XML usado para criar a assinatura.</span><span class="sxs-lookup"><span data-stu-id="a97c9-133">This identifier is specified in the **SubscriptionId** element in the XML configuration file used to create the subscription.</span></span>

</dd> <dt>

<span data-ttu-id="a97c9-134"><span id="EVENT_SOURCE"></span><span id="event_source"></span>**origem do evento \_**</span><span class="sxs-lookup"><span data-stu-id="a97c9-134"><span id="EVENT_SOURCE"></span><span id="event_source"></span>**EVENT\_SOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="a97c9-135">Um valor que identifica um computador que é uma origem de evento para uma assinatura de evento.</span><span class="sxs-lookup"><span data-stu-id="a97c9-135">A value that identifies a computer that is an event source for an event subscription.</span></span> <span data-ttu-id="a97c9-136">Esse valor pode ser o nome de domínio totalmente qualificado para o computador, o nome NetBIOS ou o endereço IP.</span><span class="sxs-lookup"><span data-stu-id="a97c9-136">This value can be the fully qualified domain name for the computer, NetBIOS name, or IP address.</span></span>

</dd> </dl>

## <a name="set-subscription-configuration-information"></a><span data-ttu-id="a97c9-137">Definir informações de configuração de assinatura</span><span class="sxs-lookup"><span data-stu-id="a97c9-137">Set Subscription Configuration Information</span></span>

<span data-ttu-id="a97c9-138">A sintaxe a seguir é usada para definir os dados de configuração da assinatura alterando os parâmetros de assinatura da linha de comando ou usando um arquivo de configuração XML.</span><span class="sxs-lookup"><span data-stu-id="a97c9-138">The following syntax is used to set subscription configuration data by changing subscription parameters from the command line or using an XML configuration file.</span></span>

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

### <a name="remarks"></a><span data-ttu-id="a97c9-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="a97c9-139">Remarks</span></span>

<span data-ttu-id="a97c9-140">Quando um nome de usuário ou senha incorretos for especificado no comando **wecutil SS** , nenhum erro será relatado até que você exiba o status de tempo de execução da assinatura usando o comando **wecutil gr** .</span><span class="sxs-lookup"><span data-stu-id="a97c9-140">When an incorrect username or password is specified in the **wecutil ss** command, no error is reported until you view the runtime status of the subscription using the **wecutil gr** command.</span></span>

## <a name="set-configuration-parameters"></a><span data-ttu-id="a97c9-141">Definir parâmetros de configuração</span><span class="sxs-lookup"><span data-stu-id="a97c9-141">Set Configuration Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a97c9-142"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**ID da assinatura \_**</span><span class="sxs-lookup"><span data-stu-id="a97c9-142"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**SUBSCRIPTION\_ID**</span></span>
</dt> <dd>

<span data-ttu-id="a97c9-143">Uma cadeia de caracteres que identifica exclusivamente uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="a97c9-143">A string that uniquely identifies a subscription.</span></span> <span data-ttu-id="a97c9-144">Esse identificador é especificado no elemento **SubscriptionId** no arquivo de configuração XML usado para criar a assinatura.</span><span class="sxs-lookup"><span data-stu-id="a97c9-144">This identifier is specified in the **SubscriptionId** element in the XML configuration file used to create the subscription.</span></span>

</dd> <dt>

<span data-ttu-id="a97c9-145"><span id="_c_CONGIG_FILE"></span><span id="_c_congig_file"></span><span id="_C_CONGIG_FILE"></span>**/c: *\_ arquivo CONGIG***</span><span class="sxs-lookup"><span data-stu-id="a97c9-145"><span id="_c_CONGIG_FILE"></span><span id="_c_congig_file"></span><span id="_C_CONGIG_FILE"></span>**/c: *CONGIG\_FILE***</span></span>
</dt> <dd>

<span data-ttu-id="a97c9-146">Um valor que especifica o caminho para o arquivo XML que contém informações de configuração de assinatura.</span><span class="sxs-lookup"><span data-stu-id="a97c9-146">A value that specifies the path to the XML file that contains subscription configuration information.</span></span> <span data-ttu-id="a97c9-147">O caminho pode ser absoluto ou relativo ao diretório atual.</span><span class="sxs-lookup"><span data-stu-id="a97c9-147">The path can be absolute or relative to the current directory.</span></span> <span data-ttu-id="a97c9-148">Esse parâmetro só pode ser usado com os parâmetros optional/cus e/Cup, e é mutuamente exclusivo com todos os outros parâmetros.</span><span class="sxs-lookup"><span data-stu-id="a97c9-148">This parameter can only be used with the optional /cus and /cup parameters, and is mutually exclusive with all the other parameters.</span></span>

</dd> <dt>

<span data-ttu-id="a97c9-149"><span id="_e_VALUE"></span><span id="_e_value"></span><span id="_E_VALUE"></span>**/e: *valor***</span><span class="sxs-lookup"><span data-stu-id="a97c9-149"><span id="_e_VALUE"></span><span id="_e_value"></span><span id="_E_VALUE"></span>**/e: *VALUE***</span></span>
</dt> <dd>

<span data-ttu-id="a97c9-150">Um valor que determina se a assinatura deve ser habilitada ou desabilitada.</span><span class="sxs-lookup"><span data-stu-id="a97c9-150">A value that determines whether to enable or disable the subscription.</span></span> <span data-ttu-id="a97c9-151">O valor pode ser true ou false.</span><span class="sxs-lookup"><span data-stu-id="a97c9-151">VALUE can be true or false.</span></span> <span data-ttu-id="a97c9-152">O valor padrão é true, que habilita a assinatura.</span><span class="sxs-lookup"><span data-stu-id="a97c9-152">The default value is true, which enables the subscription.</span></span>

> [!Note]  
> <span data-ttu-id="a97c9-153">Quando você desabilita uma assinatura iniciada pelo coletor, a origem do evento se torna inativa em vez de desabilitada.</span><span class="sxs-lookup"><span data-stu-id="a97c9-153">When you disable a collector initiated subscription, the event source becomes inactive instead of disabled.</span></span> <span data-ttu-id="a97c9-154">Em uma assinatura iniciada pelo coletor, você pode desabilitar uma origem de evento independente da assinatura.</span><span class="sxs-lookup"><span data-stu-id="a97c9-154">In a collector initiated subscription, you can disable an event source independent of the subscription.</span></span>

 

</dd> <dt>

<span data-ttu-id="a97c9-155"><span id="_d_DESCRIPTION"></span><span id="_d_description"></span><span id="_D_DESCRIPTION"></span>**/d: *Descrição***</span><span class="sxs-lookup"><span data-stu-id="a97c9-155"><span id="_d_DESCRIPTION"></span><span id="_d_description"></span><span id="_D_DESCRIPTION"></span>**/d: *DESCRIPTION***</span></span>
</dt> <dd>

<span data-ttu-id="a97c9-156">Um valor que especifica uma descrição para a assinatura de evento.</span><span class="sxs-lookup"><span data-stu-id="a97c9-156">A value that specifies a description for the event subscription.</span></span>

</dd> <dt>

<span data-ttu-id="a97c9-157"><span id="_ex_DATE_TIME"></span><span id="_ex_date_time"></span><span id="_EX_DATE_TIME"></span>**/ex: *data e \_ hora***</span><span class="sxs-lookup"><span data-stu-id="a97c9-157"><span id="_ex_DATE_TIME"></span><span id="_ex_date_time"></span><span id="_EX_DATE_TIME"></span>**/ex: *DATE\_TIME***</span></span>
</dt> <dd>

<span data-ttu-id="a97c9-158">Um valor que especifica o tempo de expiração da assinatura.</span><span class="sxs-lookup"><span data-stu-id="a97c9-158">A value that specifies the subscription expiration time.</span></span> <span data-ttu-id="a97c9-159">*Data de início \_ O tempo* é um valor especificado no formato de data/hora padrão XML ou ISO8601: "aaaa-mm-ddThh: mm: SS \[ . SSS \] \[ Z \] ", em que "T" é o separador de tempo e "Z" indica a hora UTC.</span><span class="sxs-lookup"><span data-stu-id="a97c9-159">*DATE\_TIME* is a value specified in standard XML or ISO8601 date-time format: "yyyy-MM-ddThh:mm:ss\[.sss\]\[Z\]" where "T" is the time separator and "Z" indicates UTC time.</span></span> <span data-ttu-id="a97c9-160">Por exemplo, se *data e \_ hora* for "2007-01-12T01:20:00", o tempo de expiração da assinatura será 12 de janeiro de 2007, 01:20.</span><span class="sxs-lookup"><span data-stu-id="a97c9-160">For example, if *DATE\_TIME* is "2007-01-12T01:20:00", then the subscription expiration time is January 12th, 2007, 01:20.</span></span>

</dd> <dt>

<span data-ttu-id="a97c9-161"><span id="_uri_URI"></span><span id="_uri_uri"></span><span id="_URI_URI"></span>**/URI: *URI***</span><span class="sxs-lookup"><span data-stu-id="a97c9-161"><span id="_uri_URI"></span><span id="_uri_uri"></span><span id="_URI_URI"></span>**/uri: *URI***</span></span>
</dt> <dd>

<span data-ttu-id="a97c9-162">Um valor que especifica o tipo de eventos consumidos pela assinatura.</span><span class="sxs-lookup"><span data-stu-id="a97c9-162">A value that specifies the type of events consumed by the subscription.</span></span> <span data-ttu-id="a97c9-163">O endereço do computador de origem do evento junto com o URI (Uniform Resource Identifier) identifica exclusivamente a origem dos eventos.</span><span class="sxs-lookup"><span data-stu-id="a97c9-163">The address of the event source computer along with the uniform resource identifier (URI) uniquely identifies the source of the events.</span></span> <span data-ttu-id="a97c9-164">A cadeia de caracteres do URI é usada para todos os endereços de origem do evento na assinatura.</span><span class="sxs-lookup"><span data-stu-id="a97c9-164">The URI string is used for all event source addresses in the subscription.</span></span>

</dd> <dt>

<span data-ttu-id="a97c9-165"><span id="_cm_CONFIGURATION_MODE"></span><span id="_cm_configuration_mode"></span><span id="_CM_CONFIGURATION_MODE"></span>**/cm: *\_ modo de configuração***</span><span class="sxs-lookup"><span data-stu-id="a97c9-165"><span id="_cm_CONFIGURATION_MODE"></span><span id="_cm_configuration_mode"></span><span id="_CM_CONFIGURATION_MODE"></span>**/cm: *CONFIGURATION\_MODE***</span></span>
</dt> <dd>

<span data-ttu-id="a97c9-166">Um valor que especifica o modo de configuração da assinatura de evento.</span><span class="sxs-lookup"><span data-stu-id="a97c9-166">A value that specifies the configuration mode of the event subscription.</span></span> <span data-ttu-id="a97c9-167">*Configuração \_ do O modo* pode ser uma das seguintes cadeias de caracteres: "normal", "Custom", "MinLatency" ou "MinBandwidth".</span><span class="sxs-lookup"><span data-stu-id="a97c9-167">*CONFIGURATION\_MODE* can be one of the following strings: "Normal", "Custom", "MinLatency", or "MinBandwidth".</span></span> <span data-ttu-id="a97c9-168">A enumeração do modo de configuração de assinatura do EC define os modos de configuração. [**\_ \_ \_**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_configuration_mode)</span><span class="sxs-lookup"><span data-stu-id="a97c9-168">The [**EC\_SUBSCRIPTION\_CONFIGURATION\_MODE**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_configuration_mode) enumeration defines the configuration modes.</span></span> <span data-ttu-id="a97c9-169">Os parâmetros/DM,/DMI,/Hi e/dmlt só poderão ser especificados se o modo de configuração for definido como personalizado.</span><span class="sxs-lookup"><span data-stu-id="a97c9-169">The /dm, /dmi, /hi, and /dmlt parameters can only be specified if the configuration mode is set to Custom.</span></span>

</dd> <dt>

<span data-ttu-id="a97c9-170"><span id="_q_QUERY"></span><span id="_q_query"></span><span id="_Q_QUERY"></span>**/q: *consulta***</span><span class="sxs-lookup"><span data-stu-id="a97c9-170"><span id="_q_QUERY"></span><span id="_q_query"></span><span id="_Q_QUERY"></span>**/q: *QUERY***</span></span>
</dt> <dd>

<span data-ttu-id="a97c9-171">Um valor que especifica a cadeia de caracteres de consulta para a assinatura.</span><span class="sxs-lookup"><span data-stu-id="a97c9-171">A value that specifies the query string for the subscription.</span></span> <span data-ttu-id="a97c9-172">O formato dessa cadeia de caracteres pode ser diferente para valores de URI diferentes e se aplica a todas as origens de evento na assinatura.</span><span class="sxs-lookup"><span data-stu-id="a97c9-172">The format of this string can be different for different URI values and applies to all event sources in the subscription.</span></span>

</dd> <dt>

<span data-ttu-id="a97c9-173"><span id="_dia_DIALECT"></span><span id="_dia_dialect"></span><span id="_DIA_DIALECT"></span>**/dia: *dialeto***</span><span class="sxs-lookup"><span data-stu-id="a97c9-173"><span id="_dia_DIALECT"></span><span id="_dia_dialect"></span><span id="_DIA_DIALECT"></span>**/dia: *DIALECT***</span></span>
</dt> <dd>

<span data-ttu-id="a97c9-174">Um valor que especifica o dialeto que a cadeia de caracteres de consulta usa.</span><span class="sxs-lookup"><span data-stu-id="a97c9-174">A value that specifies the dialect the query string uses.</span></span>

</dd> <dt>

<span data-ttu-id="a97c9-175"><span id="_cf_FORMAT"></span><span id="_cf_format"></span><span id="_CF_FORMAT"></span>**/CF: *formato***</span><span class="sxs-lookup"><span data-stu-id="a97c9-175"><span id="_cf_FORMAT"></span><span id="_cf_format"></span><span id="_CF_FORMAT"></span>**/cf: *FORMAT***</span></span>
</dt> <dd>

<span data-ttu-id="a97c9-176">Um valor que especifica o formato dos eventos retornados.</span><span class="sxs-lookup"><span data-stu-id="a97c9-176">A value that specifies the format of the returned events.</span></span> <span data-ttu-id="a97c9-177">O *formato* pode ser "Events" ou "RenderedText".</span><span class="sxs-lookup"><span data-stu-id="a97c9-177">*FORMAT* can be "Events" or "RenderedText".</span></span> <span data-ttu-id="a97c9-178">Quando o valor é "RenderedText", os eventos são retornados com as cadeias de caracteres localizadas (como cadeias de caracteres de descrição do evento) anexadas aos eventos.</span><span class="sxs-lookup"><span data-stu-id="a97c9-178">When the value is "RenderedText", the events are returned with the localized strings (such as event description strings) attached to the events.</span></span> <span data-ttu-id="a97c9-179">O valor padrão do *formato* é "RenderedText".</span><span class="sxs-lookup"><span data-stu-id="a97c9-179">The default value of *FORMAT* is "RenderedText".</span></span>

</dd> <dt>

<span data-ttu-id="a97c9-180"><span id="_l_LOCALE"></span><span id="_l_locale"></span><span id="_L_LOCALE"></span>**/l: *localidade***</span><span class="sxs-lookup"><span data-stu-id="a97c9-180"><span id="_l_LOCALE"></span><span id="_l_locale"></span><span id="_L_LOCALE"></span>**/l: *LOCALE***</span></span>
</dt> <dd>

<span data-ttu-id="a97c9-181">Um valor que especifica a localidade para entrega das cadeias de caracteres localizadas no formato de texto renderizado.</span><span class="sxs-lookup"><span data-stu-id="a97c9-181">A value that specifies the locale for delivery of the localized strings in rendered text format.</span></span> <span data-ttu-id="a97c9-182">A *localidade* é um identificador de cultura de idioma/país, por exemplo, "en-US".</span><span class="sxs-lookup"><span data-stu-id="a97c9-182">*LOCALE* is a language/country culture identifier, for example, "EN-us".</span></span> <span data-ttu-id="a97c9-183">Esse parâmetro só é válido quando o parâmetro/CF é definido como "RenderedText".</span><span class="sxs-lookup"><span data-stu-id="a97c9-183">This parameter is only valid when the /cf parameter is set to "RenderedText".</span></span>

</dd> <dt>

<span data-ttu-id="a97c9-184"><span id="_ree__VALUE_"></span><span id="_ree__value_"></span><span id="_REE__VALUE_"></span>**/Ree: \[ *valor*\]**</span><span class="sxs-lookup"><span data-stu-id="a97c9-184"><span id="_ree__VALUE_"></span><span id="_ree__value_"></span><span id="_REE__VALUE_"></span>**/ree:\[*VALUE*\]**</span></span>
</dt> <dd>

<span data-ttu-id="a97c9-185">Um valor que especifica quais eventos devem ser entregues para a assinatura.</span><span class="sxs-lookup"><span data-stu-id="a97c9-185">A value that specifies which events are to be delivered for the subscription.</span></span> <span data-ttu-id="a97c9-186">O *valor* pode ser true ou false.</span><span class="sxs-lookup"><span data-stu-id="a97c9-186">*VALUE* can be true or false.</span></span> <span data-ttu-id="a97c9-187">Quando o *valor* for true, todos os eventos existentes serão lidos das fontes de evento de assinatura.</span><span class="sxs-lookup"><span data-stu-id="a97c9-187">When *VALUE* is true, all existing events are read from the subscription event sources.</span></span> <span data-ttu-id="a97c9-188">Quando o *valor* for false, somente os eventos futuros (chegando) serão entregues.</span><span class="sxs-lookup"><span data-stu-id="a97c9-188">When *VALUE* is false, only future (arriving) events are delivered.</span></span> <span data-ttu-id="a97c9-189">O padrão é true quando/Ree é especificado sem um valor, e o padrão é false se/Ree não for especificado.</span><span class="sxs-lookup"><span data-stu-id="a97c9-189">The default is true when /ree is specified without a value, and the default is false if /ree is not specified.</span></span>

</dd> <dt>

<span data-ttu-id="a97c9-190"><span id="_lf_FILENAME"></span><span id="_lf_filename"></span><span id="_LF_FILENAME"></span>**/LF: *filename***</span><span class="sxs-lookup"><span data-stu-id="a97c9-190"><span id="_lf_FILENAME"></span><span id="_lf_filename"></span><span id="_LF_FILENAME"></span>**/lf: *FILENAME***</span></span>
</dt> <dd>

<span data-ttu-id="a97c9-191">Um valor que especifica o log de eventos local que é usado para armazenar eventos recebidos da assinatura de evento.</span><span class="sxs-lookup"><span data-stu-id="a97c9-191">A value that specifies the local event log that is used to store events received from the event subscription.</span></span>

</dd> <dt>

<span data-ttu-id="a97c9-192"><span id="_pn_PUBLISHER"></span><span id="_pn_publisher"></span><span id="_PN_PUBLISHER"></span>**/PN: *Publicador***</span><span class="sxs-lookup"><span data-stu-id="a97c9-192"><span id="_pn_PUBLISHER"></span><span id="_pn_publisher"></span><span id="_PN_PUBLISHER"></span>**/pn: *PUBLISHER***</span></span>
</dt> <dd>

<span data-ttu-id="a97c9-193">Um valor que especifica o nome do editor de eventos (provedor).</span><span class="sxs-lookup"><span data-stu-id="a97c9-193">A value that specifies the event publisher (provider) name.</span></span> <span data-ttu-id="a97c9-194">Ele deve ser um Publicador que possui ou importa o log especificado pelo parâmetro/LF.</span><span class="sxs-lookup"><span data-stu-id="a97c9-194">It must be a publisher which owns or imports the log specified by the /lf parameter.</span></span>

</dd> <dt>

<span data-ttu-id="a97c9-195"><span id="_dm_MODE"></span><span id="_dm_mode"></span><span id="_DM_MODE"></span>**/DM: *modo***</span><span class="sxs-lookup"><span data-stu-id="a97c9-195"><span id="_dm_MODE"></span><span id="_dm_mode"></span><span id="_DM_MODE"></span>**/dm: *MODE***</span></span>
</dt> <dd>

<span data-ttu-id="a97c9-196">Um valor que especifica o modo de entrega da assinatura.</span><span class="sxs-lookup"><span data-stu-id="a97c9-196">A value that specifies the subscription delivery mode.</span></span> <span data-ttu-id="a97c9-197">O *modo* pode ser Push ou pull.</span><span class="sxs-lookup"><span data-stu-id="a97c9-197">*MODE* can be either push or pull.</span></span> <span data-ttu-id="a97c9-198">Essa opção só será válida se o parâmetro/cm for definido como Custom.</span><span class="sxs-lookup"><span data-stu-id="a97c9-198">This option is only valid if the /cm parameter is set to Custom.</span></span>

</dd> <dt>

<span data-ttu-id="a97c9-199"><span id="_dmi_NUMBER"></span><span id="_dmi_number"></span><span id="_DMI_NUMBER"></span>**/DMI: *número***</span><span class="sxs-lookup"><span data-stu-id="a97c9-199"><span id="_dmi_NUMBER"></span><span id="_dmi_number"></span><span id="_DMI_NUMBER"></span>**/dmi: *NUMBER***</span></span>
</dt> <dd>

<span data-ttu-id="a97c9-200">Um valor que especifica o número máximo de itens para entrega em lote na assinatura do evento.</span><span class="sxs-lookup"><span data-stu-id="a97c9-200">A value that specifies the maximum number of items for batched delivery in the event subscription.</span></span> <span data-ttu-id="a97c9-201">Essa opção só será válida se o parâmetro/cm for definido como Custom.</span><span class="sxs-lookup"><span data-stu-id="a97c9-201">This option is only valid if the /cm parameter is set to Custom.</span></span>

</dd> <dt>

<span data-ttu-id="a97c9-202"><span id="_dmlt_MS"></span><span id="_dmlt_ms"></span><span id="_DMLT_MS"></span>**/dmlt: *MS***</span><span class="sxs-lookup"><span data-stu-id="a97c9-202"><span id="_dmlt_MS"></span><span id="_dmlt_ms"></span><span id="_DMLT_MS"></span>**/dmlt: *MS***</span></span>
</dt> <dd>

<span data-ttu-id="a97c9-203">Um valor que especifica a latência máxima permitida no fornecimento de um lote de eventos.</span><span class="sxs-lookup"><span data-stu-id="a97c9-203">A value that specifies the maximum latency allowed in delivering a batch of events.</span></span> <span data-ttu-id="a97c9-204">MS é o número de milissegundos permitidos.</span><span class="sxs-lookup"><span data-stu-id="a97c9-204">MS is the number of milliseconds allowed.</span></span> <span data-ttu-id="a97c9-205">Esse parâmetro só será válido se o parâmetro/cm for definido como Custom.</span><span class="sxs-lookup"><span data-stu-id="a97c9-205">This parameter is only valid if the /cm parameter is set to Custom.</span></span>

</dd> <dt>

<span data-ttu-id="a97c9-206"><span id="_hi_MS"></span><span id="_hi_ms"></span><span id="_HI_MS"></span>**/Hi: *MS***</span><span class="sxs-lookup"><span data-stu-id="a97c9-206"><span id="_hi_MS"></span><span id="_hi_ms"></span><span id="_HI_MS"></span>**/hi: *MS***</span></span>
</dt> <dd>

<span data-ttu-id="a97c9-207">Um valor que especifica o intervalo de pulsação para a assinatura.</span><span class="sxs-lookup"><span data-stu-id="a97c9-207">A value that specifies the heartbeat interval for the subscription.</span></span> <span data-ttu-id="a97c9-208">*MS* é o número de milissegundos usados no intervalo.</span><span class="sxs-lookup"><span data-stu-id="a97c9-208">*MS* is the number of milliseconds used in the interval.</span></span> <span data-ttu-id="a97c9-209">Esse parâmetro só será válido se o parâmetro/cm for definido como Custom.</span><span class="sxs-lookup"><span data-stu-id="a97c9-209">This parameter is only valid if the /cm parameter is set to Custom.</span></span>

</dd> <dt>

<span data-ttu-id="a97c9-210"><span id="_tn_TRANSPORTNAME"></span><span id="_tn_transportname"></span><span id="_TN_TRANSPORTNAME"></span>**/TN: *TRANSportname***</span><span class="sxs-lookup"><span data-stu-id="a97c9-210"><span id="_tn_TRANSPORTNAME"></span><span id="_tn_transportname"></span><span id="_TN_TRANSPORTNAME"></span>**/tn: *TRANSPORTNAME***</span></span>
</dt> <dd>

<span data-ttu-id="a97c9-211">Um valor que especifica o nome do transporte usado para se conectar ao computador de origem do evento remoto.</span><span class="sxs-lookup"><span data-stu-id="a97c9-211">A value that specifies the name of the transport used to connect to the remote event source computer.</span></span>

</dd> <dt>

<span data-ttu-id="a97c9-212"><span id="_esa_EVENT_SOURCE"></span><span id="_esa_event_source"></span><span id="_ESA_EVENT_SOURCE"></span>**/ESA: *\_ origem do evento***</span><span class="sxs-lookup"><span data-stu-id="a97c9-212"><span id="_esa_EVENT_SOURCE"></span><span id="_esa_event_source"></span><span id="_ESA_EVENT_SOURCE"></span>**/esa: *EVENT\_SOURCE***</span></span>
</dt> <dd>

<span data-ttu-id="a97c9-213">Um valor que especifica o endereço de um computador de origem do evento.</span><span class="sxs-lookup"><span data-stu-id="a97c9-213">A value that specifies the address of an event source computer.</span></span> <span data-ttu-id="a97c9-214">*Evento \_ de SOURCE* é uma cadeia de caracteres que identifica um computador de origem de evento usando o nome de domínio totalmente qualificado para o computador, o nome NetBIOS ou o endereço IP.</span><span class="sxs-lookup"><span data-stu-id="a97c9-214">*EVENT\_SOURCE* is a string that identifies an event source computer using the fully qualified domain name for the computer, NetBIOS name, or IP address.</span></span> <span data-ttu-id="a97c9-215">Esse parâmetro pode ser usado com os parâmetros/ese,/AES,/res ou/un e/up.</span><span class="sxs-lookup"><span data-stu-id="a97c9-215">This parameter can be used with the /ese, /aes, /res, or /un and /up parameters.</span></span>

</dd> <dt>

<span data-ttu-id="a97c9-216"><span id="_ese_VALUE"></span><span id="_ese_value"></span><span id="_ESE_VALUE"></span>**/ESE: *valor***</span><span class="sxs-lookup"><span data-stu-id="a97c9-216"><span id="_ese_VALUE"></span><span id="_ese_value"></span><span id="_ESE_VALUE"></span>**/ese: *VALUE***</span></span>
</dt> <dd>

<span data-ttu-id="a97c9-217">Um valor que determina se uma origem de evento deve ser habilitada ou desabilitada.</span><span class="sxs-lookup"><span data-stu-id="a97c9-217">A value that determines whether to enable or disable an event source.</span></span> <span data-ttu-id="a97c9-218">O *valor* pode ser true ou false.</span><span class="sxs-lookup"><span data-stu-id="a97c9-218">*VALUE* can be true or false.</span></span> <span data-ttu-id="a97c9-219">O valor padrão é true, que habilita a origem do evento.</span><span class="sxs-lookup"><span data-stu-id="a97c9-219">The default value is true, which enables the event source.</span></span> <span data-ttu-id="a97c9-220">Esse parâmetro só será usado se o parâmetro/ESA for usado.</span><span class="sxs-lookup"><span data-stu-id="a97c9-220">This parameter is only used if the /esa parameter is used.</span></span>

</dd> <dt>

<span data-ttu-id="a97c9-221"><span id="_aes"></span><span id="_AES"></span>**/aes**</span><span class="sxs-lookup"><span data-stu-id="a97c9-221"><span id="_aes"></span><span id="_AES"></span>**/aes**</span></span>
</dt> <dd>

<span data-ttu-id="a97c9-222">Um valor que adiciona a origem do evento especificada pelo parâmetro/ESA se a origem do evento ainda não faz parte da assinatura do evento.</span><span class="sxs-lookup"><span data-stu-id="a97c9-222">A value that adds the event source specified by the /esa parameter if the event source is not already part of the event subscription.</span></span> <span data-ttu-id="a97c9-223">Se o computador especificado pelo parâmetro/ESA já for uma parte da assinatura, será exibido um erro.</span><span class="sxs-lookup"><span data-stu-id="a97c9-223">If the computer specified by the /esa parameter is already a part of the subscription, then an error is displayed.</span></span> <span data-ttu-id="a97c9-224">Esse parâmetro só será permitido se o parâmetro/ESA for usado.</span><span class="sxs-lookup"><span data-stu-id="a97c9-224">This parameter is allowed only if the /esa parameter is used.</span></span>

</dd> <dt>

<span data-ttu-id="a97c9-225"><span id="_res"></span><span id="_RES"></span>**/res**</span><span class="sxs-lookup"><span data-stu-id="a97c9-225"><span id="_res"></span><span id="_RES"></span>**/res**</span></span>
</dt> <dd>

<span data-ttu-id="a97c9-226">Um valor que remove a origem do evento especificada pelo parâmetro/ESA se a origem do evento já faz parte da assinatura do evento.</span><span class="sxs-lookup"><span data-stu-id="a97c9-226">A value that removes the event source specified by the /esa parameter if the event source is already part of the event subscription.</span></span> <span data-ttu-id="a97c9-227">Se o computador especificado pelo parâmetro/ESA não fizer parte da assinatura, será exibido um erro.</span><span class="sxs-lookup"><span data-stu-id="a97c9-227">If the computer specified by the /esa parameter is not part of the subscription, then an error is displayed.</span></span> <span data-ttu-id="a97c9-228">Esse parâmetro só será permitido se o parâmetro/ESA for usado.</span><span class="sxs-lookup"><span data-stu-id="a97c9-228">This parameter is allowed only if the /esa parameter is used.</span></span>

</dd> <dt>

<span data-ttu-id="a97c9-229"><span id="_un_USERNAME"></span><span id="_un_username"></span><span id="_UN_USERNAME"></span>**/un: *nome de usuário***</span><span class="sxs-lookup"><span data-stu-id="a97c9-229"><span id="_un_USERNAME"></span><span id="_un_username"></span><span id="_UN_USERNAME"></span>**/un: *USERNAME***</span></span>
</dt> <dd>

<span data-ttu-id="a97c9-230">Um valor que especifica o nome de usuário usado nas credenciais para se conectar à origem do evento especificada no parâmetro/ESA.</span><span class="sxs-lookup"><span data-stu-id="a97c9-230">A value that specifies the user name used in the credentials to connect to the event source specified in the /esa parameter.</span></span> <span data-ttu-id="a97c9-231">Esse parâmetro só será permitido se o parâmetro/ESA for usado.</span><span class="sxs-lookup"><span data-stu-id="a97c9-231">This parameter is allowed only if the /esa parameter is used.</span></span>

</dd> <dt>

<span data-ttu-id="a97c9-232"><span id="_up_PASSWORD"></span><span id="_up_password"></span><span id="_UP_PASSWORD"></span>**/up: *senha***</span><span class="sxs-lookup"><span data-stu-id="a97c9-232"><span id="_up_PASSWORD"></span><span id="_up_password"></span><span id="_UP_PASSWORD"></span>**/up: *PASSWORD***</span></span>
</dt> <dd>

<span data-ttu-id="a97c9-233">Um valor que especifica a senha para o nome de usuário especificado no parâmetro/un.</span><span class="sxs-lookup"><span data-stu-id="a97c9-233">A value that specifies the password for the user name specified in the /un parameter.</span></span> <span data-ttu-id="a97c9-234">As credenciais de nome de usuário e senha são usadas para se conectar à origem do evento especificada no parâmetro/ESA.</span><span class="sxs-lookup"><span data-stu-id="a97c9-234">The user name and password credentials are used to connect to the event source specified in the /esa parameter.</span></span> <span data-ttu-id="a97c9-235">Esse parâmetro só será permitido se o parâmetro/un for usado.</span><span class="sxs-lookup"><span data-stu-id="a97c9-235">This parameter is allowed only if the /un parameter is used.</span></span>

</dd> <dt>

<span data-ttu-id="a97c9-236"><span id="_tp_TRANSPORTPORT"></span><span id="_tp_transportport"></span><span id="_TP_TRANSPORTPORT"></span>**/TP: *TRANSPORTPORT***</span><span class="sxs-lookup"><span data-stu-id="a97c9-236"><span id="_tp_TRANSPORTPORT"></span><span id="_tp_transportport"></span><span id="_TP_TRANSPORTPORT"></span>**/tp: *TRANSPORTPORT***</span></span>
</dt> <dd>

<span data-ttu-id="a97c9-237">Um valor que especifica o número da porta usado pelo transporte ao se conectar a um computador de origem do evento remoto.</span><span class="sxs-lookup"><span data-stu-id="a97c9-237">A value that specifies the port number used by the transport when connecting to a remote event source computer.</span></span>

</dd> <dt>

<span data-ttu-id="a97c9-238"><span id="_hn_NAME"></span><span id="_hn_name"></span><span id="_HN_NAME"></span>**/HN: *nome***</span><span class="sxs-lookup"><span data-stu-id="a97c9-238"><span id="_hn_NAME"></span><span id="_hn_name"></span><span id="_HN_NAME"></span>**/hn: *NAME***</span></span>
</dt> <dd>

<span data-ttu-id="a97c9-239">Um valor que especifica o nome DNS do computador local.</span><span class="sxs-lookup"><span data-stu-id="a97c9-239">A value that specifies the DNS name of the local computer.</span></span> <span data-ttu-id="a97c9-240">Esse nome é usado por fontes de eventos remotas para enviar eventos por push e deve ser usado somente para assinaturas push.</span><span class="sxs-lookup"><span data-stu-id="a97c9-240">This name is used by remote event sources to push back events and must be used for push subscriptions only.</span></span>

</dd> <dt>

<span data-ttu-id="a97c9-241"><span id="_ct_TYPE"></span><span id="_ct_type"></span><span id="_CT_TYPE"></span>**/CT: *tipo***</span><span class="sxs-lookup"><span data-stu-id="a97c9-241"><span id="_ct_TYPE"></span><span id="_ct_type"></span><span id="_CT_TYPE"></span>**/ct: *TYPE***</span></span>
</dt> <dd>

<span data-ttu-id="a97c9-242">Um valor que especifica o tipo de credencial usado para acessar fontes de eventos remotas.</span><span class="sxs-lookup"><span data-stu-id="a97c9-242">A value that specifies the credential type used for accessing remote event sources.</span></span> <span data-ttu-id="a97c9-243">O *tipo* pode ser "default", "Negotiate", "Digest", "Basic" ou "LocalMachine".</span><span class="sxs-lookup"><span data-stu-id="a97c9-243">*TYPE* can be "default", "negotiate", "digest", "basic", or "localmachine".</span></span> <span data-ttu-id="a97c9-244">O padrão é "default".</span><span class="sxs-lookup"><span data-stu-id="a97c9-244">The default is "default".</span></span> <span data-ttu-id="a97c9-245">Esses valores são definidos na enumeração [**de \_ \_ \_ tipo de credenciais de assinatura do EC**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_credentials_type) .</span><span class="sxs-lookup"><span data-stu-id="a97c9-245">These values are defined in the [**EC\_SUBSCRIPTION\_CREDENTIALS\_TYPE**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_credentials_type) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="a97c9-246"><span id="_cun_USERNAME"></span><span id="_cun_username"></span><span id="_CUN_USERNAME"></span>**/cun: *nome de usuário***</span><span class="sxs-lookup"><span data-stu-id="a97c9-246"><span id="_cun_USERNAME"></span><span id="_cun_username"></span><span id="_CUN_USERNAME"></span>**/cun: *USERNAME***</span></span>
</dt> <dd>

<span data-ttu-id="a97c9-247">Um valor que define as credenciais de usuário compartilhadas usadas para fontes de eventos que não têm suas próprias credenciais de usuário.</span><span class="sxs-lookup"><span data-stu-id="a97c9-247">A value that sets the shared user credentials used for event sources that do not have their own user credentials.</span></span>

> [!Note]  
> <span data-ttu-id="a97c9-248">Se esse parâmetro for usado com a opção/c, as configurações de nome de usuário e senha para origens de eventos individuais do arquivo de configuração serão ignoradas.</span><span class="sxs-lookup"><span data-stu-id="a97c9-248">If this parameter is used with the /c option, then user name and password settings for individual event sources from the configuration file are ignored.</span></span> <span data-ttu-id="a97c9-249">Se você quiser usar credenciais diferentes para uma origem de evento específica, poderá substituir esse valor especificando os parâmetros/un e/up para uma origem de evento específica na linha de comando de outro comando Set-Subscription.</span><span class="sxs-lookup"><span data-stu-id="a97c9-249">If you want to use different credentials for a specific event source, you can override this value by specifying the /un and /up parameters for a specific event source on the command line of another set-subscription command.</span></span>

 

</dd> <dt>

<span data-ttu-id="a97c9-250"><span id="_cup_PASSWORD"></span><span id="_cup_password"></span><span id="_CUP_PASSWORD"></span>**/Cup: *senha***</span><span class="sxs-lookup"><span data-stu-id="a97c9-250"><span id="_cup_PASSWORD"></span><span id="_cup_password"></span><span id="_CUP_PASSWORD"></span>**/cup: *PASSWORD***</span></span>
</dt> <dd>

<span data-ttu-id="a97c9-251">Um valor que define a senha do usuário para as credenciais de usuário compartilhado.</span><span class="sxs-lookup"><span data-stu-id="a97c9-251">A value that sets the user password for the shared user credentials.</span></span> <span data-ttu-id="a97c9-252">Quando a *senha* é definida como \* (asterisco), a senha é lida no console do.</span><span class="sxs-lookup"><span data-stu-id="a97c9-252">When *PASSWORD* is set to \* (asterisk), then the password is read from the console.</span></span> <span data-ttu-id="a97c9-253">Essa opção só é válida quando o parâmetro/cun é especificado.</span><span class="sxs-lookup"><span data-stu-id="a97c9-253">This option is only valid when the /cun parameter is specified.</span></span>

</dd> <dt>

<span data-ttu-id="a97c9-254"><span id="_ica_THUMBPRINTS"></span><span id="_ica_thumbprints"></span><span id="_ICA_THUMBPRINTS"></span>**/ICA: *impressões digitais***</span><span class="sxs-lookup"><span data-stu-id="a97c9-254"><span id="_ica_THUMBPRINTS"></span><span id="_ica_thumbprints"></span><span id="_ICA_THUMBPRINTS"></span>**/ica: *THUMBPRINTS***</span></span>
</dt> <dd>

<span data-ttu-id="a97c9-255">Um valor que define a lista de impressões no thumb do certificado do emissor, em uma lista separada por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="a97c9-255">A value that sets the list of issuer certificate thumb prints, in a comma-separated list.</span></span>

> [!Note]  
> <span data-ttu-id="a97c9-256">Essa opção é específica apenas para assinaturas iniciadas pelo código-fonte.</span><span class="sxs-lookup"><span data-stu-id="a97c9-256">This option is specific to source initiated subscriptions only.</span></span>

 

</dd> <dt>

<span data-ttu-id="a97c9-257"><span id="_as_ALLOWED"></span><span id="_as_allowed"></span><span id="_AS_ALLOWED"></span>**/as: *permitido***</span><span class="sxs-lookup"><span data-stu-id="a97c9-257"><span id="_as_ALLOWED"></span><span id="_as_allowed"></span><span id="_AS_ALLOWED"></span>**/as: *ALLOWED***</span></span>
</dt> <dd>

<span data-ttu-id="a97c9-258">Um valor que define uma lista separada por vírgulas de cadeia de caracteres que especificam os nomes DNS de computadores que não são de domínio que têm permissão para iniciar assinaturas.</span><span class="sxs-lookup"><span data-stu-id="a97c9-258">A value that sets a comma-separated list of string that specify the DNS names of non-domain computers that are allowed to initiate subscriptions.</span></span> <span data-ttu-id="a97c9-259">Os nomes podem ser especificados usando curingas, como " \* . mydomain.com".</span><span class="sxs-lookup"><span data-stu-id="a97c9-259">The names can be specified using wildcards, such as "\*.mydomain.com".</span></span> <span data-ttu-id="a97c9-260">Por padrão, essa lista está vazia.</span><span class="sxs-lookup"><span data-stu-id="a97c9-260">By default, this list is empty.</span></span>

> [!Note]  
> <span data-ttu-id="a97c9-261">Essa opção é específica apenas para assinaturas iniciadas pelo código-fonte.</span><span class="sxs-lookup"><span data-stu-id="a97c9-261">This option is specific to source initiated subscriptions only.</span></span>

 

</dd> <dt>

<span data-ttu-id="a97c9-262"><span id="_ds_DENIED"></span><span id="_ds_denied"></span><span id="_DS_DENIED"></span>**/DS: *negado***</span><span class="sxs-lookup"><span data-stu-id="a97c9-262"><span id="_ds_DENIED"></span><span id="_ds_denied"></span><span id="_DS_DENIED"></span>**/ds: *DENIED***</span></span>
</dt> <dd>

<span data-ttu-id="a97c9-263">Um valor que define uma lista separada por vírgulas de cadeias de caracteres que especificam os nomes DNS de computadores que não são de domínio que não têm permissão para iniciar assinaturas.</span><span class="sxs-lookup"><span data-stu-id="a97c9-263">A value that sets a comma-separated list of string that specify the DNS names of non-domain computers that are not allowed to initiate subscriptions.</span></span> <span data-ttu-id="a97c9-264">Os nomes podem ser especificados usando curingas, como " \* . mydomain.com".</span><span class="sxs-lookup"><span data-stu-id="a97c9-264">The names can be specified using wildcards, such as "\*.mydomain.com".</span></span> <span data-ttu-id="a97c9-265">Por padrão, essa lista está vazia.</span><span class="sxs-lookup"><span data-stu-id="a97c9-265">By default, this list is empty.</span></span>

> [!Note]  
> <span data-ttu-id="a97c9-266">Essa opção é específica apenas para assinaturas iniciadas pelo código-fonte.</span><span class="sxs-lookup"><span data-stu-id="a97c9-266">This option is specific to source initiated subscriptions only.</span></span>

 

</dd> <dt>

<span data-ttu-id="a97c9-267"><span id="_adc_SDDL"></span><span id="_adc_sddl"></span><span id="_ADC_SDDL"></span>**/ADC: *SDDL***</span><span class="sxs-lookup"><span data-stu-id="a97c9-267"><span id="_adc_SDDL"></span><span id="_adc_sddl"></span><span id="_ADC_SDDL"></span>**/adc: *SDDL***</span></span>
</dt> <dd>

<span data-ttu-id="a97c9-268">Um valor que define uma cadeia de caracteres, no formato SDDL, que especifica quais computadores de domínio têm permissão ou não permissão para iniciar assinaturas.</span><span class="sxs-lookup"><span data-stu-id="a97c9-268">A value that sets a string, in SDDL format, that specifies which domain computers are allowed or not allowed to initiate subscriptions.</span></span> <span data-ttu-id="a97c9-269">O padrão é permitir que todos os computadores de domínio iniciem assinaturas.</span><span class="sxs-lookup"><span data-stu-id="a97c9-269">The default is to allow all domain computers to initiate subscriptions.</span></span>

> [!Note]  
> <span data-ttu-id="a97c9-270">Essa opção é específica apenas para assinaturas iniciadas pelo código-fonte.</span><span class="sxs-lookup"><span data-stu-id="a97c9-270">This option is specific to source initiated subscriptions only.</span></span>

 

</dd> </dl>

## <a name="create-a-new-subscription"></a><span data-ttu-id="a97c9-271">Criar uma nova assinatura</span><span class="sxs-lookup"><span data-stu-id="a97c9-271">Create a New Subscription</span></span>

<span data-ttu-id="a97c9-272">A sintaxe a seguir é usada para criar uma assinatura de evento para eventos em um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="a97c9-272">The following syntax is used to create an event subscription for events on a remote computer.</span></span>

``` syntax
wecutil {cs | create-subscription } CONFIGURATION_FILE [/cun:USERNAME]
[/cup:PASSWORD] 
```

### <a name="remarks"></a><span data-ttu-id="a97c9-273">Comentários</span><span class="sxs-lookup"><span data-stu-id="a97c9-273">Remarks</span></span>

<span data-ttu-id="a97c9-274">Quando um nome de usuário ou senha incorretos for especificado no comando **wecutil cs** , nenhum erro será relatado até que você exiba o status de tempo de execução da assinatura usando o comando **wecutil gr** .</span><span class="sxs-lookup"><span data-stu-id="a97c9-274">When an incorrect username or password is specified in the **wecutil cs** command, no error is reported until you view the runtime status of the subscription using the **wecutil gr** command.</span></span>

## <a name="creation-parameters"></a><span data-ttu-id="a97c9-275">Parâmetros de criação</span><span class="sxs-lookup"><span data-stu-id="a97c9-275">Creation Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a97c9-276"><span id="CONFIGURATION_FILE"></span><span id="configuration_file"></span>**arquivo de configuração \_**</span><span class="sxs-lookup"><span data-stu-id="a97c9-276"><span id="CONFIGURATION_FILE"></span><span id="configuration_file"></span>**CONFIGURATION\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="a97c9-277">Um valor que especifica o caminho para o arquivo XML que contém informações de configuração de assinatura.</span><span class="sxs-lookup"><span data-stu-id="a97c9-277">A value that specifies the path to the XML file that contains subscription configuration information.</span></span> <span data-ttu-id="a97c9-278">O caminho pode ser absoluto ou relativo ao diretório atual.</span><span class="sxs-lookup"><span data-stu-id="a97c9-278">The path can be absolute or relative to the current directory.</span></span>

<span data-ttu-id="a97c9-279">O XML a seguir é um exemplo de um arquivo de configuração de assinatura que cria uma assinatura iniciada pelo coletor para encaminhar eventos do log de eventos do aplicativo de um computador remoto para o log ForwardedEvents.</span><span class="sxs-lookup"><span data-stu-id="a97c9-279">The following XML is an example of a subscription configuration file that creates a collector initiated subscription to forward events from the Application event log of a remote computer to the ForwardedEvents log.</span></span>


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



<span data-ttu-id="a97c9-280">O XML a seguir é um exemplo de um arquivo de configuração de assinatura que cria uma assinatura iniciada de origem para encaminhar eventos do log de eventos do aplicativo de um computador remoto para o log ForwardedEvents.</span><span class="sxs-lookup"><span data-stu-id="a97c9-280">The following XML is an example of a subscription configuration file that creates a source initiated subscription to forward events from the Application event log of a remote computer to the ForwardedEvents log.</span></span>


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
> <span data-ttu-id="a97c9-281">Ao criar uma assinatura iniciada pela origem, se **AllowedSourceDomainComputers**, **AllowedSourceNonDomainComputers** / **IssuerCAList**, **AllowedSubjectList** e **DeniedSubjectList** estiverem todos vazios, um padrão será fornecido para **AllowedSourceDomainComputers** -"O:NSG: NSD: (a;; GA;;;D C) (A;; GA;;; NS) ".</span><span class="sxs-lookup"><span data-stu-id="a97c9-281">When creating a source initiated subscription, if **AllowedSourceDomainComputers**, **AllowedSourceNonDomainComputers**/**IssuerCAList**, **AllowedSubjectList**, and **DeniedSubjectList** are all empty, then a default will be provided for **AllowedSourceDomainComputers** - "O:NSG:NSD:(A;;GA;;;DC)(A;;GA;;;NS)".</span></span> <span data-ttu-id="a97c9-282">Esse padrão de SDDL concede membros do grupo de domínio computadores de domínio, bem como o grupo de serviços de rede local (para o encaminhador local), a capacidade de gerar eventos para essa assinatura.</span><span class="sxs-lookup"><span data-stu-id="a97c9-282">This SDDL default grants members of the Domain Computers domain group, as well as the local Network Service group (for the local forwarder), the ability to raise events for this subscription.</span></span>

 

</dd> <dt>

<span data-ttu-id="a97c9-283"><span id="_cun_USERNAME"></span><span id="_cun_username"></span><span id="_CUN_USERNAME"></span>**/cun: *nome de usuário***</span><span class="sxs-lookup"><span data-stu-id="a97c9-283"><span id="_cun_USERNAME"></span><span id="_cun_username"></span><span id="_CUN_USERNAME"></span>**/cun: *USERNAME***</span></span>
</dt> <dd>

<span data-ttu-id="a97c9-284">Um valor que define as credenciais de usuário compartilhadas usadas para fontes de eventos que não têm suas próprias credenciais de usuário.</span><span class="sxs-lookup"><span data-stu-id="a97c9-284">A value that sets the shared user credentials used for event sources that do not have their own user credentials.</span></span> <span data-ttu-id="a97c9-285">Esse valor se aplica somente às assinaturas iniciadas pelo coletor.</span><span class="sxs-lookup"><span data-stu-id="a97c9-285">This value applies to collector initiated subscriptions only.</span></span>

> [!Note]  
> <span data-ttu-id="a97c9-286">Se esse parâmetro for especificado, as configurações de nome de usuário e senha para origens de eventos individuais do arquivo de configuração serão ignoradas.</span><span class="sxs-lookup"><span data-stu-id="a97c9-286">If this parameter is specified, then user name and password settings for individual event sources from the configuration file are ignored.</span></span> <span data-ttu-id="a97c9-287">Se você quiser usar credenciais diferentes para uma origem de evento específica, poderá substituir esse valor especificando os parâmetros/un e/up para uma origem de evento específica na linha de comando de outro comando Set-Subscription.</span><span class="sxs-lookup"><span data-stu-id="a97c9-287">If you want to use different credentials for a specific event source, you can override this value by specifying the /un and /up parameters for a specific event source on the command line of another set-subscription command.</span></span>

 

</dd> <dt>

<span data-ttu-id="a97c9-288"><span id="_cup_PASSWORD"></span><span id="_cup_password"></span><span id="_CUP_PASSWORD"></span>**/Cup: *senha***</span><span class="sxs-lookup"><span data-stu-id="a97c9-288"><span id="_cup_PASSWORD"></span><span id="_cup_password"></span><span id="_CUP_PASSWORD"></span>**/cup: *PASSWORD***</span></span>
</dt> <dd>

<span data-ttu-id="a97c9-289">Um valor que define a senha do usuário para as credenciais de usuário compartilhado.</span><span class="sxs-lookup"><span data-stu-id="a97c9-289">A value that sets the user password for the shared user credentials.</span></span> <span data-ttu-id="a97c9-290">Quando a *senha* for definida como " \* " (asterisco), a senha será lida no console do.</span><span class="sxs-lookup"><span data-stu-id="a97c9-290">When *PASSWORD* is set to "\*" (asterisk), then the password is read from the console.</span></span> <span data-ttu-id="a97c9-291">Essa opção só é válida quando o parâmetro/cun é especificado.</span><span class="sxs-lookup"><span data-stu-id="a97c9-291">This option is only valid when the /cun parameter is specified.</span></span>

</dd> </dl>

## <a name="delete-a-subscription"></a><span data-ttu-id="a97c9-292">Excluir uma assinatura</span><span class="sxs-lookup"><span data-stu-id="a97c9-292">Delete a Subscription</span></span>

<span data-ttu-id="a97c9-293">A sintaxe a seguir é usada para excluir uma assinatura de evento.</span><span class="sxs-lookup"><span data-stu-id="a97c9-293">The following syntax is used to delete an event subscription.</span></span>

``` syntax
wecutil { ds | delete-subscription } SUBSCRIPTION_ID
```

## <a name="deletion-parameters"></a><span data-ttu-id="a97c9-294">Parâmetros de exclusão</span><span class="sxs-lookup"><span data-stu-id="a97c9-294">Deletion Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a97c9-295"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**ID da assinatura \_**</span><span class="sxs-lookup"><span data-stu-id="a97c9-295"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**SUBSCRIPTION\_ID**</span></span>
</dt> <dd>

<span data-ttu-id="a97c9-296">Uma cadeia de caracteres que identifica exclusivamente uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="a97c9-296">A string that uniquely identifies a subscription.</span></span> <span data-ttu-id="a97c9-297">Esse identificador é especificado no elemento **SubscriptionId** no arquivo de configuração XML usado para criar a assinatura.</span><span class="sxs-lookup"><span data-stu-id="a97c9-297">This identifier is specified in the **SubscriptionId** element in the XML configuration file used to create the subscription.</span></span> <span data-ttu-id="a97c9-298">A assinatura identificada neste parâmetro será excluída.</span><span class="sxs-lookup"><span data-stu-id="a97c9-298">The subscription identified in this parameter will be deleted.</span></span>

</dd> </dl>

## <a name="retry-a-subscription"></a><span data-ttu-id="a97c9-299">Repetir uma assinatura</span><span class="sxs-lookup"><span data-stu-id="a97c9-299">Retry a subscription</span></span>

<span data-ttu-id="a97c9-300">A sintaxe a seguir é usada para repetir uma assinatura inativa ao tentar reativar todas as fontes de evento ou origens de eventos específicas, estabelecendo uma conexão com cada origem de evento e enviando uma solicitação de assinatura remota para a origem do evento.</span><span class="sxs-lookup"><span data-stu-id="a97c9-300">The following syntax is used to retry an inactive subscription by attempting to reactivate all or specified event sources by establishing a connection to each event source and sending a remote subscription request to the event source.</span></span> <span data-ttu-id="a97c9-301">As fontes de eventos desabilitadas não são repetidas.</span><span class="sxs-lookup"><span data-stu-id="a97c9-301">Disabled event sources are not retried.</span></span>

``` syntax
wecutil { rs | retry-subscription } SUBSCRIPTION_ID 
[EVENT_SOURCE [EVENT_SOURCE] ...]
```

## <a name="retry-parameters"></a><span data-ttu-id="a97c9-302">Parâmetros de repetição</span><span class="sxs-lookup"><span data-stu-id="a97c9-302">Retry Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a97c9-303"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**ID da assinatura \_**</span><span class="sxs-lookup"><span data-stu-id="a97c9-303"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**SUBSCRIPTION\_ID**</span></span>
</dt> <dd>

<span data-ttu-id="a97c9-304">Uma cadeia de caracteres que identifica exclusivamente uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="a97c9-304">A string that uniquely identifies a subscription.</span></span> <span data-ttu-id="a97c9-305">Esse identificador é especificado no elemento **SubscriptionId** no arquivo de configuração XML usado para criar a assinatura.</span><span class="sxs-lookup"><span data-stu-id="a97c9-305">This identifier is specified in the **SubscriptionId** element in the XML configuration file used to create the subscription.</span></span> <span data-ttu-id="a97c9-306">A assinatura identificada neste parâmetro será repetida.</span><span class="sxs-lookup"><span data-stu-id="a97c9-306">The subscription identified in this parameter will be retried.</span></span>

</dd> <dt>

<span data-ttu-id="a97c9-307"><span id="EVENT_SOURCE"></span><span id="event_source"></span>**origem do evento \_**</span><span class="sxs-lookup"><span data-stu-id="a97c9-307"><span id="EVENT_SOURCE"></span><span id="event_source"></span>**EVENT\_SOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="a97c9-308">Um valor que identifica um computador que é uma origem de evento para uma assinatura de evento.</span><span class="sxs-lookup"><span data-stu-id="a97c9-308">A value that identifies a computer that is an event source for an event subscription.</span></span> <span data-ttu-id="a97c9-309">Esse valor pode ser o nome de domínio totalmente qualificado para o computador, o nome NetBIOS ou o endereço IP.</span><span class="sxs-lookup"><span data-stu-id="a97c9-309">This value can be the fully qualified domain name for the computer, NetBIOS name, or IP address.</span></span>

</dd> </dl>

## <a name="configure-the-windows-event-collector-service"></a><span data-ttu-id="a97c9-310">Configurar o serviço coletor de eventos do Windows</span><span class="sxs-lookup"><span data-stu-id="a97c9-310">Configure the Windows Event Collector Service</span></span>

<span data-ttu-id="a97c9-311">A sintaxe a seguir é usada para configurar o serviço coletor de eventos do Windows para garantir que as assinaturas de evento possam ser criadas e mantidas por meio de reinicializações do computador.</span><span class="sxs-lookup"><span data-stu-id="a97c9-311">The following syntax is used to configure the Windows Event Collector service to ensure event subscriptions can be created and sustained through computer restarts.</span></span> <span data-ttu-id="a97c9-312">Isso inclui o seguinte procedimento:</span><span class="sxs-lookup"><span data-stu-id="a97c9-312">This includes the following procedure:</span></span>

<span data-ttu-id="a97c9-313">**Para configurar o serviço coletor de eventos do Windows**</span><span class="sxs-lookup"><span data-stu-id="a97c9-313">**To configure the Windows Event Collector service**</span></span>

1.  <span data-ttu-id="a97c9-314">Habilite o canal ForwardedEvents se ele estiver desabilitado.</span><span class="sxs-lookup"><span data-stu-id="a97c9-314">Enable the ForwardedEvents channel if it is disabled.</span></span>
2.  <span data-ttu-id="a97c9-315">Atrase o início do serviço coletor de eventos do Windows.</span><span class="sxs-lookup"><span data-stu-id="a97c9-315">Delay the start of the Windows Event Collector service.</span></span>
3.  <span data-ttu-id="a97c9-316">Inicie o serviço coletor de eventos do Windows se ele não estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="a97c9-316">Start the Windows Event Collector service if it is not running.</span></span>

``` syntax
wecutil { qc | quick-config } /q:VALUE
```

## <a name="configure-event-collector-parameters"></a><span data-ttu-id="a97c9-317">Configurar parâmetros do coletor de eventos</span><span class="sxs-lookup"><span data-stu-id="a97c9-317">Configure Event Collector Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a97c9-318"><span id="_q_VALUE"></span><span id="_q_value"></span><span id="_Q_VALUE"></span>**/q: *valor***</span><span class="sxs-lookup"><span data-stu-id="a97c9-318"><span id="_q_VALUE"></span><span id="_q_value"></span><span id="_Q_VALUE"></span>**/q: *VALUE***</span></span>
</dt> <dd>

<span data-ttu-id="a97c9-319">Um valor que determina se o comando de configuração rápida solicitará confirmação.</span><span class="sxs-lookup"><span data-stu-id="a97c9-319">A value that determines whether the quick-config command will prompt for confirmation.</span></span> <span data-ttu-id="a97c9-320">O valor pode ser true ou false.</span><span class="sxs-lookup"><span data-stu-id="a97c9-320">VALUE can be true or false.</span></span> <span data-ttu-id="a97c9-321">Se VALUE for true, o comando solicitará a confirmação.</span><span class="sxs-lookup"><span data-stu-id="a97c9-321">If VALUE is true, then the command will prompt for confirmation.</span></span> <span data-ttu-id="a97c9-322">O valor padrão é false.</span><span class="sxs-lookup"><span data-stu-id="a97c9-322">The default value is false.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a97c9-323">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a97c9-323">Requirements</span></span>



| <span data-ttu-id="a97c9-324">Requisito</span><span class="sxs-lookup"><span data-stu-id="a97c9-324">Requirement</span></span> | <span data-ttu-id="a97c9-325">Valor</span><span class="sxs-lookup"><span data-stu-id="a97c9-325">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="a97c9-326">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a97c9-326">Minimum supported client</span></span><br/> | <span data-ttu-id="a97c9-327">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a97c9-327">Windows Vista</span></span><br/>       |
| <span data-ttu-id="a97c9-328">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a97c9-328">Minimum supported server</span></span><br/> | <span data-ttu-id="a97c9-329">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a97c9-329">Windows Server 2008</span></span><br/> |



 

 





