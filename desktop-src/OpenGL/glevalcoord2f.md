---
title: Função glEvalCoord2f (Gl.h)
description: A função glEvalCoord2f avalia mapas bidimensionais habilitados.
ms.assetid: feb2a324-9148-4e3f-8e6e-c545e36962c6
keywords:
- Função glEvalCoord2f OpenGL
topic_type:
- apiref
api_name:
- glEvalCoord2f
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0147890cab18fc8e3c3f32fa44d0967bfb059bf952bc2019f471162dddef842
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061714"
---
# <a name="glevalcoord2f-function"></a>Função glEvalCoord2f

A [**função glEvalCoord2f**](glevalcoord2d.md) avalia mapas bidimensionais habilitados.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glEvalCoord2f(
   GLfloat u,
   GLfloat v
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*u* 
</dt> <dd>

Um valor que é a coordenada de *domínio u* para a função base definida em uma função [**glMap2**](glmap2.md) anterior.

</dd> <dt>

*v* 
</dt> <dd>

Um valor que é a coordenada de *domínio v* para a função base definida em uma função [**glMap2**](glmap2.md) anterior.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

A [**função glEvalCoord2f**](glevalcoord2d.md) avalia mapas bidimensionais habilitados usando dois valores de domínio, *u* e *v.* Defina mapas [**com glMap2.**](glmap2.md) Habilita ou desabilite-os [**com glEnable**](glenable.md) e [**glDisable.**](gldisable.md)

Quando uma das **funções glEvalCoord** é emitida, todos os mapas atualmente habilitados da dimensão indicada são avaliados. Em seguida, para cada mapa habilitado, é como se a função OpenGL correspondente fosse emitida com o valor computado. Ou seja, se GL \_ MAP1 INDEX ou GL MAP2 INDEX estiver \_ \_ \_ habilitado, uma [**função glIndex**](glindex-functions.md) será simulada. Se GL \_ MAP1 \_ COLOR \_ 4 ou GL \_ MAP2 COLOR 4 estiver \_ \_ habilitado, uma função **glcolor** será simulada. Se GL MAP1 NORMAL ou GL MAP2 NORMAL estiver habilitado, um vetor normal é produzido e se qualquer um de \_ \_ GL \_ \_ \_ MAP1 TEXTURE \_ \_ \_ COORD 1, GL \_ MAP1 TEXTURE \_ \_ COORD \_ 2, \_ GL MAP1 TEXTURE \_ \_ \_ COORD 3, GL \_ \_ \_ \_ \_ \_ MAP1 TEXTURE COORD 4, GL MAP2 TEXTURE \_ COORD \_ 1, GL \_ MAP2 \_ TEXTURE \_ COORD \_ 2, GL \_ MAP2 TEXTURE \_ COORD 3 e GL \_ MAP2 TEXTURE COORD \_ 4 \_ \_ \_ \_ [](gltexcoord-functions.md) estiver habilitado, uma função glTexCoord apropriada será simulada.

O OpenGL usa valores avaliados em vez de valores atuais para as avaliações habilitadas e os valores atuais, caso contrário, para coordenadas de cor, índice de cores, normal e textura. No entanto, os valores avaliados não atualizam os valores atuais. Portanto, se as funções [**glVertex**](glvertex-functions.md) são intercaladas com funções **glEvalCoord,** as coordenadas de cor, normal e textura associadas às funções **glVertex** não são afetadas pelos valores gerados pelas funções **glEvalCoord,** mas apenas pelas funções [**glColor,**](glcolor-functions.md) [**glIndex**](glindex-functions.md), [**glNormal**](glnormal-functions.md)e [**glTexCoord**](gltexcoord-functions.md) mais recentes.

Se a geração normal automática estiver habilitada, [**glEvalCoord2f**](glevalcoord2d.md) chamará [**glEnable**](glenable.md) com o argumento GL AUTO NORMAL para gerar normais de superfície analíticamente, independentemente do conteúdo ou da habilitação do mapa \_ GL \_ \_ MAP2 \_ NORMAL. Permitir

![Equação mostrando um valor entre produtos para um mapa m.](images/evlcrd01.png)

O n normal **gerado** é

![Equação mostrando o n normal gerado para o mapa.](images/evlcrd02.png)

As funções a seguir recuperam informações relacionadas à [**função glEvalCoord2f:**](glevalcoord2d.md)

[**glIsEnabled com**](glisenabled.md) o argumento GL \_ MAP1 \_ VERTEX \_ 3

[**glIsEnabled com**](glisenabled.md) o argumento GL \_ MAP1 \_ VERTEX \_ 4

[**glIsEnabled com**](glisenabled.md) o argumento GL \_ MAP1 \_ INDEX

[**glIsEnabled com**](glisenabled.md) o argumento GL \_ MAP1 \_ COLOR \_ 4

[**glIsEnabled com**](glisenabled.md) o argumento GL \_ MAP1 \_ NORMAL

[**glIsEnabled com**](glisenabled.md) o argumento GL \_ MAP1 \_ TEXTURE \_ COORD \_ 1

[**glIsEnabled com**](glisenabled.md) o argumento GL \_ MAP1 \_ TEXTURE \_ COORD \_ 2

[**glIsEnabled com**](glisenabled.md) o argumento GL \_ MAP1 \_ TEXTURE \_ COORD \_ 3

[**glIsEnabled com**](glisenabled.md) o argumento GL \_ MAP1 \_ TEXTURE \_ COORD \_ 4

[**glIsEnabled com**](glisenabled.md) o argumento GL \_ MAP2 \_ VERTEX \_ 3

[**glIsEnabled com**](glisenabled.md) o argumento GL \_ MAP2 \_ VERTEX \_ 4

[**glIsEnabled com**](glisenabled.md) o argumento GL \_ MAP2 \_ INDEX

[**glIsEnabled com**](glisenabled.md) o argumento GL \_ MAP2 \_ COLOR \_ 4

[**glIsEnabled com**](glisenabled.md) o argumento GL \_ MAP2 \_ NORMAL

[**glIsEnabled com**](glisenabled.md) o argumento GL \_ MAP2 \_ TEXTURE \_ COORD \_ 1

[**glIsEnabled com**](glisenabled.md) o argumento GL \_ MAP2 \_ TEXTURE \_ COORD \_ 2

[**glIsEnabled com**](glisenabled.md) o argumento GL \_ MAP2 \_ TEXTURE \_ COORD \_ 3

[**glIsEnabled com**](glisenabled.md) o argumento GL \_ MAP2 \_ TEXTURE \_ COORD \_ 4

[**glIsEnabled com**](glisenabled.md) o argumento GL \_ AUTO \_ NORMAL

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

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glDisable**](gldisable.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glEvalMesh**](glevalmesh-functions.md)
</dt> <dt>

[**glEvalPoint**](glevalpoint.md)
</dt> <dt>

[**glGetMap**](glgetmap.md)
</dt> <dt>

[**glIndex**](glindex-functions.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glMap1**](glmap1.md)
</dt> <dt>

[**glMap2**](glmap2.md)
</dt> <dt>

[**glMapGrid**](glmapgrid-functions.md)
</dt> <dt>

[**glNormal**](glnormal-functions.md)
</dt> <dt>

[**glTexCoord**](gltexcoord-functions.md)
</dt> <dt>

[**glVertex**](glvertex-functions.md)
</dt> </dl>

 

 





