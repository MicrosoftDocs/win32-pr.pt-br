---
description: A \_ \_ classe de sistema abstrata Do usuário confiável representa um usuário confiável. Um nome ou um SID (matriz de byte) pode ser usado.
ms.assetid: 92d17c7c-ebca-4dd0-80d8-6edd999ca394
ms.tgt_platform: multiple
title: __Trustee classe
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
ms.openlocfilehash: ac1e80bceb3dc584a22e342780bbf32660276868e473ff33ff01d6c2ad65d504
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131949"
---
# <a name="__trustee-class"></a>\_\_Classe Trustee

A classe do sistema abstrato do [**\_ \_ Trustee**](--securitydescriptor.md) representa um [*usuário confiável.*](/windows/desktop/SecGloss/t-gly) Um nome ou um SID (matriz de byte) pode ser usado.

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

A **\_ \_ classe Trustee** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **\_ \_ classe Trustee** tem essas propriedades.

<dl> <dt>

**Domínio**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Parte do domínio da conta.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Parte do nome da conta.

</dd> <dt>

**SID**
</dt> <dd> <dl> <dt>

Tipo de dados: **matriz uint8**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

O SID do usuário confiável no formulário de matriz de byte binário.

</dd> <dt>

**SidLength**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

O comprimento do SID em bytes.

</dd> <dt>

**SidString**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

O SID do usuário confiável no formato de cadeia de caracteres, por exemplo, "S-1-1-0".

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

Essa classe fornece propriedades herdadas pela classe [**Win32 \_ Trustee,**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) que é membro da [**classe Win32 \_ SecurityDescriptor.**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) Para obter mais informações, consulte [Objetos do descritor de](wmi-security-descriptor-objects.md) segurança WMI e Alterando a segurança de acesso em objetos [securáveis.](changing-access-security-on-securable-objects.md) Para obter mais informações sobre ACEs, consulte [Componentes de controle de acesso](/windows/desktop/SecAuthZ/access-control-components).

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

[**Win32 \_ Trustee**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee)
</dt> <dt>

[Mantendo a segurança WMI](maintaining-wmi-security.md)
</dt> </dl>

 

