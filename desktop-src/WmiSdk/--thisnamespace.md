---
description: Mantém os direitos de segurança do namespace na forma de um descritor de segurança.
ms.assetid: 84e514f5-b114-4bfc-ab0b-9745f249168b
ms.tgt_platform: multiple
title: classe __thisNAMESPACE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __thisNAMESPACE
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 440ccdf0eda794b5d648cae756f9a9c808eb2db6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759926"
---
# <a name="__thisnamespace-class"></a>\_\_classe thisNAMESPACE

A classe de sistema **\_ \_ thisNamespace** mantém os direitos de segurança para o namespace na forma de um descritor de segurança. Essa classe e uma única instância são encontradas em todos os namespaces.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[singleton]
class __thisNAMESPACE : __SystemClass
{
  uint8 SECURITY_DESCRIPTOR[];
};
```

## <a name="members"></a>Membros

A classe **\_ \_ thisNamespace** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **\_ \_ thisNamespace** tem essas propriedades.

<dl> <dt>

**\_descritor de segurança**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descritor de segurança que descreve quem pode acessar o namespace e quem pode ler ou gravar no namespace. Esta propriedade é herdada do [**\_ \_ evento**](--event.md). Para obter mais informações sobre o formato dos descritores de segurança, consulte [descritores de segurança](/windows/desktop/SecAuthZ/security-descriptors) na seção segurança do SDK do Windows.

</dd> </dl>

## <a name="remarks"></a>Comentários

A instância singleton de **\_ \_ thisNamespace** é somente leitura. Para alterar as configurações da propriedade descritor de segurança, use os métodos da classe [**\_ \_ SystemSecurity**](--systemsecurity.md) . A classe **\_ \_ thisNamespace** deriva de [**\_ \_ SystemClass**](--systemclass.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Todos os namespaces do WMI<br/>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_\_SystemClass**](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[Classes do sistema WMI](wmi-system-classes.md)
</dt> </dl>

 

