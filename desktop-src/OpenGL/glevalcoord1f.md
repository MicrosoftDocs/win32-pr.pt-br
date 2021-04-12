---
title: função glEvalCoord1f (GL. h)
description: A função glEvalCoord1f avalia mapas unidimensionais habilitados.
ms.assetid: 520e2d31-b9c2-4b06-ab61-c2c7aa18448a
keywords:
- função glEvalCoord1f OpenGL
topic_type:
- apiref
api_name:
- glEvalCoord1f
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 135d1b7faebf155c6027b715c64573fbb9463868
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454853"
---
# <a name="glevalcoord1f-function"></a>função glEvalCoord1f

A função **glEvalCoord1f** avalia mapas unidimensionais habilitados.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glEvalCoord1f(
   GLfloat u
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*u* 
</dt> <dd>

Um valor que é o domínio coordena *u* para a função base definida em uma função [**glMap1**](glmap1.md) anterior.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

A função **glEvalCoord1f** avalia os mapas unidimensionais habilitados no argumento *u*. Defina mapas com [**glMap1**](glmap1.md). Habilite ou desabilite-os com [**glEnable**](glenable.md) e [**glDisable**](gldisable.md).

Quando uma das funções **glEvalCoord** é emitida, todos os mapas atualmente habilitados da dimensão indicada são avaliados. Em seguida, para cada mapa habilitado, é como se a função OpenGL correspondente fosse emitida com o valor calculado. Ou seja, se \_ \_ o índice GL MAP1 index ou GL \_ map2 \_ estiver habilitado, uma função [**glIndex**](glindex-functions.md) será simulada. Se GL \_ MAP1 \_ Color \_ 4 ou GL \_ map2 \_ Color \_ 4 estiver habilitado, uma função **glColor** será simulada. Se GL \_ MAP1 \_ normal ou GL \_ map2 \_ normal estiver habilitado, um vetor normal é produzido e, se qualquer uma das \_ MAP1 de \_ textura GL \_ coord \_ 1, GL \_ MAP1 \_ Texture \_ coord \_ 2, GL \_ MAP1 de textura coord \_ \_ \_ 3, GL \_ MAP1 de \_ textura \_ coord \_ 4, GL map2 de textura coord \_ \_ \_ \_ 1, GL \_ map2 \_ Texture \_ coord \_ 2, GL map2 de textura \_ \_ \_ coord \_ 3 e GL \_ map2 Texture coord \_ \_ \_ 4 estiver habilitado, uma função [**glTexCoord**](gltexcoord-functions.md) apropriada será simulada.

O OpenGL usa valores avaliados em vez de valores atuais para as avaliações habilitadas e valores atuais de outra forma, para as coordenadas de cor, índice de cor, normal e textura. No entanto, os valores avaliados não atualizam os valores atuais. Portanto, se as funções [**glVertex**](glvertex-functions.md) estiverem intercaladas com as funções **glEvalCoord** , as coordenadas Color, normal e Texture associadas às funções **glVertex** não serão afetadas pelos valores gerados pelas funções **glEvalCoord** , mas somente pelas funções [**glColor**](glcolor-functions.md), [**glIndex**](glindex-functions.md), [**glNormal**](glnormal-functions.md)e [**glTexCoord**](gltexcoord-functions.md) mais recentes.

As funções a seguir recuperam informações relacionadas à função **glEvalCoord1f** :

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

 

 





