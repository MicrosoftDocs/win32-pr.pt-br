---
description: A função DbgSetModuleLevel define o nível de log para um ou mais tipos de mensagem. Ignorado em compilações de varejo.
ms.assetid: 89d25106-8018-4089-8b77-d3c87529e984
title: Função DbgSetModuleLevel (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgSetModuleLevel
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 06f8cccbf7212514ae9f5cbd338f4e8876137cf038992ae111e7eeb743284774
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118654046"
---
# <a name="dbgsetmodulelevel-function"></a>Função DbgSetModuleLevel

A função **DbgSetModuleLevel** define o nível de log para um ou mais tipos de mensagem. Ignorado em compilações de varejo.

## <a name="syntax"></a>Sintaxe


```C++
void DbgSetModuleLevel(
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

Nível de log para os tipos de mensagem especificados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxdebug. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de saída de depuração](debug-output-functions.md)
</dt> </dl>

 

 




