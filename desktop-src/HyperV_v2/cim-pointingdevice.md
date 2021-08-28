---
description: Representa um dispositivo usado para apontar para regiões de uma exibição.
ms.assetid: ffc675c3-29bd-4c54-8e54-8b6212daf66d
title: Classe CIM_PointingDevice (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PointingDevice
- CIM_PointingDevice.PointingType
- CIM_PointingDevice.NumberOfButtons
- CIM_PointingDevice.Handedness
- CIM_PointingDevice.Resolution
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9eeb3d039f94b2011c2a5a0187a520cb7800623e52e8a983c1dd20d6d05349e2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694666"
---
# <a name="cim_pointingdevice-class-hyper-v-management"></a>Classe CIM_PointingDevice (gerenciamento do Hyper-V)

Representa um dispositivo usado para apontar para regiões de uma exibição.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Device::UserDevices"), AMENDMENT]
class CIM_PointingDevice : CIM_UserDevice
{
  uint16 PointingType;
  uint8  NumberOfButtons;
  uint16 Handedness;
  uint32 Resolution;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ PointingDevice** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ PointingDevice** tem essas propriedades.

<dl> <dt>

**Direção**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se o dispositivo apontador está configurado para a operação de mão direita ou esquerda.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**Não aplicável** (1)


</dt> <dd></dd> <dt>

<span id="Right_Handed_Operation"></span><span id="right_handed_operation"></span><span id="RIGHT_HANDED_OPERATION"></span>

**Operação da mão direita** (2)


</dt> <dd></dd> <dt>

<span id="Left_Handed_Operation"></span><span id="left_handed_operation"></span><span id="LEFT_HANDED_OPERATION"></span>

**Operação da mão esquerda** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**NumberOfButtons**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo apontador DMTF \| 3,4 ")
</dt> </dl>

O número de botões no dispositivo. Se o dispositivo apontador não tiver botões, esse valor deverá ser definido como "0".

</dd> <dt>

**Ponto de apontar**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo apontador DMTF \| 3,1 ")
</dt> </dl>

O tipo do dispositivo apontador.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (2)


</dt> <dd></dd> <dt>

<span id="Mouse"></span><span id="mouse"></span><span id="MOUSE"></span>

**Mouse** (3)


</dt> <dd></dd> <dt>

<span id="Track_Ball"></span><span id="track_ball"></span><span id="TRACK_BALL"></span>

**Rastrear bola** (4)


</dt> <dd></dd> <dt>

<span id="Track_Point"></span><span id="track_point"></span><span id="TRACK_POINT"></span>

**Ponto de controle** (5)


</dt> <dd></dd> <dt>

<span id="Glide_Point"></span><span id="glide_point"></span><span id="GLIDE_POINT"></span>

**Ponto de deslizamento** (6)


</dt> <dd></dd> <dt>

<span id="Touch_Pad"></span><span id="touch_pad"></span><span id="TOUCH_PAD"></span>

**Touch pad** (7)


</dt> <dd></dd> <dt>

<span id="Touch_Screen"></span><span id="touch_screen"></span><span id="TOUCH_SCREEN"></span>

**Tela sensível ao toque** (8)


</dt> <dd></dd> <dt>

<span id="Mouse_-_Optical_Sensor"></span><span id="mouse_-_optical_sensor"></span><span id="MOUSE_-_OPTICAL_SENSOR"></span>

**Sensor de mouse-óptico** (9)


</dt> <dd></dd> </dl>

</dd> <dt>

**Resolução**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("contagens por polegada"), **PUnit** ("contagem/polegada")
</dt> </dl>

A resolução de rastreamento do dispositivo apontador, em contagens por polegada.

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

[**Userdevice do CIM \_**](cim-userdevice.md)
</dt> </dl>

 

