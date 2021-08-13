---
description: A função DbgInitialise Inicializa a biblioteca de depuração. Ignorado em compilações de varejo.
ms.assetid: d4ca739e-cd39-4692-81da-c5a88a09d546
title: Função DbgInitialise (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgInitialise
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 13aad8d0214c65c01237c8e74548c3915af9287c935b53e33c6d229b2da5b12e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118654211"
---
# <a name="dbginitialise-function"></a>Função DbgInitialise

A função **DbgInitialise** Inicializa a biblioteca de depuração. Ignorado em compilações de varejo.

## <a name="syntax"></a>Sintaxe


```C++
void DbgInitialise(
   HINSTANCE hInst
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hInst* 
</dt> <dd>

Identificador para a instância do módulo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

em um executável, chame esse método antes de usar os DirectShow depurar instalações. Antes de o executável sair, chame a função [**DbgTerminate**](dbgterminate.md) para limpar a biblioteca de depuração.

Em uma DLL que vincula à biblioteca de classe base (Strmbase. lib), não é necessário chamar essa função. A função é chamada automaticamente quando a DLL é carregada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxdebug. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de saída de depuração](debug-output-functions.md)
</dt> </dl>

 

 




