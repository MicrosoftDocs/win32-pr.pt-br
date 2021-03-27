---
Description: O valor COLORREF é usado para especificar uma cor RGB.
ms.assetid: b87d3de2-7a13-44ef-8253-c6851a75fa54
title: COLORREF (windef. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 6836cfcc1b18d0b20d5e347fb83206551b27de06
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "104989460"
---
# <a name="colorref"></a>COLORREF

O valor COLORREF é usado para especificar uma cor [RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb) .


```C++
typedef DWORD COLORREF;
typedef DWORD* LPCOLORREF;
```



## <a name="remarks"></a>Comentários

Ao especificar uma cor [RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb) explícita, o valor de **COLORREF** tem o seguinte formato hexadecimal:

`0x00bbggrr`

O byte de ordem inferior contém um valor para a intensidade relativa de vermelho; o segundo byte contém um valor para verde; e o terceiro byte contém um valor para Blue. O byte de ordem superior deve ser zero. O valor máximo de um único byte é 0xFF.

Para criar um valor de cor **COLORREF** , use a macro [RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb) . Para extrair os valores individuais dos componentes vermelho, verde e azul de um valor de cor, use as macros [**GetRValue**](/windows/desktop/api/Wingdi/nf-wingdi-getrvalue), [GetGValue](/windows/desktop/api/Wingdi/nf-wingdi-getgvalue)e [GetBValue](/windows/desktop/api/Wingdi/nf-wingdi-getbvalue) , respectivamente.

## <a name="example"></a>Exemplo

```cpp
// Color constants.
const COLORREF rgbRed   =  0x000000FF;
const COLORREF rgbGreen =  0x0000FF00;
const COLORREF rgbBlue  =  0x00FF0000;
const COLORREF rgbBlack =  0x00000000;
const COLORREF rgbWhite =  0x00FFFFFF;
```

Exemplo de [exemplos clássicos do Windows](https://github.com/microsoft/Windows-classic-samples) no github.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                    |
| Cabeçalho<br/>                   | <dl> <dt>Windef. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral das cores](colors.md)
</dt> <dt>

[Estruturas de cores](color-structures.md)
</dt> <dt>

[GetBValue](/windows/desktop/api/Wingdi/nf-wingdi-getbvalue)
</dt> <dt>

[GetGValue](/windows/desktop/api/Wingdi/nf-wingdi-getgvalue)
</dt> <dt>

[**GetRValue**](/windows/desktop/api/Wingdi/nf-wingdi-getrvalue)
</dt> <dt>

[RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb)
</dt> </dl>

 

 




