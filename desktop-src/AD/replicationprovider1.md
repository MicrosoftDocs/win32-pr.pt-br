---
title: Classe ReplicationProvider1
description: A classe base para a instância do provedor.
ms.assetid: c3c6efda-faa7-42af-a635-060967fdcc35
ms.tgt_platform: multiple
keywords:
- Classe ReplicationProvider1 Active Directory
- Classe ReplicationProvider1 Active Directory , descrita
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
ms.openlocfilehash: d3e8ca70d2bb5f37303c20117ddba59db6950d1dda58779179c6ef08c95abc4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025124"
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

A **classe ReplicationProvider1** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe ReplicationProvider1** tem essas propriedades.

<dl> <dt>

**ClientLoadableCLSID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Identificador de classe que o WMI usa para determinar se deve ou não carregar um provedor de alto desempenho no processo do cliente ou no processo WMI. Se o provedor e o cliente estão localizados no mesmo computador, o WMI carrega o provedor em processo para o cliente usando **ClientLoadableCLSID** como o identificador de classe. Quando o provedor e o cliente estão localizados em computadores diferentes, o WMI carrega o provedor em processo para o WMI. O WMI também usa **ClientLoadableCLSID para** dar suporte a operações de atualização.

Para obter mais informações, [consulte Registrando um provedor High-Performance dados.](/windows/desktop/WmiSdk/registering-a-high-performance-provider)

Essa propriedade é herdada [**\_ \_ de Win32Provider.**](/windows/desktop/WmiSdk/--win32provider)

</dd> <dt>

**Clsid**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

**GUID** que representa o **CLSID**(identificador de classe) do objeto COM do provedor. Esse objeto COM deve conter uma implementação da interface [**IWbemProviderInit.**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit)

Essa propriedade é herdada [**\_ \_ de Win32Provider.**](/windows/desktop/WmiSdk/--win32provider)

</dd> <dt>

**Simultaneidade**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Não usado.

Essa propriedade é herdada [**\_ \_ de Win32Provider.**](/windows/desktop/WmiSdk/--win32provider)

</dd> <dt>

**DefaultMachineName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Identifica o computador no qual iniciar o provedor. Se o provedor for executado no computador local, será **NULL.**

Essa propriedade é herdada [**\_ \_ de Win32Provider.**](/windows/desktop/WmiSdk/--win32provider)

</dd> <dt>

**Habilitada**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Se **TRUE**, essa instância estará habilitada e poderá ser usada para concluir solicitações de cliente.

Essa propriedade é herdada [**\_ \_ de Win32Provider.**](/windows/desktop/WmiSdk/--win32provider)

</dd> <dt>

**HostingModel**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("HostingModel")
</dt> </dl>

Contém o modelo de hospedagem do provedor.

</dd> <dt>

**ImpersonationLevel**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Reservado. O valor padrão é zero (0).

Essa propriedade é herdada [**\_ \_ de Win32Provider.**](/windows/desktop/WmiSdk/--win32provider)

</dd> <dt>

**InitializationReentrancy**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Conjunto de sinalizadores que fornecem informações sobre serialização. O valor padrão é zero (0).

Essa propriedade é herdada [**\_ \_ de Win32Provider.**](/windows/desktop/WmiSdk/--win32provider)

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Toda a inicialização desse provedor deve ser serializada.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Todas as inicializações desse provedor no mesmo namespace devem ser serializadas.

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Nenhuma serialização de inicialização é necessária.

</dd> </dl>

</dd> <dt>

**InitializationTimeoutInterval**
</dt> <dd> <dl> <dt>

Tipo de dados: **datetime**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Não usado.

Essa propriedade é herdada [**\_ \_ de Win32Provider.**](/windows/desktop/WmiSdk/--win32provider)

</dd> <dt>

**InitializeAsAdminFirst**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

**Windows Server 2003:** Essa propriedade está desabilitada.

Essa propriedade é herdada [**\_ \_ de Win32Provider.**](/windows/desktop/WmiSdk/--win32provider)

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Qualificadores: [ **Chave**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

O nome do provedor.

Essa propriedade é herdada [**\_ \_ de Win32Provider.**](/windows/desktop/WmiSdk/--win32provider)

</dd> <dt>

**OperationTimeoutInterval**
</dt> <dd> <dl> <dt>

Tipo de dados: **datetime**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Não usado.

Essa propriedade é herdada [**\_ \_ de Win32Provider.**](/windows/desktop/WmiSdk/--win32provider)

</dd> <dt>

**PerLocaleInitialization**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Se **TRUE**, o provedor será inicializado para cada localidade quando um usuário se conectar ao mesmo namespace mais de uma vez usando localidades diferentes. O valor padrão é **FALSE**.

Essa propriedade é herdada [**\_ \_ de Win32Provider.**](/windows/desktop/WmiSdk/--win32provider)

</dd> <dt>

**PerUserInitialization**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Se **TRUE**, o provedor será inicializado uma vez para cada usuário do NTLM (NT LAN Manager) que faz solicitações ao provedor. Se **FALSE** (padrão), o provedor será inicializado uma vez para todos os usuários.

Essa propriedade é herdada [**\_ \_ de Win32Provider.**](/windows/desktop/WmiSdk/--win32provider)

</dd> <dt>

**Puro**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Se **TRUE**, o provedor concorda em se preparar para descarregar chamando [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) em todos os pontos de interface pendentes quando o WMI chama o método **Release** de sua interface primária. Provedores que devem permanecer clientes do WMI depois que não funcionarem como provedores devem definir **Puro** como **FALSE.** A configuração padrão é **TRUE.** Para obter mais informações, consulte a seção Comentários deste tópico.

Essa propriedade é herdada [**\_ \_ de Win32Provider.**](/windows/desktop/WmiSdk/--win32provider)

</dd> <dt>

**SecurityDescriptor**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

SD (descritor de segurança) na SDDL (Linguagem de Definição do Descritor de Segurança) que determina o conjunto de usuários que podem chamar [**IWbemDecoupledRegistrar:Register**](/windows/desktop/api/wbemprov/nf-wbemprov-iwbemdecoupledregistrar-register) para o provedor desafinido. Para obter mais informações, consulte [o tópico Linguagem de Definição](/windows/desktop/SecAuthZ/security-descriptor-definition-language) do Descritor de Segurança na seção Segurança do SDK do Windows. Esse descritor de segurança é usado apenas para provedores desaplados e não afeta outros provedores. Para obter mais informações, [consulte Incorporando um provedor em um aplicativo](/windows/desktop/WmiSdk/incorporating-a-provider-in-an-application).

O WMI executa verificações de acesso para provedores desaplados que usam as interfaces [**IWbemProviderInit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) e [**IWbemObjectSink.**](/windows/desktop/WmiSdk/iwbemobjectsink) Se o descritor de segurança for **NULL,** somente os aplicativos ou serviços executados nas contas LocalSystem, NetworkService e LocalService poderão executar um provedor desaplados.

A cadeia de caracteres a seguir mostra um provedor desaplados a ser executado somente por administradores integrados." O:BAG:BAD:(A;;0 x1;;; BA)"

Para obter mais informações sobre como definir **a propriedade SecurityDescriptor,** consulte [Mantendo a segurança WMI](/windows/desktop/WmiSdk/maintaining-wmi-security).

Essa propriedade é herdada [**\_ \_ de Win32Provider.**](/windows/desktop/WmiSdk/--win32provider)

</dd> <dt>

**SupportsExplicitShutdown**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Não usado.

Essa propriedade é herdada [**\_ \_ de Win32Provider.**](/windows/desktop/WmiSdk/--win32provider)

</dd> <dt>

**SupportsExtendedStatus**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Não usado.

Essa propriedade é herdada [**\_ \_ de Win32Provider.**](/windows/desktop/WmiSdk/--win32provider)

</dd> <dt>

**SupportsQuotas**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Não usado.

Essa propriedade é herdada [**\_ \_ de Win32Provider.**](/windows/desktop/WmiSdk/--win32provider)

</dd> <dt>

**SupportsSendStatus**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Não usado.

Essa propriedade é herdada [**\_ \_ de Win32Provider.**](/windows/desktop/WmiSdk/--win32provider)

</dd> <dt>

**SupportsShutdown**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Não usado.

Essa propriedade é herdada [**\_ \_ de Win32Provider.**](/windows/desktop/WmiSdk/--win32provider)

</dd> <dt>

**SupportsThrottling**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Não usado.

Essa propriedade é herdada [**\_ \_ de Win32Provider.**](/windows/desktop/WmiSdk/--win32provider)

</dd> <dt>

**UnloadTimeout**
</dt> <dd> <dl> <dt>

Tipo de dados: **datetime**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

[Formato de data e hora](/windows/desktop/WmiSdk/date-and-time-format) que especifica por quanto tempo o WMI permite que o provedor permaneça ocioso antes de ser descarregado. Normalmente, os provedores solicitam que o WMI aguarde não mais de cinco minutos.

Para a versão atual do WMI, o valor dessa propriedade é ignorado. O WMI descarrega o provedor com base no valor de tempo-máximo em uma classe interna no \\ namespace raiz. É recomendável que os provedores devam **definir UnloadTimeout.** Para obter mais informações, [consulte Descarregando um provedor](/windows/desktop/WmiSdk/unloading-a-provider).

Essa propriedade é herdada [**\_ \_ de Win32Provider.**](/windows/desktop/WmiSdk/--win32provider)

</dd> <dt>

**Versão**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Versão do provedor. As versões com suporte são 1 e 2. A versão 2 reforça as verificações de validade para todos os registros de propriedade associados, especificamente a [**propriedade ImpersonationLevel.**](/windows/desktop/WmiSdk/swbemsecurity-impersonationlevel)

Essa propriedade é herdada [**\_ \_ de Win32Provider.**](/windows/desktop/WmiSdk/--win32provider)

</dd> </dl>

## <a name="remarks"></a>Comentários

Uma instância dessa classe representa o provedor WMI para Domínio do Active Directory serviços. Os padrões são os seguinte:

-   Nome = "ReplProv1"
-   ClsID = "{29288F43-39B1-40db-B41F-CE899450E911}"
-   HostingModel = "NetworkServiceHost"

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\MicrosoftActiveDirectory raiz<br/>                                               |
| MOF<br/>                      | <dl> <dt>Replprov.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider)
</dt> </dl>

 

