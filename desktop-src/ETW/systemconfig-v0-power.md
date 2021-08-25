---
description: Classe SystemConfig_V0_Power-essa classe é a classe de tipo de evento para eventos de configuração de energia. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: b3391435-dac0-4c48-b788-eb4d4a7aa635
title: Classe SystemConfig_V0_Power
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_Power
- SystemConfig_V0_Power.s1
- SystemConfig_V0_Power.s2
- SystemConfig_V0_Power.s3
- SystemConfig_V0_Power.s4
- SystemConfig_V0_Power.s5
- SystemConfig_V0_Power.Pad1
- SystemConfig_V0_Power.Pad2
- SystemConfig_V0_Power.Pad3
api_type:
- NA
api_location: ''
ms.openlocfilehash: 588622fb010cf9ca43f7253adc269e86b1755e5e459cbd6320a28d1d5416706a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914336"
---
# <a name="systemconfig_v0_power-class"></a>\_Classe de \_ energia SystemConfig V0

Essa classe é a classe de tipo de evento para eventos de configuração de energia.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[EventType(16), EventTypeName("Power")]
class SystemConfig_V0_Power : SystemConfig_V0
{
  boolean s1;
  boolean s2;
  boolean s3;
  boolean s4;
  boolean s5;
  uint8   Pad1;
  uint8   Pad2;
  uint8   Pad3;
};
```

## <a name="members"></a>Membros

A classe de **\_ \_ energia SystemConfig V0** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe de **\_ \_ energia SystemConfig V0** tem essas propriedades.

<dl> <dt>

Pad1
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (6)
</dt> </dl>

Reservado.

</dd> <dt>

Pad2
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (7)
</dt> </dl>

Reservado.

</dd> <dt>

Pad3
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (8)
</dt> </dl>

Reservado.

</dd> <dt>

s1
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (1)
</dt> </dl>

Verdadeiro indica que o sistema dá suporte ao estado de suspensão S1.

</dd> <dt>

S2
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (2)
</dt> </dl>

Verdadeiro indica que o sistema dá suporte ao estado de suspensão S2.

</dd> <dt>

s3
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (3)
</dt> </dl>

Verdadeiro indica que o sistema dá suporte ao estado de suspensão S3.

</dd> <dt>

S4
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (4)
</dt> </dl>

Verdadeiro indica que o sistema dá suporte ao estado de suspensão S4.

</dd> <dt>

S5
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (5)
</dt> </dl>

Verdadeiro indica que o sistema dá suporte ao estado de suspensão s5.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                            |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SystemConfig \_ V0**](systemconfig-v0.md)
</dt> </dl>

 

 




