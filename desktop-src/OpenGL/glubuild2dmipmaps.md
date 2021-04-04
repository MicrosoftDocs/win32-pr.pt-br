---
title: função gluBuild2DMipmaps (Glu. h)
description: A função gluBuild2DMipmaps cria mipmaps 2-D.
ms.assetid: ea19a9b0-baf7-436f-afd5-609bc364b3ba
keywords:
- função gluBuild2DMipmaps OpenGL
topic_type:
- apiref
api_name:
- gluBuild2DMipmaps
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92402792e41701711e99f469ead67410d6a8c1b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918150"
---
# <a name="glubuild2dmipmaps-function"></a>função gluBuild2DMipmaps

A função **gluBuild2DMipmaps** cria mipmaps 2-D.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI gluBuild2DMipmaps(
         GLenum target,
         GLint  components,
         GLint  width,
         GLInt  height,
         GLenum format,
         GLenum type,
   const void   *data
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*destino* 
</dt> <dd>

A textura de destino. Deve ser GL de \_ textura \_ 2D.

</dd> <dt>

*QC* 
</dt> <dd>

O número de componentes de cor na textura. Deve ser 1, 2, 3 ou 4.

</dd> <dt>

*width* 
</dt> <dd>

A largura da imagem de textura.

</dd> <dt>

*altura* 
</dt> <dd>

A altura da imagem de textura.

</dd> <dt>

*format* 
</dt> <dd>

O formato dos dados de pixel. Deve ser um dos seguintes: \_ \_ índice de cores GL, GL \_ vermelho, GL \_ verde, GL \_ Blue, GL \_ alfa, GL \_ RGB, GL \_ RGBA, GL \_ BGR \_ ext, GL \_ BGRA \_ ext, GL \_ luminescência ou GL de \_ luminância \_ alfa.

</dd> <dt>

*tipo* 
</dt> <dd>

O tipo de dados para *dados*. Deve ser um dos seguintes: GL \_ não assinado \_ byte, GL \_ byte, \_ bitmap GL, GL \_ não assinado \_ curto, GL \_ curto, GL \_ não assinado \_ int, GL \_ int ou GL \_ float.

</dd> <dt>

*data* 
</dt> <dd>

Um ponteiro para os dados da imagem na memória.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

A função **gluBuild2DMipmaps** Obtém a imagem de entrada e gera todas as imagens do mipmap (usando [**gluScaleImage**](gluscaleimage.md)) para que a imagem de entrada possa ser usada como uma imagem de textura mipmapped. Para carregar cada uma das imagens, chame [**glTexImage2D**](glteximage2d.md). Se as dimensões da imagem de entrada não forem potências de dois, a imagem será dimensionada de forma que a largura e a altura sejam potências de dois antes de os mipmaps serem gerados.

Um valor de retorno igual A zero indica êxito. Caso contrário, um código de erro GLU será retornado (consulte [**gluErrorString**](gluerrorstring.md)).

Para obter uma descrição dos valores aceitáveis para o parâmetro *Format* , consulte **glTexImage2D**. Para obter uma descrição dos valores aceitáveis para o *tipo*, consulte [**glDrawPixels**](gldrawpixels.md).

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

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**gluBuild1DMipmaps**](glubuild1dmipmaps.md)
</dt> <dt>

[**gluScaleImage**](gluscaleimage.md)
</dt> </dl>

 

 





