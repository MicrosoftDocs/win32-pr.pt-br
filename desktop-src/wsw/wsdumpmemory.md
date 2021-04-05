---
title: Função WsDumpMemory (WebServicesDebug. h)
description: Essa função despeja todas as alocações de memória para o console.
ms.assetid: 84a4f1e7-7d62-48c2-a8a3-ee4573bde5e4
keywords:
- Serviços Web da função WsDumpMemory para Windows
topic_type:
- apiref
api_name:
- WsDumpMemory
api_location:
- WebServicesDebug.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70af8d34b3ee04a9db4128ce1063bd31e81306eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918923"
---
# <a name="wsdumpmemory-function"></a>Função WsDumpMemory

Essa função despeja todas as alocações de memória para o console.

> [!Note]  
> Essa função é somente para depuração.

 

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WINAPI  WsDumpMemory(
  _In_opt_ WS_ERROR* error
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*erro* \[ do em, opcional\]
</dt> <dd>

Um ponteiro para um objeto de [ \_ erro WS](ws-error.md) em que informações adicionais sobre o erro devem ser armazenadas se a função falhar.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se essa função for bem sucedido, ela retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]<br/>                                |
| parâmetro<br/>                   | <dl> <dt>WebServicesDebug. h</dt> </dl> |



 

 





