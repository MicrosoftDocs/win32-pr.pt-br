---
description: Obtém o tipo do token de ponto de extremidade, como um token WS-Security SAML (Security Assertion Markup Language) 1.1.
ms.assetid: 1C6FFAD7-DC80-4957-96B4-FA0D954786DD
title: Método IUpdateEndpointAuthToken::TokenType (UpdateEndpointAuth.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.TokenType
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: a4479adc05eba8160098bd60c349645c4e30853abc693396f18f69ec722a06d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118815287"
---
# <a name="iupdateendpointauthtokentokentype-method"></a>Método IUpdateEndpointAuthToken::TokenType

Obtém o tipo do token de ponto de extremidade, como um token WS-Security SAML (Security Assertion Markup Language) 1.1.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT TokenType(
  [out] UpdateEndpointAuthTokenType *pTokenType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pTokenType* \[ out\]
</dt> <dd>

O tipo do token de ponto de extremidade.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **S \_ OK** se for bem-sucedido. Caso contrário, retornará um com ou Windows código de erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP, Windows 2000 Professional somente com aplicativos da área de trabalho SP3 \[\]<br/>                   |
| Servidor mínimo com suporte<br/> | Windows Server 2003, Windows 2000 Server somente com aplicativos da área de trabalho SP3 \[\]<br/>                |
| Cabeçalho<br/>                   | <dl> <dt>UpdateEndpointAuth.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>UpdateEndpointAuth.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>UpdateEndpointAuth.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>UpdateEndpointAuth.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IUpdateEndpointAuthToken**](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




