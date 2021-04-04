---
title: função glIndexs (GL. h)
description: A função glIndexs define o índice de cores atual.
ms.assetid: 193304e6-c88a-49a6-935b-29bcf1954564
keywords:
- função glIndexs OpenGL
topic_type:
- apiref
api_name:
- glIndexs
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cdc2036b3aec37c8f727dc38a5186998a5bc80c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085196"
---
# <a name="glindexs-function"></a>função glIndexs

A função **glIndexs** define o índice de cores atual.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glIndexs(
   GLshort c
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*c* 
</dt> <dd>

O novo valor para o índice de cores atual.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

A função **glIndexs** atualiza o índice de cores atual (de valor único). Ele usa um argumento: o novo valor para o índice de cores atual.

O índice atual é armazenado como um valor de ponto flutuante. Os valores inteiros são convertidos diretamente em valores de ponto flutuante, sem mapeamento especial.

Os valores de índice fora do intervalo representável do buffer de índice de cor não são clamped. No entanto, antes que um índice seja dicedido (se habilitado) e gravado no framebuffer, ele é convertido em formato de ponto fixo. Todos os bits na parte inteira do valor de ponto fixo resultante que não correspondem aos bits no framebuffer são mascarados.

O índice atual pode ser atualizado a qualquer momento. Em particular, **glIndexs** pode ser chamado entre uma chamada para [**glBegin**](/windows/desktop/OpenGL/glbegin) e a chamada correspondente para [**glEnd**](glend.md).

A função a seguir recupera informações relacionadas a **glIndexs**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL o \_ \_ índice atual

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

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

