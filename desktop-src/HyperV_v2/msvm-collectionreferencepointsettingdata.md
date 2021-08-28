---
description: Fornece informações adicionais a serem usadas com o método CreateReferencePoint da classe Msvm \_ CollectionReferencePointService.
ms.assetid: abf7953a-e10e-4dab-962f-a7dde5126fbe
title: Classe Msvm_CollectionReferencePointSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointSettingData
- Msvm_CollectionReferencePointSettingData.ConsistencyLevel
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1164c61f9335ce900dfbcf0b317dd0c4c9a8f84c0a97aaf13b2ea851a80dbd17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130666"
---
# <a name="msvm_collectionreferencepointsettingdata-class"></a>\_Classe Msvm CollectionReferencePointSettingData

Fornece informações adicionais a serem usadas com o método [**CreateReferencePoint**](msvm-collectionreferencepointservice-createreferencepoint.md) da classe [**Msvm \_ CollectionReferencePointService**](msvm-collectionreferencepointservice.md) .

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[AMENDMENT]
class Msvm_CollectionReferencePointSettingData : CIM_SettingData
{
  uint8 ConsistencyLevel;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ CollectionReferencePointSettingData** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ CollectionReferencePointSettingData** tem essas propriedades.

<dl> <dt>

**ConsistencyLevel**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Nível de consistência do ponto de referência.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Consistente** com o aplicativo (1)


</dt> <dd>

O ponto de referência indica um ponto no tempo em que o sistema virtual estava em estado de falha consistente.

</dd> <dt>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Falha consistente** (2)


</dt> <dd>

O ponto de referência indica um ponto no tempo em que o sistema virtual estava no estado consistente do aplicativo.

</dd> </dl>

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

[**CIM \_ SettingData**](cim-settingdata.md)
</dt> </dl>

 

 




