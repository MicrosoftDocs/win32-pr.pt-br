---
title: função gluScaleImage (Glu. h)
description: A função gluScaleImage dimensiona uma imagem para um tamanho arbitrário.
ms.assetid: f47191e8-b22d-4f6a-949a-9c7782d6d338
keywords:
- função gluScaleImage OpenGL
topic_type:
- apiref
api_name:
- gluScaleImage
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7da95f1545996a83adeb27deaceb7fab6290005e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369205"
---
# <a name="gluscaleimage-function"></a>função gluScaleImage

A função **gluScaleImage** dimensiona uma imagem para um tamanho arbitrário.

## <a name="syntax"></a>Sintaxe


```C++
int WINAPI gluScaleImage(
         GLenum format,
         GLint  widthin,
         GLint  heightin,
         GLenum typein,
   const void   *datain,
         GLint  widthout,
         GLint  heightout,
         GLenum typeout,
         void   *dataout
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*format* 
</dt> <dd>

O formato dos dados de pixel. Os seguintes valores simbólicos são válidos: \_ \_ índice de cores GL \_ , \_ índice de estêncil GL, \_ componente de profundidade do GL \_ , GL \_ vermelho, GL \_ verde, GL \_ azul, GL \_ alfa, GL \_ RGB, GL \_ RGBA, GL \_ BGR \_ ext, GL \_ BGRA \_ ext, GL \_ luminescência e a luminância de GL \_ \_ alfa.

</dd> <dt>

*largura* 
</dt> <dd>

A largura da imagem de origem dimensionada.

</dd> <dt>

*altura* 
</dt> <dd>

A altura da imagem de origem dimensionada.

</dd> <dt>

*tipo* 
</dt> <dd>

O tipo de dados para *dados*. Deve ser um dos seguintes: GL \_ não assinado \_ byte, GL \_ byte, \_ bitmap GL, GL \_ não assinado \_ curto, GL \_ curto, GL \_ não assinado \_ int, GL \_ int ou GL \_ float.

</dd> <dt>

*dados de* 
</dt> <dd>

Um ponteiro para a imagem de origem.

</dd> <dt>

*largura* 
</dt> <dd>

A largura da imagem de destino.

</dd> <dt>

*altura de* 
</dt> <dd>

A altura da imagem de destino.

</dd> <dt>

*tipoout* 
</dt> <dd>

O tipo de dados para *dataout*. Deve ser um dos seguintes: GL \_ não assinado \_ byte, GL \_ byte, \_ bitmap GL, GL \_ não assinado \_ curto, GL \_ curto, GL \_ não assinado \_ int, GL \_ int ou GL \_ float.

</dd> <dt>

*Data de* 
</dt> <dd>

Um ponteiro para a imagem de destino.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função obtiver êxito, o valor retornado será zero.

Se a função falhar, o valor de retorno será um código de erro GLU (consulte [**gluErrorString**](gluerrorstring.md)).

## <a name="remarks"></a>Comentários

A função **gluScaleImage** dimensiona uma imagem de pixel usando os modos de armazenamento de pixel apropriados para desempacotar dados da imagem de origem e os dados de pacote na imagem de destino.

Ao reduzir uma imagem, o **gluScaleImage** usa um filtro de caixa para exemplificar a imagem de origem e criar pixels para a imagem de destino. Ao ampliar uma imagem, os pixels da imagem de origem são interpolados linearmente para criar a imagem de destino.

Para obter uma descrição dos valores aceitáveis para o *formato*, *digite* e parâmetros de *tipoout* , consulte [**glReadPixels**](glreadpixels.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>GLU. h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> <dt>

[**gluBuild1DMipmaps**](glubuild1dmipmaps.md)
</dt> <dt>

[**gluBuild2DMipmaps**](glubuild2dmipmaps.md)
</dt> <dt>

[**gluErrorString**](gluerrorstring.md)
</dt> </dl>

 

 





