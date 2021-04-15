---
description: A função DbgDumpObjectRegister exibe informações sobre objetos ativos. Ignorado em compilações de varejo.
ms.assetid: 362d9912-662c-4a72-95b4-01f3d808e299
title: Função DbgDumpObjectRegister (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgDumpObjectRegister
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 727d9c00ebbe3d48bb46797a1e27b9dd27c7b2c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747369"
---
# <a name="dbgdumpobjectregister-function"></a>Função DbgDumpObjectRegister

A `DbgDumpObjectRegister` função exibe informações sobre objetos ativos. Ignorado em compilações de varejo.

## <a name="syntax"></a>Sintaxe


```C++
void DbgDumpObjectRegister(void);
```



## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Em compilações de depuração, a biblioteca de depuração mantém uma lista de objetos ativos. A lista inclui todos os objetos que derivam de [**CBaseObject**](cbaseobject.md), foram criados pelo módulo atual e não foram destruídos. O construtor **CBaseObject** e os métodos do destruidor atualizam a lista.

Essa função gera várias mensagens de memória de LOG \_ . No nível de log 1, a função exibe apenas o número total de objetos. No nível de log 2 ou superior, ele exibe uma lista dos objetos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxdebug. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de saída de depuração](debug-output-functions.md)
</dt> </dl>

 

 




