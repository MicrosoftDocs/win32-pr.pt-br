---
title: função glGetTexGeniv (GL. h)
description: As funções glGetTexGendv, glGetTexGenfv e glGetTexGeniv retornam parâmetros de geração de coordenadas de textura. | função glGetTexGeniv (GL. h)
ms.assetid: 62c481d1-4862-43bb-9319-5a282c4e47d3
keywords:
- função glGetTexGeniv OpenGL
topic_type:
- apiref
api_name:
- glGetTexGeniv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29569c84d21dbb2cd69579c78747e844cfd23ba4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105779971"
---
# <a name="glgettexgeniv-function"></a>função glGetTexGeniv

As funções [**glGetTexGendv**](glgettexgendv.md), [**glGetTexGenfv**](glgettexgenfv.md)e **glGetTexGeniv** retornam parâmetros de geração de coordenadas de textura.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glGetTexGeniv(
   GLenum coord,
   GLenum pname,
   GLint  *params
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*coord* 
</dt> <dd>

Uma coordenada de textura. Deve ser GL \_ S, GL \_ T, GL \_ R ou GL \_ Q.

</dd> <dt>

*pname* 
</dt> <dd>

O nome simbólico do (s) valor (es) a ser retornado. Deve ser o \_ \_ modo do GL Texture Gen \_ ou o nome de uma das equações do plano de geração de textura: plano de \_ objeto GL \_ ou plano de \_ olho GL \_ . Esses valores são os seguintes.



| Valor                                                                                                                                                                             | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_GEN_MODE"></span><span id="gl_texture_gen_mode"></span><dl> <dt>**modo do GL \_ Texture \_ Gen \_**</dt> </dl> | O parâmetro *params* retorna a função de geração de textura de valor único, uma constante simbólica.<br/>                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_OBJECT_PLANE"></span><span id="gl_object_plane"></span><dl> <dt>**\_plano de objeto GL \_**</dt> </dl>              | O parâmetro *params* retorna os quatro coeficientes da equação do plano que especificam a geração da coordenada linear do objeto. Os valores inteiros, quando solicitado, são mapeados diretamente da representação de ponto flutuante interna.<br/>                                                                                                                                                                                                                                    |
| <span id="GL_EYE_PLANE"></span><span id="gl_eye_plane"></span><dl> <dt>**\_plano de olho GL \_**</dt> </dl>                       | O parâmetro *params* retorna os quatro coeficientes da equação do plano que especificam a geração de coordenadas lineares. Os valores inteiros, quando solicitado, são mapeados diretamente da representação de ponto flutuante interna. Os valores retornados são aqueles mantidos em coordenadas de olho. Eles não são iguais aos valores especificados usando [**glTexGen**](gltexgen-functions.md), a menos que a matriz modelview tenha sido identificada no momento em que **glTexGen** foi chamado.<br/> |



 

</dd> <dt>

*params* 
</dt> <dd>

Retorna os dados solicitados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Name                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | *coord* ou *pname* não era um valor aceito.<br/>                                                                              |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

A função **glGetTexGen** retorna em *params* parâmetros selecionados de uma função de geração de coordenada de textura que você especificou com **glTexGen**. O parâmetro *coord* nomeia uma das coordenadas de textura (*s*, *t*, *r*, *q*), usando a constante simbólica GL \_ s, GL \_ t, GL \_ r ou GL \_ q.

Se um erro for gerado, nenhuma alteração será feita no conteúdo de *params*.

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

[**glTexGen**](gltexgen-functions.md)
</dt> </dl>

 

 





