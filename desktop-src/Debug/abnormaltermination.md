---
description: Indica se o bloco \_ \_ try de um manipulador de encerramento terminou normalmente. A função pode ser chamada somente de dentro do bloco \_ \_ finally de um manipulador de encerramento.
ms.assetid: 0ddaef1f-03f0-45fc-9c5e-8d6a26a73245
title: Macro AbnormalTermination
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AbnormalTermination
api_type:
- NA
api_location: ''
ms.openlocfilehash: 137d6667c993d4a107be057e46c4ee469a513ec95d358b6d3cc50654a5bba520
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957125"
---
# <a name="abnormaltermination-macro"></a>Macro AbnormalTermination

Indica se o bloco **\_ \_ try** de um manipulador de encerramento terminou normalmente. A função pode ser chamada somente de dentro do bloco **\_ \_ finally** de um manipulador de encerramento.

> [!Note]  
> O Compilador de Otimização do Microsoft C/C++ interpreta essa função como uma palavra-chave e seu uso fora da sintaxe de tratamento de exceção apropriada gera um erro do compilador.

 

## <a name="syntax"></a>Sintaxe


```C++
BOOL AbnormalTermination(void);
```



## <a name="parameters"></a>Parâmetros

Essa macro não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Se o **\_ \_ bloco try** for encerrado de forma anormal, o valor de retorno será diferente de zero.

Se o **\_ \_ bloco try** for encerrado normalmente, o valor de retorno será zero.

## <a name="remarks"></a>Comentários

O **\_ \_ bloco** try será encerrado normalmente somente se a execução deixar o bloco sequencialmente depois de executar a última instrução no bloco. Instruções (como **return**, **goto**, **continue** ou **break** **\_ \_** ) que causam a execução deixar o bloco try resultam em encerramento anormal do bloco. Esse é o caso, mesmo que essa instrução seja a última instrução no **\_ \_ bloco try.**

A terminação anormal de um **\_ \_ bloco try** faz com que o sistema pesquise para trás em todos os quadros de pilha para determinar se algum manipulador de encerramento deve ser chamado. Isso pode resultar na execução de centenas de instruções, portanto, é importante evitar o encerramento anormal de um bloco **\_ \_ try** devido **a** uma instrução return , **goto**, **continue** ou **break.** Observe que essas instruções não geram uma exceção, mesmo que a terminação seja anormal.

Para evitar o encerramento anormal, a execução deve continuar até o final do bloco. Você também pode executar a **\_ \_ instrução leave.** A **\_ \_ instrução leave** permite o encerramento imediato do bloco **\_ \_ try** sem causar encerramento anormal e sua penalidade de desempenho. Verifique a documentação do compilador para determinar se há suporte **\_ \_ para a instrução leave.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de tratamento de exceção estruturadas](structured-exception-handling-functions.md)
</dt> <dt>

[Visão geral do tratamento de exceções estruturadas](structured-exception-handling.md)
</dt> </dl>

 

 




