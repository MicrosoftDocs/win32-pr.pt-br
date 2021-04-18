---
title: UI_PKEY_FontProperties_Family
description: Identifica a \_ \_ propriedade da família PKEY fontproperties da interface do usuário \_ .
ms.assetid: 95064588-9c14-401f-a86e-7b11e86faaf9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a7183e51105a397f14154639512ca11f7c03d44
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105789400"
---
# <a name="ui_pkey_fontproperties_family"></a>IU \_ \_ da família PKEY fontproperties \_

Identifica a \_ \_ propriedade da família PKEY fontproperties da interface do usuário \_ .

```
propertyDescription
   name = UI_PKEY_FontProperties_Family
   shellPKey = UI_PKEY_FontProperties_Family
   formatID = 00000301-7363-696e-8441798acf5aebb7
   propID = 301
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>Comentários

Interface do usuário \_ PKEY \_ fontproperties \_ Family é usada por um aplicativo para consultar o valor da Galeria suspensa **família de fontes** .

O valor da família da interface do usuário \_ PKEY \_ fontproperties \_ corresponde a um nome de [famílias de fontes GDI do Windows](../gdi/font-families.md) recuperado com a [função EnumFontFamilies](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) ou a [função EnumFontFamiliesEx](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa).

O valor padrão é uma cadeia de caracteres vazia.

Se uma cadeia de caracteres vazia for fornecida para o valor para a família de fontes PKEY da interface do usuário \_ \_ \_ , a seleção de fonte será desmarcada.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Propriedades de controle de fonte](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[Controle de fonte](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 