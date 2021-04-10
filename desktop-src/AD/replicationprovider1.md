---
title: Classe ReplicationProvider1
description: A classe base para a instância do provedor.
ms.assetid: c3c6efda-faa7-42af-a635-060967fdcc35
ms.tgt_platform: multiple
keywords:
- Active Directory classe ReplicationProvider1
- Active Directory classe ReplicationProvider1, descrita
topic_type:
- apiref
api_name:
- ReplicationProvider1
- ReplicationProvider1.ClientLoadableCLSID
- ReplicationProvider1.CLSID
- ReplicationProvider1.Concurrency
- ReplicationProvider1.DefaultMachineName
- ReplicationProvider1.Enabled
- ReplicationProvider1.ImpersonationLevel
- ReplicationProvider1.InitializationReentrancy
- ReplicationProvider1.InitializationTimeoutInterval
- ReplicationProvider1.InitializeAsAdminFirst
- ReplicationProvider1.Name
- ReplicationProvider1.OperationTimeoutInterval
- ReplicationProvider1.PerLocaleInitialization
- ReplicationProvider1.PerUserInitialization
- ReplicationProvider1.Pure
- ReplicationProvider1.SecurityDescriptor
- ReplicationProvider1.SupportsExplicitShutdown
- ReplicationProvider1.SupportsExtendedStatus
- ReplicationProvider1.SupportsQuotas
- ReplicationProvider1.SupportsSendStatus
- ReplicationProvider1.SupportsShutdown
- ReplicationProvider1.SupportsThrottling
- ReplicationProvider1.UnloadTimeout
- ReplicationProvider1.Version
- ReplicationProvider1.HostingModel
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0098556fcbc1400ccd1042198903fec7e018ed57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009274"
---
# <a name="replicationprovider1-class"></a>Classe ReplicationProvider1

A classe base para a instância do provedor.

A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
class ReplicationProvider1 : __Win32Provider
{
  string   ClientLoadableCLSID;
  string   CLSID;
  sint32   Concurrency;
  string   DefaultMachineName;
  boolean  Enabled;
  sint32   ImpersonationLevel = 0;
  sint32   InitializationReentrancy = 0;
  datetime InitializationTimeoutInterval;
  boolean  InitializeAsAdminFirst;
  string   Name;
  datetime OperationTimeoutInterval;
  boolean  PerLocaleInitialization = FALSE;
  boolean  PerUserInitialization = FALSE;
  boolean  Pure = TRUE;
  string   SecurityDescriptor;
  boolean  SupportsExplicitShutdown;
  boolean  SupportsExtendedStatus;
  boolean  SupportsQuotas;
  boolean  SupportsSendStatus;
  boolean  SupportsShutdown;
  boolean  SupportsThrottling;
  datetime UnloadTimeout;
  uint32   Version;
  string   HostingModel;
};
```

## <a name="members"></a>Membros

A classe **ReplicationProvider1** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **ReplicationProvider1** tem essas propriedades.

<dl> <dt>

**ClientLoadableCLSID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Identificador de classe que o WMI usa para determinar se um provedor de alto desempenho deve ou não ser carregado no processo do cliente ou no processo WMI. Se o provedor e o cliente estiverem localizados no mesmo computador, o WMI carregará o provedor em processo para o cliente usando **ClientLoadableCLSID** como o identificador de classe. Quando o provedor e o cliente estão localizados em computadores diferentes, o WMI carrega o provedor em processo para o WMI. O WMI também usa **ClientLoadableCLSID** para dar suporte a operações de atualização.

Para obter mais informações, consulte [registrando um provedor de High-Performance.](/windows/desktop/WmiSdk/registering-a-high-performance-provider)

Essa propriedade é herdada de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**CLSID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

O **GUID** que representa o identificador de classe (**CLSID**) do objeto com do provedor. Esse objeto COM deve conter uma implementação da interface [**IWbemProviderInit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) .

Essa propriedade é herdada de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**Simultaneidade**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Não usado.

Essa propriedade é herdada de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**Defaultmachinename**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Identifica o computador no qual o provedor deve ser iniciado. Se o provedor for executado no computador local, ele será **nulo**.

Essa propriedade é herdada de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**Enabled**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Se for **true**, essa instância será habilitada e poderá ser usada para concluir as solicitações do cliente.

Essa propriedade é herdada de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**HostingModel**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("HostingModel")
</dt> </dl>

Contém o modelo de hospedagem do provedor.

</dd> <dt>

**ImpersonationLevel**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Reservado. O valor padrão é zero (0).

Essa propriedade é herdada de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**InitializationReentrancy**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Conjunto de sinalizadores que fornecem informações sobre a serialização. O valor padrão é zero (0).

Essa propriedade é herdada de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Todas as inicializações desse provedor devem ser serializadas.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Todas as inicializações deste provedor no mesmo namespace devem ser serializadas.

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Nenhuma serialização de inicialização é necessária.

</dd> </dl>

</dd> <dt>

**InitializationTimeoutInterval**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Não usado.

Essa propriedade é herdada de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**InitializeAsAdminFirst**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

**Windows Server 2003:** Esta propriedade está desabilitada.

Essa propriedade é herdada de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

O nome do provedor.

Essa propriedade é herdada de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**OperationTimeoutInterval**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Não usado.

Essa propriedade é herdada de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**PerLocaleInitialization**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Se for **true**, o provedor será inicializado para cada localidade quando um usuário se conectar ao mesmo namespace mais de uma vez usando localidades diferentes. O valor padrão é **false**.

Essa propriedade é herdada de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**PerUserInitialization**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Se for **true**, o provedor será inicializado uma vez para cada usuário do NT LAN Manager (NTLM) que faz solicitações ao provedor. Se **for false** (padrão), o provedor será inicializado uma vez para todos os usuários.

Essa propriedade é herdada de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**Mero**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Se **for true**, o provedor concorda em se preparar para descarregar chamando [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) em todos os pontos de interface pendentes quando o WMI chama o método **Release** de sua interface primária. Provedores que devem permanecer clientes do WMI depois que não funcionam como provedores devem definir **Pure** como **false**. A configuração padrão é **true**. Para obter mais informações, consulte a seção comentários deste tópico.

Essa propriedade é herdada de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**SecurityDescriptor**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Descritor de segurança (SD) na linguagem de definição do descritor de segurança (SDDL) que determina o conjunto de usuários que podem chamar [**IWbemDecoupledRegistrar: Register**](/windows/desktop/api/wbemprov/nf-wbemprov-iwbemdecoupledregistrar-register) para o provedor dissociado com êxito. Para obter mais informações, consulte o tópico [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) na seção security da SDK do Windows. Esse descritor de segurança é usado apenas para provedores dissociados e não afeta outros provedores. Para obter mais informações, consulte [incorporando um provedor em um aplicativo](/windows/desktop/WmiSdk/incorporating-a-provider-in-an-application).

O WMI executa verificações de acesso para provedores dissociados que usam as interfaces [**IWbemProviderInit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) e [**IWbemObjectSink**](/windows/desktop/WmiSdk/iwbemobjectsink) . Se o descritor de segurança for **nulo**, somente aplicativos ou serviços executados nas contas LocalSystem, NetworkService e LocalService poderão executar um provedor dissociado.

A cadeia de caracteres a seguir mostra um provedor dissociado a ser executado somente por administradores internos. " O:BAG: INADEQUADO: (A;; 0 X1;;; BA) "

Para obter mais informações sobre como definir a propriedade **SecurityDescriptor** , consulte [mantendo a segurança do WMI](/windows/desktop/WmiSdk/maintaining-wmi-security).

Essa propriedade é herdada de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**SupportsExplicitShutdown**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Não usado.

Essa propriedade é herdada de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**SupportsExtendedStatus**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Não usado.

Essa propriedade é herdada de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**SupportsQuotas**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Não usado.

Essa propriedade é herdada de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**SupportsSendStatus**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Não usado.

Essa propriedade é herdada de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**SupportsShutdown**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Não usado.

Essa propriedade é herdada de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**SupportsThrottling**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Não usado.

Essa propriedade é herdada de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**UnloadTimeout**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

[Formato de data e hora](/windows/desktop/WmiSdk/date-and-time-format) que especifica por quanto tempo o WMI permite que o provedor permaneça ocioso antes de ser descarregado. Normalmente, os provedores solicitam que o WMI não aguarde mais do que cinco minutos.

Para a versão atual do WMI, o valor dessa propriedade é ignorado. O WMI descarrega o provedor com base no valor de tempo limite em uma classe interna no \\ namespace raiz. É recomendável que os provedores definam **UnloadTimeout**. Para obter mais informações, consulte [descarregando um provedor](/windows/desktop/WmiSdk/unloading-a-provider).

Essa propriedade é herdada de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**Versão**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Versão do provedor. As versões com suporte são 1 e 2. A versão 2 reforça as verificações de validade para todos os registros de propriedade associados, especificamente a propriedade [**ImpersonationLevel**](/windows/desktop/WmiSdk/swbemsecurity-impersonationlevel) .

Essa propriedade é herdada de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> </dl>

## <a name="remarks"></a>Comentários

Uma instância dessa classe representa o provedor WMI para serviços de Domínio do Active Directory. Os padrões são os seguintes:

-   Nome = "ReplProv1"
-   ClsID = "{29288F43-39B1-40db-B41F-CE899450E911}"
-   HostingModel = "NetworkServiceHost"

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\MicrosoftActiveDirectory raiz<br/>                                               |
| MOF<br/>                      | <dl> <dt>Replprov. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider)
</dt> </dl>

 

