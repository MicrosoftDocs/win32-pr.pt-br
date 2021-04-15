---
title: função glGetTexParameteriv (GL. h)
description: As funções glGetTexParameterfv e glGetTexParameteriv retornam valores de parâmetro de textura. | função glGetTexParameteriv (GL. h)
ms.assetid: b89d10f1-5e30-4d25-8953-fbd59781fdac
keywords:
- função glGetTexParameteriv OpenGL
topic_type:
- apiref
api_name:
- glGetTexParameteriv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ca78983594487fd22917c15a5b211c529b6b14d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105753736"
---
# <a name="glgettexparameteriv-function"></a>função glGetTexParameteriv

As funções [**glGetTexParameterfv**](glgettexparameterfv.md) e **glGetTexParameteriv** retornam valores de parâmetro de textura.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glGetTexParameteriv(
   GLenum target,
   GLenum pname,
   GLint  *params
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*destino* 
</dt> <dd>

O nome simbólico da textura de destino. A textura GL \_ \_ 1D e GL de \_ textura \_ 2D são aceitas.

</dd> <dt>

*pname* 
</dt> <dd>

O nome simbólico de um parâmetro de textura. Os valores a seguir são aceitos.



| Valor                                                                                                                                                                                         | Significado                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span><dl> <dt>**\_ \_ filtro mag de textura GL \_**</dt> </dl>       | Retorna o filtro de ampliação de textura de valor único, uma constante simbólica.<br/>                                                                                                                                                                                                                                                                                                      |
| <span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span><dl> <dt>**\_filtro de \_ mínimo de textura GL \_**</dt> </dl>       | Retorna o filtro de minificação de textura de valor único, uma constante simbólica.<br/>                                                                                                                                                                                                                                                                                                       |
| <span id="GL_TEXTURE_WRAP_S"></span><span id="gl_texture_wrap_s"></span><dl> <dt>**\_S de \_ encapsulamento de textura GL \_**</dt> </dl>                   | Retorna a função de disposição de valor único para as coordenadas de textura *s*, uma constante simbólica.<br/>                                                                                                                                                                                                                                                                                      |
| <span id="GL_TEXTURE_WRAP_T"></span><span id="gl_texture_wrap_t"></span><dl> <dt>**\_ \_ & encapsulamento de textura GL \_**</dt> </dl>                   | Retorna a função de disposição de valor único para a coordenada de textura *t*, uma constante simbólica.<br/>                                                                                                                                                                                                                                                                                      |
| <span id="GL_TEXTURE_BORDER_COLOR"></span><span id="gl_texture_border_color"></span><dl> <dt>**\_cor da \_ borda da textura GL \_**</dt> </dl> | Retorna quatro números inteiros ou de ponto flutuante que compõem a cor RGBA da borda da textura. Os valores de ponto flutuante são retornados no intervalo de \[ 0, 1 \] . Os valores inteiros são retornados como um mapeamento linear da representação de ponto flutuante interno, de modo que 1,0 é mapeado para o inteiro representável mais positivo e-1,0 é mapeado para o número de inteiro reapresentável mais negativo.<br/> |
| <span id="GL_TEXTURE_PRIORITY"></span><span id="gl_texture_priority"></span><dl> <dt>**\_prioridade de textura GL \_**</dt> </dl>              | Retorna a prioridade de residência da textura de destino (ou a textura nomeada associada a ela). O valor inicial é 1. Consulte [**glPrioritizeTextures**](glprioritizetextures.md).<br/>                                                                                                                                                                                                        |
| <span id="GL_TEXTURE_RESIDENT"></span><span id="gl_texture_resident"></span><dl> <dt>**de \_ textura GL \_ residente**</dt> </dl>              | Retorna o status de residência da textura de destino. Se o valor retornado em params for GL \_ true, a textura será residente na memória de textura. Consulte [**glAreTexturesResident**](glaretexturesresident.md).<br/>                                                                                                                                                                           |



 

</dd> <dt>

*params* 
</dt> <dd>

Retorna os parâmetros de textura.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | o *destino* ou o *nome* não era um valor aceito.<br/>                                                                              |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

A função **glGetTexParameter** retorna em *params* o valor ou os valores do parâmetro de textura especificado como *pname*. O parâmetro de *destino* define a textura de destino, ou seja, GL \_ textura \_ 1D ou GL \_ \_ de textura 2D, para especificar um texturing unidimensional ou bidimensional. O parâmetro *pname* aceita os mesmos símbolos que [**glTexParameter**](gltexparameter-functions.md), com as mesmas interpretações.

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

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





