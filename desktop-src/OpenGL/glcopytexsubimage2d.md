---
title: função glCopyTexSubImage2D (GL. h)
description: A função glCopyTexSubImage2D copia uma subimagem de uma imagem de textura bidimensional do framebuffer.
ms.assetid: cbb644d4-6a23-4d66-8599-5f8b48e9b91f
keywords:
- função glCopyTexSubImage2D OpenGL
topic_type:
- apiref
api_name:
- glCopyTexSubImage2D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c966d031bb154b59cc54ae2e5d254347aa88d2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369696"
---
# <a name="glcopytexsubimage2d-function"></a>função glCopyTexSubImage2D

A função **glCopyTexSubImage2D** copia uma subimagem de uma imagem de textura bidimensional do framebuffer.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glCopyTexSubImage2D(
   GLenum  target,
   GLint   level,
   GLint   xoffset,
   GLint   yoffset,
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*destino* 
</dt> <dd>

O destino para o qual os dados da imagem serão alterados. Deve ter o valor GL de \_ textura \_ 2D.

</dd> <dt>

*level* 
</dt> <dd>

O número de nível de detalhe. Nível 0 é a imagem base. O nível *n* é a imagem de redução *n* º mipmap.

</dd> <dt>

*xoffset* 
</dt> <dd>

O deslocamento de Texel na direção *x* dentro da matriz de textura.

</dd> <dt>

*yoffset* 
</dt> <dd>

O deslocamento de Texel na direção *y* dentro da matriz de textura.

</dd> <dt>

*x* 
</dt> <dd>

As coordenadas do plano x da janela do canto inferior esquerdo da linha de pixels a serem copiadas.

</dd> <dt>

*y* 
</dt> <dd>

As coordenadas do plano y da janela do canto inferior esquerdo da linha de pixels a serem copiadas.

</dd> <dt>

*width* 
</dt> <dd>

A largura da subimagem da imagem de textura. A especificação de uma subimagem de textura com largura zero não tem efeito.

</dd> <dt>

*altura* 
</dt> <dd>

A altura da subimagem da imagem de textura. A especificação de uma subimagem de textura com largura zero não tem efeito.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | o *destino* não era um valor aceito.<br/>                                                                                                                                                                                                                                                                              |
| <dl> <dt>**\_valor inválido do GL \_**</dt> </dl>     | o *nível* era menor que zero ou maior que o *log* 2 (*Max*), em que *Max* é o valor retornado do \_ tamanho de textura Max GL \_ \_ .<br/>                                                                                                                                                                                          |
| <dl> <dt>**\_valor inválido do GL \_**</dt> </dl>     | *xoffset* era menor do que *Border* ou (largura de *xoffset*  +  ) era maior que (*l*  +  *Border*), *yoffset* era menor que *Border* ou (*yoffset*  +  *Height*) era maior que(a  +  *Border*), em que *w* é a largura de textura GL \_ \_ e *Border* é a borda de textura GL \_ \_ . Observe que *w* inclui duas vezes a largura da *borda* .<br/> |
| <dl> <dt>**\_valor inválido do GL \_**</dt> </dl>     | a *largura* era menor *que Border* ou *y* era menor que *Border*, em que *Border* é a largura da borda da matriz de textura.<br/>                                                                                                                                                                                           |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A matriz de textura não foi definida por uma operação [**glTexImage1D**](glteximage1d.md) anterior.<br/>                                                                                                                                                                                                                  |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/>                                                                                                                                                                                       |



## <a name="remarks"></a>Comentários

A função **glCopyTexSubImage2D** substitui uma parte retangular de uma imagem de textura bidimensional por pixels da framebuffer atual, e não da memória principal, como é o caso de [**glTexSubImage2D**](gltexsubimage2d.md).

Um retângulo de pixels que começa com as coordenadas da janela *x* e *y* e com a *largura* e a *altura* das dimensões substitui a parte da matriz de textura com os índices *xoffset* por meio de *xoffset* + (*Width* -1), pelos índices *yoffset* por meio de *yoffset* + (*Width* -1) no nível de mipmap especificado pelo *nível*. O retângulo de destino na matriz de textura não pode incluir nenhum texels fora da matriz de textura especificada originalmente.

A função **glCopyTexSubImage2D** processa os pixels em uma linha da mesma maneira que [**glCopyPixels**](glcopypixels.md), exceto que antes da conversão final dos pixels, todos os valores de componentes de pixel são clamped para o intervalo de \[ 0, 1 \] e convertidos para o formato interno da textura para armazenamento na matriz de textura. A ordenação de pixels é determinada com coordenadas *x* inferiores correspondentes às coordenadas de textura inferiores. Se qualquer um dos pixels dentro de uma linha especificada da framebuffer atual estiver fora da janela associada ao contexto de renderização atual, seus valores serão indefinidos.

Se qualquer um dos pixels dentro do retângulo especificado do framebuffer atual estiver fora da janela de leitura associada ao contexto de renderização atual, os valores obtidos para esses pixels serão indefinidos. Nenhuma alteração é feita no parâmetro *internalFormat*, *largura*, *altura* ou *borda* da matriz de textura especificada ou Texel valores fora da subimagem de textura especificada.

Você não pode incluir chamadas para **glCopyTexSubImage2D** em listas de exibição.

> [!Note]  
> A função **glCopyTexSubImage2D** só está disponível no OpenGL versão 1,1 ou posterior.

 

Texturing não tem efeito no modo de índice de cor. As funções [**glPixelStore**](glpixelstore-functions.md) e [**glPixelTransfer**](glpixeltransfer.md) afetam as imagens de textura exatamente como elas afetam a maneira como os pixels são desenhados usando [**glDrawPixels**](gldrawpixels.md).

As funções a seguir recuperam informações relacionadas ao **glCopyTexSubImage2D**:

[**glGetTexImage**](glgetteximage.md)

[**glIsEnabled**](glisenabled.md) com a textura do argumento GL \_ \_ 2D

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glCopyTexSubImage1D**](glcopytexsubimage1d.md)
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

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexSubImage2D**](gltexsubimage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





