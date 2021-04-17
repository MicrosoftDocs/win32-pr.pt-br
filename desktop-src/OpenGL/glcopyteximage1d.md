---
title: função glCopyTexImage1D (GL. h)
description: A função glCopyTexImage1D copia os pixels da framebuffer em uma imagem de textura unidimensional.
ms.assetid: 3b4d12d5-5efe-40d2-ac5f-95ea5ef243dd
keywords:
- função glCopyTexImage1D OpenGL
topic_type:
- apiref
api_name:
- glCopyTexImage1D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e63180386c094f0c4e4de0f1a361bc3bcb1c6e5e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755984"
---
# <a name="glcopyteximage1d-function"></a>função glCopyTexImage1D

A função **glCopyTexImage1D** copia os pixels da framebuffer em uma imagem de textura unidimensional.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glCopyTexImage1D(
   GLenum  target,
   GLint   level,
   GLenum  internalFormat,
   GLint   x,
   GLint   y,
   GLsizei width,
   GLint   border
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*destino* 
</dt> <dd>

O destino para o qual os dados da imagem serão alterados. Deve ter o valor GL \_ Texture \_ 1D.

</dd> <dt>

*level* 
</dt> <dd>

O número de nível de detalhe. Nível 0 é a imagem base. O nível *n* é a imagem de redução *n* º mipmap.

</dd> <dt>

*internalFormat* 
</dt> <dd>

O formato interno e a resolução dos dados de textura. Esse parâmetro deve ser um dos valores simbólicos a seguir.



| Constante                 | Bits de R | G bits | Bits B | Um bits | Bits L | I bits |
|--------------------------|--------|--------|--------|--------|--------|--------|
| GL \_ alfa                |        |        |        |        |        |        |
| \_ALPHA4 GL               |        |        |        | 4      |        |        |
| \_ALPHA8 GL               |        |        |        | 8      |        |        |
| \_ALPHA12 GL              |        |        |        | 12     |        |        |
| \_ALPHA16 GL              |        |        |        | 16     |        |        |
| \_luminância GL            |        |        |        |        |        |        |
| \_LUMINANCE4 GL           |        |        |        |        | 4      |        |
| \_LUMINANCE8 GL           |        |        |        |        | 8      |        |
| \_LUMINANCE12 GL          |        |        |        |        | 12     |        |
| \_LUMINANCE16 GL          |        |        |        |        | 16     |        |
| luminância do GL \_ \_ alfa     |        |        |        |        |        |        |
| GL \_ LUMINANCE4 \_ ALPHA4   |        |        |        | 4      | 4      |        |
| GL \_ LUMINANCE6 \_ ALPHA2   |        |        |        | 2      | 6      |        |
| GL \_ LUMINANCE8 \_ ALPHA8   |        |        |        | 8      | 8      |        |
| GL \_ LUMINANCE12 \_ ALPHA4  |        |        |        | 4      | 12     |        |
| GL \_ LUMINANCE12 \_ ALPHA12 |        |        |        | 12     | 12     |        |
| GL \_ LUMINANCE16 \_ ALPHA16 |        |        |        | 16     | 16     |        |
| intensidade do GL \_            |        |        |        |        |        |        |
| \_INTENSITY4 GL           |        |        |        |        |        | 4      |
| \_INTENSITY8 GL           |        |        |        |        |        | 8      |
| \_INTENSITY12 GL          |        |        |        |        |        | 12     |
| \_INTENSITY16 GL          |        |        |        |        |        | 16     |
| GL em \_ RGB                  |        |        |        |        |        |        |
| GL \_ R3 \_ G3 \_ B2           | 3      | 3      | 2      |        |        |        |
| \_RGB4 GL                 | 4      | 4      | 4      |        |        |        |
| \_RGB5 GL                 | 5      | 5      | 5      |        |        |        |
| \_RGB8 GL                 | 8      | 8      | 8      |        |        |        |
| \_RGB10 GL                | 10     | 10     | 10     |        |        |        |
| \_RGB12 GL                | 12     | 12     | 12     |        |        |        |
| \_RGB16 GL                | 16     | 16     | 16     |        |        |        |
| Se \_ RGBA                 |        |        |        |        |        |        |
| \_RGBA2 GL                | 2      | 2      | 2      | 2      |        |        |
| \_RGBA4 GL                | 4      | 4      | 4      | 4      |        |        |
| GL \_ RGB5 \_ a1             | 5      | 5      | 5      | 1      |        |        |
| \_RGBA8 GL                | 8      | 8      | 8      | 8      |        |        |
| GL \_ RGB10 \_ a2            | 10     | 10     | 10     | 2      |        |        |
| \_RGBA12 GL               | 12     | 12     | 12     | 12     |        |        |
| \_RGBA16 GL               | 16     | 16     | 16     | 16     |        |        |



 

</dd> <dt>

*x* 
</dt> <dd>

A coordenada do plano x da janela do canto inferior esquerdo da linha de pixels a ser copiada.

</dd> <dt>

*y* 
</dt> <dd>

A coordenada de plano y da janela do canto inferior esquerdo da linha de pixels a ser copiada.

</dd> <dt>

*width* 
</dt> <dd>

A largura da imagem de textura. Deve ser zero ou 2n + 2 (*Border*) para algum número inteiro *n*. A altura da imagem de textura é 1.

</dd> <dt>

*borda* 
</dt> <dd>

A largura da borda. Deve ser zero ou 1.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | o *destino* não era um valor aceito.<br/>                                                                                                           |
| <dl> <dt>**\_valor inválido do GL \_**</dt> </dl>     | o *nível* era menor que zero ou maior que log2 *Max*, em que *Max* é o valor RETORNADO de \_ tamanho de textura Max GL \_ \_ .<br/>                           |
| <dl> <dt>**\_valor inválido do GL \_**</dt> </dl>     | a *borda* não era zero ou 1.<br/>                                                                                                                   |
| <dl> <dt>**\_valor inválido do GL \_**</dt> </dl>     | *a largura* era menor que zero, maior que 2 + \_ GL tamanho máximo de \_ textura \_ ou a *largura* não pode ser representada como 2n + (*Border*) para algum número inteiro *n*.<br/> |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/>                    |



## <a name="remarks"></a>Comentários

A função **glCopyTexImage1D** define uma imagem de textura unidimensional usando pixels do framebuffer atual, em vez de memória principal, como é o caso para [**glTexImage1D**](glteximage1d.md).

Usando o nível de mipmap especificado com o *nível*, as matrizes de textura são definidas como uma linha de pixel alinhada ao canto inferior esquerdo da janela nas coordenadas especificadas por *x* e *y*, com um comprimento igual à *largura* + 2 \* *borda*. O formato interno da matriz de textura é especificado com o parâmetro *internalFormat* .

A função **glCopyTexImage1D** processa os pixels em uma linha da mesma maneira que [**glCopyPixels**](glcopypixels.md), exceto que antes da conversão final dos pixels, todos os valores de componentes de pixel são clamped para o intervalo de \[ 0, 1 \] e convertidos para o formato interno da textura para armazenamento na matriz de textura. A ordenação de pixels é determinada com coordenadas *x* inferiores correspondentes às coordenadas de textura inferiores. Se qualquer um dos pixels dentro de uma linha especificada da framebuffer atual estiver fora da janela associada ao contexto de renderização atual, seus valores serão indefinidos.

Você não pode incluir chamadas para **glCopyTexImage1D** em listas de exibição.

> [!Note]  
> A função **glCopyTexImage1D** só está disponível no OpenGL versão 1,1 ou posterior.

 

Texturing não tem efeito no modo de índice de cor. As funções [**glPixelStore**](glpixelstore-functions.md) e [**glPixelTransfer**](glpixeltransfer.md) afetam as imagens de textura exatamente como elas afetam o [**glDrawPixels**](gldrawpixels.md).

A função a seguir recupera informações relacionadas a **glCopyTexImage1D**:

[**glIsEnabled**](glisenabled.md) com a textura do argumento GL \_ \_ 1D

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

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glCopyTexImage2D**](glcopyteximage2d.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
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

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





