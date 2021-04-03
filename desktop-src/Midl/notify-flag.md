---
title: notify_flag atributo
description: O atributo \ notificar \_ sinalizador \ fornece uma notificação identificando se uma rotina de servidor é chamada.
ms.assetid: a40b7114-d2e3-40c1-a0b1-599428188611
keywords:
- notify_flag do atributo MIDL
topic_type:
- apiref
api_name:
- notify_flag
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af61999f0527b599cf358c38288a8c67473445a9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006370"
---
# <a name="notify_flag-attribute"></a>notificar \_ atributo de sinalizador

O atributo **\[ notificar \_ sinalizador \]** fornece uma notificação identificando se uma rotina de servidor é chamada.

``` syntax
[notify_flag] procedure-name();
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nome do procedimento* 
</dt> <dd>

Nome do procedimento remoto ao qual o procedimento do \_ sinalizador de notificação está associado.

</dd> </dl>

## <a name="remarks"></a>Comentários

O atributo **\[ notificar \_ sinalizador \]** é semelhante ao uso para o atributo **\[ Notify \]** .

O nome do procedimento do **\[ \_ sinalizador \] de notificação** é o nome do procedimento remoto sufixado pelo **\_ \_ sinalizador Notify**. O procedimento **\_ notificar \_ sinalizador** não requer nenhum parâmetro e não retorna um resultado. Um protótipo desse procedimento também é gerado no arquivo de cabeçalho. Por exemplo, se o arquivo IDL contiver o seguinte:

``` syntax
MyProcedure([in] short S);
```

Especifique o seguinte no ACF para MIDL para gerar a chamada do **\_ \_ sinalizador Notify** :

``` syntax
[notify_flag] MyProcedure();
```

O compilador MIDL gerará código stub de servidor que contém a seguinte chamada para o procedimento **\_ notificar \_ sinalizador** :

``` syntax
MyProcedure_notify_flag();
```

O arquivo de cabeçalho conterá um protótipo:

``` syntax
void MyProcedure_notify_flag(boolean __MIDL_NotifyFlag);
```

**\_ MIDL \_ NotifyFlag** será **true** se a rotina do servidor for chamada.

## <a name="examples"></a>Exemplos

``` syntax
[notify_flag] MyProcedure();
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**sobre**](notify.md)
</dt> </dl>

 

 




