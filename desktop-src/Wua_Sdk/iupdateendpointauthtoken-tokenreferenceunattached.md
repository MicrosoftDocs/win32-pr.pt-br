---
description: Obtém o formato XML de uma referência desanexada ao token.
ms.assetid: D5D61ED7-68FB-4FC0-9C2A-90D3B1219351
title: 'Método IUpdateEndpointAuthToken:: TokenReferenceUnattached (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.TokenReferenceUnattached
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 2dada627d6e2b8832f4317c47e54a9c4417e14b821f6cd84bce44d9f53c99aaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049244"
---
# <a name="iupdateendpointauthtokentokenreferenceunattached-method"></a>Método IUpdateEndpointAuthToken:: TokenReferenceUnattached

Obtém o formato XML de uma referência desanexada ao token.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT TokenReferenceUnattached(
  [out] BSTR *pszTokenReference
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pszTokenReference* \[ fora\]
</dt> <dd>

Ponteiro para a referência de token desanexado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **S \_ OK** se for bem-sucedido. caso contrário, retorna um código de erro COM ou Windows.

## <a name="remarks"></a>Comentários

Uma referência desanexada refere-se a um referece (como o assinatura que está usando o token) que não está na mensagem em que o token reside.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP, Windows 2000 Professional somente com \[ aplicativos da área de trabalho do SP3\]<br/>                   |
| Servidor mínimo com suporte<br/> | Windows servidor 2003, Windows 2000 servidor somente com \[ aplicativos de área de trabalho do SP3\]<br/>                |
| Cabeçalho<br/>                   | <dl> <dt>UpdateEndpointAuth. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>UpdateEndpointAuth. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>UpdateEndpointAuth. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>UpdateEndpointAuth.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IUpdateEndpointAuthToken**](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




