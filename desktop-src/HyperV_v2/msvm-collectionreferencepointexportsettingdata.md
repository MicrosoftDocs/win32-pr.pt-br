---
description: Exporte os dados de configuração a serem passados para o método ExportReferencePoint da \_ classe Msvm CollectionReferencePointService.
ms.assetid: 38299050-a53a-496c-8792-9199c394591d
title: Classe Msvm_CollectionReferencePointExportSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointExportSettingData
- Msvm_CollectionReferencePointExportSettingData.BaseReferencePointCollection
- Msvm_CollectionReferencePointExportSettingData.VirtualMachinesToDisksToExport
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b8b160f16a71e25eca4afa445fd05fd1faba58c82c6ba6e08afd25bbc9ba41b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118149239"
---
# <a name="msvm_collectionreferencepointexportsettingdata-class"></a>\_Classe Msvm CollectionReferencePointExportSettingData

Exporte os dados de configuração a serem passados para o método [**ExportReferencePoint**](msvm-collectionreferencepointservice-exportreferencepoint.md) da classe [**Msvm \_ CollectionReferencePointService**](msvm-collectionreferencepointservice.md) .

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[AMENDMENT]
class Msvm_CollectionReferencePointExportSettingData : CIM_SettingData
{
  string BaseReferencePointCollection;
  string VirtualMachinesToDisksToExport[];
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ CollectionReferencePointExportSettingData** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ CollectionReferencePointExportSettingData** tem essas propriedades.

<dl> <dt>

**BaseReferencePointCollection**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Caminho para uma instância de [**Msvm \_ ReferencePointCollection**](msvm-referencepointcollection.md) que representa a coleção de pontos de referência base a ser usada para exportação diferencial.

</dd> <dt>

**VirtualMachinesToDisksToExport**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: **HyperVEmbeddedInstance** ("Msvm \_ VirtualMachineToDisks")
</dt> </dl>

Lista de "VirtualMachines para DisksToExport" informações de mapa para as quais os dados precisam ser exportados.

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

 

 




