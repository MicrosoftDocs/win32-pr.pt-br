---
title: Instrução FONT
description: Define a fonte com a qual o sistema desenhará texto na caixa de diálogo. A fonte deve ter sido carregada anteriormente; por exemplo, chamando a função LoadResource.
ms.assetid: d7b0f382-bc45-4405-a30e-0b571fdfd1db
keywords:
- Menus de instrução FONT e outros recursos
topic_type:
- apiref
api_name:
- FONT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad289923503866ba2bcd9338bb59a556d0e37cd0a839d4eede0f95a0bec5fd76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972065"
---
# <a name="font-statement"></a>Instrução FONT

Define a fonte com a qual o sistema desenhará texto na caixa de diálogo. A fonte deve ter sido carregada anteriormente; por exemplo, chamando a [**função LoadResource.**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource)

``` syntax
FONT pointsize, "typeface", weight, italic, charset
```

<dl> <dt>

<span id="pointsize"></span><span id="POINTSIZE"></span>*Pointsize*
</dt> <dd>

O tamanho da fonte, em pontos.

</dd> <dt>

<span id="typeface"></span><span id="TYPEFACE"></span>*Tipo*
</dt> <dd>

O nome da face de tipo. Esse parâmetro deve estar entre aspas (").

</dd> <dt>

<span id="weight"></span><span id="WEIGHT"></span>*Peso*
</dt> <dd>

O peso da fonte no intervalo de 0 a 1000. Por exemplo, 400 é normal e 700 está em negrito. Se esse valor for 0, o peso padrão será usado. Para ver uma lista de valores predefinidos, consulte os **valores de FW \_ \*** definidos em WinGDI.h.

</dd> <dt>

<span id="italic"></span><span id="ITALIC"></span>*Itálico*
</dt> <dd>

Indica uma fonte itálico se definida como TRUE.

</dd> <dt>

<span id="charset"></span><span id="CHARSET"></span>*Charset*
</dt> <dd>

O conjunto de caracteres. Para ver uma lista de valores, consulte **o membro lfCharSet** da [**estrutura LOGFONT.**](/windows/win32/api/wingdi/ns-wingdi-logfonta)

</dd> </dl>

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra o uso da **instrução FONT:**

``` syntax
FONT 12, "MS Shell Dlg"
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Loadresource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource)
</dt> </dl>

 

 