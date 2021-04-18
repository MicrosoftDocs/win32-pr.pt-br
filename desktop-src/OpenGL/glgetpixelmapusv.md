---
title: função glGetPixelMapusv (GL. h)
description: As funções glGetPixelMapfv, glGetPixelMapuiv e glGetPixelMapusv retornam o mapa de pixel especificado. | função glGetPixelMapusv (GL. h)
ms.assetid: 68b71f9b-5666-4183-aeb8-4c9f09bc5d9c
keywords:
- função glGetPixelMapusv OpenGL
topic_type:
- apiref
api_name:
- glGetPixelMapusv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a91d7784288c7a98b82814cdaadb352e7ff5b5c3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105756397"
---
# <a name="glgetpixelmapusv-function"></a>função glGetPixelMapusv

As funções [**glGetPixelMapfv**](glgetpixelmapfv.md), [**glGetPixelMapuiv**](glgetpixelmapuiv.md)e **glGetPixelMapusv** retornam o mapa de pixel especificado.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glGetPixelMapusv(
   GLenum   map,
   GLushort *values
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*map* 
</dt> <dd>

O nome do mapa de pixel a ser retornado. Os valores aceitos são o mapa do pixel GL i, o mapa de \_ \_ \_ \_ \_ \_ pixel GL \_ \_ s \_ para \_ s, o \_ \_ \_ RESIDER pixel MAP i \_ para \_ R, GL \_ pixel \_ map \_ i para G, GL pixel MAP i para b, GL pixel MAP i para \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ a, GL pixel map \_ \_ \_ R \_ para \_ r, GL pixel \_ \_ map \_ G \_ to \_ G, GL pixel \_ \_ map \_ B \_ para \_ b \_ \_ \_ \_ \_

</dd> <dt>

*os* 
</dt> <dd>

Retorna o conteúdo do mapa de pixel.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | o *mapa* não era um valor aceito.<br/>                                                                                           |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

Consulte [**glPixelMap**](glpixelmap.md) para obter uma descrição dos valores aceitáveis para o parâmetro *MAP* . A função **glGetPixelMap** retorna em *valores* o conteúdo do mapa de pixel especificado no *mapa*. Use mapas de pixel durante a execução de [**glReadPixels**](glreadpixels.md), [**glDrawPixels**](gldrawpixels.md), [**glCopyPixels**](glcopypixels.md), [**glTexImage1D**](glteximage1d.md)e [**glTexImage2D**](glteximage2d.md) para mapear índices de cores, índices de estêncil, componentes de cores e componentes de profundidade para outros valores.

Valores inteiros não assinados, se solicitados, são mapeados linearmente da representação interna fixa ou de ponto flutuante, de modo que 1,0 é mapeado para o maior valor inteiro representável e 0,0 é mapeado para zero. Os valores inteiros sem sinal de retorno serão indefinidos se o valor do mapa não estava no intervalo de \[ 0, 1 \] .

Para determinar o tamanho necessário do *mapa*, chame [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com a constante simbólica apropriada.

Se um erro for gerado, nenhuma alteração será feita no conteúdo dos *valores*.

As funções a seguir recuperam informações relacionadas ao **glGetPixelMap**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com Argument GL \_ pixel \_ mapa \_ i \_ i \_ \_ size

**glGet** com o argumento GL \_ pixel \_ mapa \_ S para o \_ \_ \_ tamanho s

**glGet** com Argument GL \_ pixel \_ mapa \_ I \_ para \_ R \_ tamanho

**glGet** com Argument GL \_ pixel \_ mapa \_ I \_ para \_ G \_ tamanho

**glGet** com Argument GL \_ pixel \_ mapa \_ I \_ para \_ o \_ tamanho B

**glGet** com Argument GL \_ pixel \_ mapa \_ I \_ para \_ um \_ tamanho

**glGet** com argumento GL \_ pixel \_ mapa \_ r \_ para \_ r \_ tamanho

**glGet** com Argument GL \_ o \_ mapa \_ \_ de pixel de tamanho de g a \_ G \_

**glGet** com Argument GL \_ pixel \_ mapa \_ b \_ para \_ B \_ tamanho

**glGet** com Argument GL \_ pixel \_ Mapear \_ um \_ para \_ um \_ tamanho

tabela de mapa de pixels de **glGet** com Argument GL \_ Max \_ \_ \_

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

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glPixelMap**](glpixelmap.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> </dl>

 

 





