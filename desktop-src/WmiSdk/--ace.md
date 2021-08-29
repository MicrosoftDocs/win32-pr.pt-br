---
description: Representa uma ACE (entrada de controle de acesso).
ms.assetid: 47daffd0-b9db-4367-b0b8-654a2da30fed
ms.tgt_platform: multiple
title: Classe __ACE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ACE
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
ms.openlocfilehash: ad6713cea39f02e59b49b69e2fa2a8a060cb7a6f78d3b6143bc2c2dbc0de1965
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051104"
---
# <a name="__ace-class"></a>\_\_Classe ACE

A classe de sistema abstrato **\_ \_ Ace** representa uma [*Ace*](/windows/desktop/SecGloss/a-gly)(entrada de controle de acesso).

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class  __ACE : __SecurityRelatedClass
{
            AceFlags;
            AccessMask;
            AceType;
            GuidInheritedObjectType;
            GuidObjectType;
  uint64    TIME_CREATED;
  __Trustee Trustee;
};
```

## <a name="members"></a>Membros

A classe **\_ \_ Ace** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **\_ \_ Ace** tem essas propriedades.

<dl> <dt>

**AccessMask**
</dt> <dd> <dl> <dt>

Tipo de dados: 
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Sinalizadores de bits que representam direitos que são concedidos ou negados ao confiável. Para obter mais informações e uma descrição dos sinalizadores, consulte a propriedade **AccessMask** na classe do [**Win32 \_ Ace**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) .

</dd> <dt>

**AceFlags**
</dt> <dd> <dl> <dt>

Tipo de dados: 
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Sinalizadores de bit que especificam a herança da ACE. Para obter mais informações e uma descrição dos sinalizadores, consulte Propriedade **AceFlags** na classe do [**Win32 \_ Ace**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) .

</dd> <dt>

**AceType**
</dt> <dd> <dl> <dt>

Tipo de dados: 
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

O tipo de entrada da ACE que essa instância representa.

</dd> <dt>

**GuidInheritedObjectType**
</dt> <dd> <dl> <dt>

Tipo de dados: 
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

O GUID do pai do objeto ao qual os direitos de acesso na propriedade **AccessMask** se aplicam.

</dd> <dt>

**GuidObjectType**
</dt> <dd> <dl> <dt>

Tipo de dados: 
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

O GUID que indica o tipo de objeto ao qual os direitos na propriedade **AccessMask** se aplicam.

</dd> <dt>

**HORA da \_ criação**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A hora, no formato [de \_ data e hora CIM](cim-datetime.md) , quando o descritor de segurança foi criado.

</dd> <dt>

**Confiança**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **\_ \_ Trustee**](--trustee.md)**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

O Trustee da entrada Ace representada por essa instância da classe **\_ \_ Ace** .

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa classe fornece as propriedades que são herdadas pela classe [**Win32 \_ Ace**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) , que é um membro da classe [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) . Para obter mais informações, consulte [objetos do descritor de segurança do WMI](wmi-security-descriptor-objects.md) e [alterando a segurança de acesso em objetos protegíveis](changing-access-security-on-securable-objects.md). Para obter mais informações sobre ACEs, consulte [componentes de controle de acesso](/windows/desktop/SecAuthZ/access-control-components).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Todos os namespaces do WMI<br/>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_\_SecurityRelatedClass**](--securityrelatedclass.md)
</dt> <dt>

[Classes do sistema WMI](wmi-system-classes.md)
</dt> <dt>

[**Ace do Win32 \_**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[Mantendo a segurança do WMI](maintaining-wmi-security.md)
</dt> </dl>

 

