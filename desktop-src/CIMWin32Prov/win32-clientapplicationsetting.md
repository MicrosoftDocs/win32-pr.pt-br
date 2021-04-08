---
description: A \_ classe WMI de associação ClientApplicationSetting do Win32 relaciona um arquivo executável e um aplicativo de Component Object Model (com) que contém as opções de configuração com do arquivo executável.
ms.assetid: c43d80ee-0f29-4452-b51f-f18543bc1d35
ms.tgt_platform: multiple
title: Classe Win32_ClientApplicationSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClientApplicationSetting
- Win32_ClientApplicationSetting.Application
- Win32_ClientApplicationSetting.Client
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fda1f1305904fa919bb2080fe5de02f0e5850a8a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920500"
---
# <a name="win32_clientapplicationsetting-class"></a>\_Classe Win32 ClientApplicationSetting

A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de associação **\_ ClientApplicationSetting do Win32** relaciona um arquivo executável e um aplicativo de Component Object Model (com) que contém as opções de configuração com do arquivo executável.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{0F73ED5E-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ClientApplicationSetting
{
  Win32_DCOMApplication REF Application;
  CIM_DataFile          REF Client;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ ClientApplicationSetting** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ ClientApplicationSetting** tem essas propriedades.

<dl> <dt>

**Aplicativo**
</dt> <dd> <dl> <dt>

Tipo de dados: **Win32 \_ DCOMApplication**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ DCOMApplication")
</dt> </dl>

Referência à instância que representa o aplicativo COM que contém as opções de configuração do arquivo executável.

</dd> <dt>

**Cliente**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ DataFile do CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ DataFile")
</dt> </dl>

Referência à instância que representa o arquivo executável que usa as configurações de COM.

</dd> </dl>

## <a name="remarks"></a>Comentários

**Win32 \_ ClientApplicationSetting** não dá suporte à enumeração.

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

[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

