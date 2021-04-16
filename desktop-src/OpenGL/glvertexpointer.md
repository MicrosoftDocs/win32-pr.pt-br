---
title: função glVertexPointer (GL. h)
description: A função glVertexPointer define uma matriz de dados de vértice.
ms.assetid: e5f97fdc-9448-4389-8533-3855a3213feb
keywords:
- função glVertexPointer OpenGL
topic_type:
- apiref
api_name:
- glVertexPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 422dd1a7938cc5adb183ff7e17c59a8f52eb4909
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455650"
---
# <a name="glvertexpointer-function"></a>função glVertexPointer

A função **glVertexPointer** define uma matriz de dados de vértice.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glVertexPointer(
         GLint   size,
         GLenum  type,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*size* 
</dt> <dd>

O número de coordenadas por vértice. O valor do *tamanho* deve ser 2, 3 ou 4.

</dd> <dt>

*tipo* 
</dt> <dd>

O tipo de dados de cada coordenada na matriz usando as seguintes constantes simbólicas: GL \_ short, GL \_ int, GL \_ float e GL \_ Double.

</dd> <dt>

*Stride* 
</dt> <dd>

O deslocamento de bytes entre vértices consecutivos. Quando *Stride* é zero, os vértices são totalmente empacotados na matriz.

</dd> <dt>

*ponteiro* 
</dt> <dd>

Um ponteiro para a primeira coordenada do primeiro vértice na matriz.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                              | Significado                                       |
|---------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**\_valor inválido do GL \_**</dt> </dl> | o *tamanho* não era 2, 3 ou 4. <br/>        |
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>  | o *tipo* não era um valor aceito.<br/>  |
| <dl> <dt>**\_valor inválido do GL \_**</dt> </dl> | *Stride* ou *Count* era negativo. <br/> |



## <a name="remarks"></a>Comentários

A função **glVertexPointer** especifica o local e os dados de uma matriz de coordenadas de vértice a ser usada durante a renderização. O parâmetro *size* especifica o número de coordenadas por vértice. O parâmetro de *tipo* especifica o tipo de dados de cada coordenada de vértice. O parâmetro *Stride* determina o deslocamento de bytes de um vértice para o próximo, habilitando a embalagem de vértices e atributos em uma única matriz ou armazenamento em matrizes separadas. Em algumas implementações, armazenar os vértices e atributos em uma única matriz pode ser mais eficiente do que usar matrizes separadas (consulte [**glInterleavedArrays**](glinterleavedarrays.md)).

Uma matriz de vértice é habilitada quando você especifica a \_ constante de matriz de vértice GL \_ com [**glEnableClientState**](glenableclientstate.md). Quando habilitado, [**glDrawArrays**](gldrawarrays.md), [**glDrawElements**](gldrawelements.md)e [**glArrayElement**](glarrayelement.md) usam a matriz de vértice. Por padrão, a matriz de vértices está desabilitada.

Você não pode incluir **glVertexPointer** em listas de exibição.

Quando você especifica uma matriz de vértice usando **glVertexPointer**, os valores de todos os parâmetros de matriz de vértice da função são salvos em um estado do lado do cliente e os elementos estáticos da matriz podem ser armazenados em cache. Como os parâmetros de matriz de vértice são um estado do lado do cliente, seus valores não são salvos nem restaurados por [**glPushAttrib**](glpushattrib.md) e **glPopAttrib**.

Embora nenhum erro seja gerado se você chamar **glVertexPointer** nos pares [**glBegin**](glbegin.md) e [**glEnd**](glend.md) , os resultados serão indefinidos.

As funções a seguir recuperam informações relacionadas ao **glVertexPointer**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o \_ tamanho da \_ matriz de vértice GL do argumento \_

**glGet** com Stride de \_ matriz de vértice do Argument GL \_ \_

 \_ \_ contagem de matrizes de vértice glGet com Argument GL \_

**glGet** com tipo de \_ matriz de vértice GL do argumento \_ \_

[](glgetpointerv.md) ponteiro de matriz de vértice glGetPointerv com Argument GL \_ \_ \_

[**glIsEnabled**](glisenabled.md) com matriz de vértice do Argument GL \_ \_

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

[**glEnableClientState**](glenableclientstate.md)
</dt> <dt>

[**glGetPointerv**](glgetpointerv.md)
</dt> <dt>

[**glGetString**](glgetstring.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> </dl>

 

 





