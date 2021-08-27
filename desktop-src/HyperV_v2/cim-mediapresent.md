---
description: Representa uma relação na qual uma extensão de armazenamento deve ser acessada por meio de um dispositivo de acesso à mídia.
ms.assetid: 436a7e2d-2c14-4058-aca0-669373b8004a
title: Classe CIM_MediaPresent (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MediaPresent
- CIM_MediaPresent.Antecedent
- CIM_MediaPresent.Dependent
- CIM_MediaPresent.FixedMedia
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6694c945594f0ea5008f6b5f574b84accd338f89a45819a8fb02793bc619ea1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046796"
---
# <a name="cim_mediapresent-class-hyper-v-management"></a>Classe CIM_MediaPresent (gerenciamento do Hyper-V)

Representa uma relação na qual uma extensão de armazenamento deve ser acessada por meio de um dispositivo de acesso à mídia.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::StorageExtents"), MappingStrings("MIF.DMTF|Storage Devices|001.8"), AMENDMENT]
class CIM_MediaPresent : CIM_Dependency
{
  CIM_MediaAccessDevice REF Antecedent;
  CIM_StorageExtent     REF Dependent;
  boolean                   FixedMedia;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ MediaPresent** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ MediaPresent** tem essas propriedades.

<dl> <dt>

**Antecedent**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ MediaAccessDevice**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

O dispositivo de acesso à mídia.

</dd> <dt>

**Depende**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ StorageExtent**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")
</dt> </dl>

A extensão de armazenamento que é acessada ao usar o dispositivo de acesso à mídia.

</dd> <dt>

**FixedMedia**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

**true** se a extensão de armazenamento for fixada no dispositivo de acesso à mídia e não puder ser ejetada; caso contrário, **false**.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Dependência CIM**](cim-dependency.md)
</dt> </dl>

 

