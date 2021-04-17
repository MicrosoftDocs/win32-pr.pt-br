---
title: função glShadeModel (GL. h)
description: A função glShadeModel seleciona sombreamento simples ou suave.
ms.assetid: 52985ad7-1d6c-48fc-8f1e-4eb2c0324c8e
keywords:
- função glShadeModel OpenGL
topic_type:
- apiref
api_name:
- glShadeModel
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 142ac518c91c6378f1606235e25502be8c06dd6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105754312"
---
# <a name="glshademodel-function"></a>função glShadeModel

A função **glShadeModel** seleciona sombreamento simples ou suave.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glShadeModel(
   GLenum mode
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*mode* 
</dt> <dd>

Um valor simbólico que representa uma técnica de sombreamento. Os valores aceitos são o GL \_ Flat e GL \_ Smooth. O padrão é o GL \_ Smooth.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | o *modo* era um valor diferente de GL \_ GLAT ou GL \_ Smooth.<br/>                                                                      |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

Os primitivos OpenGL podem ter um sombreamento simples ou suave. O sombreamento suave, o padrão, faz com que as cores computadas dos vértices sejam interpoladas conforme o primitivo é rasterizado, normalmente atribuindo cores diferentes a cada fragmento de pixel resultante. O sombreamento simples seleciona a cor computada de apenas um vértice e o atribui a todos os fragmentos de pixel gerados pela rasterização de um único primitivo. Em ambos os casos, a cor computada de um vértice é o resultado da iluminação, se a iluminação estiver habilitada ou se for a cor atual no momento em que o vértice foi especificado, se a iluminação estiver desabilitada.

Sombreamento simples e suaves são indistinguíveis para pontos. Contando vértices e primitivas de um, iniciando quando [**glBegin**](glbegin.md) é emitido, cada segmento de linha com sombreamento simples *que* recebe a cor computada do vértice *i* + 1, seu segundo vértice. Contando de forma semelhante a uma, cada polígono com sombreamento simples recebe a cor computada do vértice listado na tabela a seguir. Este é o último vértice para especificar o polígono em todos os casos, exceto polígonos únicos, em que o primeiro vértice especifica a cor de sombreamento simples.



| Tipo primitivo de polígono i | Vértice   |
|-----------------------------|----------|
| Polígono único (*I*= 1)      | 1        |
| Faixa de triângulo              | *i* + 2  |
| Ventilador de triângulo                | *i* + 2  |
| Triângulo independente        | 3 *I*     |
| Faixa quádrupla                  | 2 *i* + 2 |
| Quádruplo independente            | 4 *I*     |



 

Sombreamento simples e suaves são especificados por **glShadeModel** com o *modo* definido como GL \_ Flat e GL \_ Smooth, respectivamente.

A função a seguir recupera informações relacionadas a **glShadeModel**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o \_ modelo de sombra do argumento GL \_

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

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glLight**](gllight-functions.md)
</dt> <dt>

[**glLightModel**](gllightmodel-functions.md)
</dt> </dl>

 

 





