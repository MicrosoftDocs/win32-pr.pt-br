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
ms.openlocfilehash: 33a62c8dad7ef6e15b9b11461303b1bced977a96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754767"
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

Em um executável, chame esse método antes de usar os recursos de depuração do DirectShow. Antes de o executável sair, chame a função [**DbgTerminate**](dbgterminate.md) para limpar a biblioteca de depuração.

Em uma DLL que vincula à biblioteca de classe base (Strmbase. lib), não é necessário chamar essa função. A função é chamada automaticamente quando a DLL é carregada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxdebug. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de saída de depuração](debug-output-functions.md)
</dt> </dl>

 

 




