---
title: função glColorPointer (GL. h)
description: A função glColorPointer define uma matriz de cores.
ms.assetid: 4d9d05fb-691d-4b71-b079-c42dc7103055
keywords:
- função glColorPointer OpenGL
topic_type:
- apiref
api_name:
- glColorPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9abced52f0d0664e998ad8380e33d43d4af36bcc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454856"
---
# <a name="glcolorpointer-function"></a>função glColorPointer

A função **glColorPointer** define uma matriz de cores.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glColorPointer(
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

O número de componentes por cor. O valor deve ser 3 ou 4.

</dd> <dt>

*tipo* 
</dt> <dd>

O tipo de dados de cada componente de cor em uma matriz de cores. Tipos de dados aceitáveis são especificados com as seguintes constantes: GL \_ byte, GL \_ não assinado \_ byte, GL \_ short, GL \_ não assinado \_ curto, GL \_ int, GL \_ não assinado \_ int, GL \_ float ou GL \_ Double.

</dd> <dt>

*Stride* 
</dt> <dd>

O deslocamento de bytes entre as cores consecutivas. Quando *Stride* é zero, as cores são totalmente empacotadas na matriz.

</dd> <dt>

*ponteiro* 
</dt> <dd>

Um ponteiro para o primeiro componente do primeiro elemento Color em uma matriz Color.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                              | Significado                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_valor inválido do GL \_**</dt> </dl> | o *tamanho* não era 3 ou 4.<br/>            |
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>  | o *tipo* não era um valor aceito.<br/> |
| <dl> <dt>**\_valor inválido do GL \_**</dt> </dl> | *Stride* ou *Count* era negativo.<br/> |



## <a name="remarks"></a>Comentários

A função **glColorPointer** especifica o local e o formato de dados de uma matriz de componentes de cor a serem usados durante a renderização. O parâmetro *Stride* determina o deslocamento de bytes de uma cor para a próxima, habilitando a embalagem de atributos de vértice em uma única matriz ou armazenamento em matrizes separadas. Em algumas implementações, armazenar atributos de vértice em uma única matriz pode ser mais eficiente do que o uso de matrizes separadas.

Habilitada a matriz de cores especificando a \_ constante de matriz de cores GL \_ com [**glEnableClientState**](glenableclientstate.md). Chamar [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)ou [**glDrawArrays**](gldrawarrays.md) usa a matriz de cores que, portanto, é habilitada. Por padrão, a matriz de cores está desabilitada. As chamadas **glColorPointer** não podem ser inseridas em listas de exibição.

Quando você especifica uma matriz de cores usando **glColorPointer**, os valores de todos os parâmetros de matriz de cor da função são salvos em um estado do lado do cliente e você pode armazenar em cache elementos estáticos da matriz. Como os parâmetros de matriz de cor estão em um estado do lado do cliente, [**glPushAttrib**](glpushattrib.md) e [**glPopAttrib**](glpopattrib.md) não salvam nem restauram os valores dos parâmetros.

Embora a especificação da matriz de cores nos pares [**glBegin**](glbegin.md) e [**glend**](glend.md) não gere um erro, os resultados são indefinidos.

As funções a seguir recuperam informações relacionadas à função **glColorPointer** :

matriz de cores [**glIsEnabled**](glisenabled.md) com Argument GL \_ \_

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o \_ tamanho da \_ matriz de cores do argumento GL \_

 tipo de matriz de cores glGet com Argument GL \_ \_ \_

**glGet** com Stride de \_ matriz de cores do argumento GL \_ \_

 \_ \_ contagem de matrizes de cores glGet com Argument GL \_

[](glgetpointerv.md) ponteiro de matriz de cores glGetPointerv com Argument GL \_ \_ \_

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

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnableClientState**](glenableclientstate.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetString**](glgetstring.md)
</dt> <dt>

[**glGetPointerv**](glgetpointerv.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glPopAttrib**](glpopattrib.md)
</dt> <dt>

[**glPushAttrib**](glpushattrib.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





