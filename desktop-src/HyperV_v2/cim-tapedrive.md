---
description: Representa os recursos e o gerenciamento de uma unidade de fita.
ms.assetid: 8140fd9a-8a12-43b4-bc61-ec143e5d754c
title: Classe CIM_TapeDrive (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TapeDrive
- CIM_TapeDrive.EOTWarningZoneSize
- CIM_TapeDrive.MaxPartitionCount
- CIM_TapeDrive.Padding
- CIM_TapeDrive.MaxRewindTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b4c12dce8e67a2f46d9c7e7a1ab4ae0772b9e20517da6ab58c00c45a9ea8c71b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118646704"
---
# <a name="cim_tapedrive-class-hyper-v-management"></a>Classe CIM_TapeDrive (gerenciamento do Hyper-V)

Representa os recursos e o gerenciamento de uma unidade de fita.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::StorageDevices")]
class CIM_TapeDrive : CIM_MediaAccessDevice
{
  uint32 EOTWarningZoneSize;
  uint32 MaxPartitionCount;
  uint32 Padding;
  uint64 MaxRewindTime;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ TapeDrive** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ TapeDrive** tem essas propriedades.

<dl> <dt>

**EOTWarningZoneSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), **PUnit** ("byte")
</dt> </dl>

O tamanho, em bytes, da área designada como "fim da fita". O acesso nessa área gera um aviso de "fim da fita".

</dd> <dt>

**MaxPartitionCount**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A contagem máxima de partições para a unidade de fita.

</dd> <dt>

**MaxRewindTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("milissegundos"), **PUnit** ("segundo \* 10 ^-3")
</dt> </dl>

O tempo, em milissegundos, para mover do ponto mais distante fisicamente na fita até o início.

</dd> <dt>

**Preenchimento**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), **PUnit** ("byte")
</dt> </dl>

O número de bytes inseridos entre os blocos na mídia de fita.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_MEDIAACCESSDEVICE CIM**](cim-mediaaccessdevice.md)
</dt> </dl>

 

