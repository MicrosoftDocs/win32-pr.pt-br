---
title: Função WsSetAutoFail (WebServicesDebug.h)
description: Define o próximo ponto para injetar uma falha. Essa é uma função DEBUG ONLY.
ms.assetid: b453dbc5-01ff-486d-8767-254b74cc5b6e
keywords:
- Serviços Web da função WsSetAutoFail para Windows
topic_type:
- apiref
api_name:
- WsSetAutoFail
api_location:
- WebServicesDebug.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e2ae3ed731edce429aac78700d52d0e7504a5688d1bf35bbb9c64a5d34bc0a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119838536"
---
# <a name="wssetautofail-function"></a>Função WsSetAutoFail

Define o próximo ponto para injetar uma falha. Essa é uma função DEBUG ONLY.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WINAPI  WsSetAutoFail(
  _In_     ULONG     count,
  _In_opt_ WS_ERROR* error
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*count* \[ Em\]
</dt> <dd>

Especifica quantas operações antes que as falhas comecem a ocorrer.

</dd> <dt>

*erro* \[ in, opcional\]
</dt> <dd>

Um ponteiro para um [objeto ERROR \_ do WS](ws-error.md) em que informações adicionais sobre o erro devem ser armazenadas se a função falhar.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se essa função for bem-sucedida, ela retornará **S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                                       |
| Cabeçalho<br/>                   | <dl> <dt>WebServicesDebug.h</dt> </dl> |



 

 





