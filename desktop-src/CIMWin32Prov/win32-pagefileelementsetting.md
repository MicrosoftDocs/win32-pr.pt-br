---
description: A classe WMI de associação Win32 PageFileElementSetting relaciona as configurações iniciais de um arquivo de página e o estado dessas configurações durante \_ o uso normal.
ms.assetid: efc1f20d-166e-4e27-9767-f6ec0bbd6c14
ms.tgt_platform: multiple
title: Win32_PageFileElementSetting classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFileElementSetting
- Win32_PageFileElementSetting.Element
- Win32_PageFileElementSetting.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 366f2b8ae14e57d17b4f6a48fb59cdd6c5cfd5c2c12068e40650e410c7c1f45f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119972256"
---
# <a name="win32_pagefileelementsetting-class"></a>Classe \_ PageFileElementSetting do Win32

A classe [WMI](../wmisdk/retrieving-a-class.md) de associação **Win32 \_ PageFileElementSetting** relaciona as configurações iniciais de um arquivo de página e o estado dessas configurações durante o uso normal.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades e os métodos estão em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8E7F70E8-C856-11D2-B364-00105A1F77A1}"), AMENDMENT]
class Win32_PageFileElementSetting : CIM_ElementSetting
{
  Win32_PageFileUsage   REF Element;
  Win32_PageFileSetting REF Setting;
};
```

## <a name="members"></a>Membros

A **classe \_ PageFileElementSetting do Win32** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ PageFileElementSetting do Win32** tem essas propriedades.

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

Tipo de dados: **\_ PageFileUsage do Win32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ PageFileUsage")
</dt> </dl>

Referência à instância que representa as propriedades de um arquivo de página enquanto o sistema Win32 está em uso.

</dd> <dt>

**Configuração**
</dt> <dd> <dl> <dt>

Tipo de dados: **\_ PageFileSetting do Win32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**chave**](../wmisdk/key-qualifier.md), [**Substituir**](../wmisdk/standard-qualifiers.md) ("Configuração"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ PageFileSetting")
</dt> </dl>

Referência à instância que representa as configurações iniciais de um arquivo de página quando o sistema Win32 está sendo inicializado.

</dd> </dl>

## <a name="remarks"></a>Comentários

A **classe \_ PageFileElementSetting do Win32** é derivada de [**\_ ElementSetting cim.**](cim-elementsetting.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | RAIZ \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento \_ CIMSetting**](cim-elementsetting.md)
</dt> <dt>

[Classes do sistema operacional](./operating-system-classes.md)
</dt> </dl>

 

 
