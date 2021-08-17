---
description: Uma estrutura que descreve um único valor de cor.
ms.assetid: 710f3ef1-bbc3-416d-9faf-aa4a716007c2
title: XPS_COLOR (Xpsobjectmodel.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f771bcbb516352b2ef689060c11003808d434be8059d16af78fe8db646c97000
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971145"
---
# <a name="xps_color"></a>XPS \_ COLOR

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

O formato da estrutura depende do valor de *colorType*.

<dl>

[**TIPO DE COR XPS \_ \_ \_ SRGB**](/previous-versions/windows/desktop/dd372944(v=vs.85))  
[**TIPO DE \_ COR \_ \_ XPS SCRGB**](/previous-versions/windows/desktop/dd372943(v=vs.85))  
[**CONTEXTO DE TIPO \_ \_ DE COR XPS \_**](/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_color)  
</dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7, Windows Vista com SP2 e Atualização de Plataforma para Windows aplicativos \[ UWP da área de trabalho do Vista \|\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2, Windows Server 2008 com SP2 e Atualização de Plataforma para aplicativos \[ UWP do Windows Server 2008 \|\]<br/> |
| Cabeçalho<br/>                   | <dl> <dt>Xpsobjectmodel.h</dt> </dl>                                              |
| Idl<br/>                      | <dl> <dt>XpsObjectModel.idl</dt> </dl>                                            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Especificação de Papel XML](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

