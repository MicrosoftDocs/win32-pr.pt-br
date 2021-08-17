---
description: Você pode armazenar e recuperar metadados de imagem com a ajuda de um objeto PropertyItem. O membro de dados de tipo de um objeto PropertyItem especifica o tipo de dados dos valores armazenados no membro de dados de valor do mesmo objeto PropertyItem.
ms.assetid: d05cdf42-4b30-45ce-85a1-025d4f4e9d13
title: Constantes de tipo de marca de propriedade image (Gdiplusimaging.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb565972b2dc8b8962e367c7d2f3c09b4f857382156538a83f7d6ee338c66ab6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977596"
---
# <a name="image-property-tag-type-constants"></a>Constantes de tipo de marca de propriedade image

Você pode armazenar e recuperar metadados de imagem com a ajuda de um [**objeto PropertyItem.**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) O **membro** de dados de tipo de um objeto **PropertyItem** especifica o tipo de dados dos valores armazenados no membro de dados de valor do mesmo **objeto PropertyItem.**

As constantes a seguir, definidas em Gdiplusimaging.h, podem ser atribuídas ao membro de dados de tipo de um [**objeto PropertyItem.**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) 



| Constante                                                                                                                                                                                                                                 | Descrição                                                                                                                                                                                                                                                                                                                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PixelFormat4bppIndexed"></span><span id="pixelformat4bppindexed"></span><span id="PIXELFORMAT4BPPINDEXED"></span><dl> <dt>**PixelFormat4bppIndexed**</dt> </dl>         | Especifica que o formato é 4 bits por pixel, indexado.<br/>                                                                                                                                                                                                                                                                                                                       |
| <span id="PropertyTagTypeASCII"></span><span id="propertytagtypeascii"></span><span id="PROPERTYTAGTYPEASCII"></span><dl> <dt>**Propertytagtypeascii**</dt> </dl>                 | Especifica que o membro de **dados** de valor é uma cadeia de caracteres ASCII terminada em nulo. Se você  definir o membro de dados de tipo de um objeto [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) como PropertyTagTypeASCII, deverá definir o membro de dados de comprimento para o comprimento da cadeia de caracteres, incluindo o terminador NULL.  Por exemplo, a cadeia `HELLO` de caracteres teria um comprimento de 6.<br/> |
| <span id="PropertyTagTypeByte"></span><span id="propertytagtypebyte"></span><span id="PROPERTYTAGTYPEBYTE"></span><dl> <dt>**Propertytagtypebyte**</dt> </dl>                     | Especifica que o membro **de dados** de valor é uma matriz de bytes.<br/>                                                                                                                                                                                                                                                                                                                |
| <span id="PropertyTagTypeLong"></span><span id="propertytagtypelong"></span><span id="PROPERTYTAGTYPELONG"></span><dl> <dt>**Propertytagtypelong**</dt> </dl>                     | Especifica que o membro **de dados** de valor é uma matriz de inteiros longos sem sinal (32 bits).<br/>                                                                                                                                                                                                                                                                                      |
| <span id="PropertyTagTypeRational"></span><span id="propertytagtyperational"></span><span id="PROPERTYTAGTYPERATIONAL"></span><dl> <dt>**Propertytagtyperational**</dt> </dl>     | Especifica que o membro **de dados** de valor é uma matriz de pares de inteiros longos sem sinal. Cada par representa uma fração; o primeiro inteiro é o numerador e o segundo inteiro é o denominador.<br/>                                                                                                                                                                       |
| <span id="PropertyTagTypeShort"></span><span id="propertytagtypeshort"></span><span id="PROPERTYTAGTYPESHORT"></span><dl> <dt>**Propertytagtypeshort**</dt> </dl>                 | Especifica que o membro **de dados** de valor é uma matriz de inteiros curtos (16 bits) sem sinal.<br/>                                                                                                                                                                                                                                                                                     |
| <span id="PropertyTagTypeSLONG"></span><span id="propertytagtypeslong"></span><span id="PROPERTYTAGTYPESLONG"></span><dl> <dt>**PropertyTagTypeSLONG**</dt> </dl>                 | Especifica que o membro **de dados** de valor é uma matriz de inteiros longos (32 bits) assinados.<br/>                                                                                                                                                                                                                                                                                        |
| <span id="PropertyTagTypeSRational"></span><span id="propertytagtypesrational"></span><span id="PROPERTYTAGTYPESRATIONAL"></span><dl> <dt>**PropertyTagTypeSRational**</dt> </dl> | Especifica que o membro **de dados** de valor é uma matriz de pares de inteiros longos com sinal. Cada par representa uma fração; o primeiro inteiro é o numerador e o segundo inteiro é o denominador.<br/>                                                                                                                                                                         |
| <span id="PropertyTagTypeUndefined"></span><span id="propertytagtypeundefined"></span><span id="PROPERTYTAGTYPEUNDEFINED"></span><dl> <dt>**Propertytagtypeundefined**</dt> </dl> | Especifica que o membro **de dados** de valor é uma matriz de bytes que pode conter valores de qualquer tipo de dados. <br/>                                                                                                                                                                                                                                                                         |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Gdiplusimaging.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes de marca de propriedade de imagem](-gdiplus-constant-image-property-tag-constants.md)
</dt> <dt>

[Especificações de formato de arquivo de imagem](-gdiplus-constant-image-file-format-specifications.md)
</dt> <dt>

[Lendo e escrevendo metadados](-gdiplus-reading-and-writing-metadata-use.md)
</dt> </dl>

 

 
