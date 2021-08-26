---
title: função glEvalCoord2d (GL. h)
description: A função glEvalCoord2d avalia os mapas bidimensionais habilitados.
ms.assetid: 95963abc-841a-4154-92d5-5ae3e6de0f97
keywords:
- função glEvalCoord2d OpenGL
topic_type:
- apiref
api_name:
- glEvalCoord2d
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 845379985a95fe7514d197bc62a97cb67aa1a7f560f136ab8b9cda7caf31560e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081526"
---
# <a name="glevalcoord2d-function"></a>função glEvalCoord2d

A função **glEvalCoord2d** avalia os mapas bidimensionais habilitados.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glEvalCoord2d(
   GLdouble u,
   GLdouble v
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*u* 
</dt> <dd>

Um valor que é o domínio coordena *u* para a função base definida em uma função [**glMap2**](glmap2.md) anterior.

</dd> <dt>

*v* 
</dt> <dd>

Um valor que é o domínio coordena *v* para a função base definida em uma função [**glMap2**](glmap2.md) anterior.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

A função **glEvalCoord2d** avalia os mapas bidimensionais habilitados usando dois valores de domínio, *u* e *v*. Defina mapas com [**glMap1**](glmap1.md) e [**glMap2**](glmap2.md). Habilite ou desabilite-os com [**glEnable**](glenable.md) e [**glDisable**](gldisable.md).

Quando uma das funções **glEvalCoord** é emitida, todos os mapas atualmente habilitados da dimensão indicada são avaliados. Em seguida, para cada mapa habilitado, é como se a função OpenGL correspondente fosse emitida com o valor calculado. Ou seja, se \_ \_ o índice GL MAP1 index ou GL \_ map2 \_ estiver habilitado, uma função [**glIndex**](glindex-functions.md) será simulada. Se GL \_ MAP1 \_ Color \_ 4 ou GL \_ map2 \_ Color \_ 4 estiver habilitado, uma função **glColor** será simulada. Se GL \_ MAP1 \_ normal ou GL \_ map2 \_ normal estiver habilitado, um vetor normal é produzido e, se qualquer uma das \_ MAP1 de \_ textura GL \_ coord \_ 1, GL \_ MAP1 \_ Texture \_ coord \_ 2, GL \_ MAP1 de textura coord \_ \_ \_ 3, GL \_ MAP1 de \_ textura \_ coord \_ 4, GL map2 de textura coord \_ \_ \_ \_ 1, GL \_ map2 \_ Texture \_ coord \_ 2, GL map2 de textura \_ \_ \_ coord \_ 3 e GL \_ map2 Texture coord \_ \_ \_ 4 estiver habilitado, uma função [**glTexCoord**](gltexcoord-functions.md) apropriada será simulada.

O OpenGL usa valores avaliados em vez de valores atuais para as avaliações habilitadas e valores atuais de outra forma, para as coordenadas de cor, índice de cor, normal e textura. No entanto, os valores avaliados não atualizam os valores atuais. Portanto, se as funções [**glVertex**](glvertex-functions.md) estiverem intercaladas com as funções **glEvalCoord** , as coordenadas Color, normal e Texture associadas às funções **glVertex** não serão afetadas pelos valores gerados pelas funções **glEvalCoord** , mas somente pelas funções [**glColor**](glcolor-functions.md), [**glIndex**](glindex-functions.md), [**glNormal**](glnormal-functions.md)e [**glTexCoord**](gltexcoord-functions.md) mais recentes.

Se a geração normal automática estiver habilitada, **glEvalCoord2d** chamará [**glEnable**](glenable.md) com o argumento GL \_ automático \_ normal para gerar Normals de superfície de modo analítico, independentemente do conteúdo ou da habilitação do \_ mapa normal do GL map2 \_ . Permitir

![Equação mostrando um valor de produto cruzado para um mapa m.](images/evlcrd01.png)

O **n** normal gerado é

![Equação mostrando o n normal gerado para o mapa.](images/evlcrd02.png)

As funções a seguir recuperam informações relacionadas à função **glEvalCoord2d** :

[**glIsEnabled**](glisenabled.md) com Argument GL \_ MAP1 \_ vértice \_ 3

[**glIsEnabled**](glisenabled.md) com Argument GL \_ MAP1 \_ vértice \_ 4

índice de [**glIsEnabled**](glisenabled.md) com Argument GL \_ MAP1 \_

[**glIsEnabled**](glisenabled.md) com Argument GL \_ MAP1 \_ cor \_ 4

[**glIsEnabled**](glisenabled.md) com Argument GL \_ MAP1 \_ normal

[**glIsEnabled**](glisenabled.md) com Argument GL \_ MAP1 \_ Texture \_ coord \_ 1

[**glIsEnabled**](glisenabled.md) com Argument GL \_ MAP1 \_ Texture \_ coord \_ 2

[**glIsEnabled**](glisenabled.md) com Argument GL \_ MAP1 \_ Texture \_ coord \_ 3

[**glIsEnabled**](glisenabled.md) com Argument GL \_ MAP1 \_ Texture \_ coord \_ 4

[**glIsEnabled**](glisenabled.md) com Argument GL \_ map2 \_ vértice \_ 3

[**glIsEnabled**](glisenabled.md) com Argument GL \_ map2 \_ vértice \_ 4

índice de [**glIsEnabled**](glisenabled.md) com Argument GL \_ map2 \_

[**glIsEnabled**](glisenabled.md) com Argument GL \_ map2 \_ cor \_ 4

[**glIsEnabled**](glisenabled.md) com Argument GL \_ map2 \_ normal

[**glIsEnabled**](glisenabled.md) com Argument GL \_ map2 \_ Texture \_ coord \_ 1

[**glIsEnabled**](glisenabled.md) com Argument GL \_ map2 \_ Texture \_ coord \_ 2

[**glIsEnabled**](glisenabled.md) com Argument GL \_ map2 \_ Texture \_ coord \_ 3

[**glIsEnabled**](glisenabled.md) com Argument GL \_ map2 \_ Texture \_ coord \_ 4

[**glIsEnabled**](glisenabled.md) com Argument GL \_ automático \_ normal

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

 

 





