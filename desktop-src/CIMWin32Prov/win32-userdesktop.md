---
description: A \_ classe WMI de associação do Userdesktop do Win32 relaciona uma conta de usuário e configurações de área de trabalho que são específicas a ela.
ms.assetid: 5ea83ad6-bd0a-4c16-85b2-e3e61ef05903
ms.tgt_platform: multiple
title: Classe Win32_UserDesktop
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_UserDesktop
- Win32_UserDesktop.Element
- Win32_UserDesktop.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 39b45ee7859fea9f1068123041a87309cf40c2d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826241"
---
# <a name="win32_userdesktop-class"></a>\_Classe Win32 Userdesktop

A [classe WMI](../wmisdk/retrieving-a-class.md) de associação do **\_ userdesktop do Win32** relaciona uma conta de usuário e configurações de área de trabalho que são específicas a ela.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4FF-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_UserDesktop : CIM_ElementSetting
{
  Win32_UserAccount REF Element;
  Win32_Desktop     REF Setting;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ userdesktop** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ userdesktop** tem essas propriedades.

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ conta de userwin32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**chave**](../wmisdk/key-qualifier.md), [**substituição**](../wmisdk/standard-qualifiers.md) ("elemento"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("conta de userwmi \| Win32 \_ ")
</dt> </dl>

Referência à instância que representa a conta de usuário cuja área de trabalho pode ser personalizada pela propriedade **Settings** dessa classe.

</dd> <dt>

**Configuração**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ Desktop Win32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**chave**](../wmisdk/key-qualifier.md), [**substituição**](../wmisdk/standard-qualifiers.md) ("configuração"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("área de trabalho do WMI \| Win32 \_ ")
</dt> </dl>

Referência à instância que representa as configurações da área de trabalho que servem para personalizar uma área de trabalho de conta de usuário específica.

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **Win32 \_ userdesktop** é derivada do [**CIM \_ ElementSetting**](cim-elementsetting.md).

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

[Classes do sistema operacional](./operating-system-classes.md)
</dt> </dl>

 

 
