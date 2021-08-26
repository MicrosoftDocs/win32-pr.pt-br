---
description: Contém os métodos usados para negociar qual tipo de token é usado para autenticar o ponto de extremidade de um serviço.
ms.assetid: F6177B24-C166-4BEC-83D6-3AD5B5B3CF08
title: Interface IUpdateEndpointAuthProvider (UpdateEndpointAuth.h)
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
ms.openlocfilehash: 3cbc51ab0f1192e20612829532b907e3644a7da3f99fdedd8e3dbd45a780c54d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119994566"
---
# <a name="iupdateendpointauthprovider-interface"></a>Interface IUpdateEndpointAuthProvider

A interface **IUpdateEndpointAuthProvider** contém os métodos usados para negociar qual tipo de token é usado para autenticar o ponto de extremidade de um serviço.

## <a name="members"></a>Membros

A interface **IUpdateEndpointAuthProvider** herda da interface [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IUpdateEndpointAuthProvider** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IUpdateEndpointAuthProvider** tem esses métodos.



| Método                                                                                             | Descrição                                                                                    |
|:---------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**GetEndpointToken**](iupdateendpointauthprovider-getendpointtoken.md)                           | Solicite um token para o ponto de extremidade do serviço usando as credenciais especificadas.<br/>    |
| [**GetPreferredEndpointTokenType**](iupdateendpointauthprovider-getpreferredendpointtokentype.md) | Retorna o tipo preferencial de token de autenticação para o ponto de extremidade do serviço.<br/> |



 

## <a name="remarks"></a>Comentários

WUA chama o [**método GetPreferredEndpointTokenType**](iupdateendpointauthprovider-getpreferredendpointtokentype.md) dessa interface para iniciar o processo de negociação. Quando a chamada é feita, o WUA passa o identificador de serviço, o tipo de ponto de extremidade implementado pelo serviço e os tipos de token disponíveis. A implementação dessa interface retorna os tipos de token que ela prefere usar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP, Windows 2000 Professional somente com aplicativos da área de trabalho SP3 \[\]<br/>                   |
| Servidor mínimo com suporte<br/> | Windows Server 2003, Windows 2000 Server somente com aplicativos da área de trabalho SP3 \[\]<br/>                |
| Cabeçalho<br/>                   | <dl> <dt>UpdateEndpointAuth.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>UpdateEndpointAuth.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>UpdateEndpointAuth.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>UpdateEndpointAuth.dll</dt> </dl> |



 

 
