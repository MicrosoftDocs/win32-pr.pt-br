---
description: O Win32 \_ PrivilegesStatus&\# 8194; A classe WMI relata informações sobre os privilégios necessários para concluir uma operação. Ele pode ser retornado quando uma operação falha ou quando uma instância parcialmente preenchida tiver sido retornada.
ms.assetid: 295ec2bd-7996-4031-8503-d4e869d8368d
ms.tgt_platform: multiple
title: Classe Win32_PrivilegesStatus (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrivilegesStatus
- Win32_PrivilegesStatus.Description
- Win32_PrivilegesStatus.Operation
- Win32_PrivilegesStatus.ParameterInfo
- Win32_PrivilegesStatus.ProviderName
- Win32_PrivilegesStatus.StatusCode
- Win32_PrivilegesStatus.PrivilegesNotHeld
- Win32_PrivilegesStatus.PrivilegesRequired
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4e2c2b2329884b22eecdc00a629abb8d05bc87435ce06d35e51907cb4095c8fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119020084"
---
# <a name="win32_privilegesstatus-class-cimwin32-wmi-providers"></a>Classe Win32_PrivilegesStatus (provedores WMI CIMWin32)

A  [classe WMI](../wmisdk/retrieving-a-class.md) **\_ PrivilegesStatus do Win32** relata informações sobre os privilégios necessários para concluir uma operação. Ele pode ser retornado quando uma operação falha ou quando uma instância parcialmente preenchida tiver sido retornada.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[UUID("{BE46D060-7A7C-11d2-BC85-00104B2CF71C}"), AMENDMENT]
class Win32_PrivilegesStatus : __ExtendedStatus
{
  string Description;
  string Operation;
  string ParameterInfo;
  string ProviderName;
  uint32 StatusCode;
  string PrivilegesNotHeld[];
  string PrivilegesRequired[];
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ PrivilegesStatus** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ PrivilegesStatus** tem essas propriedades.

<dl> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Qualquer cadeia de caracteres definida pelo usuário que descreva um erro ou status operacional.

Essa propriedade é herdada de [**\_ \_ ExtendedStatus**](../wmisdk/--extendedstatus.md).

</dd> <dt>

**Operação**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Operação que ocorre no momento de uma falha ou anomalia. normalmente, Instrumentação de Gerenciamento do Windows (WMI) define essa propriedade como o nome de uma API COM para o método WMI, como o seguinte: [**IWbemServices:: CreateInstanceEnum**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenum).

Essa propriedade é herdada de [**\_ \_ ExtendedStatus**](../wmisdk/--extendedstatus.md).

</dd> <dt>

**ParameterInfo**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Parâmetros envolvidos em um erro ou alteração de status. Por exemplo, se um aplicativo tentar recuperar uma classe que não existe, essa propriedade será definida como o nome da classe incorreta.

Essa propriedade é herdada de [**\_ \_ ExtendedStatus**](../wmisdk/--extendedstatus.md).

</dd> <dt>

**PrivilegesNotHeld**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| AccessControl \| Windows NT privileges")
</dt> </dl>

Listando os privilégios de acesso necessários ausentes para concluir uma operação. os tipos de privilégios de acesso podem ser encontrados sob os privilégios de Windows.

exemplo: " \_ nome de desligamento de ES \_ "

</dd> <dt>

**PrivilegesRequired**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| AccessControl \| Windows NT privileges")
</dt> </dl>

Listagem de todos os privilégios necessários para executar uma operação. Isso inclui valores da propriedade **PrivilegesNotHeld** .

exemplo: " \_ nome de desligamento de ES \_ "

</dd> <dt>

**ProviderName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Identifica o provedor que causa ou relata um erro ou uma alteração de status. se um provedor não estiver envolvido, essa cadeia de caracteres será definida como "gerenciamento de Windows".

Essa propriedade é herdada de [**\_ \_ ExtendedStatus**](../wmisdk/--extendedstatus.md).

</dd> <dt>

**StatusCode**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Contém um código de erro ou informações para uma operação. Pode ser qualquer valor definido pelo provedor, mas o valor 0 (zero) geralmente é reservado para indicar êxito.

Essa propriedade é herdada de [**\_ \_ NotifyStatus**](../wmisdk/--notifystatus.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **Win32 \_ PrivilegesStatus** é derivada de [**\_ \_ ExtendedStatus**](../wmisdk/--extendedstatus.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_\_ExtendedStatus**](../wmisdk/--extendedstatus.md)
</dt> </dl>

 

 
