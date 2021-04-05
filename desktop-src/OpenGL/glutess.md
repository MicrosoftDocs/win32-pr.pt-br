---
title: função gluTessCallback (Glu. h)
description: A função gluTessCallback define um retorno de chamada para um objeto de mosaico.
ms.assetid: a9709919-d34c-42c4-82b8-6a503f2b39b0
keywords:
- função gluTessCallback OpenGL
topic_type:
- apiref
api_name:
- gluTessCallback
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17cdba8b9dd9a3e762a93923a3c353fbc9578377
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919057"
---
# <a name="glutesscallback-function"></a>função gluTessCallback

A função **gluTessCallback** define um retorno de chamada para um objeto de mosaico.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI gluTessCallback(
   GLUtesselator *tess,
   GLenum        which,
   void (CALLBACK *fn)()
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*tess* 
</dt> <dd>

O objeto de mosaico (criado com [**gluNewTess**](glunewtess.md)).

</dd> <dt>

*Onde* 
</dt> <dd>

O retorno de chamada que está sendo definido. Os valores a seguir são válidos: GLU \_ Tess \_ begin, glu \_ Tess \_ begin \_ data, GLU \_ Tess \_ \_ endflag, glu Tess \_ \_ \_ endflag \_ data, glu \_ Tess \_ vértice, glu \_ Tess \_ Vertex \_ data, glu \_ Tess \_ end, glu \_ Tess \_ end \_ data, glu \_ Tess combine, glu Tess \_ \_ \_ Combine dados, glu Tess \_ \_ \_ Error e Glu Tess \_ \_ Error \_ Data.

Para obter mais informações sobre esses retornos de chamada, consulte a seção de comentários a seguir.

</dd> <dt>

*fn* 
</dt> <dd>

A função a ser chamada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Use **gluTessCallback** para especificar um retorno de chamada a ser usado por um objeto de mosaico. Se o retorno de chamada especificado já estiver definido, ele será substituído. Se *FN* for **NULL**, o retorno de chamada existente se tornará indefinido.

O objeto de mosaico usa esses retornos de chamada para descrever como um polígono especificado é dividido em triângulos.

Há duas versões de cada retorno de chamada, uma com dados de polígono que você pode definir e uma sem. Se ambas as versões de um retorno de chamada específico forem especificadas, o retorno de chamada com os dados de polígono que você especificar será usado. O parâmetro de *\_ dados Polygon* de [**gluTessBeginPolygon**](glutessbeginpolygon.md) é uma cópia do ponteiro que foi especificado quando **gluTessBeginPolygon** foi chamado.

Veja a seguir os retornos de chamada válidos:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Callback</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>GLU_TESS_BEGIN</td>
<td>O retorno de chamada GLU_TESS_BEGIN é invocado como <a href="glbegin.md"><strong>glBegin</strong></a> para indicar o início de um primitivo (triângulo). A função usa um único argumento do tipo <strong>GLenum</strong>. Se você definir a propriedade GLU_TESS_BOUNDARY_ONLY como GL_FALSE, o argumento será definido como GL_TRIANGLE_FAN, GL_TRIANGLE_STRIP ou GL_TRIANGLES. Se você definir a propriedade GLU_TESS_BOUNDARY_ONLY como GL_TRUE, o argumento será definido como GL_LINE_LOOP. O protótipo de função para esse retorno de chamada é o seguinte: <strong>void</strong> <strong>begin</strong> ( <em>tipo</em><strong>GLenum</strong> );<br/></td>
</tr>
<tr class="even">
<td>GLU_TESS_BEGIN_DATA</td>
<td>GLU_TESS_BEGIN_DATA é o mesmo que o retorno de chamada GLU_TESS_BEGIN, exceto pelo fato de que ele usa um argumento de ponteiro adicional. Esse ponteiro é idêntico ao ponteiro opaco fornecido quando você chama <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>. O protótipo de função para este retorno de chamada é: <strong>void</strong> <strong>beginData</strong> ( <em>tipo</em><strong>GLenum</strong> , <strong>void</strong> * <em>polygon_data</em>);<br/></td>
</tr>
<tr class="odd">
<td>GLU_TESS_EDGE_FLAG</td>
<td>O retorno de chamada GLU_TESS_EDGE_FLAG é semelhante a <a href="gledgeflag-functions.md"><strong>glEdgeFlag</strong></a>. A função usa um único sinalizador booliano que indica quais bordas se encontram no limite do polígono. Se o sinalizador for GL_TRUE, cada vértice a seguir iniciará uma borda que está no limite do polígono; ou seja, uma borda que separa uma região interior de um exterior. Se o sinalizador for GL_FALSE, cada vértice a seguir iniciará uma borda que está no interior do polígono. O retorno de chamada GLU_TESS_EDGE_FLAG (se definido) é invocado antes de o primeiro retorno de chamada de vértice ser feito. Como os ventiladores de triângulo e as faixas de triângulo não dão suporte a sinalizadores de borda, o retorno de chamada de início não é chamado com GL_TRIANGLE_FAN ou GL_TRIANGLE_STRIP se um retorno de chamada de sinalizador de borda for fornecido. Em vez disso, os ventiladores e as faixas são convertidos em triângulos independentes. O protótipo de função para este retorno de chamada é:<br/> <strong>void</strong> <strong>edgeFlag</strong> (<strong></strong> <em>sinalizador</em>GLboolean);<br/></td>
</tr>
<tr class="even">
<td>GLU_TESS_EDGE_FLAG_DATA</td>
<td>O retorno de chamada GLU_TESS_EDGE_FLAG_DATA é o mesmo que o GLU_TESS_EDGE_FLAG retorno de chamada, exceto pelo fato de que ele usa um argumento de ponteiro adicional. Esse ponteiro é idêntico ao ponteiro opaco fornecido quando você chama <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>. O protótipo de função para este retorno de chamada é: <strong>void</strong> <strong>edgeFlagData</strong> ( <em>sinalizador</em><strong>GLboolean</strong> , <strong>void</strong> * <em>polygon_data</em>);<br/></td>
</tr>
<tr class="odd">
<td>GLU_TESS_VERTEX</td>
<td>O retorno de chamada GLU_TESS_VERTEX é invocado entre os retornos de chamada Begin e end. Ele é semelhante a glVertex e define os vértices dos triângulos criados pelo processo de mosaico. A função usa um ponteiro como seu único argumento. Esse ponteiro é idêntico ao ponteiro opaco que você forneceu quando definiu o vértice (consulte <a href="glutessvertex.md"><strong>gluTessVertex</strong></a>). O protótipo de função para este retorno de chamada é: <strong>void</strong> <strong>vertex</strong> (<strong>void</strong> * <em>vertex_data</em>);<br/></td>
</tr>
<tr class="even">
<td>GLU_TESS_VERTEX_DATA</td>
<td>O GLU_TESS_VERTEX_DATA é o mesmo que o retorno de chamada GLU_TESS_VERTEX, exceto pelo fato de que ele usa um argumento de ponteiro adicional. Esse ponteiro é idêntico ao ponteiro opaco fornecido quando você chama <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>. O protótipo de função para este retorno de chamada é: <strong>void</strong>  <strong>vertexData</strong> (void * <em>vertex_data</em>, <strong>void</strong> * <em>polygon_data</em>);<br/></td>
</tr>
<tr class="odd">
<td>GLU_TESS_END</td>
<td>O retorno de chamada GLU_TESS_END tem a mesma finalidade que <a href="glend.md"><strong>glEnd</strong></a>. Indica o fim de um primitivo e não usa argumentos. O protótipo de função para este retorno de chamada é: <strong>void</strong> <strong>end</strong> (<strong>void</strong>);<br/></td>
</tr>
<tr class="even">
<td>GLU_TESS_END_DATA</td>
<td>O retorno de chamada GLU_TESS_END_DATA é o mesmo que o GLU_TESS_END retorno de chamada, exceto pelo fato de que ele usa um argumento de ponteiro adicional. Esse ponteiro é idêntico ao ponteiro opaco fornecido quando você chama <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>. O protótipo de função para este retorno de chamada é: <strong>void</strong> <strong>endData</strong> (<strong>void</strong> * <em>polygon_data</em>);<br/></td>
</tr>
<tr class="odd">
<td>GLU_TESS_COMBINE</td>
<td>Chame o GLU_TESS_COMBINE retorno de chamada para criar um novo vértice quando o mosaico detectar uma interseção ou para mesclar recursos. A função usa quatro argumentos: uma matriz de três elementos, cada um do tipo Gldouble.<br/> Uma matriz de quatro ponteiros.<br/> Uma matriz de quatro elementos, cada um do tipo GLfloat.<br/> Um ponteiro para um ponteiro.<br/> O protótipo de função para este retorno de chamada é: <br/> <strong>void</strong> <strong>Combine</strong>(<strong>GLdouble</strong> <em>CoOrds</em>[3], <strong>void</strong> * <em>vertex_data</em>[4], <strong></strong> <em>peso</em>de GLfloat [4], <strong></strong>  ** <em>indados</em>nulos);<br/> O vértice é definido como uma combinação linear de até quatro vértices existentes, armazenados em vertex_data. Os coeficientes da combinação linear são fornecidos por peso; esses pesos sempre somam 1,0. Todos os ponteiros de vértice são válidos mesmo quando alguns dos pesos são zero. O parâmetro CoOrds fornece o local do novo vértice.<br/> Aloque outro vértice, interpolar parâmetros usando vertex_data e peso e retornar o novo ponteiro de vértice em OutData. Esse identificador é fornecido durante os retornos de chamada de renderização. Libere a memória em algum momento depois de chamar <a href="glutessendpolygon.md"><strong>gluTessEndPolygon</strong></a>.<br/> Por exemplo, se o polígono estiver em um plano arbitrário no espaço tridimensional e você associar uma cor a cada vértice, o retorno de chamada GLU_TESS_COMBINE poderá ser semelhante ao seguinte:<br/>
<pre data-space="preserve"><code>void myCombine( GLdouble coords[3], VERTEX *d[4], 
                GLfloat w[4], VERTEX **dataOut ) 
{ 
    VERTEX *newVertex = new_vertex(); 
    newVertex->x = coords[0]; 
    newVertex->y = coords[1]; 
    newVertex->z = coords[2]; 
    newVertex->r = w[0]*d[0]->r + w[1]*d[1]->r + w[2]*d[2]->r + 
                   w[3]*d[3]->r; 
    newVertex->g = w[0]*d[0]->g + w[1]*d[1]->g + w[2]*d[2]->g + 
                   w[3]*d[3]->g; 
    newVertex->b = w[0]*d[0]->b + w[1]*d[1]->b + w[2]*d[2]->b + 
                   w[3]*d[3]->b; 
    newVertex->a = w[0]*d[0]->a + w[1]*d[1]->a + w[2]*d[2]->a + 
                   w[3]*d[3]->a; 
    *dataOut = newVertex; 
}</code></pre>
Quando o mosaico detecta uma interseção, o GLU_TESS_COMBINE ou GLU_TESS_COMBINE_DATA retorno de chamada (veja abaixo) deve ser definido e deve gravar um ponteiro não<strong>nulo</strong> no dataout. Caso contrário, o erro GLU_TESS_NEED_COMBINE_CALLBACK ocorrerá e nenhuma saída será gerada. (Esse é o único erro que pode ocorrer durante o mosaico e a renderização.)<br/></td>
</tr>
<tr class="even">
<td>GLU_TESS_COMBINE_DATA</td>
<td>O retorno de chamada GLU_TESS_COMBINE_DATA é o mesmo que o GLU_TESS_COMBINE retorno de chamada, exceto pelo fato de que ele usa um argumento de ponteiro adicional. Esse ponteiro é idêntico ao ponteiro opaco fornecido quando você chama <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>. O protótipo de função para este retorno de chamada é: <strong>void</strong> <strong>combineData</strong> (<strong>GLdouble</strong> <em>CoOrds</em>[3], <strong>void</strong> *<em>vertex_data</em>[4], <strong>GLfloat</strong> <em>Weight</em>[4], <strong>void</strong>  ** <em>Indata</em>, <strong>void</strong> * <em>polygon_data</em>);<br/></td>
</tr>
<tr class="odd">
<td>GLU_TESS_ERROR</td>
<td>O retorno de chamada GLU_TESS_ERROR é chamado quando um erro é encontrado. O argumento One é do tipo <strong>GLenum</strong>; Ele indica o erro específico que ocorreu e é definido como um dos seguintes: GLU_TESS_MISSING_BEGIN_POLYGON<br/> GLU_TESS_MISSING_END_POLYGON<br/> GLU_TESS_MISSING_BEGIN_CONTOUR<br/> GLU_TESS_MISSING_END_CONTOUR<br/> GLU_TESS_COORD_TOO_LARGE<br/> GLU_TESS_NEED_COMBINE_CALLBACK<br/> Chame gluErrorString para recuperar cadeias de caracteres que descrevem esses erros. O protótipo de função para esse retorno de chamada é o seguinte:<br/> <strong></strong> <strong>erro</strong> de void (<strong>GLenum</strong> <em>errno</em>);<br/> A biblioteca GLU recupera os quatro primeiros erros inserindo a chamada ou chamadas ausentes. GLU_TESS_COORD_TOO_LARGE indica que alguma coordenada de vértice excedeu a constante predefinida GLU_TESS_MAX_COORD em valor absoluto e que o valor foi clamped. (Os valores de coordenadas devem ser pequenos o suficiente para que dois possam ser multiplicados em conjunto sem estouro.) GLU_TESS_NEED_COMBINE_CALLBACK indica que o mosaico detectou uma interseção entre duas bordas nos dados de entrada e o retorno de chamada GLU_TESS_COMBINE ou GLU_TESS_COMBINE_DATA não foi fornecido. Nenhuma saída será gerada.<br/></td>
</tr>
<tr class="even">
<td>GLU_TESS_ERROR_DATA</td>
<td>O retorno de chamada GLU_TESS_ERROR_DATA é o mesmo que o GLU_TESS_ERROR retorno de chamada, exceto pelo fato de que ele usa um argumento de ponteiro adicional. Esse ponteiro é idêntico ao ponteiro opaco fornecido quando você chama <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>. O protótipo de função para este retorno de chamada é: <strong>void</strong> <strong>ErrorData</strong> (<strong>GLenum</strong> <em>errno</em>, <strong>void</strong> * <em>polygon_data</em>);<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>GLU. h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEdgeFlag**](gledgeflag-functions.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glVertex**](glvertex-functions.md)
</dt> <dt>

[**gluDeleteTess**](gludeletetess.md)
</dt> <dt>

[**gluErrorString**](gluerrorstring.md)
</dt> <dt>

[**gluNewTess**](glunewtess.md)
</dt> <dt>

[**gluTessBeginPolygon**](glutessbeginpolygon.md)
</dt> <dt>

[**gluTessEndPolygon**](glutessendpolygon.md)
</dt> <dt>

[**gluTessVertex**](glutessvertex.md)
</dt> </dl>

 

 





