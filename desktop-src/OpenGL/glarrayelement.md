---
title: Função glArrayElement (Gl.h)
description: A função glArrayElement especifica os elementos de matriz usados para renderizar um vértice.
ms.assetid: 2c4d76bb-e4c9-4baa-a190-66298b8a4335
keywords:
- Função glArrayElement OpenGL
topic_type:
- apiref
api_name:
- glArrayElement
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb6fdf3b90c5145c46730e530f26ba7d4f7f3875e51cc4d510e9763d03e27207
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118618055"
---
# <a name="glarrayelement-function"></a>Função glArrayElement

A **função glArrayElement** especifica os elementos de matriz usados para renderizar um vértice.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glArrayElement(
   GLint index
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*index* 
</dt> <dd>

Um índice nas matrizes habilitadas.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Use a **função glArrayElement** em pares [**glBegin**](glbegin.md) e [**glEnd**](glend.md) para especificar dados de vértice e atributo para primitivos de ponto, linha e polígono. A **função glArrayElement** especifica os dados de um único vértice usando dados de vértice e atributo localizados no índice das matrizes de vértice habilitadas. 

Você pode usar **glArrayElement** para construir primitivos indexando dados de vértice, em vez de transmitir por meio de matrizes de dados na primeira para a última ordem. Como **glArrayElement** especifica apenas um único vértice, você pode especificar explicitamente atributos para primitivos individuais. Por exemplo, você pode definir um único normal para cada triângulo individual.

Quando você inclui chamadas para **glArrayElement** em listas de exibição, os dados de matriz necessários, determinados pelos ponteiros de matriz e habilitam valores, também são inseridos na lista de exibição. Os valores de ponteiro de matriz e de habilitar são determinados quando as listas de exibição são criadas, não quando as listas de exibição são executadas.

Você pode ler e armazenar em cache dados de matriz estática a qualquer momento **com glArrayElement**. Quando você modifica os elementos de uma matriz estática sem especificar a matriz novamente, os resultados de todas as chamadas subsequentes para **glArrayElement** são indefinido.

Quando você chama **glArrayElement** sem chamar **glEnableClientState**(GL VERTEX ARRAY), nenhum desenho ocorre, mas os atributos correspondentes às matrizes habilitadas \_ são \_ modificados. Embora nenhum erro seja gerado quando você especifica uma matriz dentro dos pares **glBegin** e **glEnd,** os resultados são indefinido.

> [!Note]  
> A **função glArrayElement** só está disponível no OpenGL versão 1.1 ou posterior.

 

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

[**glBegin**](glbegin.md)
</dt> <dt>

[**glColorPointer**](glcolorpointer.md)
</dt> <dt>

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnableClientState**](glenableclientstate.md)
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

 

 





