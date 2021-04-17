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
ms.openlocfilehash: 7f9a25c444cf1ba8421d3787a9ead242750e5756
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782541"
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

## <a name="return-value"></a>Retornar valor

Retornará **S \_ OK** se for bem-sucedido. Caso contrário, retorna um código de erro COM do Windows.

## <a name="remarks"></a>Comentários

Uma referência desanexada refere-se a um referece (como o assinatura que está usando o token) que não está na mensagem em que o token reside.

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

 

 




