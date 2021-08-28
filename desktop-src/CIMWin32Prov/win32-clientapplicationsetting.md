---
description: A classe WMI de associação Win32 ClientApplicationSetting relaciona um arquivo executável e um aplicativo COM (Component Object Model) que contém as opções de configuração COM para o \_ arquivo executável.
ms.assetid: c43d80ee-0f29-4452-b51f-f18543bc1d35
ms.tgt_platform: multiple
title: Win32_ClientApplicationSetting classe
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
ms.openlocfilehash: 359478d7cf6069e17ae02358f4ea48ffc44169f6822f4f8b3e33dad332fab020
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119546366"
---
# <a name="win32_clientapplicationsetting-class"></a>Classe Win32 \_ ClientApplicationSetting

A classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) de associação **Win32 \_ ClientApplicationSetting** relaciona um arquivo executável e um aplicativo COM (Component Object Model) que contém as opções de configuração COM para o arquivo executável.

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

A **classe Win32 \_ ClientApplicationSetting** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ ClientApplicationSetting do Win32** tem essas propriedades.

<dl> <dt>

**Aplicativo**
</dt> <dd> <dl> <dt>

Tipo de dados: **\_ Win32 DCOMApplication**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ DCOMApplication")
</dt> </dl>

Referência à instância que representa o aplicativo COM que contém opções de configuração do arquivo executável.

</dd> <dt>

**Cliente**
</dt> <dd> <dl> <dt>

Tipo de dados: **Cim \_ DataFile**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ DataFile")
</dt> </dl>

Referência à instância que representa o arquivo executável que usa configurações COM.

</dd> </dl>

## <a name="remarks"></a>Comentários

**Win32 \_ ClientApplicationSetting** não dá suporte à enumeração .

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

[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

