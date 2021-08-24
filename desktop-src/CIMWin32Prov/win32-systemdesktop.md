---
description: A classe WMI de associação Win32 SystemDesktop relaciona um sistema \_ de computador e sua configuração de área de trabalho.
ms.assetid: 2b024660-d707-4463-8207-73df74bfa7d6
ms.tgt_platform: multiple
title: Win32_SystemDesktop classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDesktop
- Win32_SystemDesktop.Element
- Win32_SystemDesktop.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a7158e42589018364b9d55b578941bc3e6897576c6633b2a9fa0b0d09e4fede9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751336"
---
# <a name="win32_systemdesktop-class"></a>Classe Win32 \_ SystemDesktop

A classe [WMI](../wmisdk/retrieving-a-class.md) de associação **\_ Win32 SystemDesktop** relaciona um sistema de computador e sua configuração de área de trabalho.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades e os métodos estão em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C506-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemDesktop : Win32_SystemSetting
{
  Win32_ComputerSystem REF Element;
  Win32_Desktop        REF Setting;
};
```

## <a name="members"></a>Membros

A **classe \_ SystemDesktop do Win32** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ SystemDesktop do Win32** tem essas propriedades.

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

Tipo de dados: **Win32 \_ ComputerSystem**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Substituir**](../wmisdk/standard-qualifiers.md) ("Elemento"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")
</dt> </dl>

Referência à instância que representa o sistema de computador em que a configuração da área de trabalho existe.

</dd> <dt>

**Configuração**
</dt> <dd> <dl> <dt>

Tipo de dados: **Win32 \_ Desktop**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Substituir**](../wmisdk/standard-qualifiers.md) ("Configuração"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ Desktop")
</dt> </dl>

Referência à instância que representa a configuração existente no sistema de computador.

</dd> </dl>

## <a name="remarks"></a>Comentários

A **classe \_ SystemDesktop win32** é derivada de [**Win32 \_ SystemSetting**](win32-systemsetting.md).

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

[**SystemSetting do Win32 \_**](win32-systemsetting.md)
</dt> <dt>

[Classes do sistema operacional](./operating-system-classes.md)
</dt> </dl>

 

 
