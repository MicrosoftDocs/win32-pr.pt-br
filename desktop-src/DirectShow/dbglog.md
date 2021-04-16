---
description: A macro DbgLog envia uma cadeia de caracteres para o local de saída de depuração, se o registro em log estiver habilitado para o tipo e o nível especificados. Essa macro é ignorada em compilações de varejo.
ms.assetid: 10e95d63-14f2-4fdb-a1b8-c5bf654f9819
title: Macro DbgLog (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgLog
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 1cd3f4e53c61fef1f030f654bbb0363cd7c97381
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754216"
---
# <a name="dbglog-macro"></a>Macro DbgLog

A macro **DbgLog** envia uma cadeia de caracteres para o local de saída de depuração, se o registro em log estiver habilitado para o tipo e o nível especificados. Essa macro é ignorada em compilações de varejo.

## <a name="syntax"></a>Sintaxe


```C++
void DbgLog(
         DWORD Types,
         DWORD Level,
   const TCHAR *pFormat,
               ...
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

Nível de log desta mensagem.

</dd> <dt>

*pFormat* 
</dt> <dd>

Uma cadeia de caracteres de formato de estilo **printf** .

</dd> <dt>

*...* 
</dt> <dd>

Argumentos adicionais para a cadeia de caracteres de formato.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa macro não retorna um valor.

## <a name="remarks"></a>Comentários

Se o log de depuração de qualquer um dos tipos de mensagem for definido como o nível especificado ou superior, essa macro enviará a cadeia de caracteres formatada para o local de saída de depuração.

A macro adiciona automaticamente um caractere de nova linha à cadeia de caracteres de saída.

> [!Note]  
> Um conjunto adicional de parênteses deve incluir os parâmetros da macro:

 


```C++
DbgLog((LOG_TRACE, 3, TEXT("Connected input pin %d"), nPinNumber));
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wxdebug. h (incluir fluxos. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de saída de depuração](debug-output-functions.md)
</dt> </dl>

 

 




