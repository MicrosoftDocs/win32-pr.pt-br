---
title: Função WsSetAutoFail (WebServicesDebug. h)
description: Define o próximo ponto para injetar uma falha. Esta é uma função somente depuração.
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
ms.openlocfilehash: 0ba10b8b038f270f764b064fac1cb81e675f5239
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499628"
---
# <a name="wssetautofail-function"></a>Função WsSetAutoFail

Define o próximo ponto para injetar uma falha. Esta é uma função somente depuração.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WINAPI  WsSetAutoFail(
  _In_     ULONG     count,
  _In_opt_ WS_ERROR* error
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*contagem* \[ de no\]
</dt> <dd>

Especifica quantas operações antes de falhas começam a ocorrer.

</dd> <dt>

*erro* \[ do em, opcional\]
</dt> <dd>

Um ponteiro para um objeto de [ \_ erro WS](ws-error.md) em que informações adicionais sobre o erro devem ser armazenadas se a função falhar.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se essa função for bem sucedido, ela retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                       |
| parâmetro<br/>                   | <dl> <dt>WebServicesDebug. h</dt> </dl> |



 

 





