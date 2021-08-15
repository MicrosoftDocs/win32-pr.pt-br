---
description: Avalia uma expressão em compilações de depuração e de varejo. Em builds de depuração, exibe uma mensagem de diagnóstico se a expressão for FALSE.
ms.assetid: 259a3d30-0b20-4430-8b74-83ec619576ae
title: Macro EXECUTE_ASSERT (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXECUTE_ASSERT
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 871a8e4a04ec1dc31f3240b539a943c9c1733f083166fa4b7e6f6b52d14a466c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118401781"
---
# <a name="execute_assert-macro"></a>EXECUTAR \_ macro Assert

Avalia uma expressão em compilações de depuração e de varejo. Em builds de depuração, exibe uma mensagem de diagnóstico se a expressão for **false**.

## <a name="syntax"></a>Sintaxe


```C++
void EXECUTE_ASSERT(
    cond
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*condicional* 
</dt> <dd>

Expressão para avaliar.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa macro não retorna um valor.

## <a name="remarks"></a>Comentários

Ao contrário da macro [**Assert**](assert.md) , essa macro avalia a expressão em compilações de varejo. Em compilações de depuração, se a expressão for **false**, a macro exibirá uma caixa de mensagem com o texto da expressão, o nome do arquivo de origem e o número da linha. O usuário pode ignorar a asserção, inserir o depurador ou sair do aplicativo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wxdebug. h (incluir Fluxos. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Macros Assert e Breakpoint](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




