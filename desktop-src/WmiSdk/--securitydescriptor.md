---
description: Representa um descritor de segurança.
ms.assetid: 1ade1751-52a2-4ada-8255-323321111663
ms.tgt_platform: multiple
title: __SecurityDescriptor classe
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
ms.openlocfilehash: c248a437651396811f71c04e72dd8b209c5d10823f49d03abbe7e9d9ee6b6867
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118110193"
---
# <a name="__securitydescriptor-class"></a>\_\_Classe SecurityDescriptor

A **\_ \_ classe de sistema abstrata SecurityDescriptor** representa um [*descritor de segurança*](/windows/desktop/SecGloss/s-gly).

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

A **\_ \_ classe SecurityDescriptor** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **\_ \_ classe SecurityDescriptor** tem essas propriedades.

<dl> <dt>

**Controlflags**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Sinalizadores de bits que fornecem informações sobre o conteúdo e o formato do descritor. Consulte a **propriedade ControlFlags** na classe [**\_ Win32 SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) para ver uma descrição dos sinalizadores.

</dd> <dt>

**Dacl**
</dt> <dd> <dl> <dt>

Tipo de dados: **[**\_ \_ matriz ACE**](--ace.md)**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Uma matriz de [**\_ \_ entradas ACE**](--ace.md) que especificam o acesso ao objeto.

</dd> <dt>

**Grupo**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **\_ \_ ACE**](--ace.md)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

ACE que identifica o objeto de confiança que representa o grupo do objeto .

</dd> <dt>

**Proprietário**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **\_ \_ ACE**](--ace.md)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

ACE que identifica o objeto de confiança que representa o proprietário do objeto.

</dd> <dt>

**Sacl**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **\_ \_ ACE**](--ace.md)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma matriz de [**\_ \_ entradas ACE**](--ace.md) que identifica usuários e grupos para os quais as informações de auditoria são coletadas.

</dd> <dt>

**TEMPO \_ CRIADO**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Hora no formato [ \_ DATETIME cim](cim-datetime.md) quando o descritor de segurança foi criado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa classe fornece propriedades herdadas por [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor). Para obter mais informações, consulte [Objetos do descritor de](wmi-security-descriptor-objects.md) segurança WMI e Alterando a segurança de acesso em objetos [securáveis.](changing-access-security-on-securable-objects.md) Para obter mais informações sobre ACEs, consulte [Componentes de controle de acesso](/windows/desktop/SecAuthZ/access-control-components).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Todos os namespaces WMI<br/>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Classes do sistema WMI](wmi-system-classes.md)
</dt> <dt>

[**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[Mantendo a segurança WMI](maintaining-wmi-security.md)
</dt> </dl>

 

