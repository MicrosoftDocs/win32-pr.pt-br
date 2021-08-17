---
title: notify_flag atributo
description: O atributo \ notify \_ flag\ fornece notificação que identifica se uma rotina de servidor é chamada.
ms.assetid: a40b7114-d2e3-40c1-a0b1-599428188611
keywords:
- notify_flag atributo MIDL
topic_type:
- apiref
api_name:
- notify_flag
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9fb7479667fb9757924dcba765c34138cf01c1ad6645ce7bfdc525be393e77f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066866"
---
# <a name="notify_flag-attribute"></a>atributo notify \_ flag

O **\[ atributo de \_ sinalizador \]** de notificação fornece notificação que identifica se uma rotina de servidor é chamada.

``` syntax
[notify_flag] procedure-name();
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nome do procedimento* 
</dt> <dd>

Nome do procedimento remoto ao qual o procedimento de \_ sinalizador de notificação está associado.

</dd> </dl>

## <a name="remarks"></a>Comentários

O **\[ atributo de \_ sinalizador \]** de notificação é semelhante em uso ao **\[ atributo notify. \]**

O **\[ nome do \_ procedimento \]** de sinalizador de notificação é o nome do procedimento remoto sufixo pelo **\_ sinalizador de \_ notificação**. O **\_ procedimento de \_ sinalizador** de notificação não requer nenhum parâmetro e não retorna um resultado. Um protótipo desse procedimento também é gerado no arquivo de header. Por exemplo, se o arquivo IDL contiver o seguinte:

``` syntax
MyProcedure([in] short S);
```

Especifique o seguinte no ACF para MIDL para gerar a chamada **\_ de sinalizador \_ de** notificação:

``` syntax
[notify_flag] MyProcedure();
```

O compilador MIDL gerará o código stub do servidor que contém a seguinte chamada para o procedimento **\_ de sinalizador de \_ notificação:**

``` syntax
MyProcedure_notify_flag();
```

O arquivo de header conterá um protótipo:

``` syntax
void MyProcedure_notify_flag(boolean __MIDL_NotifyFlag);
```

**\_ MIDL \_ NotifyFlag** será **TRUE se** a rotina do servidor for chamada.

## <a name="examples"></a>Exemplos

``` syntax
[notify_flag] MyProcedure();
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Notificar**](notify.md)
</dt> </dl>

 

 




