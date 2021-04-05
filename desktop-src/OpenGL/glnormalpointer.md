---
title: função glNormalPointer (GL. h)
description: A função glNormalPointer define uma matriz de Normals.
ms.assetid: 6ffb0522-87cc-4be1-a5b1-f6fd30e04b43
keywords:
- função glNormalPointer OpenGL
topic_type:
- apiref
api_name:
- glNormalPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c2f3abbfbd989351af647557ec64f8ee3172dc5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919188"
---
# <a name="glnormalpointer-function"></a>função glNormalPointer

A função **glNormalPointer** define uma matriz de Normals.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glNormalPointer(
         GLenum  type,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*tipo* 
</dt> <dd>

O tipo de dados de cada coordenada na matriz usando as seguintes constantes simbólicas: GL \_ byte, GL \_ short, GL \_ int, GL \_ float e GL \_ Double.

</dd> <dt>

*Stride* 
</dt> <dd>

O deslocamento de byte entre os Normals consecutivos. Quando *Stride* é zero, os normais são empacotados rigidamente na matriz.

</dd> <dt>

*ponteiro* 
</dt> <dd>

Um ponteiro para o primeiro normal na matriz.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | o *tipo* não era um valor aceito.<br/> |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | *Stride* ou *Count* era negativo.<br/> |



## <a name="remarks"></a>Comentários

A função **glNormalPointer** especifica o local e os dados de uma matriz de Normals a serem usados durante a renderização. O parâmetro de *tipo* especifica o tipo de dados de cada coordenada normal. O parâmetro *Stride* determina o deslocamento de bytes de um normal para o próximo, habilitando a embalagem de vértices e atributos em uma única matriz ou armazenamento em matrizes separadas. Em algumas implementações, armazenar os vértices e os atributos em uma única matriz pode ser mais eficiente do que usar matrizes separadas; consulte [**glInterleavedArrays**](glinterleavedarrays.md) para obter detalhes.

Uma matriz normal é habilitada quando você especifica a \_ constante de matriz do GL normal \_ com [**glEnableClientState**](glenableclientstate.md). Quando habilitado, [**glDrawArrays**](gldrawarrays.md), [**glDrawElements**](gldrawelements.md) e [**glArrayElement**](glarrayelement.md) usam a matriz normal. Por padrão, a matriz normal está desabilitada.

Você não pode incluir **glNormalPointer** em listas de exibição.

Quando você especifica uma matriz normal usando **glNormalPointer**, os valores de todos os parâmetros de matriz normais da função são salvos em um estado do lado do cliente. Como os parâmetros de matriz normais são salvos em um estado do lado do cliente, seus valores não são salvos nem restaurados por [**glPushAttrib**](glpushattrib.md) e [**glPopAttrib**](glpopattrib.md).

Embora nenhum erro seja gerado quando você chama **glNormalPointer** nos pares [**glBegin**](glbegin.md) e [**glEnd**](glend.md) , os resultados são indefinidos.

As funções a seguir estão associadas a **glNormalPointer**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL a \_ \_ matriz normal \_ Stride

 \_ \_ contagem de matrizes glGet com Argument GL normal \_

**glGet** com o argumento \_ GL \_ normal \_ tipo de matriz

 \_ \_ ponteiro de matriz normal glGetPointerv com Argument GL \_

[**glIsEnabled**](glisenabled.md) com o Argument GL \_ normal \_ array

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

[**glDrawElements**](gldrawelements.md)
</dt> <dt>

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glGetPointerv**](glgetpointerv.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glInterleavedArrays**](glinterleavedarrays.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> <dt>

[**glGetString**](glgetstring.md)
</dt> </dl>

 

 





