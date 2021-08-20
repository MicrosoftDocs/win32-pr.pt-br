---
description: Fornece informações adicionais a serem usadas com o método CreateReferencePoint da classe Msvm \_ VirtualSystemReferencePointService.
ms.assetid: 6b997ba5-871c-4c33-9ed5-b9a13cbfaacd
title: Msvm_VirtualSystemReferencePointSettingData classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointSettingData
- Msvm_VirtualSystemReferencePointSettingData.ConsistencyLevel
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 703b0b1cedc93e670ff8ac97c7dddf9041145a4eccc064e07562947aec898c0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118146368"
---
# <a name="msvm_virtualsystemreferencepointsettingdata-class"></a>Classe Msvm \_ VirtualSystemReferencePointSettingData

Fornece informações adicionais a serem usadas com o [**método CreateReferencePoint**](msvm-virtualsystemreferencepointservice-createreferencepoint.md) da classe [**Msvm \_ VirtualSystemReferencePointService.**](msvm-virtualsystemreferencepointservice.md)

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[AMENDMENT]
class Msvm_VirtualSystemReferencePointSettingData : CIM_SettingData
{
  uint8 ConsistencyLevel;
};
```

## <a name="members"></a>Membros

A **classe Msvm \_ VirtualSystemReferencePointSettingData** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe Msvm \_ VirtualSystemReferencePointSettingData** tem essas propriedades.

<dl> <dt>

**ConsistencyLevel**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nível de consistência do ponto de referência.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 10 somente aplicativos da área de trabalho\]<br/>                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | Virtualização \\ raiz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Configuração \_ cimData**](cim-settingdata.md)
</dt> </dl>

 

 




