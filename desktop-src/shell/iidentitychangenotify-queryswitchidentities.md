---
description: Chamado quando o usuário atual solicitou que a identidade do usuário fosse alternada, mas antes do comutador ocorrer.
ms.assetid: f159b829-623c-4348-9692-7317663811a7
title: 'Método IIdentityChangeNotify:: QuerySwitchIdentities (Msident. h)'
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
ms.openlocfilehash: 42f8033c943e402d434c973f8c768ed5a951811d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828280"
---
# <a name="iidentitychangenotifyqueryswitchidentities-method"></a>Método IIdentityChangeNotify:: QuerySwitchIdentities

\[O **QuerySwitchIdentities** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.\]

Chamado quando o usuário atual solicitou que a identidade do usuário fosse alternada, mas antes do comutador ocorrer.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT QuerySwitchIdentities();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Resultado da consulta de comutador. Se a opção continuar, retorne S \_ OK. Caso contrário, \_ a opção retornar E processar \_ cancelada \_ para indicar que a opção de identidade do usuário deve ser anulada.

## <a name="remarks"></a>Comentários

Você pode implementar esse método para fornecer um comportamento personalizado para seu aplicativo quando um usuário solicitar que as identidades sejam alternadas. Você pode interromper a opção de identidade pendente retornando o valor E \_ processar a \_ opção cancelada \_ .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Fim do suporte do cliente<br/>    | Windows 2000 Professional<br/>                                                   |
| Fim do suporte do servidor<br/>    | Windows 2000 Server<br/>                                                         |
| parâmetro<br/>                   | <dl> <dt>Msident. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Msident. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msoe.dll</dt> </dl>    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IIdentityChangeNotify**](iidentitychangenotify.md)
</dt> <dt>

[**IIdentityChangeNotify::SwitchIdentities**](iidentitychangenotify-switchidentities.md)
</dt> </dl>

 

 




