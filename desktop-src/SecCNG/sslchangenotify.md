---
description: Não implementado e não pode ser usado.
ms.assetid: b41ba894-5cee-458d-935f-e89363925968
title: Função SslChangeNotify (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslChangeNotify
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: ff8bd1d23315894a3e858a536d10883f2fedcced792575157de824c02f3217ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907174"
---
# <a name="sslchangenotify-function"></a>Função SslChangeNotify

A **função SslChangeNotify** não é implementada e não pode ser usada.

## <a name="syntax"></a>Sintaxe


```C++
SECURITY_STATUS WINAPI SslChangeNotify(
  _In_ HANDLE hEvent,
  _In_ DWORD  dwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hEvent* \[ Em\]
</dt> <dd>

Esse parâmetro é reservado para uso futuro.

</dd> <dt>

*dwFlags* \[ Em\]
</dt> <dd>

Esse parâmetro é reservado para uso futuro.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **NTE \_ NOT \_ SUPPORTED**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

 




