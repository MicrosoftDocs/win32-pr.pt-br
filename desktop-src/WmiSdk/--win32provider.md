---
description: Registra informações sobre a implementação física de um provedor no WMI. Provedores que não definem a Propriedade HostingModel são carregados, por padrão, para serem executados em um processo de Wmiprvse.exe como NetworkServiceHostOrSelfHost.
ms.assetid: 41e0d938-00c6-4f4c-8027-8b8512398dee
ms.tgt_platform: multiple
title: Classe __Win32Provider
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0240c459ea2d09013379bfd7c3190ce691cf4cc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922603"
---
# <a name="__win32provider-class"></a>\_\_Classe Win32Provider

A classe de sistema **\_ \_ Win32Provider** registra informações sobre a implementação física de um provedor no WMI. Provedores que não definem a propriedade **HostingModel** são carregados, por padrão, para serem executados em um processo de Wmiprvse.exe como **NetworkServiceHostOrSelfHost**.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class __Win32Provider : __Provider
{
  string   ClientLoadableCLSID;
  string   CLSID;
  sint32   Concurrency;
  string   DefaultMachineName;
  boolean  Enabled;
  string   HostingModel;
  sint32   ImpersonationLevel = 0;
  sint32   InitializationReentrancy;
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
};
```

## <a name="members"></a>Membros

A classe **\_ \_ Win32Provider** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **\_ \_ Win32Provider** tem essas propriedades.

<dl> <dt>

**ClientLoadableCLSID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Identificador de classe que o WMI usa para determinar se um provedor de alto desempenho deve ou não ser carregado no processo do cliente ou no processo WMI. Se o provedor e o cliente estiverem localizados no mesmo computador, o WMI carregará o provedor em processo para o cliente usando **ClientLoadableCLSID** como o identificador de classe. Quando o provedor e o cliente estão localizados em computadores diferentes, o WMI carrega o provedor em processo para o WMI. O WMI também usa **ClientLoadableCLSID** para dar suporte a operações de atualização.

Para obter mais informações, consulte [registrando um provedor de High-Performance.](registering-a-high-performance-provider.md)

</dd> <dt>

**CLSID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

O **GUID** que representa o identificador de classe (**CLSID**) do objeto com do provedor. Esse objeto COM deve conter uma implementação da interface [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) .

</dd> <dt>

**Simultaneidade**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Não usado.

</dd> <dt>

**Defaultmachinename**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Identifica o computador no qual o provedor deve ser iniciado. Se o provedor for executado no computador local, ele será **nulo**.

</dd> <dt>

**Enabled**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Se for **true**, essa instância será habilitada e poderá ser usada para concluir as solicitações do cliente.

</dd> <dt>

**HostingModel**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Essa propriedade é composta de valores das propriedades de **hospedagem** e **HostingSpecification** de [**\_ provedores de MSFT**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) . O valor dessa propriedade especifica como o WMI carrega o provedor e a conta de segurança na qual ele é executado. Para obter mais informações sobre como definir a propriedade **HostingModel** , consulte [provedor de hospedagem e segurança](provider-hosting-and-security.md) e [registrando um provedor](registering-a-provider.md).

</dd> <dt>

**ImpersonationLevel**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Reservado. O valor padrão é zero (0).

</dd> <dt>

**InitializationReentrancy**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Conjunto de sinalizadores que fornecem informações sobre a serialização. O valor padrão é zero (0).

<dt>

0
</dt> <dd>

Todas as inicializações desse provedor devem ser serializadas.

</dd> <dt>

1
</dt> <dd>

Todas as inicializações deste provedor no mesmo namespace devem ser serializadas.

</dd> <dt>

2
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

</dd> <dt>

**InitializeAsAdminFirst**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

TBD

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [ **chave**](standard-qualifiers.md)
</dt> </dl>

O nome do provedor.

</dd> <dt>

**OperationTimeoutInterval**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Não usado.

</dd> <dt>

**PerLocaleInitialization**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Se for **true**, o provedor será inicializado para cada localidade quando um usuário se conectar ao mesmo namespace mais de uma vez usando localidades diferentes. O valor padrão é **false**.

</dd> <dt>

**PerUserInitialization**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Se for **true**, o provedor será inicializado uma vez para cada usuário do NT LAN Manager (NTLM) que faz solicitações ao provedor. Se **for false** (padrão), o provedor será inicializado uma vez para todos os usuários.

</dd> <dt>

**Mero**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Se **for true**, o provedor concorda em se preparar para descarregar chamando [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) em todos os pontos de interface pendentes quando o WMI chama o método **Release** de sua interface primária. Provedores que devem permanecer clientes do WMI depois que não funcionam como provedores devem definir **Pure** como **false**. A configuração padrão é **true**. Para obter mais informações, consulte a seção comentários deste tópico.

</dd> <dt>

**SecurityDescriptor**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Descritor de segurança (SD) na linguagem de definição do descritor de segurança (SDDL) que determina o conjunto de usuários que podem chamar [**IWbemDecoupledRegistrar: Register**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemdecoupledregistrar-register) para o provedor dissociado com êxito. Para obter mais informações, consulte o tópico [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) na seção security da SDK do Windows. Esse descritor de segurança é usado apenas para provedores dissociados e não afeta outros provedores. Para obter mais informações, consulte [incorporando um provedor em um aplicativo](incorporating-a-provider-in-an-application.md).

O WMI executa verificações de acesso para provedores dissociados que usam as interfaces [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) e [**IWbemObjectSink**](iwbemobjectsink.md) . Se o descritor de segurança for **nulo**, somente aplicativos ou serviços executados nas contas LocalSystem, NetworkService e LocalService poderão executar um provedor dissociado.

A cadeia de caracteres a seguir mostra um provedor dissociado a ser executado somente por administradores internos. " O:BAG: INADEQUADO: (A;; 0 X1;;; BA) "

Para obter mais informações sobre como definir a propriedade **SecurityDescriptor** , consulte [mantendo a segurança do WMI](maintaining-wmi-security.md).

</dd> <dt>

**SupportsExplicitShutdown**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Não usado.

</dd> <dt>

**SupportsExtendedStatus**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Não usado.

</dd> <dt>

**SupportsQuotas**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Não usado.

</dd> <dt>

**SupportsSendStatus**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Não usado.

</dd> <dt>

**SupportsShutdown**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Não usado.

</dd> <dt>

**SupportsThrottling**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Não usado.

</dd> <dt>

**UnloadTimeout**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

[Formato de data e hora](date-and-time-format.md) que especifica por quanto tempo o WMI permite que o provedor permaneça ocioso antes de ser descarregado. Normalmente, os provedores solicitam que o WMI não aguarde mais do que cinco minutos.

Para a versão atual do WMI, o valor dessa propriedade é ignorado. O WMI descarrega o provedor com base no valor de tempo limite em uma classe interna no \\ namespace raiz. É recomendável que os provedores definam **UnloadTimeout**. Para obter mais informações, consulte [descarregando um provedor](unloading-a-provider.md).

</dd> <dt>

**Versão**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Versão do provedor. As versões com suporte são 1 e 2. A versão 2 reforça as verificações de validade para todos os registros de propriedade associados, especificamente a propriedade [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md) .

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **\_ \_ Win32Provider** é derivada do [**\_ \_ provedor**](--provider.md).

A maioria dos provedores pode aceitar os valores padrão para a propriedade **InitializationReentrancy** . No entanto, se um provedor puder oferecer suporte à inicialização simultânea para usuários separados, essa propriedade poderá ser definida como 1 (um). Se a inicialização serializada for necessária, **InitializationReentrancy** permanecerá 0 (zero). Em ambas as instâncias, **PerUserInitialization** é definido como **true**.

Um provedor puro ou um provedor que define a propriedade **pura** como **true**, existe apenas para atender a solicitações de aplicativos e WMI. A maioria dos provedores são provedores puros. Um provedor não puro é a exceção. Os provedores não puros fazem a transição para a função do cliente depois de concluírem as solicitações de manutenção.

Um exemplo de um provedor não puro é um provedor de envio por push que começa a emitir consultas e faz solicitações do WMI após a conclusão da inicialização. Um provedor de push não tem responsabilidades, exceto atualizar o repositório CIM com dados no momento da inicialização. Depois de atualizar o repositório, um provedor de push pode aguardar para ser descarregado ou fazer a transição para a função do cliente. O provedor de envio por push que espera para ser descarregado é um provedor puro. O provedor de envio por push que participa de atividades do cliente é não puro.

O WMI deve ser capaz de distinguir provedores puros de provedores não puros para que ele possa determinar quando é seguro desligá-lo. O WMI deve esperar que todas as operações que envolvem provedores não puros sejam concluídas antes de serem desligadas com segurança.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Todos os namespaces do WMI<br/>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_\_Provedor**](/windows/desktop/WmiSdk/--provider)
</dt> <dt>

[Classes do sistema WMI](wmi-system-classes.md)
</dt> <dt>

[Registrando um provedor](registering-a-provider.md)
</dt> </dl>

 

