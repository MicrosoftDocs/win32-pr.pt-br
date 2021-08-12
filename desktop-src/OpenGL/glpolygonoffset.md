---
title: Função glPolygonOffset (Gl.h)
description: A função glPolygonOffset define a escala e as unidades que o OpenGL usa para calcular valores de profundidade.
ms.assetid: 06bc1aba-1692-40f0-8535-2cb65b487490
keywords:
- Função glPolygonOffset OpenGL
topic_type:
- apiref
api_name:
- glPolygonOffset
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 314372c0ce87ef5b75db24e4482d6b621422546abe0c71a34cc9821cb4391997
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118614912"
---
# <a name="glpolygonoffset-function"></a>Função glPolygonOffset

A **função glPolygonOffset define** a escala e as unidades que o OpenGL usa para calcular valores de profundidade.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glPolygonOffset(
   GLfloat factor,
   GLfloat units
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Fator* 
</dt> <dd>

Especifica um fator de escala usado para criar um deslocamento de profundidade variável para cada polígono. O valor inicial é zero.

</dd> <dt>

*Unidades* 
</dt> <dd>

Especifica um valor multiplicado por um valor específico da implementação para criar um deslocamento de profundidade constante. O valor inicial é 0.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

O código de erro a seguir pode ser recuperado pela [**função glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERAÇÃO \_ GL \_ INVÁLIDA**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd.**](glend.md)<br/> |



## <a name="remarks"></a>Comentários

Quando GL POLYGON OFFSET estiver habilitado, o valor de profundidade de cada fragmento será deslocada depois que for interpolado dos valores de profundidade dos \_ \_ vértices apropriados. O valor do  deslocamento é o fator ?z + r unidades , em que ?z é uma medida da alteração em profundidade em relação à área da tela do \* polígono e r é o menor valor que tem a garantia de produzir um deslocamento resolvível para \* uma determinada implementação. O deslocamento é adicionado antes que o teste de profundidade seja executado e antes que o valor seja gravado no buffer de profundidade.

A **função glPolygonOffset** é útil para renderizar imagens de linha oculta, para aplicar decals a superfícies e para renderizar sólidos com bordas realçadas.

A **função glPolygonOffset** não tem nenhum efeito nas coordenadas de profundidade colocadas no buffer de comentários. Ele também não tem nenhum efeito na seleção.

As funções a seguir recuperam informações relacionadas **a glPolygonOffset**:

-   [**glGet com**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argumento GL \_ POLYGON \_ OFFSET \_ FACTOR
-   [**glGet com**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) o argumento GL \_ POLYGON \_ OFFSET \_ UNITS
-   [**glIsEnabled com**](glisenabled.md) o argumento GL \_ POLYGON \_ OFFSET \_ FILL
-   [**glIsEnabled com argumento**](glisenabled.md) GL \_ POLYGON OFFSET \_ \_ LINE
-   [**glIsEnabled com**](glisenabled.md) o argumento GL \_ POLYGON \_ OFFSET \_ POINT

> [!Note]  
> A **função glPolygonOffset** só está disponível no OpenGl versão 1.1 ou superior.

 

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

[**glDepthFunc**](gldepthfunc.md)
</dt> <dt>

[**glDisable**](gldisable.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glLineWidth**](gllinewidth.md)
</dt> <dt>

[**glStencilOp**](glstencilop.md)
</dt> <dt>

[**glTexEnv**](gltexenv-functions.md)
</dt> </dl>

 

 





