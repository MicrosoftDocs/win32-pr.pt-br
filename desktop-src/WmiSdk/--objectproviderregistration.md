---
description: Serve como a classe pai para classes que são usadas para registrar provedores de classe e de instância no WMI.
ms.assetid: f7c569be-8927-42a4-b96a-abe4b7e3e23c
ms.tgt_platform: multiple
title: Classe __ObjectProviderRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ObjectProviderRegistration
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
ms.openlocfilehash: a60b24278fb235cec38c127e7ebbbb481e49a140
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296829"
---
# <a name="__objectproviderregistration-class"></a>\_\_Classe ObjectProviderRegistration

A classe de sistema abstrata **\_ \_ ObjectProviderRegistration** serve como a classe pai para classes que são usadas para registrar provedores de classe e de instância no WMI.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[abstract]
class __ObjectProviderRegistration : __ProviderRegistration
{
  sint32         InteractionType = 0;
  __Provider REF provider;
  string         QuerySupportLevels[];
  boolean        SupportsBatching;
  boolean        SupportsDelete = False;
  boolean        SupportsEnumeration = False;
  boolean        SupportsGet = False;
  boolean        SupportsPut = False;
  boolean        SupportsTransactions;
};
```

## <a name="members"></a>Membros

A classe **\_ \_ ObjectProviderRegistration** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **\_ \_ ObjectProviderRegistration** tem essas propriedades.

<dl> <dt>

**Entre ações**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Indica se o provedor de classe ou instância fornece ou não seus próprios dados ou se baseia no WMI e no repositório de modelo CIM (CIM). Os provedores de pull dão suporte ao acesso dinâmico aos seus dados, e os provedores de push armazenam seus dados no repositório CIM e contam com o WMI para fornecer acesso a ele. Para obter mais informações, consulte [determinando o status de Push ou pull](determining-push-or-pull-status.md). O valor padrão é 0 (zero).

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

O provedor é um provedor de verificação por push. Observe que o push-Verify não tem suporte no momento.

</dd> </dl>

</dd> <dt>

**operador**
</dt> <dd> <dl> <dt>

Tipo de dados: **\_ \_ provedor**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Referência a uma instância do [**\_ \_ provedor**](--provider.md) que representa um caminho de objeto para o provedor de objetos. Essa propriedade é herdada de [**\_ \_ ProviderRegistration**](--providerregistration.md).

</dd> <dt>

**QuerySupportLevels**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Matriz dos tipos de suporte incluído no provedor para processamento de consulta. Os provedores de classe não dão suporte a nenhum tipo de consulta. Os provedores de instância podem definir **QuerySupportLevels** como **nulo** se não oferecerem suporte ao processamento de consulta. Provedores que dão suporte a consultas implementam o método [**IWbemServices:: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) e definem essa propriedade como um ou mais dos valores a seguir (o tipo de propriedade é uma matriz).

"WQL: UnarySelect"

"WQL: referências"

"WQL: ASSOCIATORS"

"WQL: V1ProviderDefined"

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

O provedor dá suporte à exclusão de classe ou instância implementando um dos [**IWbemServices::D eleteclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (provedores de classe) ou [**IWbemServices::D eleteinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (provedores de instância).

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

Falso
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

O provedor dá suporte à modificação de classe ou instância implementando um dos [**IWbemServices::P utclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (provedores de classe) ou [**IWbemServices::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (provedores de classe).

</dd> <dt>

Falso
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

A classe **\_ \_ ObjectProviderRegistration** é derivada de [**\_ \_ ProviderRegistration**](--providerregistration.md).

Os provedores de classe devem definir a propriedade **SupportsEnumeration** como **true** porque os provedores devem ser capazes de fornecer o WMI com uma lista de suas classes. Se um provedor de classes tentar definir essa propriedade como **false**, o WMI sinalizará o registro como inválido. Os provedores de instância não são necessários para dar suporte à enumeração e podem optar por definir **SupportsEnumeration** como **true** ou **false**.

Um provedor que define **QuerySupportLevels** como "WQL: UnarySelect" pode aceitar uma consulta que consiste na instrução SELECT básica como com suporte na versão 1,0 do WMI. Os provedores de classe e de instância devem ser capazes de lidar com a propriedade do sistema de **\_ \_ classe** . Os provedores de classe também devem processar a propriedade do sistema de **\_ \_ superclasse** e o operador ISA. O operador ISA é usado para expandir um conjunto de resultados para classes derivadas. Se um provedor receber uma consulta que não pode interpretar, ele solicitará que o WMI o manipule retornando o WBEM E um valor de erro **\_ \_ muito \_ complexo** . Para obter uma descrição da sintaxe WQL válida, consulte [consultando com WQL](querying-with-wql.md).

Um provedor que define **QuerySupportLevels** para **WQL: V1ProviderDefined** pode tentar dar suporte a um conjunto maior de sintaxe do SQL por seu próprio risco, como a `ORDER BY` cláusula. O WMI não interpreta as cláusulas adicionais ou tenta garantir que o conjunto de resultados esteja correto.

Somente os administradores podem registrar ou excluir um provedor criando uma instância do [**\_ \_ Win32Provider**](--win32provider.md) e registrando-o.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Todos os namespaces do WMI<br/>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_\_ProviderRegistration**](/windows/desktop/WmiSdk/--providerregistration)
</dt> <dt>

[Classes do sistema WMI](wmi-system-classes.md)
</dt> <dt>

[Registrando um provedor](registering-a-provider.md)
</dt> </dl>

 

