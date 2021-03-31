---
description: Representa um descritor de segurança.
ms.assetid: 1ade1751-52a2-4ada-8255-323321111663
ms.tgt_platform: multiple
title: Classe __SecurityDescriptor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SecurityDescriptor
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
ms.openlocfilehash: 5f305387a29d1d1569addafd127f53c98246e1a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169810"
---
# <a name="__securitydescriptor-class"></a>\_\_Classe SecurityDescriptor

A classe de sistema abstrata **\_ \_ SecurityDescriptor** representa um [*descritor de segurança*](/windows/desktop/SecGloss/s-gly).

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class __SecurityDescriptor
{
  uint32 ControlFlags;
  __ACE  DACL[];
  __ACE  Group;
  __ACE  Owner;
  __ACE  SACL;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>Membros

A classe **\_ \_ SecurityDescriptor** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **\_ \_ SecurityDescriptor** tem essas propriedades.

<dl> <dt>

**ControlFlags**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Sinalizadores de bits que fornecem informações sobre o conteúdo e o formato do descritor. Consulte a propriedade **ControlFlags** na classe [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) para obter uma descrição dos sinalizadores.

</dd> <dt>

**DACL**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **[**\_ \_ Ace**](--ace.md)**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Uma matriz de entradas de [**\_ \_ Ace**](--ace.md) que especificam o acesso ao objeto.

</dd> <dt>

**Grupo**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **\_ \_ Ace**](--ace.md)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

ACE que identifica os objetos de confiança que representam o grupo do objeto.

</dd> <dt>

**Proprietário**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **\_ \_ Ace**](--ace.md)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

ACE que identifica os objetos de confiança que representam o proprietário do objeto.

</dd> <dt>

**Right**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **\_ \_ Ace**](--ace.md)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma matriz de entradas de [**\_ \_ Ace**](--ace.md) que identifica usuários e grupos para os quais as informações de auditoria são coletadas.

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

Essa classe fornece propriedades herdadas por [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor). Para obter mais informações, consulte [objetos do descritor de segurança do WMI](wmi-security-descriptor-objects.md) e [alterando a segurança de acesso em objetos protegíveis](changing-access-security-on-securable-objects.md). Para obter mais informações sobre ACEs, consulte [componentes de controle de acesso](/windows/desktop/SecAuthZ/access-control-components).

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

[**\_SecurityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[Mantendo a segurança do WMI](maintaining-wmi-security.md)
</dt> </dl>

 

