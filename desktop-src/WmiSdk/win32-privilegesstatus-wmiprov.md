---
description: O Win32 \_ PrivilegesStatus &\# 8194; A classe WMI relata informações sobre privilégios necessários para concluir uma operação. Ele pode ser retornado quando uma operação falhou ou quando uma instância parcialmente populada foi retornada.
ms.assetid: 85bda855-1488-4d7a-99ed-798e9859fef7
ms.tgt_platform: multiple
title: classe Win32_PrivilegesStatus (WMI)
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
- Schema
api_location:
- Root\WMI
ms.openlocfilehash: 97276023325dc4e2a460daefd35ee01104b5c0adf5c855f145e0f11c954eba1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757626"
---
# <a name="win32_privilegesstatus-class-wmi"></a>classe Win32_PrivilegesStatus (WMI)

A **classe WMI \_ PrivilegesStatus**   [do](retrieving-a-class.md) Win32 relata informações sobre os privilégios necessários para concluir uma operação. Ele pode ser retornado quando uma operação falhou ou quando uma instância parcialmente populada foi retornada.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades e os métodos estão em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[UUID("{BE46D060-7A7C-11d2-BC85-00104B2CF71C}")]
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

A **classe \_ PrivilegesStatus do Win32** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ PrivilegesStatus do Win32** tem essas propriedades.

<dl> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Qualquer cadeia de caracteres definida pelo usuário que descreva um erro ou status operacional.

Essa propriedade é herdada de [**\_ \_ ExtendedStatus.**](--extendedstatus.md)

</dd> <dt>

**Operação**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Operação que ocorre no momento de uma falha ou anomalia. Normalmente, Windows WMI (Instrumentação de Gerenciamento) define essa propriedade como o nome de uma API COM para o método WMI, como o seguinte: [**IWbemServices::CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum).

Essa propriedade é herdada de [**\_ \_ ExtendedStatus.**](--extendedstatus.md)

</dd> <dt>

**Parameterinfo**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Parâmetros envolvidos em uma alteração de status ou erro. Por exemplo, se um aplicativo tentar recuperar uma classe que não existe, essa propriedade será definida como o nome da classe que está sendo ofensivo.

Essa propriedade é herdada de [**\_ \_ ExtendedStatus.**](--extendedstatus.md)

</dd> <dt>

**PrivilegesNotHeld**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **de cadeia de** caracteres
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Listar privilégios de acesso necessários ausentes para concluir uma operação. Os tipos de privilégios de acesso podem ser encontrados na Windows Privilégios.

Exemplo: "ES \_ NOME DE \_ DESLIGAMENTO"

</dd> <dt>

**PrivilégiosRequired**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **de cadeia de** caracteres
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Listagem de todos os privilégios necessários para executar uma operação. Isso inclui valores da **propriedade PrivilegesNotHeld.**

Exemplo: "ES \_ NOME DE \_ DESLIGAMENTO"

</dd> <dt>

**ProviderName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Identifica o provedor que causa ou relata uma alteração de status ou erro. Se um provedor não estiver envolvido, essa cadeia de caracteres será definida como "gerenciamento Windows".

Essa propriedade é herdada de [**\_ \_ ExtendedStatus.**](--extendedstatus.md)

</dd> <dt>

**StatusCode**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Contém um erro ou código de informações para uma operação. Isso pode ser qualquer valor definido pelo provedor, mas o valor 0 (zero) geralmente é reservado para indicar êxito. Essa propriedade é herdada de [**\_ \_ NotifyStatus.**](--notifystatus.md)

</dd> </dl>

## <a name="remarks"></a>Comentários

A **classe \_ PrivilegesStatus do Win32** é derivada de [**\_ \_ ExtendedStatus**](--extendedstatus.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                     |
| Namespace<br/>                | \\WMI raiz<br/>                                                               |
| MOF<br/>                      | <dl> <dt>Wmi.mof</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_\_Extendedstatus**](--extendedstatus.md)
</dt> </dl>

 

 




