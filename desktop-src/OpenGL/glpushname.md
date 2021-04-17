---
title: função glPushName (GL. h)
description: As funções glPushName e glPopName enviam por push e pop a pilha de nomes. | função glPushName (GL. h)
ms.assetid: e4319018-42c0-4567-b67f-31dbdbee9b13
keywords:
- função glPushName OpenGL
topic_type:
- apiref
api_name:
- glPushName
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ff783a108f5cb1ac34141c6c57f47b16e23531a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105782960"
---
# <a name="glpushname-function"></a>função glPushName

As funções **glPushName** e [**glPopName**](glpopname.md) enviam por push e pop a pilha de nomes.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glPushName(
   GLuint name
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*name* 
</dt> <dd>

Um nome que será enviado para a pilha de nomes.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Name                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_estouro de pilha GL \_**</dt> </dl>    | A função foi chamada enquanto a pilha de matriz atual estava cheia.<br/>                                                           |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

A função **glPushName** faz com que o nome seja enviado por push para a pilha de nomes, que inicialmente está vazia. A função [**glPopName**](glpopname.md) exibe um nome fora do topo da pilha. A pilha de nomes é usada durante o modo de seleção para permitir que conjuntos de comandos de renderização sejam identificados exclusivamente. Ele consiste em um conjunto ordenado de inteiros não assinados.

A pilha de nomes está sempre vazia enquanto o modo de renderização não é GL \_ Select. Chamadas para **glPushName** ou [**glPopName**](glpopname.md) enquanto o modo render não é GL \_ Select são ignoradas.

As funções a seguir recuperam informações relacionadas a **glPushName** e [**glPopName**](glpopname.md):

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento \_ GL \_ profundidade da pilha de nome \_

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com Argument GL \_ Max \_ name \_ pilha \_ Depth

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

[**glInitNames**](glinitnames.md)
</dt> <dt>

[**glLoadName**](glloadname.md)
</dt> <dt>

[**glRenderMode**](glrendermode.md)
</dt> <dt>

[**glSelectBuffer**](glselectbuffer.md)
</dt> </dl>

 

 





