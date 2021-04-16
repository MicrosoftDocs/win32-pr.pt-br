---
description: Obtém os dados XML (enviados pela transmissão) que representam o token.
ms.assetid: 52EC991A-0499-4182-AC4F-512BAFB4F896
title: 'Método IUpdateEndpointAuthToken:: TokenData (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.TokenData
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: e75df7f5b13eaf36854cf7ed9abc5988b02462ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765016"
---
# <a name="iupdateendpointauthtokentokendata-method"></a>Método IUpdateEndpointAuthToken:: TokenData

Obtém os dados XML (enviados pela transmissão) que representam o token.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT TokenData(
  [out] BSTR *pszTokenData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pszTokenData* \[ fora\]
</dt> <dd>

Os dados XML (enviados pela transmissão) que representam o token. Por exemplo, os dados de um token WS-Security SAML (Security Assertion Markup Language) 1,1 é o código SAML que é adicionado à solicitação.

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

 

 




