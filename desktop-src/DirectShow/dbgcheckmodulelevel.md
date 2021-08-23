---
description: A função DbgCheckModuleLevel verifica se o log está habilitado para os tipos e o nível de mensagem fornecidos. Ignorado em compilações de varejo.
ms.assetid: f4b12df7-9001-4bfb-9d84-84a0e8295a8b
title: Função DbgCheckModuleLevel (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgCheckModuleLevel
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dd6d7c61e7989987401c22386054c02f87410ce66dbb98bb6e20a813f2c851be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823696"
---
# <a name="dbgcheckmodulelevel-function"></a>Função DbgCheckModuleLevel

A `DbgCheckModuleLevel` função verifica se o log está habilitado para os tipos de mensagem e o nível determinados. Ignorado em compilações de varejo.

## <a name="syntax"></a>Sintaxe


```C++
BOOL DbgCheckModuleLevel(
   DWORD Types,
   DWORD Level
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Types* 
</dt> <dd>

Combinação de bits de um ou mais tipos de mensagem.

</dd> <dt>

*Level* 
</dt> <dd>

Nível de log

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **true** se o registro em log para qualquer um dos tipos de mensagem especificados for definido como o nível especificado ou superior. Caso contrário, retornará **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxdebug. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de saída de depuração](debug-output-functions.md)
</dt> </dl>

 

 




