---
description: Indica se o \_ \_ bloco try de um manipulador de encerramento foi encerrado normalmente. A função pode ser chamada somente de dentro do \_ \_ bloco finally de um manipulador de encerramento.
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
ms.openlocfilehash: 7c4869f36d8ba70c8dcd8ca526949d489f455e8c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920515"
---
# <a name="abnormaltermination-macro"></a>Macro AbnormalTermination

Indica se o bloco **\_ \_ try** de um manipulador de encerramento foi encerrado normalmente. A função pode ser chamada somente de dentro do bloco **\_ \_ finally** de um manipulador de encerramento.

> [!Note]  
> O compilador de otimização do Microsoft C/C++ interpreta essa função como uma palavra-chave e seu uso fora da sintaxe apropriada de tratamento de exceção gera um erro de compilador.

 

## <a name="syntax"></a>Sintaxe


```C++
BOOL AbnormalTermination(void);
```



## <a name="parameters"></a>Parâmetros

Esta macro não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Se o bloco **\_ \_ try** for encerrado de forma anormal, o valor de retorno será diferente de zero.

Se o bloco **\_ \_ try** for encerrado normalmente, o valor de retorno será zero.

## <a name="remarks"></a>Comentários

O bloco **\_ \_ try** será encerrado normalmente somente se a execução deixar o bloco sequencialmente após a execução da última instrução no bloco. Instruções (como **Return**, **goto**, **continue** ou **Break**) que causam a execução para deixar o bloco **\_ \_ try** resultam em finalização anormal do bloco. Esse é o caso, mesmo se essa instrução for a última instrução no bloco **\_ \_ try** .

A finalização anormal de um bloco **\_ \_ try** faz com que o sistema pesquise retroativamente por todos os quadros de pilha para determinar se os manipuladores de encerramento devem ser chamados. Isso pode resultar na execução de centenas de instruções, portanto, é importante evitar a finalização anormal de um bloco **\_ \_ try** devido a uma instrução **Return**, **goto**, **continue** ou **Break** . Observe que essas instruções não geram uma exceção, embora o encerramento seja anormal.

Para evitar a finalização anormal, a execução deve continuar no final do bloco. Você também pode executar a instrução **\_ \_ Leave** . A instrução **\_ \_ Leave** permite o encerramento imediato do bloco **\_ \_ try** sem causar um encerramento anormal e sua penalidade de desempenho. Verifique a documentação do compilador para determinar se a instrução **\_ \_ Leave** tem suporte.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de manipulação de exceção estruturada](structured-exception-handling-functions.md)
</dt> <dt>

[Visão geral da manipulação de exceção estruturada](structured-exception-handling.md)
</dt> </dl>

 

 




