---
title: Função glDisable (Gl.h)
description: As funções glEnable e glDisable habilitam ou desabilitam as funcionalidades do OpenGL. | Função glDisable (Gl.h)
ms.assetid: 094f730e-5e2b-485e-8d9d-fee2902d3d5f
keywords:
- Função glDisable OpenGL
topic_type:
- apiref
api_name:
- glDisable
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a124421684fc2e1b5826e149b90f9d249a6236c792f3830fa2a10e29793d0935
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119625726"
---
# <a name="gldisable-function"></a>Função glDisable

As [**funções glEnable**](glenable.md) e **glDisable** habilitam ou desabilitam as funcionalidades do OpenGL.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glDisable(
   GLenum cap
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Tampa* 
</dt> <dd>

Uma constante simbólica que indica uma funcionalidade OpenGL.

Para discussão sobre o limite de *valores* que pode ser considerado, consulte a seção Comentários a seguir.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela [**função glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *cap* não era um dos valores listados na seção Comentários anterior.<br/>                                                   |
| <dl> <dt>**OPERAÇÃO \_ GL \_ INVÁLIDA**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd.**](glend.md)<br/> |



## <a name="remarks"></a>Comentários

As [**funções glEnable**](glenable.md) e **glDisable** habilitam e desabilitam vários recursos gráficos OpenGL. Use [**glIsEnabled**](glisenabled.md) ou [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) para determinar a configuração atual de qualquer funcionalidade.

[**GlEnable e**](glenable.md) **glDisable** têm um único argumento, *cap*, que pode assumir um dos seguintes valores:



| Valor                       | Significado                                                                                                                                                                                                                                                     |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TESTE ALFA \_ \_ GL             | Se habilitado, faça testes alfa. Consulte [**glAlphaFunc**](glalphafunc.md).                                                                                                                                                                                       |
| GL \_ AUTO \_ NORMAL            | Se habilitada, a superfície de computação vetores normais analíticos quando GL \_ MAP2 \_ VERTEX 3 ou \_ GL \_ MAP2 \_ VERTEX 4 gerou \_ vértices. Consulte [**glMap2**](glmap2.md).                                                                                        |
| GL \_ BLEND                   | Se habilitada, combina os valores de cor RGBA de entrada com os valores nos buffers de cores. Consulte [**glBlendFunc**](glblendfunc.md).                                                                                                                              |
| GL \_ CLIP \_ PLANE *i*          | Se habilitada, recorte geometria no plano de recorte definido pelo usuário *i*. Consulte [**glClipPlane.**](glclipplane.md)                                                                                                                                                  |
| OPERAÇÃO \_ DE LÓGICA DE CORES \_ \_ GL        | Se habilitada, aplique a operação lógica atual aos valores de cor RGBA de entrada e buffer de cores. Consulte [**glLogicOp**](gllogicop.md).                                                                                                                     |
| MATERIAL \_ DE COR GL \_         | Se habilitado, tenha um ou mais parâmetros de material para acompanhar a cor atual. Consulte [**glColorMaterial.**](glcolormaterial.md)                                                                                                                                   |
| ROSTO \_ DE REDUÇÃO \_ GL              | Se habilitada, descarte polígonos com base em seu vento nas coordenadas da janela. Consulte [**glCullFace.**](glcullface.md)                                                                                                                                               |
| TESTE \_ DE PROFUNDIDADE DE \_ GL             | Se habilitado, faça comparações de profundidade e atualize o buffer de profundidade. Consulte [**glDepthFunc**](gldepthfunc.md) [**e glDepthRange.**](gldepthrange.md)                                                                                                              |
| GL \_ DITHER                  | Se habilitada, dither color components or indexes before they are written to the color buffer.                                                                                                                                                                 |
| GL \_ BP                     | Se habilitada, misture uma cor de cinza na cor pós-texto. Consulte [**glFog**](glfog.md).                                                                                                                                                                    |
| GL \_ INDEX \_ LOGIC \_ OP        | Se habilitada, aplique a operação lógica atual aos índices de entrada e de buffer de cores. Consulte [**glLogicOp**](gllogicop.md).                                                                                                                         |
| GL \_ LIGHT *i*                | Se habilitado, inclua light *i* na avaliação da equação de iluminação. Consulte [**glLightModel**](gllightmodel-functions.md) e [**glLight.**](gllight-functions.md)                                                                                      |
| ILUMINAÇÃO \_ GL                | Se habilitado, use os parâmetros de iluminação atuais para calcular a cor ou o índice do vértice. Se desabilitado, associe a cor ou índice atual a cada vértice. Consulte [**glMaterial,**](glmaterial-functions.md) **glLightModel** e **glLight.**                |
| GL \_ LINE \_ SMOOTH            | Se habilitado, desenhe linhas com filtragem correta. Se desabilitado, desenhe linhas com alias. Consulte [**glLineWidth.**](gllinewidth.md)                                                                                                                                     |
| GL \_ \_ LINEPPLE           | Se habilitada, use o padrão de apple de linha atual ao desenhar linhas. Consulte [**glLineStipple**](gllinestipple.md).                                                                                                                                            |
| GL \_ LOGIC \_ OP               | Se habilitada, aplique a operação lógica selecionada no momento aos índices de buffer de cores e de entrada. Consulte [**glLogicOp**](gllogicop.md).                                                                                                                    |
| GL \_ MAP1 \_ COR \_ 4          | Se habilitada, chamadas [**para glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md)e [**glEvalPoint1**](glevalpoint.md) geram valores RGBA. Consulte também [**glMap1**](glmap1.md).                                           |
| GL \_ MAP1 \_ INDEX             | Se habilitada, chamadas **para glEvalCoord1**, **glEvalMesh1** e **glEvalPoint1** geram índices de cores. Consulte também **glMap1**.                                                                                                                                   |
| GL \_ MAP1 \_ NORMAL            | Se habilitada, chamadas [**para glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md)e [**glEvalPoint1**](glevalpoint.md) geram normais. Consulte também [**glMap1**](glmap1.md).                                               |
| GL \_ MAP1 \_ TEXTURE \_ COORD \_ 1 | Se habilitada, as chamadas **para glEvalCoord1**, **glEvalMesh1** e **glEvalPoint1** geram *as coordenadas de* textura. Consulte também **glMap1**.                                                                                                                         |
| GL \_ MAP1 \_ TEXTURE \_ COORD \_ 2 | Se habilitada, chamadas [**para glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md)e [**glEvalPoint1**](glevalpoint.md) geram *coordenadas* de textura s e *t.* Consulte também [**glMap1**](glmap1.md).                       |
| GL \_ MAP1 \_ TEXTURE \_ COORD \_ 3 | Se habilitada, as chamadas **para glEvalCoord1**, **glEvalMesh1** e **glEvalPoint1** geram coordenadas de textura *s,* *t* e *r.* Consulte também **glMap1**.                                                                                                           |
| GL \_ MAP1 \_ TEXTURE \_ COORD \_ 4 | Se habilitada, chamadas [para glEvalCoord1](glevalcoord-functions.md), [glEvalMesh1](glevalmesh-functions.md)e [**glEvalPoint1**](glevalpoint.md) geram *s*, *t*, *r* e coordenadas de textura *q.* Consulte também [**glMap1**](glmap1.md).                    |
| GL \_ MAP1 \_ VÉRTICE \_ 3         | Se habilitada, chamadas para **glEvalCoord1**, **glEvalMesh1** e **glEvalPoint1** geram *coordenadas* de vértice x , *y* e *z.* Consulte também **glMap1**.                                                                                                            |
| MAP1 do GL de \_ \_ vértice \_ 4         | Se habilitada, as chamadas para [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md)e [**glEvalPoint1**](glevalpoint.md) geram coordenadas de vértice *x*, *y*, *z* e *w* homogêneos. Consulte também [**glMap1**](glmap1.md). |
| GL \_ map2 \_ cor \_ 4          | Se habilitada, as chamadas para [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md)e [**glEvalPoint2**](glevalpoint.md) geram valores RGBA. Consulte também [**glMap2**](glmap2.md).                                           |
| \_Índice map2 \_ GL             | Se habilitada, as chamadas para **glEvalCoord2**, **glEvalMesh2** e **glEvalPoint2** geram índices de cores. Consulte também **glMap2**.                                                                                                                                   |
| GL \_ map2 \_ normal            | Se habilitada, as chamadas para [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md)e [**glEvalPoint2**](glevalpoint.md) geram Normals. Consulte também [**glMap2**](glmap2.md).                                               |
| GL \_ map2 \_ Texture \_ coord \_ 1 | Se habilitada, as chamadas para **glEvalCoord2**, **glEvalMesh2** e **glEvalPoint2** geram coordenadas de textura *s* . Consulte também **glMap2**.                                                                                                                         |
| GL \_ map2 \_ Texture \_ coord \_ 2 | Se habilitada, as chamadas para [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md)e [**glEvalPoint2**](glevalpoint.md) geram coordenadas de textura *s* e *t* . Consulte também [**glMap2**](glmap2.md).                       |
| GL \_ map2 \_ Texture \_ coord \_ 3 | Se habilitada, as chamadas para **glEvalCoord2**, **glEvalMesh2** e **glEvalPoint2** geram coordenadas de textura *s*, *t* e *r* . Consulte também **glMap2**.                                                                                                           |
| GL \_ map2 \_ Texture \_ coord \_ 4 | Se habilitada, as chamadas para [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md)e [**glEvalPoint2**](glevalpoint.md) geram coordenadas *s*, *t*, *r* e *q* Texture. Consulte também [**glMap2**](glmap2.md).            |
| GL \_ map2 \_ Vertex \_ 3         | Se habilitada, as chamadas para **glEvalCoord2**, **glEvalMesh2** e **glEvalPoint2** geram coordenadas de vértice *x*, *y* e *z* . Consulte também **glMap2**.                                                                                                            |
| Map2 do GL de \_ \_ vértice \_ 4         | Se habilitada, as chamadas para [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md)e [**glEvalPoint2**](glevalpoint.md) geram coordenadas de vértice *x*, *y*, *z* e *w* homogêneos. Consulte também [**glMap2**](glmap2.md). |
| \_NORMALIZE GL               | Se habilitado, os vetores normais especificados com **glNormal** serão dimensionados para o comprimento da unidade após a transformação. Consulte [**glNormal**](glnormal-functions.md).                                                                                                          |
| \_simples ponto \_ GL           | Se habilitado, desenhe pontos com a filtragem correta. Se desabilitado, desenhe pontos com alias. Consulte [**glPointSize**](glpointsize.md).                                                                                                                                    |
| \_preenchimento de \_ deslocamento do polígono GL \_   | Se habilitado, e se o polígono for renderizado no \_ modo de preenchimento GL, um deslocamento será adicionado aos valores de profundidade dos fragmentos de um polígono antes da execução da comparação de profundidade. Consulte [**glPolygonOffset**](glpolygonoffset.md)**.**                                      |
| \_linha de \_ deslocamento do polígono GL \_   | Se habilitado, e se o polígono for renderizado no \_ modo de linha gl, um deslocamento será adicionado aos valores de profundidade dos fragmentos de um polígono antes da execução da comparação de profundidade. Consulte **glPolygonOffset**.                                                                 |
| \_ponto de \_ deslocamento do polígono GL \_  | Se habilitada, um deslocamento será adicionado aos valores de profundidade dos fragmentos de um polígono antes que a comparação de profundidade seja executada, se o polígono for renderizado no \_ modo de ponto GL. Consulte [**glPolygonOffset**](glpolygonoffset.md).                                             |
| \_suavização do polígono GL \_         | Se habilitado, desenhe polígonos com a filtragem adequada. Se desabilitado, desenhe polígonos com alias. Consulte [**glPolygonMode**](glpolygonmode.md).                                                                                                                            |
| polígono do GL \_ \_ STIPPLE        | Se habilitada, use o padrão Stipple Polygon atual ao renderizar polígonos. Consulte [**glPolygonStipple**](glpolygonstipple.md).                                                                                                                              |
| \_teste de tesoura do GL \_           | Se habilitado, descarte os fragmentos que estão fora do retângulo da mola. Consulte [**glScissor**](glscissor.md).                                                                                                                                                   |
| \_teste de estêncil GL \_           | Se habilitada, faça o teste do estêncil e atualize o buffer do estêncil. Consulte [**glStencilFunc**](glstencilfunc.md) e [**glStencilOp**](glstencilop.md).                                                                                                            |
| Somente \_ textura GL \_ 1D             | Se habilitado, o texturing unidimensional será executado (a menos que texturing bidimensional também esteja habilitado). Consulte [**glTexImage1D**](glteximage1d.md).                                                                                                            |
| A \_ textura GL \_ 2D             | Se habilitado, o texturing bidimensional será executado. Consulte [**glTexImage2D**](glteximage2d.md).                                                                                                                                                               |
| GL \_ Texture \_ Gen \_ Q         | Se habilitada, a coordenada de textura *q* é computada usando a função de geração de textura definida com [**glTexGen**](gltexgen-functions.md). Caso contrário, a coordenada de textura *q* atual será usada.                                                        |
| o GL de \_ Texture \_ Gen \_ R         | Se habilitada, a coordenada de textura do *r* é computada usando a função de geração de textura definida com [**glTexGen**](gltexgen-functions.md). Se desabilitado, a coordenada de textura do *r* atual será usada.                                                      |
| S do GL \_ Texture \_ Gen \_         | Se habilitada, a coordenada de textura *s* é computada usando a função de geração de textura definida com **glTexGen**. Se desabilitado, a coordenada de textura *s* atual será usada.                                                                                |
| \_geração de textura de Texture GL \_ \_         | Se habilitada, a coordenada de textura *t* é computada usando a função de geração de textura definida com [**glTexGen**](gltexgen-functions.md). Se desabilitado, a coordenada de textura *t* atual será usada.                                                      |



 

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

[**glAlphaFunc**](glalphafunc.md)
</dt> <dt>

[**glArrayElement**](glarrayelement.md)
</dt> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glBlendFunc**](glblendfunc.md)
</dt> <dt>

[**glClipPlane**](glclipplane.md)
</dt> <dt>

[**glColorMaterial**](glcolormaterial.md)
</dt> <dt>

[**glColorPointer**](glcolorpointer.md)
</dt> <dt>

[**glCullFace**](glcullface.md)
</dt> <dt>

[**glDepthFunc**](gldepthfunc.md)
</dt> <dt>

[**glDepthRange**](gldepthrange.md)
</dt> <dt>

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glEvalCoord1**](glevalcoord-functions.md)
</dt> <dt>

[**glEvalMesh1**](glevalmesh-functions.md)
</dt> <dt>

[**glEvalPoint1**](glevalpoint.md)
</dt> <dt>

[**glFog**](glfog.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glLight**](gllight-functions.md)
</dt> <dt>

[**glLightModel**](gllightmodel-functions.md)
</dt> <dt>

[**glLineWidth**](gllinewidth.md)
</dt> <dt>

[**glLineStipple**](gllinestipple.md)
</dt> <dt>

[**glLogicOp**](gllogicop.md)
</dt> <dt>

[**glMap1**](glmap1.md)
</dt> <dt>

[**glMap2**](glmap2.md)
</dt> <dt>

[**glMaterial**](glmaterial-functions.md)
</dt> <dt>

[**glNormal**](glnormal-functions.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glPointSize**](glpointsize.md)
</dt> <dt>

[**glPolygonMode**](glpolygonmode.md)
</dt> <dt>

[**glPolygonStipple**](glpolygonstipple.md)
</dt> <dt>

[**glScissor**](glscissor.md)
</dt> <dt>

[**glStencilFunc**](glstencilfunc.md)
</dt> <dt>

[**glStencilOp**](glstencilop.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glTexGen**](gltexgen-functions.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> </dl>

 

 





