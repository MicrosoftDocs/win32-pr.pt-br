---
description: A classe WMI de associação Win32 PnPDevice relaciona um dispositivo (conhecido como Gerenciador de Configurações como um PNPEntity) e a função que \_ ele executa.
ms.assetid: 5163a423-60f2-416d-bf82-89517b499f93
ms.tgt_platform: multiple
title: Win32_PnPDevice classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPDevice
- Win32_PnPDevice.SameElement
- Win32_PnPDevice.SystemElement
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a136c86c0fd0744c555af2071943d99ca8569a33ce9c59d9d22191c4a78d2a32
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119972036"
---
# <a name="win32_pnpdevice-class"></a>Classe Win32 \_ PnPDevice

A classe [WMI](../wmisdk/retrieving-a-class.md) de associação **\_ Win32 PnPDevice** relaciona um dispositivo (conhecido como Gerenciador de Configurações como um PNPEntity) e a função que ele executa. Sua função é representada por uma subclasse do dispositivo lógico que descreve seu uso. Por exemplo, uma [**instância do Win32 \_ Keyboard**](win32-keyboard.md) ou [**do Win32 \_ DiskDrive.**](win32-diskdrive.md) Ambos os objetos referenciados representam o mesmo dispositivo do sistema subjacente; as alterações na alocação de recursos no lado do PNPEntity terão efeito no dispositivo associado.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{FE28FD96-C875-11d2-B352-00104BC97924}"), AMENDMENT]
class Win32_PnPDevice
{
  CIM_LogicalDevice REF SameElement;
  Win32_PnPEntity   REF SystemElement;
};
```

## <a name="members"></a>Membros

A **classe Win32 \_ PnPDevice** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe Win32 \_ PnPDevice** tem essas propriedades.

<dl> <dt>

**SameElement**
</dt> <dd> <dl> <dt>

Tipo de dados: **Cim \_ LogicalDevice**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ LogicalDevice")
</dt> </dl>

Referência à instância [**\_ LogicalDevice cim**](cim-logicaldevice.md) que representa as propriedades lógicas do dispositivo associadas ao Plug and Play dispositivo.

</dd> <dt>

**SystemElement**
</dt> <dd> <dl> <dt>

Tipo de dados: **Win32 \_ PnPEntity**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ PnPEntity")
</dt> </dl>

Referência à instância [**do Win32 \_ PnPEntity que**](win32-pnpentity.md) representa Plug and Play dispositivo associado ao dispositivo lógico.

</dd> </dl>

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

[Classes de hardware do sistema de computador](computer-system-hardware-classes.md)
</dt> </dl>

 

 
