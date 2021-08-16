---
title: Função glIndexd (Gl.h)
description: A função glIndexd define o índice de cores atual.
ms.assetid: 4cd72d32-e796-4c94-94cb-591f1ee3b26e
keywords:
- Função glIndexd OpenGL
topic_type:
- apiref
api_name:
- glIndexd
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05051f42dab945ef03b5dbd82b809e6f02c9db85f24423c64f7c284c502ea05e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118359632"
---
# <a name="glindexd-function"></a>Função glIndexd

A **função glIndexd** define o índice de cores atual.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glIndexd(
   GLdouble c
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

A **função glIndexd** atualiza o índice de cor atual (com valor único). Ele aceita um argumento: o novo valor para o índice de cores atual.

O índice atual é armazenado como um valor de ponto flutuante. Os valores inteiros são convertidos diretamente em valores de ponto flutuante, sem mapeamento especial.

Os valores de índice fora do intervalo representável do buffer de índice de cores não são fixados. No entanto, antes que um índice seja dithered (se habilitado) e gravado no framebuffer, ele é convertido em formato de ponto fixo. Todos os bits na parte inteira do valor de ponto fixo resultante que não correspondem aos bits no framebuffer são mascarados.

O índice atual pode ser atualizado a qualquer momento. Em particular, **glIndexd** pode ser chamado entre uma chamada para [**glBegin**](/windows/desktop/OpenGL/glbegin) e a chamada correspondente para [**glEnd.**](glend.md)

A função a seguir recupera informações relacionadas **a glIndexd:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ CURRENT \_ INDEX

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

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

