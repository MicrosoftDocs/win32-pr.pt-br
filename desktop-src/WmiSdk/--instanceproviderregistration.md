---
description: Registra provedores de instância no WMI.
ms.assetid: 6eba9bff-a5b9-4741-94ef-7d65b33d9aff
ms.tgt_platform: multiple
title: __InstanceProviderRegistration classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceProviderRegistration
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
ms.openlocfilehash: 773bb54ec4d132e629f21513ffa617cbe3435d35941e7c98c55810d267f614c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118821151"
---
# <a name="__instanceproviderregistration-class"></a>\_\_Classe InstanceProviderRegistration

A **\_ \_ classe do sistema InstanceProviderRegistration** registra provedores de instância no WMI.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class __InstanceProviderRegistration : __ObjectProviderRegistration
{
  sint32         InteractionType = 0;
  __Provider REF provider;
  string         QuerySupportLevels[];
  boolean        SupportsBatching;
  boolean        SupportsDelete = False;
  boolean        SupportsEnumeration = True;
  boolean        SupportsGet = False;
  boolean        SupportsPut = False;
  boolean        SupportsTransactions;
};
```

## <a name="members"></a>Membros

A **\_ \_ classe InstanceProviderRegistration** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **\_ \_ classe InstanceProviderRegistration** tem essas propriedades.

<dl> <dt>

**InteractionType**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Indica que uma classe ou provedor de instância fornece dados ou recupera dados do WMI e do repositório CIM (modelo CIM). Os provedores de pull suportam o acesso dinâmico aos seus dados; Os provedores de push e armazenam seus dados no repositório CIM e usam o WMI para fornecer acesso a eles. Para obter mais informações, consulte [Determinando o status de push ou pull.](determining-push-or-pull-status.md) O valor padrão é 0 (zero).

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

O provedor é um provedor de verificação por push. Observe que os provedores de verificação por push não têm suporte no momento.

</dd> </dl>

</dd> <dt>

**Provedor**
</dt> <dd> <dl> <dt>

Tipo de dados: **\_ \_ Provedor**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Referência a uma instância do [**\_ \_ Provedor que**](--provider.md) representa o caminho do objeto para o provedor de instância. Essa propriedade é herdada [**\_ \_ de ProviderRegistration.**](--providerregistration.md)

</dd> <dt>

**QuerySupportLevels**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **de cadeia de** caracteres
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Matriz dos tipos de suporte incluído pelo provedor para processamento de consulta. Os provedores de classe não suportam todos os tipos de consultas. Os provedores de instância **podem definir QuerySupportLevels** como **NULL** se não deem suporte ao processamento de consulta. Provedores que suportam consultas implementam o método [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) e essa propriedade é definida como um ou mais dos valores a seguir.

<dt>



 ("WQL:UnarySelect")


</dt> <dd></dd> <dt>



 ("WQL:References")


</dt> <dd></dd> <dt>



 ("WQL:Associators")


</dt> <dd></dd> <dt>



 ("WQL:V1ProviderDefined")


</dt> <dd></dd> </dl>

</dd> <dt>

**SupportsBatching**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Não usado.

</dd> <dt>

**SupportsDelete**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Se **True**, o provedor dá suporte à exclusão de dados.

<dt>

Verdadeiro
</dt> <dd>

O provedor dá suporte à exclusão de classe ou instância implementando [**IWbemServices::D eleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (provedores de classe) ou [**IWbemServices::D eleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (provedores de instância).

</dd> <dt>

Falso
</dt> <dd>

O provedor não dá suporte à exclusão de dados e retorna **WBEM \_ E PROVIDER NOT CAPABLE \_ \_ \_ de** [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) ou [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync).

</dd> </dl>

</dd> <dt>

**SupportsEnumeration**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Se **True**, o provedor dá suporte à enumeração de dados.

<dt>



 (True)


</dt> <dd>

O provedor dá suporte à enumeração de dados implementando um dos [**IWbemServices::CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) (provedores de classe) ou [**IWbemServices::CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) (provedores de instância).

</dd> <dt>



 (False)


</dt> <dd>

O provedor não dá suporte à enumeração de dados e retorna **WBEM \_ E PROVIDER NOT CAPABLE \_ \_ \_ de** [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) ou [**CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync).

</dd> </dl>

</dd> <dt>

**SupportsGet**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Se **True**, a classe ou o provedor de instância dá suporte à recuperação de dados.

<dt>

Verdadeiro
</dt> <dd>

O provedor dá suporte à recuperação de dados implementando [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).

</dd> <dt>

Falso
</dt> <dd>

O provedor não dá suporte à recuperação de dados e retorna **WBEM \_ E PROVIDER NOT \_ \_ \_ CAPABLE** de [**GetObjectAsync.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)

</dd> </dl>

</dd> <dt>

**SupportsPut**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Se **True**, a classe ou o provedor de instância dá suporte à modificação de dados.

<dt>



 (True)


</dt> <dd>

O provedor dá suporte à modificação de classe ou instância implementando um dos seguintes métodos: [**IWbemServices::P utClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (provedores de classe) ou [**IWbemServices::P utInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (provedores de classe).

</dd> <dt>



 (False)


</dt> <dd>

O provedor não dá suporte à modificação de dados e retorna **WBEM \_ E PROVIDER NOT CAPABLE \_ \_ \_ de** [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) ou [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).

</dd> </dl>

</dd> <dt>

**SupportsTransactions**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Não usado.

</dd> </dl>

## <a name="remarks"></a>Comentários

A **\_ \_ classe InstanceProviderRegistration** é derivada de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md), que é derivada de [**\_ \_ ProviderRegistration**](--providerregistration.md). Somente os administradores podem registrar um provedor de instância criando uma instância de [**\_ \_ Win32Provider**](--win32provider.md) e **\_ \_ InstanceProviderRegistration**. Somente os administradores podem excluir um provedor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Todos os namespaces WMI<br/>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_\_ObjectProviderRegistration**](/windows/desktop/WmiSdk/--objectproviderregistration)
</dt> <dt>

[Classes do sistema WMI](wmi-system-classes.md)
</dt> <dt>

[Registrando um provedor de classe](registering-a-class-provider.md)
</dt> <dt>

[Registrando um provedor de instância](registering-an-instance-provider.md)
</dt> </dl>

 

