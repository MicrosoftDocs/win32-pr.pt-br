---
description: Registra provedores de instância no WMI.
ms.assetid: 6eba9bff-a5b9-4741-94ef-7d65b33d9aff
ms.tgt_platform: multiple
title: Classe __InstanceProviderRegistration
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
ms.openlocfilehash: 45923c0c3ea3bfc28e67634e3b447e46b62765f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105798384"
---
# <a name="__instanceproviderregistration-class"></a>\_\_Classe InstanceProviderRegistration

A classe de sistema **\_ \_ InstanceProviderRegistration** registra provedores de instância no WMI.

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

A classe **\_ \_ InstanceProviderRegistration** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **\_ \_ InstanceProviderRegistration** tem essas propriedades.

<dl> <dt>

**Entre ações**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Indica que um provedor de classe ou instância fornece dados ou recupera dados do WMI e do repositório de modelo CIM (CIM). Os provedores de pull dão suporte ao acesso dinâmico aos seus dados; e os provedores de push armazenam seus dados no repositório CIM e usam o WMI para fornecer acesso a ele. Para obter mais informações, consulte [determinando o status de Push ou pull](determining-push-or-pull-status.md). O valor padrão é 0 (zero).

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

**operador**
</dt> <dd> <dl> <dt>

Tipo de dados: **\_ \_ provedor**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Referência a uma instância do [**\_ \_ provedor**](--provider.md) que representa o caminho do objeto para o provedor de instância. Essa propriedade é herdada de [**\_ \_ ProviderRegistration**](--providerregistration.md).

</dd> <dt>

**QuerySupportLevels**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Matriz dos tipos de suporte incluído no provedor para processamento de consulta. Os provedores de classe não dão suporte a todos os tipos de consultas. Os provedores de instância podem definir **QuerySupportLevels** como **nulo** se não oferecerem suporte ao processamento de consulta. Provedores que dão suporte a consultas implementam o método [**IWbemServices:: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) e definem essa propriedade como um ou mais dos valores a seguir.

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

**SupportsBatching**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Não usado.

</dd> <dt>

**SupportsDelete**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Se **for true**, o provedor dará suporte à exclusão de dados.

<dt>

True
</dt> <dd>

O provedor dá suporte à exclusão de classe ou instância implementando o [**IWbemServices::D eleteclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (provedores de classe) ou [**IWbemServices::D eleteinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (provedores de instância).

</dd> <dt>

Falso
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

Se **for true**, o provedor dará suporte à enumeração de dados.

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

Se **for true**, o provedor de classe ou instância dará suporte à recuperação de dados.

<dt>

True
</dt> <dd>

O provedor dá suporte à recuperação de dados implementando [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).

</dd> <dt>

Falso
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

Se **for true**, o provedor de classe ou instância dará suporte à modificação de dados.

<dt>



 True


</dt> <dd>

O provedor dá suporte à modificação de classe ou instância implementando um dos seguintes métodos: [**IWbemServices::P utclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (provedores de classe) ou [**IWbemServices::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (provedores de classe).

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

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **\_ \_ InstanceProviderRegistration** é derivada de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md), que é derivada de [**\_ \_ ProviderRegistration**](--providerregistration.md). Somente os administradores podem registrar um provedor de instância criando uma instância do [**\_ \_ Win32Provider**](--win32provider.md) e do **\_ \_ InstanceProviderRegistration**. Somente os administradores podem excluir um provedor.

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
</dt> </dl>

 

