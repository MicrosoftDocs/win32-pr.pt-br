---
description: Chamado quando o usuário atual solicitou que sua identidade de usuário fosse alternada, mas antes que a opção ocorra.
ms.assetid: f159b829-623c-4348-9692-7317663811a7
title: Método IIdentityChangeNotify::QuerySwitchIdentities (Msident.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IIdentityChangeNotify.QuerySwitchIdentities
api_type:
- COM
api_location:
- Msoe.dll
ms.openlocfilehash: 38469490db92278c82e7935e1078181010757dd22be220203361d2d4c18ef380
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119593076"
---
# <a name="iidentitychangenotifyqueryswitchidentities-method"></a>Método IIdentityChangeNotify::QuerySwitchIdentities

\[**As entidades QuerySwitchId** estão disponíveis para uso nos sistemas operacionais especificados na seção Requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.\]

Chamado quando o usuário atual solicitou que sua identidade de usuário fosse alternada, mas antes que a opção ocorra.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT QuerySwitchIdentities();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Resultado da consulta switch. Se a opção deve continuar, retorne S \_ OK. Caso contrário, retorne E \_ PROCESS \_ CANCELLED \_ SWITCH para indicar que a opção de identidade do usuário deve ser anulada.

## <a name="remarks"></a>Comentários

Você pode implementar esse método para fornecer um comportamento personalizado para seu aplicativo quando um usuário solicita que as identidades sejam alternadas. Você pode interromper a opção de identidade pendente retornando o valor E \_ PROCESS \_ CANCELLED \_ SWITCH.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Fim do suporte ao cliente<br/>    | Windows 2000 Professional<br/>                                                   |
| Fim do suporte ao servidor<br/>    | Windows 2000 Server<br/>                                                         |
| Cabeçalho<br/>                   | <dl> <dt>Msident.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Msident.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msoe.dll</dt> </dl>    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IIdentityChangeNotify**](iidentitychangenotify.md)
</dt> <dt>

[**IIdentityChangeNotify::SwitchIdentities**](iidentitychangenotify-switchidentities.md)
</dt> </dl>

 

 




