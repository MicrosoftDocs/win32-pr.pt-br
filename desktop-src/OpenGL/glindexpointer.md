---
title: função glIndexPointer (GL. h)
description: A função glIndexPointer define uma matriz de índices de cores.
ms.assetid: b435d950-1f87-4041-93e4-f1f8786cabdb
keywords:
- função glIndexPointer OpenGL
topic_type:
- apiref
api_name:
- glIndexPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cca6858d7d1e3f13e4155bd40307a53b22e80a56
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454661"
---
# <a name="glindexpointer-function"></a>função glIndexPointer

A função **glIndexPointer** define uma matriz de índices de cores.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glIndexPointer(
         GLenum  type,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*tipo* 
</dt> <dd>

O tipo de dados de cada índice de cor na matriz usando as seguintes constantes simbólicas: GL \_ short, GL \_ int, GL \_ float, GL \_ Double.

</dd> <dt>

*Stride* 
</dt> <dd>

O deslocamento de byte entre os índices de cor consecutivos. Quando *Stride* é zero, os índices de cores são totalmente empacotados na matriz.

</dd> <dt>

*ponteiro* 
</dt> <dd>

Um ponteiro para o primeiro índice de cor na matriz.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                              | Significado                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>  | o *tipo* não era um valor aceito.<br/> |
| <dl> <dt>**\_valor inválido do GL \_**</dt> </dl> | *Stride* ou *Count* era negativo.<br/> |



## <a name="remarks"></a>Comentários

A função **glIndexPointer** especifica o local e os dados de uma matriz de índices de cores a serem usados durante a renderização. O parâmetro de *tipo* especifica o tipo de dados de cada índice de cor e *Stride* determina o deslocamento de byte de um índice de cor para o próximo, habilitando a embalagem de vértices e atributos em uma única matriz ou armazenamento em matrizes separadas. Em algumas implementações, armazenar os vértices e os atributos em uma única matriz pode ser mais eficiente do que usar matrizes separadas. Para obter mais informações, consulte [**glInterleavedArrays**](glinterleavedarrays.md).

Uma matriz de índice de cor é habilitada quando você especifica a \_ constante de matriz de índice GL \_ com [**glEnableClientState**](glenableclientstate.md). Quando habilitado, [**glDrawArrays**](gldrawarrays.md) e [**glArrayElement**](glarrayelement.md) usam a matriz de índice de cor. Por padrão, a matriz de índice de cores está desabilitada.

Você não pode incluir **glIndexPointer** em listas de exibição.

Quando você especifica uma matriz de índice de cor usando **glIndexPointer**, os valores de todos os parâmetros de matriz de índice de cor da função são salvos em um estado do lado do cliente e os elementos estáticos da matriz podem ser armazenados em cache. Como os parâmetros de matriz de índice de cor são o estado do lado do cliente, seus valores não são salvos nem restaurados por [**glPushAttrib**](glpushattrib.md) e **glPopAttrib**.

Embora nenhum erro seja gerado quando você chama **glIndexPointer** nos pares [**glBegin**](glbegin.md) e **glEnd** , os resultados são indefinidos.

As funções a seguir recuperam informações relacionadas ao **glIndexPointer**:

[**glIsEnabled**](glisenabled.md) com matriz de índice de argumento GL \_ \_

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com a matriz de índice do argumento GL \_ \_ \_ Stride

 \_ \_ contagem de matrizes de índice glGet com Argument GL \_

**glGet** com o \_ tipo de \_ matriz de índice do argumento GL \_

**glGet** com o argumento \_ GL \_ tamanho da matriz de índice \_

[](glgetpointerv.md) ponteiro de matriz de índice glGetPointerv com Argument GL \_ \_ \_

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

[**glColorPointer**](glcolorpointer.md)
</dt> <dt>

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glGetPointerv**](glgetpointerv.md)
</dt> <dt>

[**glGetString**](glgetstring.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glPushAttrib**](glpushattrib.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





