---
description: Contém as coordenadas da exibição no espaço de cores da CIE (Comissão Internacional de iluminação) XYZ.
ms.assetid: e44e8a5f-005d-4d58-84e3-135d4e396086
title: Classe XYZinCIE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- XYZinCIE
- XYZinCIE.X
- XYZinCIE.Y
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: ba7f781a83f3e6ba5aa4683003386a0478d65088
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105798019"
---
# <a name="xyzincie-class"></a>Classe XYZinCIE

A classe WMI **XYZinCIE** contém as coordenadas da exibição no espaço de cores da CIE (Comissão Internacional em iluminação) XYZ.

## <a name="syntax"></a>Sintaxe

``` syntax
class XYZinCIE : WmiMonitorColorCharacteristics
{
  uint16 X;
  uint16 Y;
};
```

## <a name="members"></a>Membros

A classe **XYZinCIE** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **XYZinCIE** tem essas propriedades.

<dl> <dt>

**X**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Coordenada X.

</dd> <dt>

**S**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Coordenada Y.

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe [**WmiMonitorColorCharacteristics**](wmimonitorcolorcharacteristics.md) contém instâncias incorporadas da classe **XYZinCIE** para descrever as características de cor de um monitor.

Para calcular a coordenada z, com base nos valores x e y, use a relação \| \| (x, y, z) \| \| = 1.

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

 

 




