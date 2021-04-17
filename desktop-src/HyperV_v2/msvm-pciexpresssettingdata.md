---
description: Representa o estado configurado de uma porta PCI Express.
ms.assetid: adb03dd7-5a47-47e6-a4e4-28224164150c
title: Classe Msvm_PciExpressSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_PciExpressSettingData
- Msvm_PciExpressSettingData.VirtualFunctions
- Msvm_PciExpressSettingData.VirtualSystemIdentifiers
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c092cbc119506c4c52bc0565cd969426feffc481
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105789800"
---
# <a name="msvm_pciexpresssettingdata-class"></a>\_Classe Msvm PciExpressSettingData

Representa o estado configurado de uma porta PCI Express.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_PciExpressSettingData : CIM_ResourceAllocationSettingData
{
  uint16 VirtualFunctions[];
  string VirtualSystemIdentifiers[];
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ PciExpressSettingData** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ PciExpressSettingData** tem essas propriedades.

<dl> <dt>

**VirtualFunctions**
</dt> <dd> <dl> <dt>

Tipo de dados: a matriz **UInt16**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

O número da função virtual a ser atribuída à VM.

</dd> <dt>

**VirtualSystemIdentifiers**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")
</dt> </dl>

Uma matriz de cadeia de caracteres de forma livre de identificadores desse recurso apresentada ao sistema operacional do sistema de computador virtual. Os índices e valores por índice são definidos por recurso (ou seja, para cada valor de **ResourceType** enumerado). Essa propriedade é definida como "GUID".

Essa é uma propriedade somente leitura, mas pode ser alterada usando o método [**ModifyVirtualSystemResources**](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice) da classe SD.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_RESOURCEALLOCATIONSETTINGDATA CIM**](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

