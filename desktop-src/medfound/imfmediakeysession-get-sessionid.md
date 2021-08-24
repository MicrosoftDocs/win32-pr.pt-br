---
description: Obtém uma ID de sessão exclusiva criada para esta sessão.
ms.assetid: 779ebea9-69ff-469a-8ee0-06d570ede6cb
title: Método IMFMediaKeySession::get_SessionId
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeySession.get_SessionId
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: f598cbb1d7122bb8597d5849778a833462b4e6d9de48942fdfabbc95bbc30898
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119724546"
---
# <a name="imfmediakeysessionget_sessionid-method"></a>Método IMFMediaKeySession::get \_ SessionId

Obtém uma ID de sessão exclusiva criada para esta sessão.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_SessionId(
   BSTR *sessionId
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sessionId* 
</dt> <dd>

A ID da sessão da chave de mídia.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8.1 somente aplicativos da área de trabalho\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2012 Somente \[ aplicativos da área de trabalho R2\]<br/>                                      |
| Idl<br/>                      | <dl> <dt>Mfmediaengine.idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMFMediaKeySession**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysession)
</dt> </dl>

 

 




