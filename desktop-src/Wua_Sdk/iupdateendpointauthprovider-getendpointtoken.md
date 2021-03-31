---
description: Solicite um token para o ponto de extremidade do serviço usando as credenciais especificadas.
ms.assetid: 2CA0F826-9A05-4385-AF1A-A8C05B3DAFE2
title: 'Método IUpdateEndpointAuthProvider:: GetEndpointToken (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthProvider.GetEndpointToken
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 55efe38ce9782b691e1ad32f7a21f6124e1f0bf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647294"
---
# <a name="iupdateendpointauthprovidergetendpointtoken-method"></a>Método IUpdateEndpointAuthProvider:: GetEndpointToken

Solicite um token para o ponto de extremidade do serviço usando as credenciais especificadas.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetEndpointToken(
  [in]  GUID                        serviceId,
  [in]  UpdateEndpointType          endpointType,
  [in]  UpdateEndpointProxySettings proxySettings,
  [in]  HANDLE_PTR                  hUserToken,
  [in]  UpdateEndpointAuthTokenType tokenType,
  [in]  BOOL                        fRefreshOnline,
  [out] IUnknown                    **ppEndpointToken
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ServiceId* \[ no\]
</dt> <dd>

Identifica o serviço a ser atualizado.

</dd> <dt>

*ponto de extremidade* \[ no\]
</dt> <dd>

Identifica o tipo de ponto de extremidade que é implementado pelo serviço.

</dd> <dt>

*proxySettings* \[ no\]
</dt> <dd>

As configurações a serem usadas ao se conectar a um servidor proxy. Consulte a estrutura [**UpdateEndpointProxySettings**](updateendpointproxysettings.md) para obter mais detalhes.

</dd> <dt>

*hUserToken* \[ no\]
</dt> <dd></dd> <dt>

*TokenType* \[ no\]
</dt> <dd>

Identifica o tipo de token de autenticação que é usado para autenticação.

</dd> <dt>

*fRefreshOnline* \[ no\]
</dt> <dd>

Indica que o WUA do clima solicita um novo token. Verdadeiro indica que um novo token é solicitado. False indica que um token novo ou armazenado em cache é solicitado. Consulte comentários para obter mais informações.

</dd> <dt>

*ppEndpointToken* \[ fora\]
</dt> <dd>

Especifique o token do ponto de extremidade a ser usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará S \_ OK se for bem-sucedido. Caso contrário, retorna um código de erro COM do Windows.

## <a name="remarks"></a>Comentários

O WUA normalmente define o parâmetro fRefreshOnline como false quando esse método é chamado pela primeira vez; em seguida, se um erro de conexão ocorrer, o WUA definirá esse parâmetro como true quando o método for chamado novamente. No entanto, a implementação desse método pode solicitar um novo token de um serviço de token de segurança (STS) ou fornecer um token em cache a qualquer momento.

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

[**IUpdateEndpointAuthProvider**](iupdateendpointauthprovider.md)
</dt> </dl>

 

 




