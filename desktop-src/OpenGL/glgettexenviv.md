---
title: função glGetTexEnviv (GL. h)
description: As funções glGetTexEnvfv e glGetTexEnviv retornam parâmetros de ambiente de textura. | função glGetTexEnviv (GL. h)
ms.assetid: c1429cb9-4392-41ef-a978-a51db66445f2
keywords:
- função glGetTexEnviv OpenGL
topic_type:
- apiref
api_name:
- glGetTexEnviv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ff222b7de0bfcd5fa50e9fa5f260e329c60c69d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105754143"
---
# <a name="glgettexenviv-function"></a>função glGetTexEnviv

As funções [**glGetTexEnvfv**](glgettexenvfv.md) e **glGetTexEnviv** retornam parâmetros de ambiente de textura.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glGetTexEnviv(
   GLenum target,
   GLenum pname,
   GLint  *params
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

O nome simbólico de um parâmetro de ambiente de textura. Os valores a seguir são aceitos.



| Valor                                                                                                                                                                                | Significado                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_ENV_MODE"></span><span id="gl_texture_env_mode"></span><dl> <dt>**modo do GL \_ Texture \_ env \_**</dt> </dl>    | O parâmetro *params* retorna o modo de ambiente de textura de valor único, uma constante simbólica.<br/>                                                                                                                                                                                                                                           |
| <span id="GL_TEXTURE_ENV_COLOR"></span><span id="gl_texture_env_color"></span><dl> <dt>**cor do GL \_ Texture \_ env \_**</dt> </dl> | O parâmetro *params* retorna quatro valores inteiros ou de ponto flutuante que são a cor do ambiente de textura. Os valores inteiros, quando solicitados, são mapeados linearmente da representação de ponto flutuante interna, de modo que 1,0 é mapeado para o inteiro representável mais positivo e-1,0 é mapeado para o inteiro representável mais negativo.<br/> |



 

</dd> <dt>

*params* 
</dt> <dd>

Retorna os dados solicitados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | *target* ou *pname* não era um valor aceito.<br/>                                                                             |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

A função **glGetTexEnv** retorna em *params* valores selecionados de um ambiente de textura que foi especificado com [**glTexEnv**](gltexenv-functions.md). O parâmetro de *destino* especifica um ambiente de textura. Atualmente, apenas um ambiente de textura é definido e tem suporte: GL \_ Texture \_ env.

O parâmetro *pname* nomeia um parâmetro de ambiente de textura específico.

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

[**glTexEnv**](gltexenv-functions.md)
</dt> </dl>

 

 





