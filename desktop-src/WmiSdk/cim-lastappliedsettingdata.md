---
description: Uma associação entre um objeto e outro objeto que foi aplicado a ele.
ms.assetid: ee6b17b7-4f01-4731-8d6b-a3421621a75a
ms.tgt_platform: multiple
title: Classe CIM_LastAppliedSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LastAppliedSettingData
- Root\CIMV2.CIM_LastAppliedSettingData.Target
- Root\CIMV2.CIM_LastAppliedSettingData.AppliedObject
api_type:
- Schema
api_location:
- Root\CIMV2
ms.openlocfilehash: fbad71cd88992673af5dd60c04b92dd3c833e5b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105793641"
---
# <a name="cim_lastappliedsettingdata-class"></a>\_Classe CIM LastAppliedSettingData

Uma associação entre um objeto e outro objeto que foi aplicado a ele.

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
class CIM_LastAppliedSettingData
{
  CIM_ManagedElement REF Target;
  CIM_ManagedElement REF AppliedObject;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ LastAppliedSettingData** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ LastAppliedSettingData** tem essas propriedades.

<dl> <dt>

**Aplicadoobject**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ managedelement**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **chave**
</dt> </dl>

O objeto que foi aplicado ao objeto de destino.

</dd> <dt>

**Target (destino)**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ managedelement**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **chave**
</dt> </dl>

O objeto que era o destino do aplicativo do objeto.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------|
| Namespace<br/> | Raiz \\ cimv2<br/> |



 

 




