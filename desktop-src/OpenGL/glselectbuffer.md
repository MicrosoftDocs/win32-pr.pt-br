---
title: função glSelectBuffer (GL. h)
description: A função glSelectBuffer estabelece um buffer para valores do modo de seleção.
ms.assetid: b5c64364-1f47-4281-96b5-95c3f5c8e753
keywords:
- função glSelectBuffer OpenGL
topic_type:
- apiref
api_name:
- glSelectBuffer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efa5b97abad6575de77a760c72e3eb05e90461c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644284"
---
# <a name="glselectbuffer-function"></a>função glSelectBuffer

A função **glSelectBuffer** estabelece um buffer para valores do modo de seleção.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glSelectBuffer(
   GLsizei size,
   GLuint  *buffer
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*size* 
</dt> <dd>

O tamanho do *buffer*.

</dd> <dt>

*completo* 
</dt> <dd>

Retorna os dados de seleção.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Name                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valor inválido do GL \_**</dt> </dl>     | o *tamanho* era negativo.<br/>                                                                                                       |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada enquanto o modo de renderização era GL \_ Select.<br/>                                                              |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

A função **glSelectBuffer** tem dois parâmetros: *buffer* é um ponteiro para uma matriz de inteiros sem sinal e *size* indica o tamanho da matriz. O parâmetro *buffer* retorna valores da pilha de nomes (consulte [**glInitNames**](glinitnames.md), [**glLoadName**](glloadname.md), [**glPushName**](glpushname.md)) quando o modo de renderização é GL \_ Select (consulte [**glRenderMode**](glrendermode.md)). A função **glSelectBuffer** deve ser emitida antes de o modo de seleção ser habilitado e não deve ser emitida enquanto o modo de RENDERIZAÇÃO é GL \_ Select.

A seleção é usada por um programador para determinar quais primitivos são desenhados em alguma região de uma janela. A região é definida pelas matrizes modelview e Perspective atuais.

No modo de seleção, nenhum fragmento de pixel é produzido da rasterização. Em vez disso, se um primitivo interceptar o volume de clipe definido pelos frustum de exibição e os planos de recorte definidos pelo usuário, esse primitivo causará uma visita de seleção. (Com polígonos, nenhuma ocorrência ocorrerá se o polígono for refeito.) Quando uma alteração é feita na pilha de nomes, ou quando [**glRenderMode**](glrendermode.md) é chamado, um registro de ocorrência é copiado para *buffer* se qualquer ocorrência ocorreu desde o último evento (uma alteração de pilha de nome ou uma chamada **glRenderMode** ). O registro de acesso consiste no número de nomes na pilha de nomes no momento do evento; seguido pelos valores mínimo e máximo de profundidade de todos os vértices que atingiram desde o evento anterior; seguido pelo conteúdo da pilha de nome, primeiro o nome inferior.

Os valores de profundidade retornados são mapeados de modo que o maior valor inteiro não assinado corresponde à profundidade da coordenada da janela 1,0 e zero corresponde à profundidade da coordenada da janela 0,0.

Um índice interno no *buffer* é redefinido para zero sempre que o modo de seleção é inserido. Cada vez que um registro de acesso é copiado no *buffer*, o índice é incrementado para apontar para a célula logo após o final do bloco de namesthat, para a próxima célula disponível. Se o registro de acesso for maior do que o número de localizações restantes no *buffer*, a quantidade de dados que puder ajustar será copiada e o sinalizador de estouro será definido. Se a pilha de nomes estiver vazia quando um registro de acesso for copiado, esse registro consistirá em zero seguido dos valores mínimo e máximo de profundidade.

O modo de seleção é encerrado chamando **glRenderMode** com um argumento diferente de GL \_ Select. Sempre que **glRenderMode** for chamado enquanto o modo de RENDERIZAÇÃO for GL \_ Select, ele retornará o número de registros de acesso copiados para *buffer*, redefinirá o sinalizador de estouro e o ponteiro de buffer de seleção e inicializará a pilha de nomes como vazia. Se o bit de estouro tiver sido definido quando **glRenderMode** foi chamado, uma contagem de registros de impacto negativo será retornada.

O conteúdo do *buffer* é indefinido até que [**glRenderMode**](glrendermode.md) seja chamado com um argumento diferente de GL \_ Select.

Os  / primitivos glBegin **glEnd** e chamadas para [**glRasterPos**](glrasterpos-functions.md) podem resultar em ocorrências.

A função a seguir recupera informações relacionadas a **glSelectBuffer**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento \_ GL \_ profundidade da pilha de nome \_

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glFeedbackBuffer**](glfeedbackbuffer.md)
</dt> <dt>

[**glInitNames**](glinitnames.md)
</dt> <dt>

[**glLoadName**](glloadname.md)
</dt> <dt>

[**glPushName**](glpushname.md)
</dt> <dt>

[**glRenderMode**](glrendermode.md)
</dt> </dl>

 

 





