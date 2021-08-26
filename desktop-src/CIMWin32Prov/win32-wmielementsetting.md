---
description: a \_ classe WMI de associação Win32 WMIElementSetting relaciona um serviço em execução no sistema Windows e as configurações de WMI que ele pode usar.
ms.assetid: 00e9f882-5f54-4042-a916-2f90ed9a37c0
ms.tgt_platform: multiple
title: Classe Win32_WMIElementSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_WMIElementSetting
- Win32_WMIElementSetting.Element
- Win32_WMIElementSetting.Setting
api_type:
- DllExport
api_location:
- Wbemcore.dll
ms.openlocfilehash: f46a9d5fd7c3f0baace1f763b9912f49fbcf318ffd07fa7cbf3138d04d8621f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922536"
---
# <a name="win32_wmielementsetting-class"></a>\_Classe Win32 WMIElementSetting

a [classe WMI](../wmisdk/retrieving-a-class.md) de associação **Win32 \_ WMIElementSetting** relaciona um serviço em execução no sistema Windows e as configurações de WMI que ele pode usar.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("WBEMCORE"), UUID("{A83EF167-CA8D-11d2-B33D-00104BCC4B4A}"), AMENDMENT]
class Win32_WMIElementSetting : CIM_ElementSetting
{
  Win32_Service    REF Element;
  Win32_WMISetting REF Setting;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ WMIElementSetting** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ WMIElementSetting** tem essas propriedades.

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ serviço Win32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**chave**](../wmisdk/key-qualifier.md), [**substituição**](../wmisdk/standard-qualifiers.md) ("element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ Service")
</dt> </dl>

referência à instância que representa o serviço de Windows usando ou identificando propriedades WMI.

</dd> <dt>

**Configuração**
</dt> <dd> <dl> <dt>

Tipo de dados: **Win32 \_ WMISetting**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**chave**](../wmisdk/key-qualifier.md), [**substituição**](../wmisdk/standard-qualifiers.md) ("configuração"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ WMISetting")
</dt> </dl>

referência à instância que representa as configurações de WMI disponíveis para o serviço de Windows.

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **Win32 \_ WMIElementSetting** é derivada de [**CIM \_ ElementSetting**](cim-elementsetting.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemcore.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_ELEMENTSETTING CIM**](cim-elementsetting.md)
</dt> <dt>

[Classes de gerenciamento de serviço WMI](./wmi-service-management-classes.md)
</dt> </dl>

 

 
