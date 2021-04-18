---
description: Controla o acesso remoto a versões sem suporte do Windows.
ms.assetid: eb326bba-a011-4b9c-b4ee-fc08ae364f6f
ms.tgt_platform: multiple
title: Classe __NTLMUser9X
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NTLMUser9X
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 79aa5153869c7337b6849e8c465dbbf8b36a0f58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105813694"
---
# <a name="__ntlmuser9x-class"></a>\_\_Classe NTLMUser9X

A classe de sistema **\_ \_ NTLMUser9X** controla o acesso remoto a versões sem suporte do Windows. A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class __NTLMUser9X : __SecurityRelatedClass
{
  string Authority;
  sint32 Flags;
  sint32 Mask;
  string Name;
  sint32 Type;
};
```

## <a name="members"></a>Membros

A classe **\_ \_ NTLMUser9X** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **\_ \_ NTLMUser9X** tem essas propriedades.

<dl> <dt>

**Autoridade**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Domínio ao qual um nome de usuário se aplica.

</dd> <dt>

**Sinalizadores**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Sinalizadores de herança.

<dt>

0
</dt> <dd>

Nenhuma herança.

</dd> <dt>

2
</dt> <dd>

Aplicar a namespaces filho, além do atual.

</dd> </dl>

</dd> <dt>

**Mask**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Bitmask que especifica os direitos de acesso ao namespace no repositório Instrumentação de Gerenciamento do Windows (WMI). Para valores de bit, consulte [**constantes de direitos de acesso de namespace**](namespace-access-rights-constants.md).

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Nome de usuário.

</dd> <dt>

**Tipo**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Acesso permitido.

<dt>

0
</dt> <dd>

Acesso permitido.

</dd> <dt>

2
</dt> <dd>

Acesso negado.

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **\_ \_ NTLMUser9X** é usada como um parâmetro de entrada para os métodos [**\_ \_ SystemSecurity:: Get9XUserList**](--systemsecurity-get9xuserlist.md) e [**\_ \_ SystemSecurity:: Set9XUserList**](--systemsecurity-set9xuserlist.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Todos os namespaces do WMI<br/>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_\_SecurityRelatedClass**](/windows/desktop/WmiSdk/--securityrelatedclass)
</dt> <dt>

[Classes do sistema WMI](wmi-system-classes.md)
</dt> <dt>

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> </dl>

 

