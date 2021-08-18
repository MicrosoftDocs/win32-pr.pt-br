---
title: Função glIndexPointer (Gl.h)
description: A função glIndexPointer define uma matriz de índices de cores.
ms.assetid: b435d950-1f87-4041-93e4-f1f8786cabdb
keywords:
- Função glIndexPointer OpenGL
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
ms.openlocfilehash: e27502420121f7373af5425e8aadffe3641ddec539a4521fe6c6bf55e6d807d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012144"
---
# <a name="glindexpointer-function"></a>Função glIndexPointer

A **função glIndexPointer** define uma matriz de índices de cores.

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

O tipo de dados de cada índice de cores na matriz usando as seguintes constantes simbólicas: GL \_ SHORT, GL \_ INT, GL \_ FLOAT, GL \_ DOUBLE.

</dd> <dt>

*Passo* 
</dt> <dd>

O deslocamento de byte entre índices de cores consecutivos. Quando *stride* é zero, os índices de cores são firmemente empacotados na matriz.

</dd> <dt>

*ponteiro* 
</dt> <dd>

Um ponteiro para o primeiro índice de cores na matriz.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela [**função glGetError.**](glgeterror.md)



| Nome                                                                                              | Significado                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>  | *type* não era um valor aceito.<br/> |
| <dl> <dt>**VALOR INVÁLIDO DE GL \_ \_**</dt> </dl> | *stride* ou *count* era negativo.<br/> |



## <a name="remarks"></a>Comentários

A **função glIndexPointer** especifica o local e os dados de uma matriz de índices de cores a usar ao renderizar. O  parâmetro type especifica o tipo de  dados de cada índice de cores e stride determina o deslocamento de byte de um índice de cor para o próximo, permitindo o empacotamento de vértices e atributos em uma única matriz ou armazenamento em matrizes separadas. Em algumas implementações, armazenar os vértices e atributos em uma única matriz pode ser mais eficiente do que usar matrizes separadas. Para obter mais informações, [**consulte glInterleavedArrays**](glinterleavedarrays.md).

Uma matriz de índice de cores é habilitada quando você especifica a constante GL \_ INDEX \_ ARRAY com [**glEnableClientState**](glenableclientstate.md). Quando habilitada, [**glDrawArrays**](gldrawarrays.md) e [**glArrayElement**](glarrayelement.md) usam a matriz de índice de cores. Por padrão, a matriz de índice de cores está desabilitada.

Não é possível incluir **glIndexPointer em** listas de exibição.

Quando você especifica uma matriz de índice de cores usando **glIndexPointer**, os valores de todos os parâmetros da matriz de índice de cores da função são salvos em um estado do lado do cliente e os elementos da matriz estática podem ser armazenados em cache. Como os parâmetros da matriz de índice de cores são o estado do lado do cliente, seus valores não são salvos nem restaurados por [**glPushAttrib**](glpushattrib.md) e **glPopAttrib.**

Embora nenhum erro seja gerado quando você chama **glIndexPointer** em pares [**glBegin**](glbegin.md) e **glEnd,** os resultados são indefinido.

As funções a seguir recuperam informações relacionadas **a glIndexPointer**:

[**glIsEnabled com**](glisenabled.md) o argumento GL \_ INDEX \_ ARRAY

[**glGet com**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) o argumento GL \_ INDEX ARRAY \_ \_ STRIDE

**glGet** com o argumento GL \_ INDEX \_ ARRAY \_ COUNT

**glGet** com o argumento GL \_ INDEX \_ ARRAY \_ TYPE

**glGet com** o argumento GL \_ INDEX ARRAY \_ \_ SIZE

[**glGetPointerv com**](glgetpointerv.md) o argumento GL \_ INDEX ARRAY \_ \_ POINTER

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

 

 





