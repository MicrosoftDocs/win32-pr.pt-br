---
description: Obtém o formato XML de uma referência anexada ao token.
ms.assetid: F4329A2E-61FD-40E0-9E24-87C9A4585E55
title: Método IUpdateEndpointAuthToken::TokenReferenceAttached (UpdateEndpointAuth.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.TokenReferenceAttached
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: eae5e616e8583e2a1da8f8aa0882ea25160faad3f064734620466a0353736efe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793856"
---
# <a name="iupdateendpointauthtokentokenreferenceattached-method"></a>Método IUpdateEndpointAuthToken::TokenReferenceAttached

Obtém o formato XML de uma referência anexada ao token.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT TokenReferenceAttached(
  [out] BSTR *pszTokenReference
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pszTokenReference* \[ out\]
</dt> <dd>

Ponteiro para a referência de token anexado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **S \_ OK** se for bem-sucedido. Caso contrário, retornará um com ou Windows código de erro.

## <a name="remarks"></a>Comentários

Uma referência anexada refere-se a uma referência (como a signiture que está usando o token) que está na mesma mensagem em que o token reside.

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

 

 




