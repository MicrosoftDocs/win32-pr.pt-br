---
description: A \_ \_ classe de sistema abstrata de confiança representa um confiável. Um nome ou um SID (matriz de bytes) pode ser usado.
ms.assetid: 92d17c7c-ebca-4dd0-80d8-6edd999ca394
ms.tgt_platform: multiple
title: Classe __Trustee
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __Trustee
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
ms.openlocfilehash: 5c6ba04760e924ffe9d86916cffdb82ea2488219
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506299"
---
# <a name="__trustee-class"></a>\_\_Classe de confiança

A classe de sistema abstrata de [**\_ \_ confiança**](--securitydescriptor.md) representa um [*confiável*](/windows/desktop/SecGloss/t-gly). Um nome ou um SID (matriz de bytes) pode ser usado.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class __Trustee
{
  string Domain;
  string Name;
  uint8  SID[];
  uint32 SidLength;
  string SidString;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>Membros

A classe **\_ \_ Trustee** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **\_ \_ Trustee** tem essas propriedades.

<dl> <dt>

**Domínio**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Parte do domínio da conta.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Nome da parte da conta.

</dd> <dt>

**SID**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **uint8**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

O SID do confiável no formulário da matriz de bytes binários.

</dd> <dt>

**SidLength**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

O comprimento do SID em bytes.

</dd> <dt>

**SidString**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

O SID do Trustee no formato de cadeia de caracteres, por exemplo, "S-1-1-0".

</dd> <dt>

**HORA da \_ criação**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Hora no formato [de \_ data e hora CIM](cim-datetime.md) quando o descritor de segurança foi criado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa classe fornece propriedades que são herdadas pela classe de [**\_ confiança do Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) , que é um membro da classe [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) . Para obter mais informações, consulte [objetos do descritor de segurança do WMI](wmi-security-descriptor-objects.md) e [alterando a segurança de acesso em objetos protegíveis](changing-access-security-on-securable-objects.md). Para obter mais informações sobre ACEs, consulte [componentes de controle de acesso](/windows/desktop/SecAuthZ/access-control-components).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Todos os namespaces do WMI<br/>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Classes do sistema WMI](wmi-system-classes.md)
</dt> <dt>

[**Confiança do Win32 \_**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee)
</dt> <dt>

[Mantendo a segurança do WMI](maintaining-wmi-security.md)
</dt> </dl>

 

