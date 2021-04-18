---
title: função glTexGendv (GL. h)
description: Controla a geração de coordenadas de textura. | função glTexGendv (GL. h)
ms.assetid: fe0e28e4-50d3-473f-a290-7745a1718618
keywords:
- função glTexGendv OpenGL
topic_type:
- apiref
api_name:
- glTexGendv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eccae96a6289d2172115763b6b6117bf184e2eb8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104550852"
---
# <a name="gltexgendv-function"></a>função glTexGendv

Controla a geração de coordenadas de textura.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glTexGendv(
         GLenum   coord,
         GLenum   pname,
   const GLdouble *params
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*coord* 
</dt> <dd>

Uma coordenada de textura. Deve ser um dos seguintes: GL \_ S, GL \_ T, GL \_ R ou GL \_ Q.

</dd> <dt>

**pname** 
</dt> <dd>

O nome simbólico da função de geração de coordenadas de textura.

</dd> <dt>

*params* 
</dt> <dd>

Uma matriz que contém os coeficientes para a função de geração de textura correspondente.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | *coord* ou *pname* não era um valor definido aceito ou *pname* o \_ \_ modo de geração de textura do GL \_ e *params* não era um valor definido aceito.<br/> |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md). <br/>                 |



## <a name="remarks"></a>Comentários

A função **glTexGen** seleciona uma função de geração de coordenadas de textura ou fornece coeficientes para uma das funções. O parâmetro *coord* nomeia uma das coordenadas de textura (s, t, r, q) e deve ser um destes símbolos: GL \_ s, GL \_ t, GL \_ r ou GL \_ q. O parâmetro *pname* deve ser uma das três constantes simbólicas: \_ \_ modo de geração de textura GL \_ , plano de \_ objeto GL \_ ou plano de \_ olho GL \_ . Se *pname* for plano de \_ objeto GL \_ ou \_ \_ plano de olho GL, *param* conterá coeficientes para a função de geração de textura correspondente.

Se a função de geração de textura for \_ Object GL \_ linear, a função

! [Equação mostrando a função glTexGen quando a função de geração de textura é GL_OBJECT_LINEAR.]

é usado, em que g é o valor calculado para a coordenada chamada em coord; P1, P2, P3 e P4 são os quatro valores fornecidos em params; e x?, y?, z? e w? são as coordenadas de objeto do vértice. Você pode usar essa função para o terreno do mapa de textura usando o nível do mar como um plano de referência (definido por P1, P2, P3 e P4). A \_ função de \_ geração de coordenada linear do objeto GL computa a altitude de um vértice do terreno como sua distância do nível do mar; essa altitude é usada para indexar a imagem de textura para o mapa de Neves brancas em picos e na grama verde em Foothills, por exemplo.

Se a função de geração de textura for a \_ atenção \_ linear, a função

! [Equação mostrando a função glTexGen quando a função de geração de textura é GL_EYE_LINEAR.]

é usado, em que

![Equação mostrando as coordenadas de olho do vértice.](images/tex03.png)

e x?, y?, z? e w? são as coordenadas de olho do vértice, P1, P2, P3 e P4 são os valores fornecidos no *param* e M é a matriz modelview quando você **callglTexGen**. Se M for insatisfatório ou o singular, as coordenadas de textura geradas pela função resultante poderão ser imprecisas ou indefinidas.

Observe que os valores no *param* definem um plano de referência em coordenadas de olho. A matriz modelview que é aplicada a elas pode não ser a mesma em vigor quando os vértices do polígono são transformados. Essa função estabelece um campo de coordenadas de textura que pode produzir linhas de delimitação dinâmicas sobre a movimentação de objetos.

Se *pname* é \_ \_ o mapa de Sphere GL e *coord* é GL \_ s ou GL \_ t, as coordenadas de textura s e t são geradas da seguinte maneira. Deixe u o vetor de unidade apontando da origem para o vértice do polígono (em coordenadas de olho). Deixe que n seja o normal atual, depois da transformação para as coordenadas de olho. Let f = (FX () AF () FZ) T ser o vetor de reflexão de forma que

![Equação mostrando o vetor de reflexo como uma função de vetor de unidade e normal atual.](images/tex05.png)

Por fim, deixe

![Equação mostrando m como uma função de vetor de reflexo.](images/tex07.png)

Em seguida, os valores atribuídos às coordenadas de textura i e t são

![Equação mostrando valores atribuídos às coordenadas de textura i e t.](images/tex06.png)

Você pode habilitar ou desabilitar uma função de geração de coordenada de textura usando [**glEnable**](glenable.md) ou [**glDisable**](gldisable.md) com um dos nomes de coordenadas de textura simbólicas (GL de textura de recriação de, GL, Reportador de textura do GL \_ \_ \_ \_ \_ \_ T \_ ou GL Texture Gen \_ \_ \_ \_ \_ p) como o argumento. Quando essa função é habilitada, a coordenada de textura especificada é computada de acordo com a função de geração associada a essa coordenada. Quando essa função é desabilitada, os vértices subsequentes usam a coordenada de textura especificada do conjunto atual de coordenadas de textura. Inicialmente, todas as funções de geração de textura são definidas como o olho de GL \_ \_ linear e estão desabilitadas. As equações do plano s são (1, 0, 0, 0); ambas as equações do plano t são (0, 1, 0, 0); e todas as equações do plano r e q são (0, 0, 0, 0).

As funções a seguir recuperam informações relacionadas ao glTexGen:

<dl>

[**glGetTexGen**](glgettexgen.md)  
[**glIsEnabled**](glisenabled.md) com Argument GL \_ Texture \_ Gen \_ S  
[**glIsEnabled**](glisenabled.md) com Argument GL \_ Texture \_ Gen \_ T  
[**glIsEnabled**](glisenabled.md) com o argumento GL \_ Texture \_ Gen \_ R  
[**glIsEnabled**](glisenabled.md) com Argument GL \_ Texture \_ Gen \_ Q  
</dl>

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

 

 





