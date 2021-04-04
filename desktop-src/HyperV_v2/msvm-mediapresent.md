---
description: Associa uma unidade de armazenamento à mídia inserida na unidade.
ms.assetid: C0B2D604-0B55-4EA0-A46E-2450D89A5B22
title: Classe Msvm_MediaPresent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MediaPresent
- Msvm_MediaPresent.Antecedent
- Msvm_MediaPresent.Dependent
- Msvm_MediaPresent.FixedMedia
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 57d46fb711ab8d4abcf27966e6ec92ed2287bc3e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103837676"
---
# <a name="msvm_mediapresent-class"></a>\_Classe Msvm MediaPresent

Associa uma unidade de armazenamento à mídia inserida na unidade. Essa associação é usada para todos os objetos da unidade de armazenamento.

A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MediaPresent : CIM_MediaPresent
{
  CIM_MediaAccessDevice REF Antecedent;
  CIM_StorageExtent     REF Dependent;
  boolean                   FixedMedia;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ MediaPresent** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ MediaPresent** tem essas propriedades.

<dl> <dt>

**Antecedent**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A referência ao dispositivo de acesso à mídia. Essa propriedade é herdada do [**CIM \_ MediaPresent**](/windows/desktop/CIMWin32Prov/cim-mediapresent).

</dd> <dt>

**Depende**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A referência à extensão de armazenamento acessada com o dispositivo de acesso à mídia. Essa propriedade é herdada do [**CIM \_ MediaPresent**](/windows/desktop/CIMWin32Prov/cim-mediapresent).

</dd> <dt>

**FixedMedia**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a extensão de armazenamento acessada é fixa e não pode ser ejetada. O valor é **true** para discos rígidos; caso contrário, **false** . Essa propriedade é herdada do [**CIM \_ MediaPresent**](/windows/desktop/CIMWin32Prov/cim-mediapresent).

</dd> </dl>

## <a name="remarks"></a>Comentários

O acesso à classe **Msvm \_ MediaPresent** pode ser restringido pela filtragem do UAC. Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                                    |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_MEDIAPRESENT CIM**](cim-mediapresent.md)
</dt> <dt>

[**\_MEDIAPRESENT CIM**](/windows/desktop/CIMWin32Prov/cim-mediapresent)
</dt> <dt>

[Classes de armazenamento](storage-classes.md)
</dt> </dl>

 

