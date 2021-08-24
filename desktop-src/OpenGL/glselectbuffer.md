---
title: Função glSelectBuffer (Gl.h)
description: A função glSelectBuffer estabelece um buffer para valores de modo de seleção.
ms.assetid: b5c64364-1f47-4281-96b5-95c3f5c8e753
keywords:
- Função glSelectBuffer OpenGL
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
ms.openlocfilehash: 17c40030c34ece43f4e24ac6937c35400fed7ab7acc005e99c653b233e08b69e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519816"
---
# <a name="glselectbuffer-function"></a>Função glSelectBuffer

A **função glSelectBuffer** estabelece um buffer para valores de modo de seleção.

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

*Buffer* 
</dt> <dd>

Retorna os dados de seleção.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela [**função glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**VALOR INVÁLIDO DE GL \_ \_**</dt> </dl>     | *size* era negativo.<br/>                                                                                                       |
| <dl> <dt>**OPERAÇÃO \_ GL \_ INVÁLIDA**</dt> </dl> | A função foi chamada enquanto o modo de renderização era GL \_ SELECT.<br/>                                                              |
| <dl> <dt>**OPERAÇÃO \_ GL \_ INVÁLIDA**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd.**](glend.md)<br/> |



## <a name="remarks"></a>Comentários

A **função glSelectBuffer** tem dois parâmetros: *buffer* é um ponteiro para uma matriz de inteiros sem sinal e *size* indica o tamanho da matriz. O *parâmetro buffer* retorna valores da pilha de nomes (consulte [**glInitNames**](glinitnames.md), [**glLoadName**](glloadname.md), [**glPushName**](glpushname.md)) quando o modo de renderização é GL \_ SELECT (consulte [**glRenderMode**](glrendermode.md)). A **função glSelectBuffer** deve ser emitida antes que o modo de seleção seja habilitado e não deve ser emitido enquanto o modo de renderização for GL \_ SELECT.

A seleção é usada por um programador para determinar quais primitivos são desenhados em alguma região de uma janela. A região é definida pelas matrizes de perspectiva e de modelview atuais.

No modo de seleção, nenhum fragmento de pixel é produzido da rasterização. Em vez disso, se um primitivo intersecção do volume de recorte definido pelo frustum de exibição e os planos de recorte definidos pelo usuário, esse primitivo causará uma queda de seleção. (Com polígonos, nenhuma ocorrência ocorrerá se o polígono for eliminado.) Quando uma alteração é feita na pilha de nomes ou quando [**glRenderMode**](glrendermode.md) é chamado, um registro de ocorrência é copiado para o *buffer* se ocorrerem ocorrências desde o último evento (uma alteração de pilha de nomes ou uma chamada **glRenderMode).** O registro de ocorrência consiste no número de nomes na pilha de nomes no momento do evento; seguido pelos valores mínimo e máximo de profundidade de todos os vértices que foram atingidos desde o evento anterior; seguido pelo conteúdo da pilha de nomes, nome inferior primeiro.

Os valores de profundidade retornados são mapeados de forma que o maior valor inteiro sem sinal corresponda à profundidade da coordenada da janela 1,0 e zero corresponde à profundidade da coordenada da janela 0,0.

Um índice interno no *buffer é* redefinido como zero sempre que o modo de seleção é inserido. Sempre que um registro de ocorrência é copiado no *buffer*, o índice é incrementado para apontar para a célula logo após o final do bloco de nomesou seja, para a próxima célula disponível. Se o registro de ocorrência for maior que o número de locais restantes no *buffer,* o máximo de dados que puder ajustar será copiado e o sinalizador de estouro será definido. Se a pilha de nomes estiver vazia quando um registro de ocorrência for copiado, esse registro consisti em zero seguido pelos valores mínimo e máximo de profundidade.

O modo de seleção é sair chamando **glRenderMode com** um argumento diferente de GL \_ SELECT. Sempre **que glRenderMode** é chamado enquanto o modo de renderização é GL SELECT, ele retorna o número de registros de ocorrência copiados para buffer , redefine o sinalizador de estouro e o ponteiro do buffer de seleção e inicializa a pilha de nomes para estar \_ vazia.  Se o bit de estouro tiver sido definido **quando glRenderMode** foi chamado, uma contagem de registros de ocorrência negativa será retornada.

O conteúdo do *buffer é* indefinido até [**que glRenderMode**](glrendermode.md) seja chamado com um argumento diferente de GL \_ SELECT.

Os **primitivos glBegin** / **glEnd** e chamadas para [**glRasterPos**](glrasterpos-functions.md) podem resultar em acertos.

A função a seguir recupera informações relacionadas **a glSelectBuffer**:

[**glGet com**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) o argumento GL \_ NAME STACK \_ \_ DEPTH

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

 

 





