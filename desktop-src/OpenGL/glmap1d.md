---
title: Função glMap1d (Gl.h)
description: A função glMap1d define um avaliador unidimensional. | Função glMap1d (Gl.h)
ms.assetid: 65f8b099-597c-4300-a7d1-3dabdd19e6cb
keywords:
- Função glMap1d OpenGL
topic_type:
- apiref
api_name:
- glMap1d
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90f1d17312cae14da955641d0009235a45fa23e65a3a04e35f692a4bb5418722
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119520426"
---
# <a name="glmap1d-function"></a>Função glMap1d

As **funções glMap1d** e [**glMap1f**](glmap1f.md) definem um avaliador unidimensional.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glMap1d(
         GLenum   target,
         GLdouble u1,
         GLdouble u2,
         GLint    stride,
         GLint    order,
   const GLdouble *points
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*destino* 
</dt> <dd>

O tipo de valores gerados pelo avaliador. Constantes simbólicas. O *parâmetro* de destino é uma constante simbólica que indica que tipo de pontos de controle são fornecidos nos pontos *e* qual saída é gerada quando o mapa é avaliado. Ele pode assumir um dos nove valores predefinidos.



| Valor                                                                                                                                                                                          | Significado                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_MAP1_VERTEX_3"></span><span id="gl_map1_vertex_3"></span><dl> <dt>**GL \_ MAP1 \_ VÉRTICE \_ 3**</dt> </dl>                       | Cada ponto de controle é três valores de ponto flutuante que *representam x, y* e *z.* Comandos [**glVertex3**](glvertex-functions.md) internos são gerados quando o mapa é avaliado.<br/>                                                                                                                                         |
| <span id="GL_MAP1_VERTEX_4"></span><span id="gl_map1_vertex_4"></span><dl> <dt>**GL \_ MAP1 \_ VÉRTICE \_ 4**</dt> </dl>                       | Cada ponto de controle é quatro valores de ponto flutuante que *representam x, y, z* e *w*. Comandos [**glVertex4**](glvertex-functions.md) internos são gerados quando o mapa é avaliado.<br/>                                                                                                                                       |
| <span id="GL_MAP1_INDEX"></span><span id="gl_map1_index"></span><dl> <dt>**GL \_ MAP1 \_ INDEX**</dt> </dl>                                 | Cada ponto de controle é um único valor de ponto flutuante que representa um índice de cores. Comandos [**glIndex**](glindex-functions.md) internos são gerados quando o mapa é avaliado. No entanto, o índice atual não é atualizado com o valor desses **comandos glIndex.**<br/>                                                    |
| <span id="GL_MAP1_COLOR_4"></span><span id="gl_map1_color_4"></span><dl> <dt>**GL \_ MAP1 \_ COR \_ 4**</dt> </dl>                          | Cada ponto de controle é quatro valores de ponto flutuante que representam vermelho, verde, azul e alfa. Comandos [**glColor4**](glcolor-functions.md) internos são gerados quando o mapa é avaliado. No entanto, a cor atual não é atualizada com o valor desses **comandos glColor4.**<br/>                                       |
| <span id="GL_MAP1_NORMAL"></span><span id="gl_map1_normal"></span><dl> <dt>**GL \_ MAP1 \_ NORMAL**</dt> </dl>                              | Cada ponto de controle é três valores de ponto flutuante que representam os *componentes x, y* e *z* de um vetor normal. Comandos [**glNormal**](glnormal-functions.md) internos são gerados quando o mapa é avaliado. No entanto, o normal atual não é atualizado com o valor desses **comandos glNormal.**<br/>              |
| <span id="GL_MAP1_TEXTURE_COORD_1"></span><span id="gl_map1_texture_coord_1"></span><dl> <dt>**GL \_ MAP1 \_ TEXTURE \_ COORD \_ 1**</dt> </dl> | Cada ponto de controle é um único valor de ponto flutuante que representa a *coordenada de* textura. Comandos [**glTexCoord1**](gltexcoord-functions.md) internos são gerados quando o mapa é avaliado. No entanto, as coordenadas de textura atuais não são atualizadas com o valor desses **comandos glTexCoord.**<br/>              |
| <span id="GL_MAP1_TEXTURE_COORD_2"></span><span id="gl_map1_texture_coord_2"></span><dl> <dt>**GL \_ MAP1 \_ TEXTURE \_ COORD \_ 2**</dt> </dl> | Cada ponto de controle é dois valores de ponto flutuante que representam as *coordenadas* de textura s e *t.* Comandos [**glTexCoord2**](gltexcoord-functions.md) internos são gerados quando o mapa é avaliado. No entanto, as coordenadas de textura atuais não são atualizadas com o valor desses **comandos glTexCoord.**<br/>         |
| <span id="GL_MAP1_TEXTURE_COORD_3"></span><span id="gl_map1_texture_coord_3"></span><dl> <dt>**GL \_ MAP1 \_ TEXTURE \_ COORD \_ 3**</dt> </dl> | Cada ponto de controle é três valores de ponto flutuante que representam as coordenadas de textura *s, t* e *r.* Comandos [**glTexCoord3**](gltexcoord-functions.md) internos são gerados quando o mapa é avaliado. No entanto, as coordenadas de textura atuais não são atualizadas com o valor desses **comandos glTexCoord.**<br/>   |
| <span id="GL_MAP1_TEXTURE_COORD_4"></span><span id="gl_map1_texture_coord_4"></span><dl> <dt>**GL \_ MAP1 \_ TEXTURE \_ COORD \_ 4**</dt> </dl> | Cada ponto de controle é quatro valores de ponto flutuante que representam as coordenadas de textura *s, t, r* e *q.* Comandos [**glTexCoord4**](gltexcoord-functions.md) internos são gerados quando o mapa é avaliado. No entanto, as coordenadas de textura atuais não são atualizadas com o valor desses **comandos glTexCoord.**<br/> |



 

</dd> <dt>

*u1* 
</dt> <dd>

Um mapeamento linear de *u*, conforme apresentado a [**glEvalCoord1**](glevalcoord-functions.md), para *u*^, a variável que é avaliada pelas equações especificadas por este comando.

</dd> <dt>

*u2* 
</dt> <dd>

Um mapeamento linear de *u*, conforme apresentado a [**glEvalCoord1**](glevalcoord-functions.md), para *u*^, a variável que é avaliada pelas equações especificadas por este comando.

</dd> <dt>

*Passo* 
</dt> <dd>

O número de floats ou doubles entre o início de um ponto de controle e o início do próximo na estrutura de dados referenciada nos *pontos*. Isso permite que os pontos de controle sejam inseridos em estruturas de dados arbitrárias. A única restrição é que os valores de um ponto de controle específico devem ocupar locais de memória contígua.

</dd> <dt>

*order* 
</dt> <dd>

O número de pontos de controle. Deve ser positivo.

</dd> <dt>

*pontos* 
</dt> <dd>

Um ponteiro para a matriz de pontos de controle.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela [**função glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *target* não era um valor aceito.<br/>                                                                                        |
| <dl> <dt>**VALOR INVÁLIDO DE GL \_ \_**</dt> </dl>     | *u1* era igual a *u2*.<br/>                                                                                                    |
| <dl> <dt>**VALOR INVÁLIDO DE GL \_ \_**</dt> </dl>     | *stride* era menor que o número de valores em um ponto de controle.<br/>                                                            |
| <dl> <dt>**VALOR INVÁLIDO DE GL \_ \_**</dt> </dl>     | *order* era menor que um ou GL \_ MAX \_ EVAL \_ ORDER.<br/>                                                                         |
| <dl> <dt>**OPERAÇÃO \_ GL \_ INVÁLIDA**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd.**](glend.md)<br/> |



## <a name="remarks"></a>Comentários

Os avaliadores fornecem uma maneira de usar o mapeamento polinomial ou racional polinomial para produzir vértices, normais, coordenadas de textura e cores. Os valores produzidos por um avaliador são enviados para estágios posteriores do processamento do OpenGL, assim como se eles tivessem sido apresentados usando os comandos [**glVertex**](glvertex-functions.md), [**glNormal**](glnormal-functions.md), [**glTexCoord**](gltexcoord-functions.md)e [**glColor,**](glcolor-functions.md) exceto que os valores gerados não atualizam o normal atual, as coordenadas de textura ou a cor.

Todos os splines polinomial ou racional de qualquer grau (até o grau máximo suportado pela implementação do OpenGL) podem ser descritos usando avaliadores. Isso inclui quase todos os splines usados em elementos gráficos de computador, incluindo B-splines, curvas de Bezier, splines de Hermite e assim por diante.

Os avaliadores definem curvas com base em polinomials DeIa. Definir **p** () como

![Equação mostrando a definição de p ().](images/map01.png)

em **que R**_i_ é um ponto de controle e () é o *i* o polynomial DeIa de grau *n* (*ordem*  = *n* + 1):

![Equação mostrando o polinomial DeIa de grau n.](images/map02.png)

Lembre-se de que

![Equações mostrando equivalência para 1.](images/map03.png)

A **função glMap1** é usada para definir a base e especificar que tipo de valores são produzidos. Depois de definido, um mapa pode ser habilitado e desabilitado chamando [**glEnable**](glenable.md) e **glDisable** com o nome do mapa, um dos nove valores predefinidos para o destino *descrito* acima. A [função glEvalCoord1](glevalcoord-functions.md) avalia os mapas unidimensionais habilitados. Quando **glEvalCoord1 apresenta** um valor *u*, as funções DeIa são avaliadas usando *u*^, em que

![Equação mostrando a definição de you^.](images/map04.png)

Os *parâmetros stride*, *order* e *points* definem o endereçamento de matriz para acessar os pontos de controle. O *parâmetro points* é o local do primeiro ponto de controle, que ocupa um, dois, três ou quatro locais de memória contígua, dependendo de qual mapa está sendo definido. O *parâmetro order* é o número de pontos de controle na matriz. O *parâmetro stride* informa quantos locais flutuantes ou duplos devem avançar o ponteiro de memória interno para alcançar o próximo ponto de controle.

Como é o caso com todos os comandos OpenGL que aceitam  ponteiros para dados, é como se o conteúdo dos pontos fosse copiado por **glMap1** antes de ser retornado. As alterações no conteúdo dos *pontos não* têm efeito depois que **glMap1** é chamado.

As seguintes funções recuperam informações relacionadas a **glMap1:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ MAX \_ EVAL \_ ORDER

[**glGetMap**](glgetmap.md)

[**glIsEnabled com**](glisenabled.md) o argumento GL \_ MAP1 \_ VERTEX \_ 3

**glIsEnabled com** o argumento GL \_ MAP1 \_ VERTEX \_ 4

**glIsEnabled com** o argumento GL \_ MAP1 \_ INDEX

**glIsEnabled com** o argumento GL \_ MAP1 \_ COLOR \_ 4

**glIsEnabled com** o argumento GL \_ MAP1 \_ NORMAL

**glIsEnabled com** o argumento GL \_ MAP1 \_ TEXTURE \_ COORD \_ 1

**glIsEnabled com** o argumento GL \_ MAP1 \_ TEXTURE \_ COORD \_ 2

**glIsEnabled com** o argumento GL \_ MAP1 \_ TEXTURE \_ COORD \_ 3

**glIsEnabled com** o argumento GL \_ MAP1 \_ TEXTURE \_ COORD \_ 4

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

 

 





