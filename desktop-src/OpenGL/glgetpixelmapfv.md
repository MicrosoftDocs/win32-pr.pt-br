---
title: Função glGetPixelMapfv (Gl.h)
description: As funções glGetPixelMapfv, glGetPixelMapuiv e glGetPixelMapusv retornam o mapa de pixel especificado. | Função glGetPixelMapfv (Gl.h)
ms.assetid: b09f4799-8e36-4d4f-90d8-4a8ed3d15718
keywords:
- Função glGetPixelMapfv OpenGL
topic_type:
- apiref
api_name:
- glGetPixelMapfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aacb74cb4cc08b283b500306d3a3456807cea8b0416a3ddb4fac85bfaa6ed5a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119554256"
---
# <a name="glgetpixelmapfv-function"></a>Função glGetPixelMapfv

As **funções glGetPixelMapfv**, [**glGetPixelMapuiv**](glgetpixelmapuiv.md)e [**glGetPixelMapusv**](glgetpixelmapusv.md) retornam o mapa de pixel especificado.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glGetPixelMapfv(
   GLenum  map,
   GLfloat *values
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*map* 
</dt> <dd>

O nome do mapa de pixel a ser retornada. Os valores aceitos são GL PIXEL MAP I TO I, GL PIXEL MAP S TO S, GL \_ \_ PIXEL MAP I \_ \_ TO \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ R, GL PIXEL MAP I TO G, GL PIXEL MAP I TO \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ B, GL PIXEL MAP I \_ TO \_ \_ \_ \_ A, GL PIXEL MAP R \_ \_ TO \_ \_ \_ R, GL PIXEL MAP \_ G TO G, GL PIXEL MAP \_ \_ \_ \_ \_ \_ \_ B \_ \_ \_ \_ \_ \_ \_ TO B e GL PIXEL MAP A PARA A.

</dd> <dt>

*Valores* 
</dt> <dd>

Retorna o conteúdo do mapa de pixel.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela [**função glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *map* não era um valor aceito.<br/>                                                                                           |
| <dl> <dt>**OPERAÇÃO \_ GL \_ INVÁLIDA**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd.**](glend.md)<br/> |



## <a name="remarks"></a>Comentários

Consulte [**glPixelMap**](glpixelmap.md) para ver uma descrição dos valores aceitáveis para o *parâmetro de* mapa. A **função glGetPixelMap** retorna em *valores* o conteúdo do mapa de pixel especificado no *mapa*. Use mapas de pixel durante a execução de [**glReadPixels**](glreadpixels.md), [**glDrawPixels**](gldrawpixels.md), [**glCopyPixels,**](glcopypixels.md) [**glTexImage1D**](glteximage1d.md)e [**glTexImage2D**](glteximage2d.md) para mapear índices de cores, índices de estêncil, componentes de cores e componentes de profundidade para outros valores.

Os valores inteiros sem sinal, se solicitado, são mapeados linearmente da representação interna de ponto fixo ou flutuante, de modo que 1.0 mapeia para o maior valor inteiro representável e 0,0 é mapeado para zero. Os valores inteiros sem sinal de retorno serão indefinidos se o valor do mapa não estiver no intervalo \[ 0,1 \] .

Para determinar o tamanho necessário do *mapa,* chame [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com a constante simbólica apropriada.

Se um erro for gerado, nenhuma alteração será feita no conteúdo dos *valores*.

As funções a seguir recuperam informações relacionadas **a glGetPixelMap**:

[**glGet com**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) o argumento GL \_ PIXEL MAP I TO I \_ \_ \_ \_ \_ SIZE

**glGet** com o argumento GL \_ PIXEL MAP S TO S \_ \_ \_ \_ \_ SIZE

**glGet com** o argumento GL \_ PIXEL MAP I TO R \_ \_ \_ \_ \_ SIZE

**glGet com** o argumento GL \_ PIXEL MAP I TO G \_ \_ \_ \_ \_ SIZE

**glGet com** o argumento GL \_ PIXEL MAP I TO B \_ \_ \_ \_ \_ SIZE

**glGet** com o argumento GL \_ PIXEL MAP I TO A \_ \_ \_ \_ \_ SIZE

**glGet com** o argumento GL \_ PIXEL MAP R TO R \_ \_ \_ \_ \_ SIZE

**glGet com** o argumento GL \_ PIXEL MAP G TO G \_ \_ \_ \_ \_ SIZE

**glGet** com o argumento GL \_ PIXEL MAP B TO B \_ \_ \_ \_ \_ SIZE

**glGet** com o argumento GL \_ PIXEL MAP A TO A \_ \_ \_ \_ \_ SIZE

**glGet com** o argumento GL \_ MAX PIXEL MAP \_ \_ \_ TABLE

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

 

 





