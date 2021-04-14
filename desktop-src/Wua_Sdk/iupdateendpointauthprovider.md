---
description: Contém os métodos usados para negociar qual tipo de token é usado para autenticar o ponto de extremidade de um serviço.
ms.assetid: F6177B24-C166-4BEC-83D6-3AD5B5B3CF08
title: Interface IUpdateEndpointAuthProvider (UpdateEndpointAuth. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthProvider
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 071bc23bdf9d67412fef561c71e17fe81485984f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501866"
---
# <a name="iupdateendpointauthprovider-interface"></a>Interface IUpdateEndpointAuthProvider

A interface **IUpdateEndpointAuthProvider** contém os métodos usados para negociar qual tipo de token é usado para autenticar o ponto de extremidade de um serviço.

## <a name="members"></a>Membros

A interface **IUpdateEndpointAuthProvider** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IUpdateEndpointAuthProvider** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IUpdateEndpointAuthProvider** tem esses métodos.



| Método                                                                                             | Descrição                                                                                    |
|:---------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**GetEndpointToken**](iupdateendpointauthprovider-getendpointtoken.md)                           | Solicite um token para o ponto de extremidade do serviço usando as credenciais especificadas.<br/>    |
| [**GetPreferredEndpointTokenType**](iupdateendpointauthprovider-getpreferredendpointtokentype.md) | Retorna o tipo preferencial de token de autenticação para o ponto de extremidade do serviço.<br/> |



 

## <a name="remarks"></a>Comentários

O WUA chama o método [**GetPreferredEndpointTokenType**](iupdateendpointauthprovider-getpreferredendpointtokentype.md) dessa interface para iniciar o processo de negociação. Quando a chamada é feita, o WUA passa no identificador de serviço, o tipo de ponto de extremidade implementado pelo serviço e os tipos de token disponíveis. Em seguida, a implementação dessa interface retorna os tipos de token que ele prefere usar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente Windows XP, Windows 2000 Professional com \[ aplicativos de área de trabalho do SP3\]<br/>                   |
| Servidor mínimo com suporte<br/> | Windows Server 2003, Windows 2000 Server com aplicativos de área de trabalho do SP3 \[ somente\]<br/>                |
| parâmetro<br/>                   | <dl> <dt>UpdateEndpointAuth. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>UpdateEndpointAuth. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>UpdateEndpointAuth. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>UpdateEndpointAuth.dll</dt> </dl> |



 

 
