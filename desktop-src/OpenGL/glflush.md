---
title: função glFlush (GL. h)
description: A função glFlush força a execução de funções OpenGL em tempo finito.
ms.assetid: 7544b724-472f-4055-8f1c-64ddb58caaf3
keywords:
- função glFlush OpenGL
topic_type:
- apiref
api_name:
- glFlush
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ece5f0aa96140b6fa16b5fbde1a857f1e14f1570ad7fc734626a27ac660a65ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118360403"
---
# <a name="glflush-function"></a>função glFlush

A função **glFlush** força a execução de funções OpenGL em tempo finito.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glFlush(void);
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

Diferentes implementações do OpenGL armazenam comandos de buffer em vários locais diferentes, incluindo buffers de rede e o acelerador de gráficos em si. A função **glFlush** esvazia todos esses buffers, fazendo com que todos os comandos emitidos sejam executados tão rapidamente quanto são aceitos pelo mecanismo de renderização real. Embora essa execução não possa ser concluída em nenhum período de tempo específico, ela é concluída em uma quantidade finita de tempo.

Como qualquer programa OpenGL pode ser executado em uma rede ou em um acelerador que armazena em buffer os comandos, certifique-se de chamar **glFlush** em todos os programas que exigem que todos os comandos emitidos anteriormente tenham sido concluídos. Por exemplo, chame **glFlush** antes de aguardar a entrada do usuário que depende da imagem gerada.

A função **glFlush** pode retornar a qualquer momento. Ele não aguarda até que a execução de todas as funções OpenGL emitidas anteriormente seja concluída.

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

[**glFinish**](glfinish.md)
</dt> </dl>

 

 





