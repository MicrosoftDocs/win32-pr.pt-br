---
description: Obtém o identificador do serviço a ser autenticado com o token de ponto de extremidade.
ms.assetid: FE110B8E-F8FB-4CC8-BDD8-6427BA8B7920
title: Método IUpdateEndpointAuthToken::ServiceID (UpdateEndpointAuth.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.ServiceID
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: fd7e15059db01062fae290d9c4da46a9ef07683acae9f2e58afe29830817c787
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855786"
---
# <a name="iupdateendpointauthtokenserviceid-method"></a>Método IUpdateEndpointAuthToken::ServiceID

Obtém o identificador do serviço a ser autenticado com o token de ponto de extremidade.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ServiceID(
  [out] GUID *pServiceID
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pServiceID* \[ out\]
</dt> <dd>

O identificador do serviço.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **S \_ OK** se for bem-sucedido. Caso contrário, retornará um com ou Windows código de erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP, Windows 2000 Professional somente com aplicativos da área de trabalho SP3 \[\]<br/>                   |
| Servidor mínimo com suporte<br/> | Windows Server 2003, Windows 2000 Server com somente aplicativos da área de trabalho SP3 \[\]<br/>                |
| Cabeçalho<br/>                   | <dl> <dt>UpdateEndpointAuth.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>UpdateEndpointAuth.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>UpdateEndpointAuth.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>UpdateEndpointAuth.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IUpdateEndpointAuthToken**](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




