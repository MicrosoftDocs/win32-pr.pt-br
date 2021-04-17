---
description: Uma associação entre um sistema virtual e os dados de configuração do instantâneo, que é o pai do sistema virtual.
ms.assetid: d11e00e0-a163-49ea-b8ef-e3909a7dc83f
ms.tgt_platform: multiple
title: Classe CIM_PreviousSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PreviousSettingData
- Root\CIMV2.CIM_PreviousSettingData.Target
- Root\CIMV2.CIM_PreviousSettingData.PreviousObject
api_type:
- Schema
api_location:
- Root\CIMV2
ms.openlocfilehash: 4422d590714b82120b610dc4eeb9377a385519d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782670"
---
# <a name="cim_previoussettingdata-class"></a>\_Classe CIM PreviousSettingData

Uma associação entre um sistema virtual e os dados de configuração do instantâneo, que é o pai do sistema virtual.

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
class CIM_PreviousSettingData
{
  CIM_ManagedElement REF Target;
  CIM_ManagedElement REF PreviousObject;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ PreviousSettingData** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ PreviousSettingData** tem essas propriedades.

<dl> <dt>

**Anteriorobject**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ managedelement**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **chave**
</dt> </dl>

Os dados de configuração de instantâneo que são o pai deste sistema de computador.

</dd> <dt>

**Target (destino)**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ managedelement**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **chave**
</dt> </dl>

O sistema de computador que foi o destino do aplicativo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------|
| Namespace<br/> | Raiz \\ cimv2<br/> |



 

 




