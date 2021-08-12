---
title: Função glCopyTexSubImage1D (Gl.h)
description: A função glCopyTexSubImage1D copia uma subimagem de uma imagem de textura unidimensional do framebuffer.
ms.assetid: 718aee8a-6dce-49e1-a441-19beccd89f8d
keywords:
- Função GlCopyTexSubImage1D OpenGL
topic_type:
- apiref
api_name:
- glCopyTexSubImage1D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38c35e28a37608ebbbdbaf331e2837f83022768cf4eb4033cad2a482d477b37f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118617131"
---
# <a name="glcopytexsubimage1d-function"></a>Função glCopyTexSubImage1D

A **função glCopyTexSubImage1D** copia uma subimagem de uma imagem de textura unidimensional do framebuffer.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glCopyTexSubImage1D(
   GLenum  target,
   GLint   level,
   GLint   xoffset,
   GLint   x,
   GLint   y,
   GLsizei width
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*destino* 
</dt> <dd>

O destino para o qual os dados da imagem serão alterados. Deve ter o valor GL \_ TEXTURE \_ 1D.

</dd> <dt>

*level* 
</dt> <dd>

O número de nível de detalhes. Nível 0 é a imagem base. O *nível n* é a n *imagem* de redução de mipmap.

</dd> <dt>

*xoffset* 
</dt> <dd>

O deslocamento de texel dentro da matriz de textura.

</dd> <dt>

*x* 
</dt> <dd>

A coordenada do plano x da janela do canto inferior esquerdo da linha de pixels a ser copiada.

</dd> <dt>

*y* 
</dt> <dd>

A coordenada do plano y da janela do canto inferior esquerdo da linha de pixels a ser copiada.

</dd> <dt>

*width* 
</dt> <dd>

A largura da subimagem da imagem de textura. Especificar uma subimagem de textura com largura zero não tem nenhum efeito.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela [**função glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significado                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *target* não era um valor aceito.<br/>                                                                                                                                                                               |
| <dl> <dt>**VALOR INVÁLIDO DE GL \_ \_**</dt> </dl>     | *level* era menor que zero ou *nível* é maior que *log* 2(*max*), em que *max* é o valor retornado de GL \_ MAX TEXTURE \_ \_ SIZE.<br/>                                                                                 |
| <dl> <dt>**VALOR INVÁLIDO DE GL \_ \_**</dt> </dl>     | *xoffset* era menor que *a* borda ou (*largura xoffset*)era maior que ( borda w ), em que w é GL TEXTURE WIDTH e  +    +  border é GL TEXTURE  \_ \_  \_ \_ BORDER. Observe que *w* inclui duas vezes a largura *da* borda.<br/> |
| <dl> <dt>**VALOR INVÁLIDO DE GL \_ \_**</dt> </dl>     | *width* era menor que *border ou* *y* era menor que *a borda*, em que *border* é a largura da borda da matriz de textura.<br/>                                                                                            |
| <dl> <dt>**OPERAÇÃO \_ GL \_ INVÁLIDA**</dt> </dl> | A matriz de textura não foi definida por uma [**operação glTexImage1D**](glteximage1d.md) anterior.<br/>                                                                                                                   |
| <dl> <dt>**OPERAÇÃO \_ GL \_ INVÁLIDA**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd.**](glend.md)<br/>                                                                                        |



## <a name="remarks"></a>Comentários

A **função glCopyTexSubImage1D** substitui uma parte de uma imagem de textura unidimensional usando pixels do framebuffer atual, em vez da memória principal, como é o caso de [**glTexSubImage1D**](gltexsubimage1d.md).

Uma linha de pixels começando com as coordenadas de janela  especificadas por *x* e *y* e com a largura de comprimento substitui a parte da matriz de textura pelos *índices xoffset* por meio de *xoffset* +*(* largura – 1). O destino na matriz de textura não pode incluir nenhum texel fora da matriz de textura especificada originalmente.

A **função glCopyTexSubImage1D** processa os pixels em uma linha da mesma maneira que [**glCopyPixels,**](glcopypixels.md) exceto que, antes da conversão final dos pixels, todos os valores de componente de pixel são fixados no intervalo 0,1 e convertidos no formato interno da textura para armazenamento na matriz de \[ \] textura. A ordenação de pixels é determinada com *coordenadas x* inferiores correspondentes a coordenadas de textura inferiores. Se qualquer um dos pixels dentro de uma linha especificada do framebuffer atual estiver fora da janela associada ao contexto de renderização atual, seus valores serão indefinido.

Nenhuma alteração é feita no parâmetro *internalFormat*, *width* ou *border* da matriz de textura especificada ou para valores de texel fora da subimagem de textura especificada.

Não é possível incluir chamadas para **glCopyTexSubImage1D em** listas de exibição.

> [!Note]  
> A **função glCopyTexSubImage1D** só está disponível no OpenGL versão 1.1 ou posterior.

 

A texturing não tem efeito no modo de índice de cores. As [**funções glPixelStore**](glpixelstore-functions.md) e [**glPixelTransfer**](glpixeltransfer.md) afetam as imagens de textura exatamente da maneira como os pixels são desenhados usando [**glDrawPixels**](gldrawpixels.md).

As funções a seguir recuperam informações relacionadas **a glCopyTexSubImage1D:**

[**glGetTexImage**](glgetteximage.md)

[**glIsEnabled com**](glisenabled.md) o argumento GL \_ TEXTURE \_ 1D

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glCopyTexSubImage2D**](glcopytexsubimage2d.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glFog**](glfog.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glTexEnv**](gltexenv-functions.md)
</dt> <dt>

[**glTexGen**](gltexgen-functions.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexSubImage1D**](gltexsubimage1d.md)
</dt> <dt>

[**glTexSubImage2D**](gltexsubimage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





