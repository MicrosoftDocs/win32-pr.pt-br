---
description: A mesclagem alfa é usada para exibir um bitmap alfa, que é um bitmap que tem pixels transparentes ou semi-transparente.
ms.assetid: 52a044cc-a471-4951-adbe-32319b8e3129
title: Mistura alfa (GDI do Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f68cb34d189fb80d23cbb5eeec9d9006aa93a1eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967719"
---
# <a name="alpha-blending-windows-gdi"></a>Mistura alfa (GDI do Windows)

A *mesclagem alfa* é usada para exibir um bitmap alfa, que é um bitmap que tem pixels transparentes ou semi-transparente. Além de um canal de cores vermelho, verde e azul, cada pixel em um bitmap alfa tem um componente de transparência conhecido como seu *canal alfa*. Normalmente, o canal alfa contém tantos bits quanto um canal de cores. Por exemplo, um canal alfa de 8 bits pode representar 256 níveis de transparência, de 0 (o bitmap inteiro é transparente) para 255 (todo o bitmap é opaco).

Os mecanismos de mesclagem Alfa são invocados chamando [**AlphaBlend**](/windows/desktop/api/WinGdi/nf-wingdi-alphablend), que referencia a estrutura [**BLENDFUNCTION**](/windows/desktop/api/Wingdi/ns-wingdi-blendfunction) .

Os valores Alfa por pixel têm suporte apenas para BI RGB de 32-bpp \_ . Esta fórmula é definida como:


```C++
typedef struct {
  BYTE   Blue;
  BYTE   Green;
  BYTE   Red;
  BYTE   Alpha;
};
```



Isso é representado na memória, conforme mostrado na tabela a seguir.



|       |       |       |       |
|-------|-------|-------|-------|
| 31:24 | 23:16 | 15:08 | 07:00 |
| Alpha | Vermelho   | Verde | Azul  |



 

Os bitmaps também podem ser exibidos com um fator de transparência aplicado ao bitmap inteiro. Qualquer formato de bitmap pode ser exibido com um valor alfa constante global definindo **SourceConstantAlpha** na estrutura [**BLENDFUNCTION**](/windows/desktop/api/Wingdi/ns-wingdi-blendfunction) . O valor alfa da constante global tem 256 níveis de transparência, de 0 (o bitmap inteiro é completamente transparente) a 255 (o bitmap inteiro é completamente opaco). O valor alfa global constante é combinado com o valor alfa por pixel.

Para obter um exemplo, consulte [alpha blending a bitmap](alpha-blending-a-bitmap.md).

 

 



