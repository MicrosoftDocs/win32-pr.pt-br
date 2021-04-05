---
title: função glDrawArrays (GL. h)
description: A função glDrawArrays especifica vários primitivos a serem renderizados.
ms.assetid: 6ebd467b-5a63-43e4-b3fd-242c704d7d13
keywords:
- função glDrawArrays OpenGL
topic_type:
- apiref
api_name:
- glDrawArrays
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88b20cf3a3e3b2c96a8172f53f8126815efe16d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918581"
---
# <a name="gldrawarrays-function"></a>função glDrawArrays

A função **glDrawArrays** especifica vários primitivos a serem renderizados.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glDrawArrays(
   GLenum  mode,
   GLint   first,
   GLsizei count
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*mode* 
</dt> <dd>

O tipo de primitivas a ser renderizada. As constantes a seguir especificam tipos aceitáveis: os \_ pontos GL, a \_ faixa de linha gl, o \_ \_ \_ loop de linha gl, \_ as linhas GL, a \_ \_ faixa de triângulo GL, o \_ \_ ventilador do triângulo GL, os \_ triângulos GL, o GL \_ Quad strip, o GL \_ \_ quads e o \_ Polygon GL.

</dd> <dt>

*first* 
</dt> <dd>

O índice inicial nas matrizes habilitadas.

</dd> <dt>

*contagem* 
</dt> <dd>

O número de índices a serem renderizados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valor inválido do GL \_**</dt> </dl>     | a *contagem* era negativa.<br/>                                                                                                      |
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | o *modo* não era um valor aceito.<br/>                                                                                          |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

Com o **glDrawArrays**, você pode especificar vários primitivos geométricos para renderização. Em vez de chamar funções OpenGL separadas para passar cada vértice, normal ou cor individual, você pode especificar matrizes separadas de vértices, normais e cores para definir uma sequência de primitivas (o mesmo tipo) com uma única chamada para **glDrawArrays**.

Quando você chama **glDrawArrays**, os elementos sequenciais de *contagem* de cada matriz habilitada são usados para construir uma sequência de primitivos geométricos, começando com o *primeiro* elemento. O parâmetro *Mode* especifica que tipo de primitiva deve ser construída e como usar os elementos da matriz para construir os primitivos.

Após o retorno de **glDrawArrays** , os valores dos atributos de vértice que são modificados por **glDrawArrays** são indefinidos. Por exemplo, se a \_ \_ matriz de cores GL estiver habilitada, o valor da cor atual será indefinido após o retorno de **glDrawArrays** . Atributos não modificados por **glDrawArrays** permanecem definidos. Quando \_ \_ a matriz de vértice GL não está habilitada, nenhum primitivo Geométrico é gerado, mas os atributos correspondentes às matrizes habilitadas são modificados.

Você pode incluir **glDrawArrays** em listas de exibição. Quando você inclui **glDrawArrays** em uma lista de exibição, os dados de matriz necessários, determinados pelos ponteiros de matriz e os habilitados, são gerados e inseridos na lista de exibição. Os valores de ponteiros de matriz e de habilitações são determinados durante a criação de listas de exibição.

Você pode ler dados de matriz estática a qualquer momento. Se qualquer elemento estático da matriz for modificado e a matriz não for especificada novamente, os resultados de todas as chamadas subsequentes para **glDrawArrays** serão indefinidos.

Embora nenhum erro seja gerado quando você especifica uma matriz mais de uma vez nos pares [**glBegin**](glbegin.md) e [**glend**](glend.md) , os resultados são indefinidos.

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

[**glArrayElement**](glarrayelement.md)
</dt> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glColorPointer**](glcolorpointer.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGetPointerv**](glgetpointerv.md)
</dt> <dt>

[**glGetString**](glgetstring.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





