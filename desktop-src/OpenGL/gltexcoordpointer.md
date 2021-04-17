---
title: função glTexCoordPointer (GL. h)
description: A função glTexCoordPointer define uma matriz de coordenadas de textura.
ms.assetid: c3640a1b-ccc7-4f1a-94a5-a164f7377dbc
keywords:
- função glTexCoordPointer OpenGL
topic_type:
- apiref
api_name:
- glTexCoordPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: febc9c79bdbc4a1ed1c14380af47f36309f12662
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105780189"
---
# <a name="gltexcoordpointer-function"></a>função glTexCoordPointer

A função **glTexCoordPointer** define uma matriz de coordenadas de textura.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glTexCoordPointer(
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

O número de coordenadas por elemento de matriz. O valor do *tamanho* deve ser 1, 2, 3 ou 4.

</dd> <dt>

*tipo* 
</dt> <dd>

O tipo de dados de cada coordenada de textura na matriz usando as seguintes constantes simbólicas: **GL \_ Short**, **GL \_ int**, **GL \_ float** e **GL \_ Double**.

</dd> <dt>

*Stride* 
</dt> <dd>

O deslocamento de bytes entre elementos de matriz consecutivos. Quando *Stride* é zero, os elementos da matriz são totalmente empacotados na matriz.

</dd> <dt>

*ponteiro* 
</dt> <dd>

Um ponteiro para a primeira coordenada do primeiro elemento na matriz.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                              | Significado                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>  | o *tipo* não era um valor aceito.<br/> |
| <dl> <dt>**\_valor inválido do GL \_**</dt> </dl> | o *tamanho* não era 1, 2, 3 ou 4.<br/>     |
| <dl> <dt>**\_valor inválido do GL \_**</dt> </dl> | o *Stride* era negativo.<br/>            |



## <a name="remarks"></a>Comentários

A função **glTexCoordPointer** especifica o local e os dados de uma matriz de coordenadas de textura a serem usadas durante a renderização. O parâmetro *size* especifica o número de coordenadas usadas para cada elemento da matriz. O parâmetro de *tipo* especifica o tipo de dados de cada coordenada de textura. O parâmetro *Stride* determina o deslocamento de bytes de um elemento de matriz para o seguinte, habilitando a embalagem de vértices e atributos em uma única matriz ou armazenamento em matrizes separadas. Em algumas implementações, armazenar os vértices e os atributos em uma única matriz pode ser mais eficiente do que usar matrizes separadas. Para obter mais informações, consulte [**glInterleavedArrays**](glinterleavedarrays.md). Quando uma matriz de coordenadas de textura é especificada, o tamanho, o tipo, o Stride e o ponteiro são salvos no estado do lado do cliente.

Uma matriz de coordenadas de textura é habilitada quando você especifica a constante de **\_ \_ \_ matriz coord de textura GL** com [**glEnableClientState**](glenableclientstate.md). Quando habilitado, [**glDrawArrays**](gldrawarrays.md), [**glDrawElements**](gldrawelements.md)e [**glArrayElement**](glarrayelement.md) usam a matriz de coordenadas de textura. Por padrão, a matriz de coordenadas de textura está desabilitada.

Você não pode incluir **glTexCoordPointer** em listas de exibição.

Quando você especifica uma matriz de coordenadas de textura usando **glTexCoordPointer**, os valores de todos os parâmetros de matriz de coordenadas de textura da função são salvos em um estado do lado do cliente e os elementos estáticos da matriz podem ser armazenados em cache. Como os parâmetros da matriz de coordenadas de textura são o estado do lado do cliente, seus valores não são salvos nem restaurados por [**glPushAttrib**](glpushattrib.md) e [**glPopAttrib**](glpopattrib.md).

Embora nenhum erro seja gerado quando você chama **glTexCoordPointer** nos pares [**glBegin**](glbegin.md) e [**glEnd**](glend.md) , os resultados são indefinidos.

As funções a seguir recuperam informações relacionadas ao **glTexCoordPointer**:

[**glIsEnabled**](glisenabled.md) com a **\_ \_ \_ matriz coord de textura Argument GL**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com Argument **GL \_ textura \_ coord da \_ matriz \_ tamanho**

**glGet** with argumento **GL \_ Texture \_ coord \_ array \_ Stride**

 **\_ \_ \_ \_ contagem de matrizes de coord de textura** glGet com Argument GL

**glGet** com o **\_ tipo de \_ \_ matriz coord \_ de textura Argument GL**

[](glgetpointerv.md) **\_ \_ \_ \_ ponteiro de matriz coord de textura** glGetPointerv com Argument GL

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

[**glDrawElements**](gldrawelements.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnable**](glenable.md)
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

[**glPopClientAttrib**](glpopclientattrib.md)
</dt> <dt>

[**glPushClientAttrib**](glpushclientattrib.md)
</dt> <dt>

[**glTexCoord**](gltexcoord-functions.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





