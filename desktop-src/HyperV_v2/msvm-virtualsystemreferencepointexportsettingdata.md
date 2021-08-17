---
description: Fornece informações adicionais a serem usadas com o método ExportReferencePoint da classe Msvm \_ VirtualSystemReferencePointService.
ms.assetid: 4897fad4-3a3f-47bc-837d-2e36434b3fab
title: Msvm_VirtualSystemReferencePointExportSettingData classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointExportSettingData
- Msvm_VirtualSystemReferencePointExportSettingData.BaseReferencePoint
- Msvm_VirtualSystemReferencePointExportSettingData.DisksToExport
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2b3fc743d8431d76582553979bb25e1269df970d70187c65c2bddd1014834c76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147939"
---
# <a name="msvm_virtualsystemreferencepointexportsettingdata-class"></a>Classe Msvm \_ VirtualSystemReferencePointExportSettingData

Fornece informações adicionais a serem usadas com [**o método ExportReferencePoint**](msvm-virtualsystemreferencepointservice-exportreferencepoint.md) da [**classe Msvm \_ VirtualSystemReferencePointService.**](msvm-virtualsystemreferencepointservice.md)

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[AMENDMENT]
class Msvm_VirtualSystemReferencePointExportSettingData : CIM_SettingData
{
  String BaseReferencePoint;
  String DisksToExport[];
};
```

## <a name="members"></a>Membros

A **classe Msvm \_ VirtualSystemReferencePointExportSettingData** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe Msvm \_ VirtualSystemReferencePointExportSettingData** tem essas propriedades.

<dl> <dt>

**BaseReferencePoint**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Caminho do ponto de referência base em relação ao qual a exportação deve ser executada.

</dd> <dt>

**DisksToExport**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **de cadeia de** caracteres
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

IDs de instância WMI dos discos para os quais os dados precisam ser exportados.

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

 

 




