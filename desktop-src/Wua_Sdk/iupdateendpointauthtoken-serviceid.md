---
description: Obtém o identificador do serviço a ser autenticado com o token do ponto de extremidade.
ms.assetid: FE110B8E-F8FB-4CC8-BDD8-6427BA8B7920
title: 'Método IUpdateEndpointAuthToken:: ServiceId (UpdateEndpointAuth. h)'
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
ms.openlocfilehash: 8384baa0a4f8bb48e603e0f2f8bed417e783b7f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105785206"
---
# <a name="iupdateendpointauthtokenserviceid-method"></a>Método IUpdateEndpointAuthToken:: ServiceId

Obtém o identificador do serviço a ser autenticado com o token do ponto de extremidade.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ServiceID(
  [out] GUID *pServiceID
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pServiceID* \[ fora\]
</dt> <dd>

O identificador do serviço.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará **S \_ OK** se for bem-sucedido. Caso contrário, retorna um código de erro COM do Windows.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente Windows XP, Windows 2000 Professional com \[ aplicativos de área de trabalho do SP3\]<br/>                   |
| Servidor mínimo com suporte<br/> | Windows Server 2003, Windows 2000 Server com aplicativos de área de trabalho do SP3 \[ somente\]<br/>                |
| parâmetro<br/>                   | <dl> <dt>UpdateEndpointAuth. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>UpdateEndpointAuth. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>UpdateEndpointAuth. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>UpdateEndpointAuth.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IUpdateEndpointAuthToken**](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




