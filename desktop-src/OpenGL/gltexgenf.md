---
title: Função glTexGenf (Gl.h)
description: Controla a geração de coordenadas de textura. | Função glTexGenf (Gl.h)
ms.assetid: 43439d34-46df-49c6-8c19-09db9f005520
keywords:
- Função glTexGenf OpenGL
topic_type:
- apiref
api_name:
- glTexGenf
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1198da9d87e79f8e3abb923ac2f5ce48ad5afc8cb06d4d97bcf40a3153367e72
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119490376"
---
# <a name="gltexgenf-function"></a>Função glTexGenf

Controla a geração de coordenadas de textura.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glTexGenf(
   GLenum  coord,
   GLenum  pname,
   GLfloat param
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Coord* 
</dt> <dd>

Uma coordenada de textura. Deve ser um dos seguintes: GL \_ S, GL \_ T, GL \_ R ou GL \_ Q.

</dd> <dt>

**Pname** 
</dt> <dd>

O nome simbólico da função de geração de coordenadas de textura.

</dd> <dt>

*param* 
</dt> <dd>

Um parâmetro de geração de textura com valor único, um de GL \_ OBJECT \_ LINEAR, GL \_ EYE LINEAR ou GL SPHERE \_ \_ \_ MAP.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela [**função glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significado                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *coord* ou *pname* não era um valor definido aceito ou *pname* era GL TEXTURE GEN MODE e \_ \_ \_ *params* não era um valor definido aceito.<br/> |
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *pname* era GL \_ TEXTURE \_ GEN \_ MODE, *params* era GL SPHERE MAP e \_ \_ *coord* era GL \_ R ou GL \_ Q<br/>                                     |
| <dl> <dt>**OPERAÇÃO \_ GL \_ INVÁLIDA**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd.**](glend.md) <br/>                 |



## <a name="remarks"></a>Comentários

A **função glTexGen** seleciona uma função de geração de coordenadas de textura ou fornece coeficientes para uma das funções. O parâmetro *coord* nomeia uma das coordenadas de textura (s, t,r,q) e deve ser um destes símbolos: GL \_ S, GL T, GL R ou \_ GL \_ \_ Q. O *parâmetro pname* deve ser uma das três constantes simbólicas: GL \_ TEXTURE GEN \_ \_ MODE, GL OBJECT PLANE ou GL \_ EYE \_ \_ \_ PLANE. Se *pname* for GL TEXTURE GEN MODE, o param especificará um modo, um de \_ GL OBJECT \_ \_  \_ \_ LINEAR, GL EYE LINEAR ou GL \_ SPHERE \_ \_ \_ MAP. Se *pname for* GL \_ OBJECT PLANE ou GL EYE \_ \_ \_ PLANE, o *param* conterá coeficientes para a função de geração de textura correspondente.

Se a função de geração de textura for GL \_ OBJECT \_ LINEAR, a função

! [Equação mostrando a função glTexGen quando a função de geração de textura é GL_OBJECT_LINEAR.]

é usado, em que g é o valor calculado para a coordenada chamada em coord; p1, p2, p3 e p4 são os quatro valores fornecidos em params; e x?, y?, z?, e w? são as coordenadas de objeto do vértice. Você pode usar essa função para mapear textura usando o nível do mar como um plano de referência (definido por p1, p2, p3 e p4). A função de geração de coordenadas GL OBJECT LINEAR calcula a altitude de um vértice de terreno como sua distância do nível do mar; essa altitude é usada para indexar a imagem de textura para mapear a neve branca em picos e grama verde em \_ \_ rodapés, por exemplo.

Se a função de geração de textura for GL \_ EYE \_ LINEAR, a função

! [Equação mostrando a função glTexGen quando a função de geração de textura é GL_EYE_LINEAR.]

é usado, em que

![Equação mostrando as coordenadas de olho do vértice.](images/tex03.png)

e x?, y?, z?, e w? são as coordenadas de olho do vértice, p1, p2, p3 e p4 são os valores fornecidos no *param* e M é a matriz de modelview quando você chama **glTexGen**. Se M estiver mal condicional ou singular, as coordenadas de textura geradas pela função resultante poderão ser imprecisas ou indefinidas.

Observe que os valores em *param definem* um plano de referência em coordenadas de olho. A matriz modelview aplicada a elas pode não ser a mesma em vigor quando os vértices de polígono são transformados. Essa função estabelece um campo de coordenadas de textura que pode produzir linhas de contorno dinâmicos em objetos móveis.

Se *pname* for GL SPHERE MAP e coord for GL S ou GL T, as coordenadas de textura s e t serão \_ \_  \_ \_ geradas da seguinte forma. Vamos ser o vetor de unidade que aponta da origem para o vértice de polígono (em coordenadas de olho). Deixe n ser o normal atual, após a transformação para coordenadas de olho. Let f = (fx ( ) fy ( ) fz)T ser o vetor de reflexão de forma que

![Equação mostrando o vetor de reflexão como uma função do vetor de unidade e normal atual.](images/tex05.png)

Por fim, vamos

![Equação mostrando m como uma função do vetor de reflexão.](images/tex07.png)

Em seguida, os valores atribuídos às coordenadas de textura i e t são

![Equação mostrando valores atribuídos às coordenadas de textura i e t.](images/tex06.png)

Você pode habilitar ou desabilitar uma função de geração de coordenadas de textura usando [**glEnable**](glenable.md) ou [**glDisable**](gldisable.md) com um dos nomes simbólicos de coordenadas de textura (GL \_ TEXTURE GEN \_ \_ S, GL TEXTURE GEN T, GL TEXTURE GEN R ou \_ GL TEXTURE GEN \_ \_ \_ \_ \_ \_ \_ \_ Q) como o argumento. Quando essa função é habilitada, a coordenada de textura especificada é calculada de acordo com a função de geração associada a essa coordenada. Quando essa função é desabilitada, os vértices subsequentes levam a coordenada de textura especificada do conjunto atual de coordenadas de textura. Inicialmente, todas as funções de geração de textura são definidas como GL \_ EYE LINEAR e são \_ desabilitadas. Ambas as equações de plano são (1,0,0,0); ambas as equações de plano t são (0,1,0,0); e todas as equações de plano r e q são (0,0,0,0).

As funções a seguir recuperam informações relacionadas a glTexGen:

<dl>

[**glGetTexGen**](glgettexgen.md)  
[**glIsEnabled com**](glisenabled.md) o argumento GL \_ TEXTURE GEN \_ \_ S  
[**glIsEnabled com**](glisenabled.md) o argumento GL \_ TEXTURE GEN \_ \_ T  
[**glIsEnabled com**](glisenabled.md) o argumento GL \_ TEXTURE GEN \_ \_ R  
[**glIsEnabled com**](glisenabled.md) o argumento GL \_ TEXTURE GEN \_ \_ Q  
</dl>

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

[**glCopyTexImage2D**](glcopyteximage2d.md)
</dt> <dt>

[**glCopyTexSubImage2D**](glcopytexsubimage2d.md)
</dt> <dt>

[**glGetTexGen**](glgettexgen.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[glTexEnv](gltexenv-functions.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[glTexParameter](gltexparameter-functions.md)
</dt> <dt>

[**glTexSubImage1D**](gltexsubimage1d.md)
</dt> <dt>

[**glTexSubImage2D**](gltexsubimage2d.md)
</dt> </dl>

 

 





