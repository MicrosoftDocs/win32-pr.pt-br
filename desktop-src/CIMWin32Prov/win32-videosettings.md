---
description: A \_ classe WMI de associação do Win32 VideoSettings relaciona um controlador de vídeo e configurações de vídeo que podem ser aplicadas a ele.
ms.assetid: 0cc42352-0a89-434d-a8b6-230c677de49c
ms.tgt_platform: multiple
title: Classe Win32_VideoSettings
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_VideoSettings
- Win32_VideoSettings.Setting
- Win32_VideoSettings.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 38e949b6b6501dc51b39448d72e6bf61f37fbecb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754383"
---
# <a name="win32_videosettings-class"></a>\_Classe Win32 VideoSettings

A [classe WMI](../wmisdk/retrieving-a-class.md) de associação do **Win32 \_ VideoSettings** relaciona um controlador de vídeo e configurações de vídeo que podem ser aplicadas a ele.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{1008CCEE-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class Win32_VideoSettings : CIM_VideoSetting
{
  CIM_VideoControllerResolution REF Setting;
  Win32_VideoController         REF Element;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ VideoSettings** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ VideoSettings** tem essas propriedades.

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

Tipo de dados: **Win32 \_ VideoController**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**chave**](../wmisdk/key-qualifier.md), [**substituição**](../wmisdk/standard-qualifiers.md) ("elemento"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ VideoController")
</dt> </dl>

Um [**\_ VideoController Win32**](win32-videocontroller.md) que contém as propriedades do controlador de vídeo em que uma configuração de vídeo pode ser usada.

</dd> <dt>

**Configuração**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ VideoControllerResolution**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**chave**](../wmisdk/key-qualifier.md), [**substituição**](../wmisdk/standard-qualifiers.md) ("configuração"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ VideoControllerResolution")
</dt> </dl>

Um [**\_ VideoControllerResolution CIM**](cim-videocontrollerresolution.md) que contém configurações que podem ser aplicadas ao controlador de vídeo.

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **Win32 \_ VideoSettings** é derivada de [**CIM \_ VideoSetting**](cim-videosetting.md).

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

[**\_VIDEOSETTING CIM**](cim-videosetting.md)
</dt> <dt>

[Classes de hardware do sistema de computador](computer-system-hardware-classes.md)
</dt> </dl>

 

 
