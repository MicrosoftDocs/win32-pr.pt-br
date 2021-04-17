---
description: Uma estrutura que descreve um único valor de cor.
ms.assetid: 710f3ef1-bbc3-416d-9faf-aa4a716007c2
title: XPS_COLOR (Xpsobjectmodel. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34c148c2a5452154bfe33b0c74d695fe78f0cdad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785308"
---
# <a name="xps_color"></a>cor do XPS \_

Uma estrutura que descreve um único valor de cor.

``` syntax
typedef union switch (XPS_COLOR_TYPE colorType) value
{
    case XPS_COLOR_TYPE_SRGB:
        struct {
            byte alpha, red, green, blue;
        } sRGB;
    case XPS_COLOR_TYPE_SCRGB:
        struct {
            FLOAT alpha, red, green, blue;
        } scRGB;
    case XPS_COLOR_TYPE_CONTEXT:
        struct {
            byte channelCount;
            FLOAT channels[9];
        } context;
} XPS_COLOR;
```

## <a name="remarks"></a>Comentários

O formato da estrutura depende do valor de *ColorType*.

<dl>

[**\_tipo de cor XPS \_ \_ sRGB**](/previous-versions/windows/desktop/dd372944(v=vs.85))  
[**\_tipo de cor XPS \_ \_ SCRGB**](/previous-versions/windows/desktop/dd372943(v=vs.85))  
[**\_contexto de \_ tipo de cor XPS \_**](/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_color)  
</dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7, Windows Vista com SP2 e atualização de plataforma para aplicativos UWP do Windows Vista \[ Desktop apps \|\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2, Windows Server 2008 com SP2 e atualização de plataforma para aplicativos de aplicativos de desktop do Windows Server 2008 \[ \| UWP\]<br/> |
| parâmetro<br/>                   | <dl> <dt>Xpsobjectmodel. h</dt> </dl>                                              |
| INSERI<br/>                      | <dl> <dt>XpsObjectModel. idl</dt> </dl>                                            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Especificação de Papel XML](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

