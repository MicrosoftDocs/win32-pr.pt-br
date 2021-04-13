---
title: função glPolygonOffset (GL. h)
description: A função glPolygonOffset define a escala e as unidades que o OpenGL usa para calcular os valores de profundidade.
ms.assetid: 06bc1aba-1692-40f0-8535-2cb65b487490
keywords:
- função glPolygonOffset OpenGL
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
ms.openlocfilehash: 84fa7d130fcc300fc1ebe33d091253e33f2d1e03
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369693"
---
# <a name="glpolygonoffset-function"></a>função glPolygonOffset

A função **glPolygonOffset** define a escala e as unidades que o OpenGL usa para calcular os valores de profundidade.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glPolygonOffset(
   GLfloat factor,
   GLfloat units
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*multi-fator* 
</dt> <dd>

Especifica um fator de escala que é usado para criar um deslocamento de profundidade variável para cada polígono. O valor inicial é zero.

</dd> <dt>

*Unit* 
</dt> <dd>

Especifica um valor que é multiplicado por um valor específico de implementação para criar um deslocamento de profundidade constante. O valor inicial é 0.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

Quando o \_ \_ deslocamento do polígono do GL estiver habilitado, o valor de profundidade de cada fragmento será deslocado após ser interpolado dos valores de profundidade dos vértices apropriados. O valor do deslocamento é *fator* \* ? unidades z + r \* , em que? z é uma medida da alteração em relação à área da tela do polígono, e r é o menor valor que é garantido para produzir um deslocamento resolvido para uma determinada implementação. O deslocamento é adicionado antes que o teste de profundidade seja executado e antes que o valor seja gravado no buffer de profundidade.

A função **glPolygonOffset** é útil para renderizar imagens de linha oculta, para aplicar decals a superfícies e para renderizar sólidos com bordas realçadas.

A função **glPolygonOffset** não tem efeito sobre as coordenadas de profundidade colocadas no buffer de comentários. Ele também não tem nenhum efeito na seleção.

As funções a seguir recuperam informações relacionadas ao **glPolygonOffset**:

-   [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com fator de \_ deslocamento do polígono GL do argumento \_ \_
-   [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com as \_ unidades de \_ deslocamento do polígono do Argument GL \_
-   [**glIsEnabled**](glisenabled.md) com argumento de \_ preenchimento de polígono do Argument GL \_ \_
-   [**glIsEnabled**](glisenabled.md) com linha de \_ deslocamento do polígono do Argument GL \_ \_
-   [**glIsEnabled**](glisenabled.md) com ponto de \_ deslocamento do polígono do Argument GL \_ \_

> [!Note]  
> A função **glPolygonOffset** só está disponível no OpenGl versão 1,1 ou superior.

 

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

 

 





