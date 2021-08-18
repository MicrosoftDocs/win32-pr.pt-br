---
description: Define uma matriz de 4 byte que contém quatro valores ASCII de 8 bits de espaço, A-Z ou a-z para identificar marcas de recurso de fonte, idioma e script OpenType.
ms.assetid: 188ad9a1-e0eb-411f-b6df-8c394d122d6f
title: OPENTYPE_TAG (Usp10.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7c784fa7f6243e7e5444dcbc64c690ce7184d6ace469759c19be9de87854732
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040776"
---
# <a name="opentype_tag"></a>MARCA \_ OPENTYPE

Define uma matriz de 4 byte que contém quatro valores ASCII de 8 bits de espaço, A-Z ou a-z para identificar marcas de recurso de fonte, idioma e script OpenType.


```C++
typedef ULONG OPENTYPE_TAG;
```



## <a name="remarks"></a>Comentários

Os exemplos a seguir definem representações de marcas de recurso OpenType.

-   A marca de recurso para o recurso de ligadura é "liga".
-   As marcas de idioma para Romeno, Urdu e Árabe são "ROM", "URD" e "FAR", respectivamente. Observe que cada uma dessas marcas termina com um espaço.
-   As marcas de script para scripts latinos e em árabe são "latn" e "árabe", respectivamente.

Para obter mais informações sobre marcas de recurso OpenType e a especificação OpenType, consulte <https://www.microsoft.com/typography/otspec/featuretags.htm> .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                               |
| Redistribuível<br/>          | Usp10.dll versão 1.600 ou superior noWindows XPand posteriormente<br/>                |
| Cabeçalho<br/>                   | <dl> <dt>Usp10.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Uniscribe](uniscribe.md)
</dt> <dt>

[Estruturas Uniscribe](uniscribe-structures.md)
</dt> <dt>

[**ScriptGetFontAlternateGlyphs**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontalternateglyphs)
</dt> <dt>

[**ScriptGetFontFeatureTags**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontfeaturetags)
</dt> <dt>

[**ScriptGetFontLanguageTags**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontlanguagetags)
</dt> <dt>

[**ScriptGetFontScriptTags**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontscripttags)
</dt> <dt>

[**ScriptItemizeOpenType**](/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype)
</dt> <dt>

[**ScriptPlaceOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptplaceopentype)
</dt> <dt>

[**ScriptPositionSingleGlyph**](/windows/desktop/api/Usp10/nf-usp10-scriptpositionsingleglyph)
</dt> <dt>

[**ScriptShapeOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptshapeopentype)
</dt> <dt>

[**ScriptSubstituteSingleGlyph**](/windows/desktop/api/Usp10/nf-usp10-scriptsubstitutesingleglyph)
</dt> </dl>

 

 




