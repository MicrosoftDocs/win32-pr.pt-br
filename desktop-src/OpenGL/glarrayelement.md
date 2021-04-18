---
title: função glArrayElement (GL. h)
description: A função glArrayElement especifica os elementos de matriz usados para renderizar um vértice.
ms.assetid: 2c4d76bb-e4c9-4baa-a190-66298b8a4335
keywords:
- função glArrayElement OpenGL
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
ms.openlocfilehash: 6a20aff9fcaa5bf922bc9447f7b7022a8cd1a9c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105784168"
---
# <a name="glarrayelement-function"></a>função glArrayElement

A função **glArrayElement** especifica os elementos de matriz usados para renderizar um vértice.

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

Use a função **glArrayElement** nos pares [**glBegin**](glbegin.md) e [**glEnd**](glend.md) para especificar os dados de vértice e de atributo para primitivas de ponto, linha e polígono. A função **glArrayElement** especifica os dados de um único vértice usando vértice e dados de atributo localizados no *índice* das matrizes de vértice habilitadas.

Você pode usar **glArrayElement** para construir primitivos indexando dados de vértice, em vez de transmitir por meio de matrizes de dados na primeira a última ordem. Como **glArrayElement** especifica apenas um único vértice, você pode especificar explicitamente atributos para primitivos individuais. Por exemplo, você pode definir um único normal para cada triângulo individual.

Quando você inclui chamadas para **glArrayElement** em listas de exibição, os dados de matriz necessários, determinados pelos ponteiros de matriz e os valores de Enable, também são inseridos na lista de exibição. Os valores de ponteiro de matriz e de habilitação são determinados quando as listas de exibição são criadas, não quando as listas de exibição são executadas.

Você pode ler e armazenar em cache os dados estáticos da matriz a qualquer momento com o **glArrayElement**. Quando você modifica os elementos de uma matriz estática sem especificar a matriz novamente, os resultados de todas as chamadas subsequentes para **glArrayElement** são indefinidos.

Quando você chama **glArrayElement** sem primeiro chamar **glEnableClientState**( \_ matriz de vértice GL \_ ), nenhum desenho ocorre, mas os atributos correspondentes a matrizes habilitadas são modificados. Embora nenhum erro seja gerado quando você especifica uma matriz nos pares **glBegin** e **glEnd** , os resultados são indefinidos.

> [!Note]  
> A função **glArrayElement** só está disponível no OpenGL versão 1,1 ou posterior.

 

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

 

 





