---
title: Função glTexEnvi (Gl.h)
description: A função glTexEnvi define um parâmetro de ambiente de textura.
ms.assetid: 3f4c10c4-524c-4cce-b42b-bc72fc3b9f31
keywords:
- Função glTexEnvi OpenGL
topic_type:
- apiref
api_name:
- glTexEnvi
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c976eec51bed7087b1202ae4e4fd9a07435bfa4d6fd0d1fe2b964426bdf0ba5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119490596"
---
# <a name="gltexenvi-function"></a>Função glTexEnvi

A **função glTexEnvi** define um parâmetro de ambiente de textura.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glTexEnvi(
   GLenum target,
   GLenum pname,
   GLint  param
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

O nome simbólico de um parâmetro de ambiente de textura com valor único. Deve ser o MODO \_ \_ ENV DE TEXTURA \_ GL.

</dd> <dt>

*param* 
</dt> <dd>

Uma única constante simbólica, uma de \_ GL MODULARTE, GL \_ DECAL, GL \_ BLEND ou GL \_ REPLACE.

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

Um ambiente de textura especifica como os valores de textura são interpretados quando um fragmento é texturizado. O *parâmetro de* destino deve ser GL TEXTURE \_ \_ ENV. O *parâmetro pname* é GL \_ TEXTURE \_ ENV \_ MODE. Três funções de textura são definidas: GL \_ MODULARTE, GL \_ DECAL e GL \_ BLEND.

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
<td><em>A<sub>v</sub> </em>  =  <em>A<sub>f</sub> </em></td>
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



 

O \_ MODO \_ ENV DE TEXTURA GL assume COMO PADRÃO \_ GL \_ MODULARTE.

A função a seguir recupera informações relacionadas **a glTexEnvi**:

[**glTexGetEn ltda**](glgettexenviv.md)

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

 

 





