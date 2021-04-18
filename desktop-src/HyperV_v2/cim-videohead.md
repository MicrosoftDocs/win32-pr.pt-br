---
description: Representa um cabeçalho de um \_ objeto CIM DisplayController.
ms.assetid: 2bb034d9-d1df-4cc8-a6a8-b6ad7289f582
title: Classe CIM_VideoHead
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoHead
- CIM_VideoHead.CurrentBitsPerPixel
- CIM_VideoHead.CurrentHorizontalResolution
- CIM_VideoHead.CurrentVerticalResolution
- CIM_VideoHead.MaxRefreshRate
- CIM_VideoHead.MinRefreshRate
- CIM_VideoHead.CurrentRefreshRate
- CIM_VideoHead.CurrentScanMode
- CIM_VideoHead.OtherCurrentScanMode
- CIM_VideoHead.CurrentNumberOfRows
- CIM_VideoHead.CurrentNumberOfColumns
- CIM_VideoHead.CurrentNumberOfColors
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 22f8176c9bdbeae460dfa22ca395e7ed8dd8351e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758805"
---
# <a name="cim_videohead-class"></a>\_Classe CIM VideoHead

Representa um cabeçalho de um objeto [**CIM \_ DisplayController**](cim-displaycontroller.md) .

## <a name="syntax"></a>Sintaxe

``` syntax
[Experimental, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Controller"), AMENDMENT]
class CIM_VideoHead : CIM_LogicalDevice
{
  uint32 CurrentBitsPerPixel;
  uint32 CurrentHorizontalResolution;
  uint32 CurrentVerticalResolution;
  uint32 MaxRefreshRate;
  uint32 MinRefreshRate;
  uint32 CurrentRefreshRate;
  uint16 CurrentScanMode;
  string OtherCurrentScanMode;
  uint32 CurrentNumberOfRows;
  uint32 CurrentNumberOfColumns;
  uint64 CurrentNumberOfColors;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ VideoHead** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ VideoHead** tem essas propriedades.

<dl> <dt>

**CurrentBitsPerPixel**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 4,12 "), **PUnit** (" bit ")
</dt> </dl>

O número de bits usados para exibir cada pixel.

</dd> <dt>

**CurrentHorizontalResolution**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 4,11 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ VideoHeadResolution. HorizontalResolution "), **PUnit** (" pixel ")
</dt> </dl>

O número atual de pixels horizontais.

</dd> <dt>

**CurrentNumberOfColors**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ VideoHeadResolution. NumberOfColors")
</dt> </dl>

O número de cores com suporte na resolução atual.

</dd> <dt>

**CurrentNumberOfColumns**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 4,14 ")
</dt> </dl>

Se estiver no modo de caractere, o número de colunas para o controlador de vídeo; caso contrário, "0".

</dd> <dt>

**CurrentNumberOfRows**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 4,13 ")
</dt> </dl>

Se estiver no modo de caractere, o número de linhas para o controlador de vídeo; caso contrário, "0".

</dd> <dt>

**CurrentRefreshRate**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hertz"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 4,15 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ VideoHeadResolution. Taxa_de_Atualização "), **PUnit** (" Hertz ")
</dt> </dl>

A taxa de atualização atual do controlador de vídeo, em Hertz.

</dd> <dt>

**CurrentScanMode**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 4,8 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VideoHead**.**OtherCurrentScanMode**, CIM \_ VideoHeadResolution. scanmode ")
</dt> </dl>

O modo de verificação atual do controlador de vídeo.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outro** (1)


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

**Sem suporte** (2)


</dt> <dd></dd> <dt>

<span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>

**Operação não entrelaçada** (3)


</dt> <dd></dd> <dt>

<span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>

**Operação entrelaçada** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**CurrentVerticalResolution**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 4,10 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ VideoHeadResolution. VerticalResolution "), **PUnit** (" pixel ")
</dt> </dl>

O número atual de pixels verticais.

</dd> <dt>

**MaxRefreshRate**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hertz"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 4,5 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ VideoHeadResolution. MaxRefreshRate "), **PUnit** (" Hertz ")
</dt> </dl>

A taxa de atualização máxima do controlador de vídeo, em Hertz.

</dd> <dt>

**MinRefreshRate**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hertz"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 4,4 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ VideoHeadResolution. MinRefreshRate "), **PUnit** (" Hertz ")
</dt> </dl>

A taxa de atualização mínima do controlador de vídeo, em Hertz.

</dd> <dt>

**OtherCurrentScanMode**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VideoHead**.**CurrentScanMode**, CIM \_ VideoHeadResolution. OtherScanMode ")
</dt> </dl>

Uma descrição do modo de verificação atual quando a propriedade **CurrentScanMode** é "1" (outra).

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

[**\_LOGICALDEVICE CIM**](cim-logicaldevice.md)
</dt> </dl>

 

