---
description: Avalia uma expressão e exibe uma mensagem de diagnóstico se a expressão for FALSE. Ignorado em builds de varejo.
ms.assetid: 8c3815bb-3164-4066-a947-974e791af5cd
title: Macro ASSERT (Wxdebug.h)
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
ms.openlocfilehash: 1c64ae2256ae132fccdca6e483fae3f79d28b0cda66d7701acbe95abb1222d14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117824425"
---
# <a name="assert-macro"></a>Macro ASSERT

Avalia uma expressão e exibe uma mensagem de diagnóstico se a expressão for **FALSE.** Ignorado em builds de varejo.

## <a name="syntax"></a>Sintaxe


```C++
void ASSERT(
   BOOL cond
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Cond* 
</dt> <dd>

Expressão para avaliar.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa macro não retorna um valor.

## <a name="remarks"></a>Comentários

Em builds de depuração, se a expressão for **FALSE**, essa macro exibirá uma caixa de mensagem com o texto da expressão, o nome do arquivo de origem e o número de linha. O usuário pode ignorar a asserção, inserir o depurador ou sair do aplicativo.

## <a name="examples"></a>Exemplos


```
ASSERT(rtStartTime <= rtEndTime);
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wxdebug.h (incluir Fluxos.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Macros assert e breakpoint](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




