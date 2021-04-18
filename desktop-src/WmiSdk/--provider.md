---
description: Serve como a classe pai para a \_ \_ classe do sistema Win32Provider.
ms.assetid: e4cad7c6-4650-4334-b8c4-ac65381bced7
ms.tgt_platform: multiple
title: Classe __Provider
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __Provider
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 733323c106a5d682e7eddbe3a41bf9c156520c51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105791427"
---
# <a name="__provider-class"></a>\_\_Classe de provedor

A classe de sistema do **\_ \_ provedor** é uma classe base abstrata que serve como a classe pai para a classe do sistema [**\_ \_ Win32Provider**](--win32provider.md) .

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[abstract]
class __Provider : __SystemClass
{
  string Name;
};
```

## <a name="members"></a>Membros

A classe **\_ \_ Provider** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **\_ \_ Provider** tem essas propriedades.

<dl> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [ **chave**](standard-qualifiers.md)
</dt> </dl>

Cadeia de caracteres neutra de idioma que identifica exclusivamente o provedor. O seguinte formato é sugerido para evitar conflitos de nomenclatura:

\|versão do provedor de fornecedor \|

Por exemplo, esse nome de provedor representa a versão 1,0 do Microsoft Testprovider:

"Microsoft \| testprovider \| v 1.0"

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe de **\_ \_ provedor** é derivada de [**\_ \_ SystemClass**](--systemclass.md), que não tem propriedades.

Os provedores criam instâncias [**\_ \_ Win32Provider**](--win32provider.md) para especificar informações sobre sua implementação física.

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
</dt> <dt>

[**\_\_Win32Provider**](--win32provider.md)
</dt> </dl>

 

