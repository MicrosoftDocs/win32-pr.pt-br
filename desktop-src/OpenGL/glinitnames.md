---
title: função glInitNames (GL. h)
description: A função glInitNames Inicializa a pilha de nomes.
ms.assetid: 26c134f5-c17c-4637-93b6-5293f316dd6c
keywords:
- função glInitNames OpenGL
topic_type:
- apiref
api_name:
- glInitNames
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a567242431fc90be3b60d8ae08875b585ff6a81794899a6c9eb69e7a0a03daa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012114"
---
# <a name="glinitnames-function"></a>função glInitNames

A função **glInitNames** Inicializa a pilha de nomes.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glInitNames(void);
```



## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

A função **glInitNames** faz com que a pilha de nomes seja inicializada para seu estado vazio padrão. A pilha de nomes é usada durante o modo de seleção para permitir que conjuntos de comandos de renderização sejam identificados exclusivamente. Ele consiste em um conjunto ordenado de inteiros não assinados.

A pilha de nomes está sempre vazia enquanto o modo de renderização não é GL \_ Select. As chamadas para **glInitNames** enquanto o modo de renderização não é GL \_ Select são ignoradas.

As funções a seguir recuperam informações relacionadas ao **glInitNames**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento \_ GL \_ profundidade da pilha de nome \_

**glGet** com Argument GL \_ Max \_ name \_ pilha \_ Depth

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

[**glEnd**](glend.md)
</dt> <dt>

[**glLoadName**](glloadname.md)
</dt> <dt>

[**glPushName**](glpushname.md)
</dt> <dt>

[**glRenderMode**](glrendermode.md)
</dt> <dt>

[**glSelectBuffer**](glselectbuffer.md)
</dt> </dl>

 

 





