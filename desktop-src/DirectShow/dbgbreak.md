---
description: Exibe uma caixa de mensagem com a cadeia de caracteres especificada, o nome do arquivo de origem e o número da linha. O usuário pode ignorar a mensagem, inserir o depurador ou sair do aplicativo. Ignorado em compilações de varejo.
ms.assetid: ac4da7da-f9d0-44ae-9ad1-9a5908b288fb
title: Macro DbgBreak (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgBreak
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 099344a295de2657b40218b993ab9c4cb6411353
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751880"
---
# <a name="dbgbreak-macro"></a>Macro DbgBreak

Exibe uma caixa de mensagem com a cadeia de caracteres especificada, o nome do arquivo de origem e o número da linha. O usuário pode ignorar a mensagem, inserir o depurador ou sair do aplicativo. Ignorado em compilações de varejo.

## <a name="syntax"></a>Sintaxe


```C++
void DbgBreak(
    strLiteral
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*strLiteral* 
</dt> <dd>

Cadeia de texto.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa macro não retorna um valor.

## <a name="examples"></a>Exemplos


```C++
DbgBreak("Unrecoverable error occurred.");
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wxdebug. h (incluir fluxos. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Macros Assert e Breakpoint](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




