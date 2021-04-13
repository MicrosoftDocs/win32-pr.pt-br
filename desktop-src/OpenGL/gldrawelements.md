---
title: função glDrawElements (GL. h)
description: A função glDrawElements processa primitivos dos dados da matriz.
ms.assetid: fb433294-106e-48d5-ad49-4434934fe072
keywords:
- função glDrawElements OpenGL
topic_type:
- apiref
api_name:
- glDrawElements
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 976e779235dc330467d610406156534b5e72841d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499482"
---
# <a name="gldrawelements-function"></a>função glDrawElements

A função **glDrawElements** processa primitivos dos dados da matriz.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glDrawElements(
         GLenum  mode,
         GLsizei count,
         GLenum  type,
   const GLvoid  *indices
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*mode* 
</dt> <dd>

O tipo de primitivas a ser renderizada. Ele pode assumir um dos seguintes valores simbólicos: os \_ pontos GL, a \_ faixa de linha gl, o \_ \_ \_ loop de linha gl, \_ as linhas GL, a \_ \_ faixa de triângulo GL, o \_ \_ ventilador do triângulo GL, os \_ triângulos GL, o GL \_ Quad strip, o GL \_ \_ quads e o \_ Polygon GL.

</dd> <dt>

*contagem* 
</dt> <dd>

O número de elementos a serem renderizados.

</dd> <dt>

*tipo* 
</dt> <dd>

O tipo dos valores em índices. Deve ser um de GL \_ não assinado, GL não \_ assinado, \_ \_ curto ou GL \_ não assinado \_ int.

</dd> <dt>

*índices* 
</dt> <dd>

Um ponteiro para o local onde os índices são armazenados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | o *modo* não era um valor aceito.<br/>                                                                                          |
| <dl> <dt>**\_valor inválido do GL \_**</dt> </dl>     | *Count* era um valor negativo.<br/>                                                                                              |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

A função **glDrawElements** permite que você especifique vários primitivos geométricos com muito poucas chamadas de função. Em vez de chamar uma função OpenGL para passar cada vértice, normal ou cor individual, você pode especificar matrizes separadas de vértices, normais e cores com antecedência e usá-las para definir uma sequência de primitivas (todas do mesmo tipo) com uma única chamada para **glDrawElements**.

Quando você chama a função **glDrawElements** , ela usa elementos sequenciais de *contagem* de *índices* para construir uma sequência de primitivos geométricos. O parâmetro *Mode* especifica que tipo de primitivas são construídos e como os elementos de matriz são usados para construir esses primitivos. Se a \_ matriz de vértice GL \_ não estiver habilitada, nenhum primitivo Geométrico será gerado.

Os atributos de vértice que são modificados por **glDrawElements** têm um valor não especificado após o retorno de **glDrawElements** . Por exemplo, se a \_ \_ matriz de cores GL estiver habilitada, o valor da cor atual será indefinido depois que **glDrawElements** for executado. Os atributos que não são modificados permanecem inalterados.

Você pode incluir a função **glDrawElements** em listas de exibição. Quando **glDrawElements** é incluído em uma lista de exibição, os dados de matriz necessários (determinados pelos ponteiros de matriz e ativações) também são inseridos na lista de exibição. Como os ponteiros de matriz e ativações são variáveis de estado do lado do cliente, seus valores afetam as listas de exibição quando as listas são criadas, não quando as listas são executadas.

> [!Note]  
> A função **glDrawElements** só está disponível no OpenGL versão 1,1 ou posterior.

 

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

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGetPointerv**](glgetpointerv.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





