---
title: função glGetTexImage (GL. h)
description: A função glGetTexImage retorna uma imagem de textura.
ms.assetid: d7235df4-2dd8-4537-aadd-284c130a3f99
keywords:
- função glGetTexImage OpenGL
topic_type:
- apiref
api_name:
- glGetTexImage
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b116bc4ae517d0767d794767ad5232d8537033d62a099a3906f9f2ca96a7166c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493746"
---
# <a name="glgetteximage-function"></a>função glGetTexImage

A função **glGetTexImage** retorna uma imagem de textura.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glGetTexImage(
   GLenum target,
   GLint  level,
   GLenum format,
   GLenum type,
   GLvoid *pixels
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*destino* 
</dt> <dd>

Especifica qual textura deve ser obtida. A textura GL \_ \_ 1D e GL de \_ textura \_ 2D são aceitas.

</dd> <dt>

*level* 
</dt> <dd>

O número de nível de detalhe da imagem desejada. Nível 0 é o nível de imagem base. O nível *n* é a imagem de redução *n* º mipmap.

</dd> <dt>

*format* 
</dt> <dd>

Um formato de pixel para os dados retornados. Os formatos com suporte são GL \_ vermelho, GL \_ verde, GL \_ Blue, GL \_ alfa, GL \_ RGB, GL \_ RGBA, GL \_ luminescência, GL \_ BGR \_ ext, GL BGRA ext e a luminância de \_ \_ GL \_ \_ alfa.

</dd> <dt>

*tipo* 
</dt> <dd>

Um tipo de pixel para os dados retornados. Os tipos com suporte são GL \_ não assinado \_ , byte GL, GL \_ \_ não assinado \_ curto, GL \_ curto, GL \_ não assinado \_ int, GL \_ int e GL \_ float.

</dd> <dt>

*pixels* 
</dt> <dd>

Retorna a imagem de textura. Deve ser um ponteiro para uma matriz do tipo especificado por *tipo*.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | o *destino*, o *formato* ou o *tipo* não era um valor aceito.<br/>                                                                    |
| <dl> <dt>**\_valor inválido do GL \_**</dt> </dl>     | o *nível* é menor que zero ou maior que o *log* 2 (*Max*), em que *Max* é o valor retornado do \_ tamanho de textura Max GL \_ \_ .<br/>      |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md) .<br/> |



## <a name="remarks"></a>Comentários

A função **glGetTexImage** retorna uma imagem de textura em *pixels*. O parâmetro de *destino* especifica se a imagem de textura desejada é uma especificada por [**glTexImage1D**](glteximage1d.md)**(** GL \_ Texture \_ 1D **)** ou por [**glTexImage2D**](glteximage2d.md)**(GL de** \_ textura \_ 2D **)**. O parâmetro *Level* especifica o número de nível de detalhe da imagem desejada. Os parâmetros *Format* e *Type* especificam o formato e o tipo da matriz de imagem desejada. Para obter uma descrição dos valores aceitáveis para os parâmetros de *formato* e *tipo* , respectivamente, consulte **glTexImage1D** e [**glDrawPixels**](gldrawpixels.md).

A operação de **glGetTexImage** é melhor compreendida considerando-se a imagem de textura de quatro componentes internos selecionada como um buffer de cores RGBA do tamanho da imagem. A semântica de **glGetTexImage** é, então, idêntica àquelas de [**glReadPixels**](glreadpixels.md) chamadas com o mesmo *formato* e *tipo*, *com x* e *y* definidos como zero, a *largura* é definida como a largura da imagem de textura (incluindo a borda, se uma tiver sido especificada) e a *altura* definida como uma para imagens de 1-d ou a altura da imagem de textura (incluindo a borda, se uma tiver sido especificada) para imagens 2D.

Como a imagem de textura interna é uma imagem RGBA, o índice de cores GL de formatos de pixel \_ \_ , o índice de \_ estêncil GL e o componente de \_ \_ profundidade GL \_ não são aceitos, e o bitmap do tipo pixel GL \_ não é aceito.

Se a imagem de textura selecionada não contiver quatro componentes, os mapeamentos a seguir serão aplicados. As texturas de componente único são tratadas como buffers RGBA com vermelho definido como o valor de componente único, e verde, azul e alfa definidos como zero.

As texturas de dois componentes são tratadas como buffers RGBA, com vermelho definido como o valor do componente zero, alfa definido como o valor do componente um, e verde e azul definidos como zero. Por fim, as texturas de três componentes são tratadas como buffers RGBA com vermelho definido como componente zero, verde definido como componente um, azul definido como componente dois e alfa definido como zero.

Para determinar o tamanho necessário de *pixels*, use [**glGetTexLevelParameter**](glgettexlevelparameter.md) para verificar as dimensões da imagem de textura interna e, em seguida, dimensione o número necessário de pixels pelo armazenamento necessário para cada pixel, com base no *formato* e no *tipo*. Certifique-se de levar os parâmetros de armazenamento de pixel em conta, especialmente o \_ alinhamento do pacote GL \_ .

Se um erro for gerado, nenhuma alteração será feita no conteúdo de *pixels*.

As funções a seguir recuperam informações relacionadas ao **glGetTexImage**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com \_ alinhamento de pacote do Argument GL \_ e outros

[**glGetTexLevelParameter**](glgettexlevelparameter.md) com largura de textura do argumento GL \_ \_

**glGetTexLevelParameter** com altura de textura do argumento GL \_ \_

**glGetTexLevelParameter** com borda de \_ textura Argument GL \_

**glGetTexLevelParameter** com componentes de \_ textura Argument GL \_

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

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGetTexLevelParameter**](glgettexlevelparameter.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> </dl>

 

 





