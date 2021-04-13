---
description: Retorna o tipo preferencial de token de autenticação para o ponto de extremidade do serviço.
ms.assetid: DF60C49A-89FE-4EEB-8E82-C2C43F2D2F2A
title: 'Método IUpdateEndpointAuthProvider:: GetPreferredEndpointTokenType (UpdateEndpointAuth. h)'
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
ms.openlocfilehash: 670835ee3c2dfd01ae46a7cf78395959ea9a26de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164610"
---
# <a name="iupdateendpointauthprovidergetpreferredendpointtokentype-method"></a>Método IUpdateEndpointAuthProvider:: GetPreferredEndpointTokenType

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

*ServiceId* \[ no\]
</dt> <dd>

Identifica o serviço a ser atualizado.

</dd> <dt>

*ponto de extremidade* \[ no\]
</dt> <dd>

Identifica o tipo de ponto de extremidade tneeded para se conectar ao serviço.

</dd> <dt>

*ulRequestedTypes* \[ no\]
</dt> <dd>

Identifica o conjunto de tokens com or sem suporte no ponto de extremidade.

</dd> <dt>

*pulPreferredTokenTypes* \[ fora\]
</dt> <dd>

Especifique o conjunto de tipos de token de autenticação com or. preferencial. (Defina como 0 para indicar que nenhum token de autenticação é necessário).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará S \_ OK se for bem-sucedido. Caso contrário, retorna um código de erro COM do Windows.

## <a name="remarks"></a>Comentários

Quando esse método é retornado, o WUA escolhe um tipo de token dos tipos preferenciais e o passa para o parâmetro TokenType do método [**GetEndpointToken**](iupdateendpointauthprovider-getendpointtoken.md) .

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
</dt> <dt>

[**GetEndpointToken**](iupdateendpointauthprovider-getendpointtoken.md)
</dt> </dl>

 

 




