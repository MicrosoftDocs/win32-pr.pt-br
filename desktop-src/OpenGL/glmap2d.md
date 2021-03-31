---
title: Função glMap2d (Gl.h)
description: A função glMap2d define um avaliador bidimensional. | função glMap2d (GL. h)
ms.assetid: d8645d19-bec1-4efd-a657-6e7d52d706a9
keywords:
- função glMap2d OpenGL
topic_type:
- apiref
api_name:
- glMap2d
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e072635c411c7a3e28977316c388a9b1597fcd1f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172628"
---
# <a name="glmap2d-function"></a>função glMap2d

As funções **glMap2d** e [**glMap2f**](glmap2f.md) definem um avaliador bidimensional.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glMap2d(
         GLenum   target,
         GLdouble u1,
         GLdouble u2,
         GLint    ustride,
         GLint    uorder,
         GLdouble v1,
         GLdouble v2,
         GLint    vstride,
         GLint    vorder,
   const GLdouble *points
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*destino* 
</dt> <dd>

O tipo de valores que são gerados pelo avaliador. As constantes simbólicas a seguir são aceitas.



| Valor                                                                                                                                                                                          | Significado                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_MAP2_VERTEX_3"></span><span id="gl_map2_vertex_3"></span><dl> <dt>**GL \_ map2 \_ Vertex \_ 3**</dt> </dl>                       | Cada ponto de controle é de três valores de ponto flutuante que representam *x, y* e *z*. Comandos internos do [**glVertex3**](glvertex-functions.md) são gerados quando o mapa é avaliado.<br/>                                                                                                                                         |
| <span id="GL_MAP2_VERTEX_4"></span><span id="gl_map2_vertex_4"></span><dl> <dt>**Map2 do GL de \_ \_ vértice \_ 4**</dt> </dl>                       | Cada ponto de controle é de quatro valores de ponto flutuante que representam *x, y, z* e *w*. Comandos internos do [**glVertex4**](glvertex-functions.md) são gerados quando o mapa é avaliado.<br/>                                                                                                                                       |
| <span id="GL_MAP2_INDEX"></span><span id="gl_map2_index"></span><dl> <dt>**\_Índice map2 \_ GL**</dt> </dl>                                 | Cada ponto de controle é um único valor de ponto flutuante que representa um índice de cor. Comandos internos do [**glIndex**](glindex-functions.md) são gerados quando o mapa é avaliado. No entanto, o índice atual não é atualizado com o valor desses comandos **glIndex** .<br/>                                                    |
| <span id="GL_MAP2_COLOR_4"></span><span id="gl_map2_color_4"></span><dl> <dt>**GL \_ map2 \_ cor \_ 4**</dt> </dl>                          | Cada ponto de controle é de quatro valores de ponto flutuante que representam vermelho, verde, azul e alfa. Comandos internos do [**glColor4**](glcolor-functions.md) são gerados quando o mapa é avaliado. No entanto, a cor atual não é atualizada com o valor desses comandos **glColor4** .<br/>                                       |
| <span id="GL_MAP2_NORMAL"></span><span id="gl_map2_normal"></span><dl> <dt>**GL \_ map2 \_ normal**</dt> </dl>                              | Cada ponto de controle é de três valores de ponto flutuante que representam os componentes *x, y* e *z* de um vetor normal. Comandos internos do [**glNormal**](glnormal-functions.md) são gerados quando o mapa é avaliado. No entanto, o normal atual não é atualizado com o valor desses comandos **glNormal** .<br/>              |
| <span id="GL_MAP2_TEXTURE_COORD_1"></span><span id="gl_map2_texture_coord_1"></span><dl> <dt>**GL \_ map2 \_ Texture \_ coord \_ 1**</dt> </dl> | Cada ponto de controle é um único valor de ponto flutuante que representa a coordenada de textura *s* . Comandos internos do [**glTexCoord1**](gltexcoord-functions.md) são gerados quando o mapa é avaliado. No entanto, as coordenadas de textura atuais não são atualizadas com o valor desses comandos **glTexCoord** .<br/>              |
| <span id="GL_MAP2_TEXTURE_COORD_2"></span><span id="gl_map2_texture_coord_2"></span><dl> <dt>**GL \_ map2 \_ Texture \_ coord \_ 2**</dt> </dl> | Cada ponto de controle é dois valores de ponto flutuante que representam as coordenadas de textura *s* e *t* . Comandos internos do [**glTexCoord2**](gltexcoord-functions.md) são gerados quando o mapa é avaliado. No entanto, as coordenadas de textura atuais não são atualizadas com o valor desses comandos **glTexCoord** .<br/>         |
| <span id="GL_MAP2_TEXTURE_COORD_3"></span><span id="gl_map2_texture_coord_3"></span><dl> <dt>**GL \_ map2 \_ Texture \_ coord \_ 3**</dt> </dl> | Cada ponto de controle é de três valores de ponto flutuante que representam as coordenadas de textura *s, t* e *r* . Comandos internos do [**glTexCoord3**](gltexcoord-functions.md) são gerados quando o mapa é avaliado. No entanto, as coordenadas de textura atuais não são atualizadas com o valor desses comandos **glTexCoord** .<br/>   |
| <span id="GL_MAP2_TEXTURE_COORD_4"></span><span id="gl_map2_texture_coord_4"></span><dl> <dt>**GL \_ map2 \_ Texture \_ coord \_ 4**</dt> </dl> | Cada ponto de controle é de quatro valores de ponto flutuante que representam as coordenadas *s, t, r* e *q* Texture. Comandos internos do [**glTexCoord4**](gltexcoord-functions.md) são gerados quando o mapa é avaliado. No entanto, as coordenadas de textura atuais não são atualizadas com o valor desses comandos **glTexCoord** .<br/> |



 

</dd> <dt>

*U1* 
</dt> <dd>

Um mapeamento linear de *u*, conforme apresentado a [**glEvalCoord2**](glevalcoord-functions.md), a *u*^, uma das duas variáveis que é avaliada pelas equações especificadas por esse comando.

</dd> <dt>

*U2* 
</dt> <dd>

Um mapeamento linear de *u*, conforme apresentado a [**glEvalCoord2**](glevalcoord-functions.md), a *u*^, uma das duas variáveis que é avaliada pelas equações especificadas por esse comando.

</dd> <dt>

*ustride* 
</dt> <dd>

O número de floats ou duplos entre o início do ponto de controle **r** *IJ* e o início do ponto de controle **r** <sub>(i + 1 \) \ j</sub>, em que *i* e *j* são os índices de ponto de controle *u* e *v* , respectivamente. Isso permite que os pontos de controle sejam inseridos em estruturas de dados arbitrárias. A única restrição é que os valores de um ponto de controle específico devem ocupar locais de memória contíguos.

</dd> <dt>

*uorder* 
</dt> <dd>

A dimensão da matriz do ponto de controle no eixo *u*. Deve ser positivo.

</dd> <dt>

*v1* 
</dt> <dd>

Um mapeamento linear de *v*, conforme apresentado a [**glEvalCoord2**](glevalcoord-functions.md), a *v*^, uma das duas variáveis que é avaliada pelas equações especificadas por esse comando.

</dd> <dt>

*v2* 
</dt> <dd>

Um mapeamento linear de *v*, conforme apresentado a [**glEvalCoord2**](glevalcoord-functions.md), a *v*^, uma das duas variáveis que é avaliada pelas equações especificadas por esse comando.

</dd> <dt>

*vstride* 
</dt> <dd>

O número de floats ou duplos entre o início do ponto de controle **r** *IJ* e o início do ponto de controle **r** <sub>i (j \ + 1 \)</sub>, em que *i* e *j* são os índices de ponto de controle *u* e *v* , respectivamente. Isso permite que os pontos de controle sejam inseridos em estruturas de dados arbitrárias. A única restrição é que os valores de um ponto de controle específico devem ocupar locais de memória contíguos.

</dd> <dt>

*vorder* 
</dt> <dd>

A dimensão da matriz do ponto de controle no eixo *v*. Deve ser positivo.

</dd> <dt>

*pontos* 
</dt> <dd>

Um ponteiro para a matriz de pontos de controle.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Name                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | o *destino* não era um valor aceito.<br/>                                                                                        |
| <dl> <dt>**\_valor inválido do GL \_**</dt> </dl>     | *U1* era igual a *U2*, ou *v1* era igual a *v2*.<br/>                                                                         |
| <dl> <dt>**\_valor inválido do GL \_**</dt> </dl>     | *Ustride* ou *vstride* era menor que o número de valores em um ponto de controle.<br/>                                       |
| <dl> <dt>**\_valor inválido do GL \_**</dt> </dl>     | *Uorder* ou *Vorder* foi menor que uma ou GL \_ Max \_ eval \_ Order.<br/>                                                     |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

Os avaliadores fornecem uma maneira de usar o mapeamento polinomial polinomial ou racional para produzir vértices, normais, coordenadas de textura e cores. Os valores produzidos por um avaliador são enviados para outros estágios do processamento do OpenGL como se tivessem sido apresentados usando os comandos [**glVertex**](glvertex-functions.md), [**glNormal**](glnormal-functions.md), [**glTexCoord**](gltexcoord-functions.md)e [**glColor**](glcolor-functions.md) , exceto que os valores gerados não atualizam o normal atual, as coordenadas de textura ou a cor.

Todas as próprias linhas polinomiais polinomiais ou lógicas de qualquer grau (até o grau máximo com suporte pela implementação OpenGL) podem ser descritas usando avaliadores. Isso inclui quase todas as superfícies usadas em gráficos de computador, incluindo superfícies B-spline, superfícies NURBS, superfícies de Bézier e assim por diante.

Os avaliadores definem superfícies baseadas em bivariable Bernstein polinomiais. Definir **p** (*u*^,*v*^) como

![Equação mostrando a definição de p ().](images/map05.png)

em que **R** *IJ* é um ponto de controle, () *é o Bernstein* polinomial de grau

*n* (*uorder*  =  *n* + 1)

![Equação mostrando o Bernstein polinomial do grau n.](images/map06.png)

and () é o Bernstein de *j* º do grau *m* (*Vorder*  =  *m* + 1)

![Equação mostrando o Bernstein polinomial do grau m.](images/map07.png)

Lembre-se de que

![Equações mostrando equivalência para 1.](images/map08.png)

A função **glMap2** é usada para definir a base e especificar que tipo de valores são produzidos. Uma vez definido, um mapa pode ser habilitado e desabilitado chamando [**glEnable**](glenable.md) e **glDisable** com o nome do mapa, um dos nove valores predefinidos para *destino*, descritos acima. Quando [**glEvalCoord2**](glevalcoord-functions.md) apresenta os valores *u* e *v*, a bivariant Bernstein polinomiais são avaliadas usando *u*^ e *v*^, em que

![Equação mostrando a definição de você ^.](images/map09.png)

e

![Equação mostrando a definição de v ^.](images/map10.png)

O parâmetro de *destino* é uma constante simbólica que indica que tipo de pontos de controle são fornecidos em *pontos* e qual saída é gerada quando o mapa é avaliado.

Os parâmetros *ustride*, *uorder*, *vstride*, *Vorder* e *Points* definem o endereçamento de matriz para acessar os pontos de controle. O parâmetro *Points* é o local do primeiro ponto de controle, que ocupa um, dois, três ou quatro locais de memória contíguos, dependendo de qual mapa está sendo definido. Há pontos de controle *uorder* x *Vorder* na matriz. O parâmetro *ustride* informa quantos locais flutuantes ou duplos são ignorados para avançar o ponteiro de memória interna do ponto de controle **r** *IJ* para o ponto de controle **r** <sub>(\ + 1 \) j</sub>. O parâmetro *vstride* informa quantos locais flutuantes ou duplos são ignorados para avançar o ponteiro de memória interna do ponto de controle **r** *IJ* para o ponto de controle **r**<sub>i (j \ + 1 \)</sub>.

Como é o caso com todos os comandos OpenGL que aceitam ponteiros para os dados, é como se o conteúdo dos *pontos* fosse copiado por **glMap2** antes de ser retornado. As alterações no conteúdo de *pontos* não têm efeito depois que **glMap2** é chamado.

As funções a seguir recuperam informações relacionadas ao **glMap2**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ Max \_ eval \_ Order

[**glGetMap**](glgetmap.md)

[**glIsEnabled**](glisenabled.md) com Argument GL \_ map2 \_ vértice \_ 3

**glIsEnabled** com Argument GL \_ map2 \_ vértice \_ 4

índice de **glIsEnabled** com Argument GL \_ map2 \_

**glIsEnabled** com Argument GL \_ map2 \_ cor \_ 4

**glIsEnabled** com Argument GL \_ map2 \_ normal

**glIsEnabled** com Argument GL \_ map2 \_ Texture \_ coord \_ 1

**glIsEnabled** com Argument GL \_ map2 \_ Texture \_ coord \_ 2

**glIsEnabled** com Argument GL \_ map2 \_ Texture \_ coord \_ 3

**glIsEnabled** com Argument GL \_ map2 \_ Texture \_ coord \_ 4

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

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glEvalCoord**](glevalcoord-functions.md)
</dt> <dt>

[**glEvalMesh**](glevalmesh-functions.md)
</dt> <dt>

[**glEvalPoint**](glevalpoint.md)
</dt> <dt>

[**glMap1**](glmap1.md)
</dt> <dt>

[**glMapGrid**](glmapgrid-functions.md)
</dt> <dt>

[**glNormal**](glnormal-functions.md)
</dt> <dt>

[**glTexCoord**](gltexcoord-functions.md)
</dt> <dt>

[**glVertex**](glvertex-functions.md)
</dt> </dl>

 

 





