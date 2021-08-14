---
title: Função glHint (Gl.h)
description: A função glHint especifica dicas específicas da implementação.
ms.assetid: 6d03e107-321a-45ee-9ce7-25fa9cab32d9
keywords:
- Função glHint OpenGL
topic_type:
- apiref
api_name:
- glHint
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7602b4f0af35c8bc9aeb38cdcb613e30ded907ced75e2241c8ed9e23b57fd98f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118359642"
---
# <a name="glhint-function"></a>Função glHint

A **função glHint** especifica dicas específicas da implementação.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glHint(
   GLenum target,
   GLenum mode
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*destino* 
</dt> <dd>

Uma constante simbólica que indica o comportamento a ser controlado. As constantes simbólicas a seguir, juntamente com a semântica sugerida, são aceitas.



| Valor                                                                                                                                                                                                              | Significado                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_FOG_HINT"></span><span id="gl_fog_hint"></span><dl> <dt>**DICA \_ GL BP \_**</dt> </dl>                                                           | Indica a precisão do cálculo da base de dados. Se o cálculo de pixel por pixel não for suportado com eficiência pela implementação do OpenGL, a dica de GL DONT CARE ou GL FASTEST poderá resultar em um cálculo por vértice de efeitos \_ \_ de \_ roda.<br/>                                                                          |
| <span id="GL_LINE_SMOOTH_HINT"></span><span id="gl_line_smooth_hint"></span><dl> <dt>**DICA SUAVE \_ DE \_ LINHA \_ GL**</dt> </dl>                                  | Indica a qualidade de amostragem de linhas antialiasdas. A dica de GL NICEST pode resultar na geração de mais fragmentos de pixel durante a rasterização, se uma função de filtro maior \_ for aplicada.<br/>                                                                                                               |
| <span id="GL_PERSPECTIVE_CORRECTION_HINT"></span><span id="gl_perspective_correction_hint"></span><dl> <dt>**DICA DE \_ \_ CORREÇÃO DE PERSPECTIVA \_ GL**</dt> </dl> | Indica a qualidade da interpolação de coordenadas de cor e textura. Se a interpolação de parâmetro corrigida pela perspectiva não for suportada com eficiência pela implementação do OpenGL, a dica de GL DONT CARE ou GL FASTEST poderá resultar em interpolação linear simples de cores \_ \_ \_ e/ou coordenadas de textura.<br/> |
| <span id="GL_POINT_SMOOTH_HINT"></span><span id="gl_point_smooth_hint"></span><dl> <dt>**DICA SUAVE DO PONTO GL \_ \_ \_**</dt> </dl>                               | Indica a qualidade de amostragem de pontos antialiados. A dica de GL NICEST pode resultar na geração de mais fragmentos de pixel durante a rasterização, se uma função de filtro maior \_ for aplicada.<br/>                                                                                                              |
| <span id="GL_POLYGON_SMOOTH_HINT"></span><span id="gl_polygon_smooth_hint"></span><dl> <dt>**DICA SUAVE \_ DE \_ POLÍGONO \_ GL**</dt> </dl>                         | Indica a qualidade de amostragem de polígonos antialiasados. A dica de GL NICEST pode resultar na geração de mais fragmentos de pixel durante a rasterização, se uma função de filtro maior \_ for aplicada.<br/>                                                                                                            |



 

</dd> <dt>

*mode* 
</dt> <dd>

Uma constante simbólica que indica o comportamento desejado. As constantes simbólicas a seguir são aceitas.



| Valor                                                                                                                                                       | Significado                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="GL_FASTEST"></span><span id="gl_fastest"></span><dl> <dt>**GL \_ MAIS RÁPIDO**</dt> </dl>        | A opção mais eficiente deve ser escolhida.<br/>                    |
| <span id="GL_NICEST"></span><span id="gl_nicest"></span><dl> <dt>**GL \_ NICEST**</dt> </dl>           | A opção mais correta ou de mais alta qualidade deve ser escolhida.<br/> |
| <span id="GL_DONT_CARE"></span><span id="gl_dont_care"></span><dl> <dt>**GL \_ DONT \_ CARE**</dt> </dl> | O cliente não tem uma preferência.<br/>                          |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela [**função glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *target* ou *mode* não era um valor aceito.<br/>                                                                              |
| <dl> <dt>**OPERAÇÃO \_ GL \_ INVÁLIDA**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd.**](glend.md)<br/> |



## <a name="remarks"></a>Comentários

Quando há espaço para interpretação, você pode controlar determinados aspectos do comportamento openGL com dicas. Especifique uma dica com dois argumentos. O *parâmetro* de destino é uma constante simbólica que indica o comportamento a ser controlado e *o* modo é outra constante simbólica que indica o comportamento desejado.

Embora os aspectos de implementação que podem ser sugeridos sejam bem definidos, a interpretação das dicas depende da implementação.

A **função glHint** pode ser ignorada.

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

[**glEnd**](glend.md)
</dt> </dl>

 

 





