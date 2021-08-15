---
description: Associa o Msvm \_ snapshotcollection aos \_ objetos Msvm VirtualSystemSettingData contidos.
ms.assetid: 21005e8a-0bc6-4ea7-8f6f-d79803b43bc0
title: Classe Msvm_CollectedSnapshots
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectedSnapshots
- Msvm_CollectedSnapshots.Collection
- Msvm_CollectedSnapshots.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5e5a1007516e5b8b7d827f0a96e1fd7fd5541cba2277111830605971c6d8a101
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119427116"
---
# <a name="msvm_collectedsnapshots-class"></a>\_Classe Msvm CollectedSnapshots

Associa o [**Msvm \_ snapshotcollection**](msvm-snapshotcollection.md) aos objetos [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) contidos.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectedSnapshots : CIM_CollectedMSEs
{
  Msvm_SnapshotCollection       REF Collection;
  Msvm_VirtualSystemSettingData REF Member;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ CollectedSnapshots** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ CollectedSnapshots** tem essas propriedades.

<dl> <dt>

**Coleção**
</dt> <dd> <dl> <dt>

Tipo de dados: **Msvm \_ snapshotcollection**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**agregação**](/windows/desktop/WmiSdk/standard-qualifiers), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("coleção")
</dt> </dl>

Um objeto de agrupamento ou ' recipiente ' do [**Msvm \_ snapshotcollection**](msvm-snapshotcollection.md) que representa a coleção.

</dd> <dt>

**Membro**
</dt> <dd> <dl> <dt>

Tipo de dados: **Msvm \_ VirtualSystemSettingData**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("membro")
</dt> </dl>

Um [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) que contém os membros da coleção.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10 \[ somente aplicativos da área de trabalho\]<br/>                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_COLLECTEDMSES CIM**](cim-collectedmses.md)
</dt> </dl>

 

