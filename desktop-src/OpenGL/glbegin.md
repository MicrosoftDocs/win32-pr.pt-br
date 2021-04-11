---
title: função glBegin (GL. h)
description: As funções glBegin e glend delimitam os vértices de um primitivo ou de um grupo de primitivas como primitivos. | função glBegin (GL. h)
ms.assetid: 8e8e98f8-89e8-40f5-89c1-492c9e3bbd74
keywords:
- função glBegin OpenGL
topic_type:
- apiref
api_name:
- glBegin
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8227d30adf97bf27fecc19603a5e5e32e4f44822
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103930416"
---
# <a name="glbegin-function"></a>função glBegin

As funções **glBegin** e [**glend**](glend.md) delimitam os vértices de um primitivo ou de um grupo de primitivas como primitivos.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glBegin(
   GLenum mode
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*mode* 
</dt> <dd>

Os primitivos ou primitivos que serão criados a partir de vértices apresentados entre **glBegin** e o [**glend**](glend.md)subsequente. As seguintes constantes simbólicas aceitas e seus significados:



| Valor                                                                                                                                                                      | Significado                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_POINTS"></span><span id="gl_points"></span><dl> <dt>**\_pontos GL**</dt> </dl>                          | Trata cada vértice como um único ponto. O vértice *n* define o ponto *n*. *N* pontos são desenhados.<br/>                                                                                                                                                                                                                                                                                                      |
| <span id="GL_LINES"></span><span id="gl_lines"></span><dl> <dt>**\_linhas GL**</dt> </dl>                             | Trata cada par de vértices como um segmento de linha independente. Os vértices *2n-1* e *2n* definem a linha *n*. As linhas *N/2* são desenhadas.<br/>                                                                                                                                                                                                                                                                |
| <span id="GL_LINE_STRIP"></span><span id="gl_line_strip"></span><dl> <dt>**\_faixa de linha gl \_**</dt> </dl>             | Desenha um grupo conectado de segmentos de linha do primeiro vértice até o último. Os vértices *n* e *n + 1* definem a linha *n*. As linhas *N-1* são desenhadas.<br/>                                                                                                                                                                                                                                                   |
| <span id="GL_LINE_LOOP"></span><span id="gl_line_loop"></span><dl> <dt>**\_loop de linha gl \_**</dt> </dl>                | Desenha um grupo conectado de segmentos de linha do primeiro vértice até o último e, em seguida, de volta para o primeiro. Os vértices *n* e *n + 1* definem a linha *n*. A última linha, no entanto, é definida pelos vértices *N* e *1*. *N* linhas são desenhadas.<br/>                                                                                                                                                                 |
| <span id="GL_TRIANGLES"></span><span id="gl_triangles"></span><dl> <dt>**\_TRIângulos GL**</dt> </dl>                 | Trata cada terceto de vértices como um triângulo independente. Os vértices *3N-2*, *3n-1* e *3N* definem o triângulo *n*. Os triângulos *N/3* são desenhados.<br/>                                                                                                                                                                                                                                              |
| <span id="GL_TRIANGLE_STRIP"></span><span id="gl_triangle_strip"></span><dl> <dt>**\_faixa de triângulo GL \_**</dt> </dl> | Desenha um grupo conectado de triângulos. Um triângulo é definido para cada vértice apresentado após os dois primeiros vértices. Para os *n* ímpares, os vértices *n*, *n + 1* e *n + 2* definem o triângulo *n*. Para até *n*, os vértices *n + 1*, *n* e *n + 2* definem o triângulo *n*. Os triângulos *N-2* são desenhados.<br/>                                                                                                  |
| <span id="GL_TRIANGLE_FAN"></span><span id="gl_triangle_fan"></span><dl> <dt>**\_ \_ ventilador do triângulo GL**</dt> </dl>       | Desenha um grupo conectado de triângulos. um triângulo é definido para cada vértice apresentado após os dois primeiros vértices. Os vértices *1*, *n + 1*, *n + 2* definem o triângulo *n*. Os triângulos *N-2* são desenhados.<br/>                                                                                                                                                                                         |
| <span id="GL_QUADS"></span><span id="gl_quads"></span><dl> <dt>**GL \_ quádruplos**</dt> </dl>                             | Trata cada grupo de quatro vértices como um diamante independente. Vértices *4n-3*, *4n-2*, *4n-1* e *4n* definem diamante *n*. *N/4* quadrilaterals são desenhados.<br/>                                                                                                                                                                                                                  |
| <span id="GL_QUAD_STRIP"></span><span id="gl_quad_strip"></span><dl> <dt>**extensão do GL \_ Quad \_**</dt> </dl>             | Desenha um grupo conectado de quadrilaterals. Um diamante é definido para cada par de vértices apresentados após o primeiro par. Os vértices *2n-1*, *2n*, *2n + 2* e *2n + 1* definem diamante *n*. *N/2-1* quadrilaterals são desenhados. Observe que a ordem na qual os vértices são usados para construir um diamante de dados de strip é diferente da usada com dados independentes.<br/> |
| <span id="GL_POLYGON"></span><span id="gl_polygon"></span><dl> <dt>**polígono do GL \_**</dt> </dl>                       | Desenha um polígono único e convexa. Os vértices de *1* a *N* definem este polígono.<br/>                                                                                                                                                                                                                                                                                                                  |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | o *modo* foi definido como um valor não aceito.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | Uma função diferente de [glVertex](glvertex-functions.md), [glColor](glcolor-functions.md), [glIndex](glindex-functions.md), [glNormal](glnormal-functions.md), [glTexCoord](gltexcoord-functions.md), [glEvalCoord](glevalcoord-functions.md), [glEvalPoint](glevalpoint.md), [glMaterial](glmaterial-functions.md), [glEdgeFlag](gledgeflag-functions.md), [**glCallList**](glcalllist.md)ou [**glCallLists**](glcalllists.md) foi chamada entre **glBegin** e o [**glend**](glend.md)correspondente. A função **glend** foi chamada antes que o **glBegin** correspondente fosse chamado ou **glBegin** foi chamado dentro de uma / sequência **glend** glBegin. <br/> |



## <a name="remarks"></a>Comentários

As funções **glBegin** e [**glend**](glend.md) delimitam os vértices que definem um primitivo ou um grupo de primitivas como primitivos. A função **glBegin** aceita um único argumento que especifica qual dos dez primitivos os vértices compõem. Colocando *n* como uma contagem de inteiros começando em um, e *n* como o número total de vértices especificado, as interpretações são as seguintes:

-   Você pode usar apenas um subconjunto de funções OpenGL entre **glBegin** e [**glend**](glend.md). As funções que você pode usar são:

    [**glVertex**](glvertex-functions.md)

     

    [**glColor**](glcolor-functions.md)

     

    [**glIndex**](glindex-functions.md)

     

    [**glNormal**](glnormal-functions.md)

     

    [**glTexCoord**](gltexcoord-functions.md)

     

    [**glEvalCoord**](glevalcoord-functions.md)

     

    [**glEvalPoint**](glevalpoint.md)

     

    [**glMaterial**](glmaterial-functions.md)

     

    [**glEdgeFlag**](gledgeflag-functions.md)

    Você também pode usar [**glCallList**](glcalllist.md) ou [**glCallLists**](glcalllists.md) para executar listas de exibição que incluem apenas as funções anteriores. Se qualquer outra função OpenGL for chamada entre **glBegin** e [**glend**](glend.md), o sinalizador de erro será definido e a função será ignorada.

-   Independentemente do valor escolhido para o *modo* em **glBegin**, não há nenhum limite para o número de vértices que você pode definir entre **glBegin** e [**glend**](glend.md). Linhas, triângulos, quadrilaterals e polígonos especificados incompletamente não são desenhadas. Resultados incompletos de especificação quando um número muito pequeno de vértices são fornecidos para especificar até mesmo um único primitivo ou quando um múltiplo incorreto de vértices é especificado. O primitivo incompleto é ignorado; os primitivos completos são desenhados.
-   A especificação mínima de vértices para cada primitivo é: 

    | Número mínimo de vértices | Tipo de primitiva |
    |----------------------------|-------------------|
    | 1                          | point             |
    | 2                          | line              |
    | 3                          | triangle          |
    | 4                          | diamante     |
    | 3                          | polygon           |

    

     

-   Os modos que exigem um determinado múltiplo de vértices são \_ linhas GL (2), \_ triângulos GL (3), GL \_ quádruplos (4) e GL \_ Quad \_ strip (2).

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

[**glCallList**](glcalllist.md)
</dt> <dt>

[**glCallLists**](glcalllists.md)
</dt> <dt>

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glEdgeFlag**](gledgeflag-functions.md)
</dt> <dt>

[**glEnd**](/windows/desktop/OpenGL/glend)
</dt> <dt>

[**glEvalCoord**](glevalcoord-functions.md)
</dt> <dt>

[**glEvalPoint**](glevalpoint.md)
</dt> <dt>

[**glIndex**](glindex-functions.md)
</dt> <dt>

[**glMaterial**](glmaterial-functions.md)
</dt> <dt>

[**glNormal**](glnormal-functions.md)
</dt> <dt>

[**glTexCoord**](gltexcoord-functions.md)
</dt> <dt>

[**glVertex**](glvertex-functions.md)
</dt> </dl>

 

