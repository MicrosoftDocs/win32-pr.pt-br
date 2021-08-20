---
title: função gluBuild1DMipmaps (Glu. h)
description: A função gluBuild1DMipmaps cria mipmaps de 1 a D.
ms.assetid: 52ed924f-7a72-4458-b1b8-8e5d3021f60a
keywords:
- função gluBuild1DMipmaps OpenGL
topic_type:
- apiref
api_name:
- gluBuild1DMipmaps
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c2b76a37fa7088835ad0238065b0647ff0beb973c1c3ffa1b892f6e0958d97a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119489686"
---
# <a name="glubuild1dmipmaps-function"></a>função gluBuild1DMipmaps

A função **gluBuild1DMipmaps** cria mipmaps de 1 a D.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI gluBuild1DMipmaps(
         GLenum target,
         GLint  components,
         GLint  width,
         GLenum format,
         GLenum type,
   const void   *data
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*destino* 
</dt> <dd>

A textura de destino. Deve ser GL \_ Texture \_ 1D.

</dd> <dt>

*QC* 
</dt> <dd>

O número de componentes de cor na textura. Deve ser 1, 2, 3 ou 4.

</dd> <dt>

*width* 
</dt> <dd>

A largura da imagem de textura.

</dd> <dt>

*format* 
</dt> <dd>

O formato dos dados de pixel. Os seguintes valores são válidos: o \_ \_ índice de cores GL, GL \_ vermelho, GL \_ verde, GL \_ Blue, GL \_ alfa, GL \_ RGB, GL \_ RGBA, GL \_ BGR \_ ext, GL \_ BGRA \_ ext, GL \_ luminescência ou o GL \_ luminância \_ alfa.

</dd> <dt>

*tipo* 
</dt> <dd>

O tipo de dados para *dados*. Os seguintes valores são válidos: GL \_ não assinado \_ , byte, GL byte, renome do GL \_ \_ , GL \_ não assinado \_ curto, GL \_ curto, GL \_ não assinado \_ int, GL \_ int ou GL \_ float.

</dd> <dt>

*data* 
</dt> <dd>

Um ponteiro para os dados da imagem na memória.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

A função **gluBuild1DMipmaps** Obtém a imagem de entrada e gera todas as imagens do mipmap (usando [**gluScaleImage**](gluscaleimage.md)) para que a imagem de entrada possa ser usada como uma imagem de textura mipmapped. Em seguida, a função [**glTexImage1D**](glteximage1d.md) é chamada para carregar cada uma das imagens. Se a largura da imagem de entrada não for uma potência de dois, a imagem será dimensionada para a potência mais próxima de dois antes de a mipmaps ser gerada.

Um valor de retorno igual A zero indica êxito. Caso contrário, um código de erro GLU será retornado (consulte [**gluErrorString**](gluerrorstring.md)).

Para obter uma descrição dos valores aceitáveis para o parâmetro *Format* , consulte **glTexImage1D**. Para obter uma descrição dos valores aceitáveis para o parâmetro de *tipo* , consulte [**glDrawPixels**](gldrawpixels.md).

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

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**gluBuild2DMipmaps**](glubuild2dmipmaps.md)
</dt> <dt>

[**gluScaleImage**](gluscaleimage.md)
</dt> </dl>

 

 





