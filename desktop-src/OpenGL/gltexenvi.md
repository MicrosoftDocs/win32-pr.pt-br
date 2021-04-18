---
title: função glTexEnvi (GL. h)
description: A função glTexEnvi define um parâmetro de ambiente de textura.
ms.assetid: 3f4c10c4-524c-4cce-b42b-bc72fc3b9f31
keywords:
- função glTexEnvi OpenGL
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
ms.openlocfilehash: c013b0e4805042ed0967e02df83f143d8bcfd991
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753152"
---
# <a name="gltexenvi-function"></a>função glTexEnvi

A função **glTexEnvi** define um parâmetro de ambiente de textura.

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

Um ambiente de textura. Deve ser GL \_ Texture \_ env.

</dd> <dt>

*pname* 
</dt> <dd>

O nome simbólico de um parâmetro de ambiente de textura de valor único. Deve ser GL \_ \_ Mode Texture env \_ .

</dd> <dt>

*param* 
</dt> <dd>

Uma única constante simbólica, uma do GL \_ modular \_ Decal, GL \_ Blend ou GL \_ replace.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | *target* ou *pname* não era um dos valores definidos aceitos, ou quando *params* deveria ter tido um valor constante definido (com base no valor de *pname*) e não.<br/> |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/>                                             |



## <a name="remarks"></a>Comentários

Um ambiente de textura especifica como os valores de textura são interpretados quando um fragmento é texturizado. O parâmetro de *destino* deve ser GL \_ Texture \_ env. O parâmetro *pname* é GL \_ Texture \_ env \_ Mode. Três funções de textura são definidas: GL \_ modular, GL \_ Decal e GL \_ Blend.

Uma função de textura age no fragmento para ser texturizada usando o valor da imagem de textura que se aplica ao fragmento (consulte [**glTexParameter**](gltexparameter-functions.md)) e produz uma cor RGBA para esse fragmento. A tabela a seguir mostra como a cor RGBA é produzida para cada uma das três funções de textura que podem ser escolhidas. *C* é um triplo de valores de cor (RGB) e *um* é o valor alfa associado. Os valores RGBA extraídos de uma imagem de textura estão no intervalo de \[ 0, 1 \] . O *f* de subscrito refere-se ao fragmento de entrada, ao *t* de subscrito à imagem de textura, ao *c* de cor do ambiente de textura e a um subscrito *v* indica um valor produzido pela função de textura.

Uma imagem de textura pode ter até quatro componentes por elemento de textura (consulte [**glTexImage1D**](glteximage1d.md) e [**glTexImage2D**](glteximage2d.md)). Em uma imagem de um componente, o lt indica que há um único componente. Uma imagem de dois componentes usa *L?*  e *um?* . Uma imagem de três componentes tem apenas um valor de cor, *C?* . Uma imagem de quatro componentes tem um valor de cor *C?*  e um valor alfa *A?* .



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
<td rowspan="2">1 $ {REMOVER} $<br />
</td>
<td><em>C<sub>v</sub> </em>  =  <em>L?</em> <em>C<sub>f</sub></em></td>
<td rowspan="2">Não definido $ {REMOVE} $<br />
</td>
<td><em>C<sub>v</sub> </em>  =  <em>(1</em> - <em>L?</em> <em>) C<sub>f</sub> </em> + <em>L?</em> <em>C<sub>c</sub></em></td>
</tr>
<tr class="even">
<td><em>Um<sub>v</sub> </em>  =  <em>Um<sub>f</sub> </em></td>
<td><em>Um<sub>v</sub> </em>  =  <em>Um<sub>f</sub> </em></td>


</tr>
<tr class="odd">
<td rowspan="2">2 $ {REMOVER} $<br />
</td>
<td><em>C<sub>v</sub> </em>  =  <em>L?</em> <em>C<sub>f</sub></em></td>
<td rowspan="2">Não definido $ {REMOVE} $<br />
</td>
<td><em>C<sub>v</sub> </em>  =  <em>(1</em> - <em>L?</em> <em>) C<sub>f</sub> </em> + <em>L?</em> <em>C<sub>c</sub></em></td>
</tr>
<tr class="even">
<td><em>Um<sub>v</sub> </em>  =  <em>Um<sub>f</sub> </em></td>
<td><em>Um<sub>v</sub> </em>  =  <em>Um<sub>f</sub> </em></td>


</tr>
<tr class="odd">
<td rowspan="2">3 $ {REMOVER} $<br />
</td>
<td><em>C<sub>v</sub> </em>  =  <em>C?</em> <em>C<sub>f</sub></em></td>
<td><em>C<sub>v</sub> </em>  =  <em>C?</em></td>
<td rowspan="2">Não definido $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td><em>Um<sub>v</sub> </em>  =  <em>Um<sub>f</sub> </em> </td>
<td><em>Um<sub>v</sub> </em>  =  <em>Um<sub>f</sub> </em></td>


</tr>
<tr class="odd">
<td rowspan="2">4 $ {REMOVER} $<br />
</td>
<td><em>C<sub>v</sub> </em>  =  <em>C?</em> <em>C<sub>f</sub></em></td>
<td><em>C<sub>v</sub> </em> = (1- <em>a?</em> <em>) C<sub>f</sub> </em> + <em>A?</em> <em>&?</em></td>
<td rowspan="2">Não definido $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td><em>Um<sub>v</sub> </em>  =  <em>R?</em> <em>Um<sub>f</sub></em> </td>
<td><em>Um<sub>v</sub> </em>  =  <em>Um<sub>f</sub> </em></td>


</tr>
</tbody>
</table>



 

O \_ modo de textura de \_ env GL \_ usa como padrão o GL \_ modular.

A função a seguir recupera informações relacionadas a **glTexEnvi**:

[**glTexGetEnviv**](glgettexenviv.md)

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

[**glEnd**](glend.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





