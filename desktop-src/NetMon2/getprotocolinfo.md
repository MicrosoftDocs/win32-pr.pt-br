---
description: A função GetProtocolInfo retorna um ponteiro para um valor de informações de protocolo.
ms.assetid: 1ba47889-b2ed-47ba-94f9-1b781af6d01f
title: Função GetProtocolInfo (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolInfo
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: e5db6e95b938747bbfdd567ebd29e396ad69c26d4e66262f96433d34dce9408c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117981922"
---
# <a name="getprotocolinfo-function"></a>Função GetProtocolInfo

A **função GetProtocolInfo** retorna um ponteiro para um valor de informações de protocolo.

## <a name="syntax"></a>Sintaxe


```C++
LPPROTOCOLINFO WINAPI GetProtocolInfo(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hProtocol* \[ Em\]
</dt> <dd>

Lidar com um protocolo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será um ponteiro para o valor de informações do protocolo.

Se a função não for bem-sucedida, o valor de retorno será **NULL.**

## <a name="remarks"></a>Comentários

[*Especialistas*](e.md) e [*analisadores podem*](p.md) chamar a **função GetProtocolInfo.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




