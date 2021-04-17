---
description: Uma associação entre uma instância do CIM \_ VirtualSystemSettingData e a \_ instância VIRTUALSYSTEMSETTINGDATA do CIM que representa o instantâneo mais recente no qual esse objeto se baseia.
ms.assetid: f6e93c22-077b-4604-8d0d-9584b1f4dce1
ms.tgt_platform: multiple
title: Classe CIM_ParentChildSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ParentChildSettingData
- Root\CIMV2.CIM_ParentChildSettingData.Antecedent
- Root\CIMV2.CIM_ParentChildSettingData.Dependent
- Root\CIMV2.CIM_ParentChildSettingData.Parent
- Root\CIMV2.CIM_ParentChildSettingData.Child
api_type:
- Schema
api_location:
- Root\CIMV2
ms.openlocfilehash: 9b2b866c3d5ae15d3f5a97c971e8efec75e9164c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105791386"
---
# <a name="cim_parentchildsettingdata-class"></a>\_Classe CIM ParentChildSettingData

Uma associação entre uma instância do [**CIM \_ VirtualSystemSettingData**](/previous-versions/windows/desktop/clushyperv/cim-virtualsystemsettingdata) e a **instância \_ VirtualSystemSettingData do CIM** que representa o instantâneo mais recente no qual esse objeto se baseia.

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
class CIM_ParentChildSettingData : CIM_Dependency
{
  CIM_ManagedSystemElement     REF Antecedent;
  CIM_ManagedSystemElement     REF Dependent;
  CIM_VirtualSystemSettingData REF Parent;
  CIM_VirtualSystemSettingData REF Child;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ ParentChildSettingData** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ ParentChildSettingData** tem essas propriedades.

<dl> <dt>

**Antecedent**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ ManagedSystemElement**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Referência ao objeto independente nesta associação.

Essa propriedade é herdada [**da \_ dependência CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).

</dd> <dt>

**Filho**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ VirtualSystemSettingData**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Os dados de configuração para o sistema virtual que representa o filho do pai.

</dd> <dt>

**Depende**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ ManagedSystemElement**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Referência ao objeto que é dependente da propriedade **Antecedent** .

Essa propriedade é herdada [**da \_ dependência CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).

</dd> <dt>

**Pai**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ VirtualSystemSettingData**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Os dados de configuração de instantâneo nos quais os dados de configuração filho se baseiam.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------|
| Namespace<br/> | Raiz \\ cimv2<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Dependência CIM**](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> </dl>

 

