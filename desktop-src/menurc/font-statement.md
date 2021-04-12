---
title: Instrução FONT
description: Define a fonte com a qual o sistema irá desenhar texto na caixa de diálogo. A fonte deve ter sido carregada anteriormente; por exemplo, chamando a função LoadResource.
ms.assetid: d7b0f382-bc45-4405-a30e-0b571fdfd1db
keywords:
- Menus de instrução de fonte e outros recursos
topic_type:
- apiref
api_name:
- FONT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4b31b280a5a973301e8410f1f74340138af07ba
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104454048"
---
# <a name="font-statement"></a>Instrução FONT

Define a fonte com a qual o sistema irá desenhar texto na caixa de diálogo. A fonte deve ter sido carregada anteriormente; por exemplo, chamando a função [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) .

``` syntax
FONT pointsize, "typeface", weight, italic, charset
```

<dl> <dt>

<span id="pointsize"></span><span id="POINTSIZE"></span>*pontos*
</dt> <dd>

O tamanho da fonte, em pontos.

</dd> <dt>

<span id="typeface"></span><span id="TYPEFACE"></span>*face*
</dt> <dd>

O nome do tipo de fonte. Esse parâmetro deve ser colocado entre aspas (").

</dd> <dt>

<span id="weight"></span><span id="WEIGHT"></span>*largura*
</dt> <dd>

O peso da fonte no intervalo de 0 a 1000. Por exemplo, 400 é normal e 700 é negrito. Se esse valor for 0, o peso padrão será usado. Para obter uma lista de valores predefinidos, consulte os valores de **FW \_ \*** definidos em WinGDI. h.

</dd> <dt>

<span id="italic"></span><span id="ITALIC"></span>*colocadas*
</dt> <dd>

Indica uma fonte em itálico se definido como TRUE.

</dd> <dt>

<span id="charset"></span><span id="CHARSET"></span>*charset*
</dt> <dd>

O conjunto de caracteres. Para obter uma lista de valores, consulte o membro **lfCharSet** da estrutura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .

</dd> </dl>

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra o uso da instrução **Font** :

``` syntax
FONT 12, "MS Shell Dlg"
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource)
</dt> </dl>

 

 