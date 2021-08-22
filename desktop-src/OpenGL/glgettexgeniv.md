---
title: Função glGetTexGeniv (Gl.h)
description: As funções glGetTexGendv, glGetTexGenfv e glGetTexGeniv retornam parâmetros de geração de coordenadas de textura. | Função glGetTexGeniv (Gl.h)
ms.assetid: 62c481d1-4862-43bb-9319-5a282c4e47d3
keywords:
- Função glGetTexGeniv OpenGL
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
ms.openlocfilehash: d6eb9fbca41f8ad9fe9564c45f3ece21af58e5e16b7bb4ac85d0f6b1d2b428bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493766"
---
# <a name="glgettexgeniv-function"></a>Função glGetTexGeniv

As [**funções glGetTexGendv**](glgettexgendv.md), [**glGetTexGenfv**](glgettexgenfv.md)e **glGetTexGeniv** retornam parâmetros de geração de coordenadas de textura.

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

*Coord* 
</dt> <dd>

Uma coordenada de textura. Deve ser GL \_ S, GL \_ T, GL \_ R ou GL \_ Q.

</dd> <dt>

*Pname* 
</dt> <dd>

O nome simbólico dos valores a serem retornados. Deve ser GL TEXTURE GEN MODE ou o nome de uma das equações do plano de geração de \_ \_ \_ textura: GL \_ OBJECT PLANE ou GL EYE \_ \_ \_ PLANE. Esses valores são os valores a seguir.



| Valor                                                                                                                                                                             | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_GEN_MODE"></span><span id="gl_texture_gen_mode"></span><dl> <dt>**MODO GL \_ TEXTURE \_ \_ GEN**</dt> </dl> | O *parâmetro params* retorna a função de geração de textura com valor único, uma constante simbólica.<br/>                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_OBJECT_PLANE"></span><span id="gl_object_plane"></span><dl> <dt>**PLANO \_ DE \_ OBJETO GL**</dt> </dl>              | O *parâmetro params* retorna os quatro coeficientes de equação de plano que especificam a geração de coordenada linear do objeto. Os valores inteiros, quando solicitados, são mapeados diretamente da representação de ponto flutuante interno.<br/>                                                                                                                                                                                                                                    |
| <span id="GL_EYE_PLANE"></span><span id="gl_eye_plane"></span><dl> <dt>**PLANO \_ DE OLHO \_ GL**</dt> </dl>                       | O *parâmetro params* retorna os quatro coeficientes de equação de plano que especificam a geração da coordenada linear do olho. Os valores inteiros, quando solicitados, são mapeados diretamente da representação de ponto flutuante interno. Os valores retornados são aqueles mantidos em coordenadas de olho. Eles não são iguais aos valores especificados usando [**glTexGen**](gltexgen-functions.md), a menos que a matriz modelview tenha sido identificada no momento em que **glTexGen** foi chamado.<br/> |



 

</dd> <dt>

*params* 
</dt> <dd>

Retorna os dados solicitados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela [**função glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *coord* ou *pname* não era um valor aceito.<br/>                                                                              |
| <dl> <dt>**OPERAÇÃO \_ GL \_ INVÁLIDA**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd.**](glend.md)<br/> |



## <a name="remarks"></a>Comentários

A **função glGetTexGen** retorna *em parâmetros selecionados params* de uma função de geração de coordenadas de textura que você especificou com **glTexGen.** O *parâmetro coord* nomeia uma das coordenadas de textura (*s*, *t*, *r*, *q*), usando a constante simbólica GL \_ S, GL \_ T, GL \_ R ou GL \_ Q.

Se um erro for gerado, nenhuma alteração será feita no conteúdo *de params*.

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

[**glTexGen**](gltexgen-functions.md)
</dt> </dl>

 

 





