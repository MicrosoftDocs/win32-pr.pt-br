---
title: notificar atributo
description: O atributo \ Notify \ instrui o compilador MIDL a gerar uma chamada para um procedimento \ Notify \ no lado do servidor do aplicativo.
ms.assetid: 24f9887b-04b7-491a-ab6e-7c078b967fbc
keywords:
- notificar MIDL do atributo
topic_type:
- apiref
api_name:
- notify
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cf1bb1c4f522cecb5fe81a317267e2cffff2da638e3a8c09a412ae8d94a149d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066856"
---
# <a name="notify-attribute"></a>notificar atributo

O atributo **\[ Notify \]** instrui o compilador MIDL a gerar uma chamada para um procedimento de **\[ notificação \]** no lado do servidor do aplicativo.

``` syntax
[notify] procedure-name();
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nome do procedimento* 
</dt> <dd>

O nome do procedimento remoto com o qual o procedimento de notificação será associado.

</dd> </dl>

## <a name="remarks"></a>Comentários

O procedimento **\[ Notify \]** chamado como resultado do atributo **\[ Notify \]** é associado a um procedimento remoto específico no servidor. Ele é semelhante em conceito a uma função de retorno de chamada. O stub chama o procedimento **\[ Notify \]** depois que todos os argumentos de saída do procedimento remoto ao qual ele está associado tenham sido empacotados e qualquer memória associada aos parâmetros for liberada. A rotina de **\[ notificação \]** é chamada se uma chamada falhar antes da execução da rotina do servidor. Por exemplo, se um servidor falhar durante o desempacotamento devido ao recebimento de dados inválidos do cliente, a \[ rotina de notificação \] será chamada.

O atributo **\[ Notify \]** é útil para desenvolver aplicativos que adquirem recursos em procedimentos remotos. Esses recursos são liberados no procedimento **\[ Notify \]** depois que os parâmetros de saída do procedimento remoto são totalmente empacotados.

O nome do procedimento de **\[ notificação \]** é o nome do procedimento remoto sufixado por **\_ Notify**. O procedimento **\_ Notify** não requer nenhum parâmetro e não retorna um resultado. Um protótipo desse procedimento também é gerado no arquivo de cabeçalho. Por exemplo, se o arquivo IDL contiver o seguinte:

``` syntax
MyProcedure([in] short S);
```

Especifique o seguinte no ACF para MIDL para gerar a chamada de **\_ notificação** :

``` syntax
[notify] MyProcedure();
```

O compilador MIDL irá gerar o código stub do servidor que contém a seguinte chamada para o procedimento **\_ Notify** :

``` syntax
MyProcedure_notify();
```

O arquivo de cabeçalho conterá um protótipo:

``` syntax
void MyProcedure_notify(void);
```

## <a name="examples"></a>Exemplos

``` syntax
[notify] MyProcedure();
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Arquivo de configuração de aplicativo (ACF)](application-configuration-file-acf-.md)
</dt> </dl>

 

 




