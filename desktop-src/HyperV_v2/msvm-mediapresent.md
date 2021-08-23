---
description: Associa uma unidade de armazenamento à mídia inserida na unidade.
ms.assetid: C0B2D604-0B55-4EA0-A46E-2450D89A5B22
title: Msvm_MediaPresent classe
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
ms.openlocfilehash: 7044cfed5a4affd628ea8008c89b4aabeee3499d65f03abf815e68d73d06a773
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119521716"
---
# <a name="msvm_mediapresent-class"></a>Classe Msvm \_ MediaPresent

Associa uma unidade de armazenamento à mídia inserida na unidade. Essa associação é usada para todos os objetos de unidade de armazenamento.

A sintaxe a seguir é simplificada Managed Object Format código MOF e inclui todas as propriedades herdadas.

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

A **classe Msvm \_ MediaPresent** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe Msvm \_ MediaPresent** tem essas propriedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **Cim \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A referência ao dispositivo de acesso à mídia. Essa propriedade é herdada de [**CIM \_ MediaPresent.**](/windows/desktop/CIMWin32Prov/cim-mediapresent)

</dd> <dt>

**Dependente**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **Cim \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A referência à extensão de armazenamento acessada com o dispositivo de acesso à mídia. Essa propriedade é herdada de [**CIM \_ MediaPresent.**](/windows/desktop/CIMWin32Prov/cim-mediapresent)

</dd> <dt>

**FixedMedia**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a extensão de armazenamento acessada é fixa e não pode ser ejetada. O valor é **True para** discos rígidos e **False caso** contrário. Essa propriedade é herdada de [**CIM \_ MediaPresent.**](/windows/desktop/CIMWin32Prov/cim-mediapresent)

</dd> </dl>

## <a name="remarks"></a>Comentários

O acesso à **classe Msvm \_ MediaPresent** pode ser restrito pela Filtragem de UAC. Para obter mais informações, consulte [Controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                                    |
| Namespace<br/>                | Virtualização \\ raiz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CIM \_ MediaPresent**](cim-mediapresent.md)
</dt> <dt>

[**CIM \_ MediaPresent**](/windows/desktop/CIMWin32Prov/cim-mediapresent)
</dt> <dt>

[Armazenamento Classes](storage-classes.md)
</dt> </dl>

 

