---
title: Função glTexEnvfv (Gl.h)
description: A função glTexEnvfv define um parâmetro de ambiente de textura.
ms.assetid: 7b8e65aa-1b5c-47ab-8d6c-df14c90075a8
keywords:
- Função glTexEnvfv OpenGL
topic_type:
- apiref
api_name:
- glTexEnvfv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ae06746d00584cb6df6aa06c434115d1b53daab680e7f6cad8b4f12c78dba91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118613532"
---
# <a name="gltexenvfv-function"></a>Função glTexEnvfv

A **função glTexEnvfv define** um parâmetro de ambiente de textura.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glTexEnvfv(
         GLenum  target,
         GLenum  pname,
   const GLfloat *params
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*destino* 
</dt> <dd>

Um ambiente de textura. Deve ser GL \_ TEXTURE \_ ENV.

</dd> <dt>

*Pname* 
</dt> <dd>

O nome simbólico de um parâmetro de ambiente de textura com valor único. Os valores aceitos são GL \_ TEXTURE \_ ENV \_ MODE e GL \_ TEXTURE \_ ENV \_ COLOR.

</dd> <dt>

*params* 
</dt> <dd>

Um ponteiro para uma matriz de parâmetros: uma única constante simbólica ou uma cor RGBA.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela [**função glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significado                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *target* ou *pname* não era um dos valores *definidos aceitos* ou quando os params deveriam ter um valor constante definido (com base no valor *de pname*) e não tinham.<br/> |
| <dl> <dt>**OPERAÇÃO \_ GL \_ INVÁLIDA**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd.**](glend.md)<br/>                                             |



## <a name="remarks"></a>Comentários

Um ambiente de textura especifica como os valores de textura são interpretados quando um fragmento é texturizado. O *parâmetro de* destino deve ser GL TEXTURE \_ \_ ENV. O *parâmetro pname* pode ser GL \_ TEXTURE \_ ENV MODE ou GL TEXTURE \_ \_ \_ ENV \_ COLOR.

Se *pname* for GL \_ TEXTURE \_ ENV \_ MODE, *params* será (ou aponta para) o nome simbólico de uma função de textura. Três funções de textura são definidas: GL \_ MODULARTE, GL \_ DECAL e GL \_ BLEND.

Uma função de textura atua no fragmento a ser texturado usando o valor da imagem de textura que se aplica ao fragmento (consulte [**glTexParameter**](gltexparameter-functions.md)) e produz uma cor RGBA para esse fragmento. A tabela a seguir mostra como a cor RGBA é produzida para cada uma das três funções de textura que podem ser escolhidas. *C* é um triplo de valores de cor (RGB) *e A* é o valor alfa associado. Os valores RGBA extraídos de uma imagem de textura estão no intervalo \[ 0, 1 \] . O subscrito *f* refere-se ao fragmento de entrada, ao subscrito *t* à imagem de textura, ao subscrito *c* à cor do ambiente de textura e ao subscrito *v* indica um valor produzido pela função de textura.

Uma imagem de textura pode ter até quatro componentes por elemento de textura (consulte [**glTexImage1D**](glteximage1d.md) e [**glTexImage2D**](glteximage2d.md)). Em uma imagem de um componente, Lt indica esse componente único. Uma imagem de dois componentes usa *L?*  e *A?* . Uma imagem de três componentes tem apenas um valor de cor, *C?* . Uma imagem de quatro componentes tem um valor de cor *C?*  e um valor alfa *A?* .



<table>
<thead>
<tr class="header">
<th>Número de componentes</th>
<th>GL_MODULATE</th>
<th>GL_DECAL</th>
<th>GL_BLEND</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2">1${REMOVE}$<br />
</td>
<td><em>C<sub>v</sub> </em>  =  <em>L?</em> <em>C<sub>f</sub></em></td>
<td rowspan="2">undefined${REMOVE}$<br />
</td>
<td><em>C<sub>v</sub> </em>  =  <em>(1</em> - <em>L?</em> <em>)C<sub>f</sub> </em> + <em>L?</em> <em>C<sub>c</sub></em></td>
</tr>
<tr class="even">
<td><em>A<sub>v</sub> </em>  =  <em>A<sub>f</sub> </em></td>
<td><em>A<sub>v</sub> </em>  =  <em>A<sub>f</sub> </em></td>


</tr>
<tr class="odd">
<td rowspan="2">2${REMOVE}$<br />
</td>
<td><em>C<sub>v</sub> </em>  =  <em>L?</em> <em>C<sub>f</sub></em></td>
<td rowspan="2">undefined${REMOVE}$<br />
</td>
<td><em>C<sub>v</sub> </em>  =  <em>(1</em> - <em>L?</em> <em>)C<sub>f</sub> </em> + <em>L?</em> <em>C<sub>c</sub></em></td>
</tr>
<tr class="even">
<td><em>A</em> <em><sub>v</sub></em>   =  <em>A<sub>f</sub> </em></td>
<td><em>A<sub>v</sub> </em>  =  <em>A<sub>f</sub> </em></td>


</tr>
<tr class="odd">
<td rowspan="2">3${REMOVE}$<br />
</td>
<td><em>C<sub>v</sub> </em>  =  <em>C?</em> <em>C<sub>f</sub></em></td>
<td><em>C<sub>v</sub> </em>  =  <em>C?</em></td>
<td rowspan="2">undefined${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td><em>A<sub>v</sub> </em>  =  <em>A<sub>f</sub> </em> </td>
<td><em>A<sub>v</sub> </em>  =  <em>A<sub>f</sub> </em></td>


</tr>
<tr class="odd">
<td rowspan="2">4${REMOVE}$<br />
</td>
<td><em>C<sub>v</sub> </em>  =  <em>C?</em> <em>C<sub>f</sub></em></td>
<td><em>C<sub>v</sub> </em> = (1 – <em>A?</em> <em>)C<sub>f</sub> </em> + <em>A?</em> <em>C?</em></td>
<td rowspan="2">undefined${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td><em>A<sub>v</sub> </em>  =  <em>A?</em> <em>A<sub>f</sub></em> </td>
<td><em>A<sub>v</sub> </em>  =  <em>A<sub>f</sub> </em></td>


</tr>
</tbody>
</table>



 

Se pname for GL \_ TEXTURE ENV COLOR, params será um ponteiro para uma matriz que contém uma cor \_ \_ RGBA que consiste em quatro valores.  Os componentes de cor de inteiro são interpretados linearmente, de modo que o inteiro mais positivo é mapeado para 1,0 e o inteiro mais negativo é mapeado para -1,0. Os valores são fixados no intervalo \[ 0, 1 \] quando são especificados. *C <sub>c</sub>* recebe esses quatro valores.

O \_ PADRÃO DE GL TEXTURE \_ ENV É GL MODULARTE e GL TEXTURE \_ \_ \_ \_ ENV \_ COLOR como (0, 0, 0, 0).

A função a seguir recupera informações relacionadas **a glTexEnvfv**:

[**glTexGetEnvfv**](glgettexenvfv.md)

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
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





