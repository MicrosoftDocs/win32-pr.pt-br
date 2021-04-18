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
ms.openlocfilehash: 1d6623793b150c600eb00f0c0843dd72c68deb4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750646"
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
| parâmetro<br/>  | <dl> <dt>Wxdebug. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de saída de depuração](debug-output-functions.md)
</dt> </dl>

 

 




