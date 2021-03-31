---
description: Fornece informações adicionais a serem usadas com o método ExportReferencePoint da classe Msvm \_ VirtualSystemReferencePointService.
ms.assetid: 4897fad4-3a3f-47bc-837d-2e36434b3fab
title: Classe Msvm_VirtualSystemReferencePointExportSettingData
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
ms.openlocfilehash: 65fc16f409fd79782ec4a91f223dfc754563f8bb
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104011940"
---
# <a name="msvm_virtualsystemreferencepointexportsettingdata-class"></a>\_Classe Msvm VirtualSystemReferencePointExportSettingData

Fornece informações adicionais a serem usadas com o método [**ExportReferencePoint**](msvm-virtualsystemreferencepointservice-exportreferencepoint.md) da classe [**Msvm \_ VirtualSystemReferencePointService**](msvm-virtualsystemreferencepointservice.md) .

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

A classe **Msvm \_ VirtualSystemReferencePointExportSettingData** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ VirtualSystemReferencePointExportSettingData** tem essas propriedades.

<dl> <dt>

**BaseReferencePoint**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Caminho do ponto de referência base com relação ao qual a exportação deve ser executada.

</dd> <dt>

**DisksToExport**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

IDs da instância do WMI dos discos para os quais os dados precisam ser exportados.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CIM \_ SettingData**](cim-settingdata.md)
</dt> </dl>

 

 




