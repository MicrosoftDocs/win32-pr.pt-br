---
description: A \_ classe WMI de associação COMApplicationSettings do Win32 relaciona um aplicativo DCOM e suas definições de configuração.
ms.assetid: b08eaff1-b42a-42f3-abf7-3664b6195acd
ms.tgt_platform: multiple
title: Classe Win32_COMApplicationSettings
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_COMApplicationSettings
- Win32_COMApplicationSettings.Setting
- Win32_COMApplicationSettings.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0a1126563b00861ab8b8168832f72189c3a3828378f5d89c4b74e49f68b09bd4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118417906"
---
# <a name="win32_comapplicationsettings-class"></a>\_Classe Win32 COMApplicationSettings

A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de associação **\_ COMApplicationSettings do Win32** relaciona um aplicativo DCOM e suas definições de configuração.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{E5D8A563-F6C0-11d2-B35E-00105A1F8569}"), AMENDMENT]
class Win32_COMApplicationSettings : CIM_ElementSetting
{
  Win32_DCOMApplicationSetting REF Setting;
  Win32_DCOMApplication        REF Element;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ COMApplicationSettings** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ COMApplicationSettings** tem essas propriedades.

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

Tipo de dados: **Win32 \_ DCOMApplication**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("elemento"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ DCOMApplication")
</dt> </dl>

Um [**\_ DCOMApplication Win32**](win32-dcomapplication.md) que representa o aplicativo DCOM no qual as configurações são aplicadas.

</dd> <dt>

**Configuração**
</dt> <dd> <dl> <dt>

Tipo de dados: **Win32 \_ DCOMApplicationSetting**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("configuração"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ DCOMApplicationSetting")
</dt> </dl>

Um [**\_ DCOMApplicationSetting Win32**](win32-dcomapplicationsetting.md) que representa os parâmetros de configuração associados ao aplicativo DCOM.

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **Win32 \_ COMApplicationSettings** é derivada de [**CIM \_ ElementSetting**](cim-elementsetting.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_ELEMENTSETTING CIM**](cim-elementsetting.md)
</dt> <dt>

[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

