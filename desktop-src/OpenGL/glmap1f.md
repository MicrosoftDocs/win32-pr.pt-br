---
title: Função glMap1f (Gl.h)
description: A função glMap1f define um avaliador unidimensional. | função glMap1f (GL. h)
ms.assetid: c016ad80-b507-4e21-829f-f173d5c8dee6
keywords:
- função glMap1f OpenGL
topic_type:
- apiref
api_name:
- glMap1f
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7547e465f940942333c3bcff3e543e77c404ced289471ccff08924da83bfc2af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118359268"
---
# <a name="glmap1f-function"></a>função glMap1f

As funções [**glMap1d**](glmap1d.md) e **glMap1f** definem um avaliador unidimensional.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glMap1f(
         GLenum  target,
         GLfloat u1,
         GLfloat u2,
         GLint   stride,
         GLint   order,
   const GLfloat *points
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*destino* 
</dt> <dd>

O tipo de valores que são gerados pelo avaliador. Constantes simbólicas. O parâmetro de *destino* é uma constante simbólica que indica que tipo de pontos de controle são fornecidos em *pontos* e qual saída é gerada quando o mapa é avaliado. Ele pode assumir um dos nove valores predefinidos.



| Valor                                                                                                                                                                                          | Significado                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_MAP1_VERTEX_3"></span><span id="gl_map1_vertex_3"></span><dl> <dt>**GL \_ MAP1 \_ Vertex \_ 3**</dt> </dl>                       | Cada ponto de controle é de três valores de ponto flutuante que representam *x, y* e *z*. Comandos internos do [**glVertex3**](glvertex-functions.md) são gerados quando o mapa é avaliado.<br/>                                                                                                                                         |
| <span id="GL_MAP1_VERTEX_4"></span><span id="gl_map1_vertex_4"></span><dl> <dt>**MAP1 do GL de \_ \_ vértice \_ 4**</dt> </dl>                       | Cada ponto de controle é de quatro valores de ponto flutuante que representam *x, y, z* e *w*. Comandos internos do [**glVertex4**](glvertex-functions.md) são gerados quando o mapa é avaliado.<br/>                                                                                                                                       |
| <span id="GL_MAP1_INDEX"></span><span id="gl_map1_index"></span><dl> <dt>**\_Índice MAP1 \_ GL**</dt> </dl>                                 | Cada ponto de controle é um único valor de ponto flutuante que representa um índice de cor. Comandos internos do [**glIndex**](glindex-functions.md) são gerados quando o mapa é avaliado. No entanto, o índice atual não é atualizado com o valor desses comandos **glIndex** .<br/>                                                    |
| <span id="GL_MAP1_COLOR_4"></span><span id="gl_map1_color_4"></span><dl> <dt>**GL \_ MAP1 \_ cor \_ 4**</dt> </dl>                          | Cada ponto de controle é de quatro valores de ponto flutuante que representam vermelho, verde, azul e alfa. Comandos internos do [**glColor4**](glcolor-functions.md) são gerados quando o mapa é avaliado. No entanto, a cor atual não é atualizada com o valor desses comandos **glColor4** .<br/>                                       |
| <span id="GL_MAP1_NORMAL"></span><span id="gl_map1_normal"></span><dl> <dt>**GL \_ MAP1 \_ normal**</dt> </dl>                              | Cada ponto de controle é de três valores de ponto flutuante que representam os componentes *x, y* e *z* de um vetor normal. Comandos internos do [**glNormal**](glnormal-functions.md) são gerados quando o mapa é avaliado. No entanto, o normal atual não é atualizado com o valor desses comandos **glNormal** .<br/>              |
| <span id="GL_MAP1_TEXTURE_COORD_1"></span><span id="gl_map1_texture_coord_1"></span><dl> <dt>**GL \_ MAP1 \_ Texture \_ coord \_ 1**</dt> </dl> | Cada ponto de controle é um único valor de ponto flutuante que representa a coordenada de textura *s* . Comandos internos do [**glTexCoord1**](gltexcoord-functions.md) são gerados quando o mapa é avaliado. No entanto, as coordenadas de textura atuais não são atualizadas com o valor desses comandos **glTexCoord** .<br/>              |
| <span id="GL_MAP1_TEXTURE_COORD_2"></span><span id="gl_map1_texture_coord_2"></span><dl> <dt>**GL \_ MAP1 \_ Texture \_ coord \_ 2**</dt> </dl> | Cada ponto de controle é dois valores de ponto flutuante que representam as coordenadas de textura *s* e *t* . Comandos internos do [**glTexCoord2**](gltexcoord-functions.md) são gerados quando o mapa é avaliado. No entanto, as coordenadas de textura atuais não são atualizadas com o valor desses comandos **glTexCoord** .<br/>         |
| <span id="GL_MAP1_TEXTURE_COORD_3"></span><span id="gl_map1_texture_coord_3"></span><dl> <dt>**GL \_ MAP1 \_ Texture \_ coord \_ 3**</dt> </dl> | Cada ponto de controle é de três valores de ponto flutuante que representam as coordenadas de textura *s, t* e *r* . Comandos internos do [**glTexCoord3**](gltexcoord-functions.md) são gerados quando o mapa é avaliado. No entanto, as coordenadas de textura atuais não são atualizadas com o valor desses comandos **glTexCoord** .<br/>   |
| <span id="GL_MAP1_TEXTURE_COORD_4"></span><span id="gl_map1_texture_coord_4"></span><dl> <dt>**GL \_ MAP1 \_ Texture \_ coord \_ 4**</dt> </dl> | Cada ponto de controle é de quatro valores de ponto flutuante que representam as coordenadas *s, t, r* e *q* Texture. Comandos internos do [**glTexCoord4**](gltexcoord-functions.md) são gerados quando o mapa é avaliado. No entanto, as coordenadas de textura atuais não são atualizadas com o valor desses comandos **glTexCoord** .<br/> |



 

</dd> <dt>

*U1* 
</dt> <dd>

Um mapeamento linear de *u*, conforme apresentado a [**glEvalCoord1**](glevalcoord-functions.md), a *u*^, a variável que é avaliada pelas equações especificadas por esse comando.

</dd> <dt>

*U2* 
</dt> <dd>

Um mapeamento linear de *u*, conforme apresentado a [**glEvalCoord1**](glevalcoord-functions.md), a *u*^, a variável que é avaliada pelas equações especificadas por esse comando.

</dd> <dt>

*Stride* 
</dt> <dd>

O número de floats ou duplos entre o início de um ponto de controle e o início do próximo na estrutura de dados referenciada em *pontos*. Isso permite que os pontos de controle sejam inseridos em estruturas de dados arbitrárias. A única restrição é que os valores de um ponto de controle específico devem ocupar locais de memória contíguos.

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

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | o *destino* não era um valor aceito.<br/>                                                                                        |
| <dl> <dt>**\_valor inválido do GL \_**</dt> </dl>     | *U1* foi igual a *U2*.<br/>                                                                                                    |
| <dl> <dt>**\_valor inválido do GL \_**</dt> </dl>     | o *Stride* era menor que o número de valores em um ponto de controle.<br/>                                                            |
| <dl> <dt>**\_valor inválido do GL \_**</dt> </dl>     | *Order* foi menor que uma ou GL \_ Max \_ eval \_ Order.<br/>                                                                         |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

Os avaliadores fornecem uma maneira de usar o mapeamento polinomial polinomial ou racional para produzir vértices, normais, coordenadas de textura e cores. Os valores produzidos por um avaliador são enviados para outros estágios do processamento do OpenGL como se tivessem sido apresentados usando os comandos [**glVertex**](glvertex-functions.md), [**glNormal**](glnormal-functions.md), [**glTexCoord**](gltexcoord-functions.md)e [**glColor**](glcolor-functions.md) , exceto que os valores gerados não atualizam o normal atual, as coordenadas de textura ou a cor.

Todas as próprias linhas polinomiais polinomiais ou lógicas de qualquer grau (até o grau máximo com suporte pela implementação OpenGL) podem ser descritas usando avaliadores. Isso inclui quase todas as linhas usadas em gráficos de computador, incluindo as linhas B, curvas de Bézier, Hermite e assim por diante.

Os avaliadores definem as curvas com base em Bernstein polinomiais. Definir **p** () como

![Equação mostrando a definição de p ().](images/map01.png)

em que **R**_i_ é um ponto de controle e () é a *i* Bernstein polinomial do grau *n* (*pedido*  = *n* + 1):

![Equação mostrando o Bernstein polinomial do grau n.](images/map02.png)

Lembre-se de que

![Equações mostrando equivalência para 1.](images/map03.png)

A função **glMap1** é usada para definir a base e especificar que tipo de valores são produzidos. Uma vez definido, um mapa pode ser habilitado e desabilitado chamando [**glEnable**](glenable.md) e **glDisable** com o nome do mapa, um dos nove valores predefinidos para o *destino* descrito acima. A função [glEvalCoord1](glevalcoord-functions.md) avalia os mapas unidimensionais que estão habilitados. Quando **glEvalCoord1** apresenta um valor *u*, as funções Bernstein são avaliadas usando *u*^, em que

![Equação mostrando a definição de você ^.](images/map04.png)

Os parâmetros *Stride*, *Order* e *Points* definem o endereçamento de matriz para acessar os pontos de controle. O parâmetro *Points* é o local do primeiro ponto de controle, que ocupa um, dois, três ou quatro locais de memória contíguos, dependendo de qual mapa está sendo definido. O parâmetro *Order* é o número de pontos de controle na matriz. O parâmetro *Stride* informa quantos locais flutuantes ou duplos para avançar o ponteiro de memória interna para alcançar o próximo ponto de controle.

Como é o caso com todos os comandos OpenGL que aceitam ponteiros para os dados, é como se o conteúdo dos *pontos* fosse copiado por **glMap1** antes de ser retornado. As alterações no conteúdo de *pontos* não têm efeito depois que **glMap1** é chamado.

As funções a seguir recuperam informações relacionadas ao **glMap1**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ Max \_ eval \_ Order

[**glGetMap**](glgetmap.md)

[**glIsEnabled**](glisenabled.md) com Argument GL \_ MAP1 \_ vértice \_ 3

**glIsEnabled** com Argument GL \_ MAP1 \_ vértice \_ 4

índice de **glIsEnabled** com Argument GL \_ MAP1 \_

**glIsEnabled** com Argument GL \_ MAP1 \_ cor \_ 4

**glIsEnabled** com Argument GL \_ MAP1 \_ normal

**glIsEnabled** com Argument GL \_ MAP1 \_ Texture \_ coord \_ 1

**glIsEnabled** com Argument GL \_ MAP1 \_ Texture \_ coord \_ 2

**glIsEnabled** com Argument GL \_ MAP1 \_ Texture \_ coord \_ 3

**glIsEnabled** com Argument GL \_ MAP1 \_ Texture \_ coord \_ 4

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

 

 





