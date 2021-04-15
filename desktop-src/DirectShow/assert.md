---
description: Avalia uma expressão e exibe uma mensagem de diagnóstico se a expressão for falsa. Ignorado em compilações de varejo.
ms.assetid: 8c3815bb-3164-4066-a947-974e791af5cd
title: Macro ASSERT (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ASSERT
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 8617d1c86f655cc9b44ea6619931f73888ae2a67
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760779"
---
# <a name="assert-macro"></a>Macro ASSERT

Avalia uma expressão e exibe uma mensagem de diagnóstico se a expressão for **falsa**. Ignorado em compilações de varejo.

## <a name="syntax"></a>Sintaxe


```C++
void ASSERT(
   BOOL cond
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*condicional* 
</dt> <dd>

Expressão para avaliar.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa macro não retorna um valor.

## <a name="remarks"></a>Comentários

Em compilações de depuração, se a expressão for **false**, essa macro exibirá uma caixa de mensagem com o texto da expressão, o nome do arquivo de origem e o número da linha. O usuário pode ignorar a asserção, inserir o depurador ou sair do aplicativo.

## <a name="examples"></a>Exemplos


```
ASSERT(rtStartTime <= rtEndTime);
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wxdebug. h (incluir fluxos. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Macros Assert e Breakpoint](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




