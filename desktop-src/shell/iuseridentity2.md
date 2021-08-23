---
description: IUserIdentity2 não tem suporte e pode ser alterado ou indisponível no futuro. Em vez disso, use contas de usuário com troca rápida de usuário e Área de Trabalho Remota.
ms.assetid: 85238574-f6bf-43d7-a41b-3ea086c45e07
title: Interface IUserIdentity2 (Msident. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity2
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: a1a23ea6e0d5832ee6d78453f3a246b9db749c0d7b24b90a2199a7e8cfd225b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118720582"
---
# <a name="iuseridentity2-interface"></a>Interface IUserIdentity2

\[**IUserIdentity2** não tem suporte e pode ser alterado ou indisponível no futuro. Em vez disso, use [contas de usuário com troca rápida de usuário e área de trabalho remota](fastuserswitching.md).\]

Expõe métodos que fornecem nomenclatura, senha e controle ordinal para uma identidade de usuário específica.

## <a name="members"></a>Membros

A interface **IUserIdentity2** herda de [**IUserIdentity**](iuseridentity.md). **IUserIdentity2** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IUserIdentity2** tem esses métodos.



| Método                                                  | Descrição                                                       |
|:--------------------------------------------------------|:------------------------------------------------------------------|
| [**ChangePassword**](iuseridentity2-changepassword.md) | Preterido. Define uma nova senha para a identidade.<br/>      |
| [**GetOrdinal**](iuseridentity2-getordinal.md)         | Preterido. Obtém o número ordinal desta identidade.<br/> |
| [**SetName**](iuseridentity2-setname.md)               | Preterido. Define o nome de exibição da identidade.<br/>     |



 

## <a name="remarks"></a>Comentários

Essa interface também fornece os métodos da interface [**IUserIdentity**](iuseridentity.md) , da qual ela é herdada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Fim do suporte do cliente<br/>    | Windows 2000 Professional<br/>                                                   |
| Fim do suporte do servidor<br/>    | Windows 2000 Server<br/>                                                         |
| Cabeçalho<br/>                   | <dl> <dt>Msident. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Msident. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IUserIdentity**](iuseridentity.md)
</dt> </dl>

 

 




