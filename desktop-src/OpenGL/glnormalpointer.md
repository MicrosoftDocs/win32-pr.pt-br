---
title: Função glNormalPointer (Gl.h)
description: A função glNormalPointer define uma matriz de normais.
ms.assetid: 6ffb0522-87cc-4be1-a5b1-f6fd30e04b43
keywords:
- Função glNormalPointer OpenGL
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
ms.openlocfilehash: 4f188a65a0a2bff0438188ae7521615de45341147b138a849d2fd375ed8a959b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118938405"
---
# <a name="glnormalpointer-function"></a>Função glNormalPointer

A **função glNormalPointer** define uma matriz de normais.

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

O tipo de dados de cada coordenada na matriz usando as seguintes constantes simbólicas: \_ GL BYTE, GL \_ SHORT, GL \_ INT, GL \_ FLOAT e GL \_ DOUBLE.

</dd> <dt>

*Passo* 
</dt> <dd>

O deslocamento de byte entre normais consecutivas. Quando *stride* é zero, os normais são firmemente empacotados na matriz.

</dd> <dt>

*ponteiro* 
</dt> <dd>

Um ponteiro para o primeiro normal na matriz.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela [**função glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significado                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *type* não era um valor aceito.<br/> |
| <dl> <dt>**OPERAÇÃO \_ GL \_ INVÁLIDA**</dt> </dl> | *stride* ou *count* era negativo.<br/> |



## <a name="remarks"></a>Comentários

A **função glNormalPointer** especifica o local e os dados de uma matriz de normais a ser usada ao renderizar. O *parâmetro* type especifica o tipo de dados de cada coordenada normal. O *parâmetro stride* determina o deslocamento de byte de um normal para o próximo, permitindo o empacotamento de vértices e atributos em uma única matriz ou armazenamento em matrizes separadas. Em algumas implementações, armazenar os vértices e atributos em uma única matriz pode ser mais eficiente do que usar matrizes separadas; consulte [**glInterleavedArrays para**](glinterleavedarrays.md) obter detalhes.

Uma matriz normal é habilitada quando você especifica a constante GL \_ NORMAL \_ ARRAY com [**glEnableClientState.**](glenableclientstate.md) Quando habilitado, [**glDrawArrays,**](gldrawarrays.md) [**glDrawElements**](gldrawelements.md) e [**glArrayElement**](glarrayelement.md) usam a matriz normal. Por padrão, a matriz normal está desabilitada.

Não é possível incluir **glNormalPointer em** listas de exibição.

Quando você especifica uma matriz normal usando **glNormalPointer**, os valores de todos os parâmetros de matriz normal da função são salvos em um estado do lado do cliente. Como os parâmetros de matriz normal são salvos em um estado do lado do cliente, seus valores não são salvos nem restaurados por [**glPushAttrib**](glpushattrib.md) e [**glPopAttrib.**](glpopattrib.md)

Embora nenhum erro seja gerado quando você chama **glNormalPointer** em pares [**glBegin**](glbegin.md) e [**glEnd,**](glend.md) os resultados são indefinido.

As seguintes funções estão associadas a **glNormalPointer**:

[**glGet com**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) o argumento GL \_ NORMAL ARRAY \_ \_ STRIDE

**glGet** com o argumento GL \_ NORMAL \_ ARRAY \_ COUNT

**glGet** com o argumento GL \_ NORMAL \_ ARRAY \_ TYPE

**glGetPointerv com** o argumento GL \_ NORMAL ARRAY \_ \_ POINTER

[**glIsEnabled com**](glisenabled.md) o argumento GL \_ NORMAL \_ ARRAY

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

 

 





