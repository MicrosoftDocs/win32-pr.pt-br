---
description: Retorna o tipo preferencial de token de autenticação para o ponto de extremidade do serviço.
ms.assetid: DF60C49A-89FE-4EEB-8E82-C2C43F2D2F2A
title: Método IUpdateEndpointAuthProvider::GetPreferredEndpointTokenType (UpdateEndpointAuth.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthProvider.GetPreferredEndpointTokenType
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: a9b7d15d6d27170106118c720d25567389884c50e27aac202adedf00290236c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119994576"
---
# <a name="iupdateendpointauthprovidergetpreferredendpointtokentype-method"></a>Método IUpdateEndpointAuthProvider::GetPreferredEndpointTokenType

Retorna o tipo preferencial de token de autenticação para o ponto de extremidade do serviço.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetPreferredEndpointTokenType(
  [in]  GUID               serviceId,
  [in]  UpdateEndpointType endpointType,
  [in]  ULONG              ulRequestedTypes,
  [out] ULONG              *pulPreferredTokenTypes
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*serviceId* \[ Em\]
</dt> <dd>

Identifica o serviço a ser atualizado.

</dd> <dt>

*endpointType* \[ Em\]
</dt> <dd>

Identifica o tipo de ponto de extremidade que precisa se conectar ao serviço.

</dd> <dt>

*ulRequestedTypes* \[ Em\]
</dt> <dd>

Identifica o conjunto ORed de tokens com suporte pelo ponto de extremidade.

</dd> <dt>

*pulPreferredTokenTypes* \[ out\]
</dt> <dd>

Especifique o conjunto ORed de tipos de token de autenticação preferenciais. (De definido como 0 para indicar que nenhum token de autenticação é necessário).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará S \_ OK se for bem-sucedido. Caso contrário, retornará um com ou Windows código de erro.

## <a name="remarks"></a>Comentários

Quando esse método é retornado, o WUA escolhe um tipo de token dos tipos preferenciais e o passa para o parâmetro tokenType do [**método GetEndpointToken.**](iupdateendpointauthprovider-getendpointtoken.md)

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

[**IUpdateEndpointAuthProvider**](iupdateendpointauthprovider.md)
</dt> <dt>

[**GetEndpointToken**](iupdateendpointauthprovider-getendpointtoken.md)
</dt> </dl>

 

 




