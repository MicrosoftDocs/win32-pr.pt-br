---
description: Representa as características de cor da CIE (Comissão Internacional de iluminação) de um monitor de computador.
ms.assetid: 476aefae-11c0-46be-a2bb-83fbafd70421
title: Classe WmiMonitorColorCharacteristics
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorColorCharacteristics
- WmiMonitorColorCharacteristics.Active
- WmiMonitorColorCharacteristics.Blue
- WmiMonitorColorCharacteristics.DefaultWhite
- WmiMonitorColorCharacteristics.Green
- WmiMonitorColorCharacteristics.InstanceName
- WmiMonitorColorCharacteristics.Red
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 9fbb7d56e56519576d257b077311a144e923d6bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296950"
---
# <a name="wmimonitorcolorcharacteristics-class"></a>Classe WmiMonitorColorCharacteristics

A classe **WmiMonitorColorCharacteristics** representa as características de cor da CIE (Comissão Internacional sobre iluminação) de um monitor de computador. Os dados correspondem aos dados no bloco de características de cores da estrutura E-EDID (dados de identificação de exibição estendida) avançada da VESA (Video Electronics Standard Association).

## <a name="syntax"></a>Sintaxe

``` syntax
class WmiMonitorColorCharacteristics : MSMonitorClass
{
  boolean  Active;
  XYZinCIE Blue;
  XYZinCIE DefaultWhite;
  XYZinCIE Green;
  string   InstanceName;
  XYZinCIE Red;
};
```

## <a name="members"></a>Membros

A classe **WmiMonitorColorCharacteristics** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **WmiMonitorColorCharacteristics** tem essas propriedades.

<dl> <dt>

**Ativo**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica o monitor ativo.

</dd> <dt>

**Azul**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **XYZinCIE**](xyzincie.md)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Coordenadas de CIE para Blue, representadas por uma instância da classe [**XYZinCIE**](xyzincie.md) .

</dd> <dt>

**Defaultwhite**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **XYZinCIE**](xyzincie.md)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Coordenadas de CIE branco padrão.

</dd> <dt>

**Verde**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **XYZinCIE**](xyzincie.md)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Coordenadas de CIE para verde, representadas por uma instância da classe [**XYZinCIE**](xyzincie.md) .

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **chave**
</dt> </dl>

Nome da instância de monitor específica.

</dd> <dt>

**Vermelho**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **XYZinCIE**](xyzincie.md)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Coordenadas de CIE para vermelho, representadas por uma instância da classe [**XYZinCIE**](xyzincie.md) .

</dd> </dl>

## <a name="remarks"></a>Comentários

Os valores de desvio e de ponto branco são expressos como números fracionários usando um formato de codificação. Esse formato é preciso para o lugar de milhares, que tem 10 bits de comprimento. O bit mais significativo (MSB) representa 2 ^-1 e o bit menos significativo (LSB) representa dois coeficientes de ^-10, respectivamente. A precisão dos valores armazenados na estrutura E-EDID v1. x deve ser precisa de +/-0, 5 do valor real.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Namespace<br/>                | \\WMI raiz<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

 




