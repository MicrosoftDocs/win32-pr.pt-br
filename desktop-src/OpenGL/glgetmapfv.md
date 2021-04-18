---
title: função glGetMapfv (GL. h)
description: As funções glGetMapdv, glGetMapfv e glGetMapiv retornam parâmetros do avaliador. | função glGetMapfv (GL. h)
ms.assetid: dc93e468-7b76-4b5d-a46c-63920ed05568
keywords:
- função glGetMapfv OpenGL
topic_type:
- apiref
api_name:
- glGetMapfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02129e9637333fb36265ce9f7b631d6cb3377d0f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105760405"
---
# <a name="glgetmapfv-function"></a>função glGetMapfv

As funções [**glGetMapdv**](glgetmapdv.md), **glGetMapfv** e [**glGetMapiv**](glgetmapiv.md) retornam parâmetros do avaliador.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glGetMapfv(
   GLenum  target,
   GLenum  query,
   GLfloat *v
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*destino* 
</dt> <dd>

O nome simbólico de um mapa. Estes são os valores aceitos: GL \_ MAP1 \_ Color \_ 4, GL \_ MAP1 \_ index, GL \_ MAP1 \_ normal, GL \_ MAP1 \_ Texture \_ coord \_ 1, GL \_ MAP1 \_ textura \_ coord \_ 2, GL \_ MAP1 \_ textura \_ coord \_ 3, GL MAP1 de \_ \_ textura \_ coord \_ 4, GL \_ MAP1 \_ vértice \_ 3, GL \_ MAP1 \_ vértice \_ 4, GL \_ map2 \_ cor \_ 4, GL \_ map2 \_ index, GL \_ map2 \_ normal, GL map2 Texture coord 1, GL map2 de \_ \_ \_ \_ \_ \_ textura \_ coord \_ 2, GL map2 de textura coord \_ \_ \_ \_ 3, GL \_ map2 \_ Texture \_ coord 4, GL map2 \_ \_ \_ vértice 3 e \_ GL \_ map2 \_ vértice \_ 4.

</dd> <dt>

*consulta* 
</dt> <dd>

Especifica qual parâmetro retornar. Os nomes simbólicos a seguir são aceitos.



| Valor                                                                                                                                             | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COEFF"></span><span id="gl_coeff"></span><dl> <dt>**\_COEFF GL**</dt> </dl>    | O parâmetro *v* retorna os pontos de controle para a função do avaliador. Os avaliadores unidimensionais retornam pontos de controle de *ordem* e avaliadores bidimensionais retornam pontos de controle *uorder* *x* *Vorder* . Cada ponto de controle consiste em um, dois, três ou quatro valores inteiros, de ponto flutuante de precisão simples ou de ponto flutuante de precisão dupla, dependendo do tipo do avaliador. Pontos de controle bidimensionais são retornados em ordem de linha principal, incrementando o índice *uorder* rapidamente e o índice *Vorder* após cada linha. Os valores inteiros, quando solicitados, são calculados arredondando os valores de ponto flutuante internos para os valores inteiros mais próximos.<br/> |
| <span id="GL_ORDER"></span><span id="gl_order"></span><dl> <dt>**\_ordem GL**</dt> </dl>    | O parâmetro *v* retorna a ordem da função do avaliador. Os avaliadores unidimensionais retornam um único valor, *ordem*. Os avaliadores bidimensionais retornam dois valores, *uorder* e *Vorder*.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="GL_DOMAIN"></span><span id="gl_domain"></span><dl> <dt>**\_domínio GL**</dt> </dl> | O parâmetro *v* retorna os parâmetros lineares de mapeamento *u* e *v* . Os avaliadores unidimensionais retornam dois valores, *u* 1 e *u* 2, conforme especificado por [**glMap1**](glmap1.md). Os avaliadores bidimensionais retornam quatro valores (*U1*, *U2*, *v1* e *v2*), conforme especificado por [**glMap2**](glmap2.md). Os valores inteiros, quando solicitados, são calculados arredondando os valores de ponto flutuante internos para os valores inteiros mais próximos.<br/>                                                                                                                                                                                                                                                  |



 

</dd> <dt>

*l* 
</dt> <dd>

Retorna os dados solicitados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | o *destino* ou a *consulta* não era um valor aceito.<br/>                                                                             |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

A função **glGetMap** retorna os parâmetros do avaliador. (As funções **glMap1** e **glMap2** definem avaliadores.) O parâmetro de *destino* especifica um mapa, a *consulta* seleciona um parâmetro específico e o *v* aponta para o armazenamento onde os valores serão retornados.

Os valores aceitáveis para o parâmetro de *destino* são descritos em [**glMap1**](glmap1.md) e [**glMap2**](glmap2.md).

Se um erro for gerado, nenhuma alteração será feita no conteúdo de *v*.

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

[**glEvalCoord**](glevalcoord-functions.md)
</dt> <dt>

[**glMap1**](glmap1.md)
</dt> <dt>

[**glMap2**](glmap2.md)
</dt> </dl>

 

 





