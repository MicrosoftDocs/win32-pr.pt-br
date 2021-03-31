---
description: Registra provedores de classe no WMI.
ms.assetid: 1af7d9ed-c5e4-47e4-839d-53d579ef7cea
ms.tgt_platform: multiple
title: Classe __ClassProviderRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ClassProviderRegistration
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 32442122624035ec376bed3be8b3ef20c80f8524
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663475"
---
# <a name="__classproviderregistration-class"></a>\_\_Classe ClassProviderRegistration

A classe de sistema **\_ \_ ClassProviderRegistration** registra provedores de classe no WMI.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class __ClassProviderRegistration : __ObjectProviderRegistration
{
  boolean        SupportsBatching;
  datetime       CacheRefreshInterval;
  sint32         InteractionType = 0;
  __Provider REF provider;
  boolean        PerUserSchema;
  string         QuerySupportLevels[];
  string         ReferencedSetQueries[];
  string         ResultSetQueries[];
  boolean        ReSynchroniseOnNamespaceOpen;
  boolean        SuppportsBatching;
  boolean        SupportsEnumeration = False;
  boolean        SupportsDelete = False;
  boolean        SupportsGet = False;
  boolean        SupportsPut = False;
  boolean        SupportsTransactions;
  string         UnsupportedQueries[];
  uint32         Version;
};
```

## <a name="members"></a>Membros

A classe **\_ \_ ClassProviderRegistration** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **\_ \_ ClassProviderRegistration** tem essas propriedades.

<dl> <dt>

**CacheRefreshInterval**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Não usado.

</dd> <dt>

**Entre ações**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Indica se o provedor de classe ou instância fornece dados ou se baseia no WMI e no repositório de modelo CIM (CIM). Os provedores de pull dão suporte ao acesso dinâmico aos dados, e os provedores de envio por push armazenam dados no repositório CIM e contam com o WMI para fornecer acesso a ele. O valor padrão é 0 (zero). Essa propriedade é herdada de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md). Para obter mais informações, consulte [determinando o status de Push ou pull](determining-push-or-pull-status.md).

<dt>

<span id="Pull"></span><span id="pull"></span><span id="PULL"></span>

<span id="Pull"></span><span id="pull"></span><span id="PULL"></span>**Pull** (0)


</dt> <dd>

O provedor é um provedor de pull.

</dd> <dt>

<span id="Push"></span><span id="push"></span><span id="PUSH"></span>

<span id="Push"></span><span id="push"></span><span id="PUSH"></span>**Push** (1)


</dt> <dd>

O provedor é um provedor de push.

</dd> <dt>

<span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>

<span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>**PushVerify** (2)


</dt> <dd>

O provedor é um provedor de verificação por push. Observe que os provedores de **PushVerify** não têm suporte no momento.

</dd> </dl>

</dd> <dt>

**PerUserSchema**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Não usado.

</dd> <dt>

**operador**
</dt> <dd> <dl> <dt>

Tipo de dados: **\_ \_ provedor**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Caminho do objeto para um provedor de classe. Essa propriedade é herdada de [**\_ \_ ProviderRegistration**](--providerregistration.md).

</dd> <dt>

**QuerySupportLevels**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Matriz dos tipos de suporte incluído no provedor para processamento de consulta. Essa propriedade é herdada de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md). Provedores de classe são necessários para dar suporte a pelo menos um tipo de consulta. Os provedores de instância podem definir **QuerySupportLevels** como **nulo** se não oferecerem suporte ao processamento de consulta. Provedores que dão suporte a consultas implementam o método [**IWbemServices:: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) e definem essa propriedade como um ou mais dos seguintes valores:

<dt>



 ("WQL: UnarySelect")


</dt> <dd></dd> <dt>



 ("WQL: referências")


</dt> <dd></dd> <dt>



 ("WQL: ASSOCIATORS")


</dt> <dd></dd> <dt>



 ("WQL: V1ProviderDefined")


</dt> <dd></dd> </dl>

</dd> <dt>

**ReferencedSetQueries**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Uma ou mais consultas que descrevem o conjunto de classes referenciadas com suporte de um provedor de classe. Provedores que podem fornecer classes de associação devem incluir pelo menos uma consulta nessa propriedade.

</dd> <dt>

**ResultSetQueries**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Uma ou mais consultas que descrevem o conjunto de todas as classes que podem ser fornecidas pelo provedor de classe ou um superconjunto dessas classes. Essa propriedade nunca especifica um subconjunto de classes com suporte.

</dd> <dt>

**ReSynchroniseOnNamespaceOpen**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Não usado.

</dd> <dt>

**SupportsBatching**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Não usado.

Essa propriedade é herdada de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md).

</dd> <dt>

**SupportsDelete**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Se **for true**, o provedor dará suporte à exclusão de dados. Essa propriedade é herdada de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md).

<dt>



 True


</dt> <dd>

O provedor dá suporte à exclusão de classe ou instância implementando um dos [**IWbemServices::D eleteclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (provedores de classe) ou [**IWbemServices::D eleteinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (provedores de instância).

</dd> <dt>



 For


</dt> <dd>

O provedor não dá suporte à exclusão de dados e retorna o **\_ provedor WBEM e \_ não é \_ \_ capaz** de [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) ou [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync).

</dd> </dl>

</dd> <dt>

**SupportsEnumeration**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Se **for true**, o provedor dará suporte à enumeração de dados. Essa propriedade é herdada de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md).

<dt>



 True


</dt> <dd>

O provedor dá suporte à enumeração de dados implementando um dos [**IWbemServices:: CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) (provedores de classe) ou [**IWbemServices:: CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) (provedores de instância).

</dd> <dt>



 For


</dt> <dd>

O provedor não oferece suporte à enumeração de dados e retorna o **\_ provedor WBEM e \_ não é \_ \_ capaz** de [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) ou [**CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync).

</dd> </dl>

</dd> <dt>

**SupportsGet**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Se **for true**, o provedor de classe ou instância dará suporte à recuperação de dados. Essa propriedade é herdada de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md).

<dt>



 True


</dt> <dd>

O provedor dá suporte à recuperação de dados implementando [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).

</dd> <dt>



 For


</dt> <dd>

O provedor não dá suporte à recuperação de dados e retorna **o \_ provedor WBEM e \_ não é \_ \_ capaz** de [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).

</dd> </dl>

</dd> <dt>

**SupportsPut**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Se **for true**, o provedor de classe ou instância dará suporte à modificação de dados. Essa propriedade é herdada de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md).

<dt>



 True


</dt> <dd>

O provedor dá suporte à modificação de classe ou instância implementando um dos [**IWbemServices::P utclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (provedores de classe) ou [**IWbemServices::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (provedores de classe).

</dd> <dt>



 For


</dt> <dd>

O provedor não dá suporte à modificação de dados e retorna o **\_ provedor WBEM e \_ não é \_ \_ compatível** com [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) ou [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).

</dd> </dl>

</dd> <dt>

**SupportsTransactions**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Não usado.

</dd> <dt>

**SuppportsBatching**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Não usado.

</dd> <dt>

**UnsupportedQueries**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Uma ou mais consultas que descrevem o conjunto de classes para as quais o provedor de classes não dá suporte. Use essa propriedade para subtrair do conjunto de classes implícitas por **ResultSetQueries**.

</dd> <dt>

**Versão**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Versão deste provedor de classes.

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **\_ \_ ClassProviderRegistration** é derivada de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md), que é derivada de [**\_ \_ ProviderRegistration**](--providerregistration.md).

As propriedades herdadas de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md) indicam se o provedor de classe dá suporte à recuperação de dados, modificação, exclusão, enumeração e processamento de consulta. A propriedade **interactiontype** especifica se o provedor de classe foi projetado ou não como um provedor de pull ou push. Para obter mais informações, consulte [determinando o status de Push ou pull](determining-push-or-pull-status.md).

A classe [**\_ \_ ProviderRegistration**](--providerregistration.md) define a propriedade do [**provedor**](/windows/desktop/api/Provider/nl-provider-provider) . Somente os administradores podem registrar um provedor criando uma instância do [**\_ \_ Win32Provider**](--win32provider.md) e do **\_ \_ ClassProviderRegistration**. Somente os administradores podem excluir um provedor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Todos os namespaces do WMI<br/>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_\_ObjectProviderRegistration**](/windows/desktop/WmiSdk/--objectproviderregistration)
</dt> <dt>

[Classes do sistema WMI](wmi-system-classes.md)
</dt> <dt>

[Registrando um provedor de classe](registering-a-class-provider.md)
</dt> <dt>

[Registrando um provedor de instância](registering-an-instance-provider.md)
</dt> <dt>

[**\_\_Win32Provider**](--win32provider.md)
</dt> </dl>

 

