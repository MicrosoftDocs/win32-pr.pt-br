---
title: função glDisable (GL. h)
description: As funções glEnable e glDisable habilitam ou desabilitam os recursos do OpenGL. | função glDisable (GL. h)
ms.assetid: 094f730e-5e2b-485e-8d9d-fee2902d3d5f
keywords:
- função glDisable OpenGL
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
ms.openlocfilehash: eff5c12e53eb060777f75ad537bed265401a7a26
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105761408"
---
# <a name="gldisable-function"></a>função glDisable

As funções [**glEnable**](glenable.md) e **glDisable** habilitam ou desabilitam os recursos do OpenGL.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glDisable(
   GLenum cap
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*extremidade* 
</dt> <dd>

Uma constante simbólica que indica um recurso OpenGL.

Para obter uma discussão sobre os valores que o *limite* pode tomar, consulte a seção de comentários a seguir.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Name                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | *Cap* não era um dos valores listados na seção de comentários anterior.<br/>                                                   |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

As funções [**glEnable**](glenable.md) e **glDisable** habilitam e desabilitam vários recursos gráficos OpenGL. Use [**glIsEnabled**](glisenabled.md) ou [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) para determinar a configuração atual de qualquer recurso.

[**GlEnable**](glenable.md) e **glDisable** usam um único argumento, *Cap*, que pode assumir um dos seguintes valores:



| Valor                       | Significado                                                                                                                                                                                                                                                     |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_teste de alfa do GL \_             | Se habilitada, faça testes alfa. Consulte [**glAlphaFunc**](glalphafunc.md).                                                                                                                                                                                       |
| GL \_ automático \_ normal            | Se habilitada, os vetores normais da superfície de computação são analíticos de forma analítica quando o GL \_ map2 \_ Vertex \_ 3 ou GL \_ map2 \_ Vertex \_ 4 gerou vértices. Consulte [**glMap2**](glmap2.md).                                                                                        |
| a \_ combinação GL                   | Se habilitado, misture os valores de cor RGBA de entrada com os valores nos buffers de cor. Consulte [**glBlendFunc**](glblendfunc.md).                                                                                                                              |
| Recorte de \_ \_ plano GL *i*          | Se habilitada, cortar a geometria em relação ao plano de recorte definido pelo usuário *i*. Consulte [**glClipPlane**](glclipplane.md).                                                                                                                                                  |
| \_ \_ operação lógica de cores GL \_        | Se habilitada, aplique a operação lógica atual aos valores de cor e buffer de cor RGBA de entrada. Consulte [**glLogicOp**](gllogicop.md).                                                                                                                     |
| \_material de cor GL \_         | Se habilitada, um ou mais parâmetros de material acompanharão a cor atual. Consulte [**glColorMaterial**](glcolormaterial.md).                                                                                                                                   |
| \_face de seleção GL \_              | Se habilitada, a seleção de polígonos com base em seu enrolamento nas coordenadas da janela. Consulte [**glCullFace**](glcullface.md).                                                                                                                                               |
| \_teste de profundidade GL \_             | Se habilitada, faça comparações de profundidade e atualize o buffer de profundidade. Consulte [**glDepthFunc**](gldepthfunc.md) e [**glDepthRange**](gldepthrange.md).                                                                                                              |
| \_pontilhamento GL                  | Se habilitado, os componentes ou índices de cores de pontilhamento antes de serem gravados no buffer de cores.                                                                                                                                                                 |
| neblina do GL \_                     | Se habilitada, misture uma cor de neblina para a cor texturing. Consulte [**glFog**](glfog.md).                                                                                                                                                                    |
| \_ \_ op lógico de índice GL \_        | Se habilitada, aplique a operação lógica atual aos índices de entrada de índice e buffer de cores. Consulte [**glLogicOp**](gllogicop.md).                                                                                                                         |
| GL \_ claro *i*                | Se habilitada, inclua a luz *i* na avaliação da equação de iluminação. Consulte [**glLightModel**](gllightmodel-functions.md) e [**glLight**](gllight-functions.md).                                                                                      |
| \_iluminação GL                | Se habilitada, use os parâmetros de iluminação atuais para computar a cor ou o índice do vértice. Se desabilitado, associe a cor ou o índice atual a cada vértice. Consulte [**glMaterial**](glmaterial-functions.md), **glLightModel** e **glLight**.                |
| linha do GL \_ \_ Smooth            | Se habilitada, desenhe linhas com a filtragem correta. Se desabilitado, desenhe linhas com alias. Consulte [**glLineWidth**](gllinewidth.md).                                                                                                                                     |
| \_STIPPLE de linha gl \_           | Se habilitada, use o padrão de Stipple de linha atual ao desenhar linhas. Consulte [**glLineStipple**](gllinestipple.md).                                                                                                                                            |
| \_op lógico \_ GL               | Se habilitada, aplique a operação lógica selecionada no momento aos índices de entrada e de buffer de cores. Consulte [**glLogicOp**](gllogicop.md).                                                                                                                    |
| GL \_ MAP1 \_ cor \_ 4          | Se habilitada, as chamadas para [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md)e [**glEvalPoint1**](glevalpoint.md) geram valores RGBA. Consulte também [**glMap1**](glmap1.md).                                           |
| \_Índice MAP1 \_ GL             | Se habilitada, as chamadas para **glEvalCoord1**, **glEvalMesh1** e **glEvalPoint1** geram índices de cores. Consulte também **glMap1**.                                                                                                                                   |
| GL \_ MAP1 \_ normal            | Se habilitada, as chamadas para [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md)e [**glEvalPoint1**](glevalpoint.md) geram Normals. Consulte também [**glMap1**](glmap1.md).                                               |
| GL \_ MAP1 \_ Texture \_ coord \_ 1 | Se habilitada, as chamadas para **glEvalCoord1**, **glEvalMesh1** e **glEvalPoint1** geram coordenadas de textura *s* . Consulte também **glMap1**.                                                                                                                         |
| GL \_ MAP1 \_ Texture \_ coord \_ 2 | Se habilitada, as chamadas para [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md)e [**glEvalPoint1**](glevalpoint.md) geram coordenadas de textura *s* e *t* . Consulte também [**glMap1**](glmap1.md).                       |
| GL \_ MAP1 \_ Texture \_ coord \_ 3 | Se habilitada, as chamadas para **glEvalCoord1**, **glEvalMesh1** e **glEvalPoint1** geram coordenadas de textura *s*, *t* e *r* . Consulte também **glMap1**.                                                                                                           |
| GL \_ MAP1 \_ Texture \_ coord \_ 4 | Se habilitada, as chamadas para [glEvalCoord1](glevalcoord-functions.md), [glEvalMesh1](glevalmesh-functions.md)e [**glEvalPoint1**](glevalpoint.md) geram coordenadas *s*, *t*, *r* e *q* Texture. Consulte também [**glMap1**](glmap1.md).                    |
| GL \_ MAP1 \_ Vertex \_ 3         | Se habilitada, as chamadas para **glEvalCoord1**, **glEvalMesh1** e **glEvalPoint1** geram coordenadas de vértice *x*, *y* e *z* . Consulte também **glMap1**.                                                                                                            |
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

 

 





