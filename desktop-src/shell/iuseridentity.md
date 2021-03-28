---
description: IUserIdentity não tem suporte e pode ser alterado ou indisponível no futuro. Em vez disso, use contas de usuário com troca rápida de usuário e Área de Trabalho Remota.
ms.assetid: c2f11f8b-f944-445b-b4fc-ac57b0fe3a74
title: Interface IUserIdentity (Msident. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 068d806086aff44db172a4a7b09f55b600204478
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967883"
---
# <a name="iuseridentity-interface"></a>Interface IUserIdentity

\[**IUserIdentity** não tem suporte e pode ser alterado ou indisponível no futuro. Em vez disso, use [contas de usuário com troca rápida de usuário e área de trabalho remota](fastuserswitching.md).\]

Expõe métodos que fornecem dados de identificação, registro e pasta para uma identidade de usuário específica.

## <a name="members"></a>Membros

A interface **IUserIdentity** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IUserIdentity** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IUserIdentity** tem esses métodos.



| Método                                                         | Descrição                                                                                      |
|:---------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**GetCookie**](iuseridentity-getcookie.md)                   | Preterido. Obtém o cookie usado para identificar exclusivamente essa identidade do usuário.<br/>             |
| [**GetIdentityFolder**](iuseridentity-getidentityfolder.md)   | Preterido. Obtém a pasta de arquivos associada a essa identidade.<br/>                       |
| [**GetName**](iuseridentity-getname.md)                       | Preterido. Obtém o nome associado a esta identidade de usuário.<br/>                         |
| [**OpenIdentityRegKey**](iuseridentity-openidentityregkey.md) | Preterido. Recupera a chave no registro que corresponde a essa identidade de usuário.<br/> |



 

## <a name="remarks"></a>Comentários

Essa interface fornece informações que correspondem a uma identidade de usuário específica presente no sistema. Você pode acessar a pasta Identity da identidade do usuário, sua chave do registro e seu cookie de identificação, bem como recuperar o nome associado à identidade do usuário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Fim do suporte do cliente<br/>    | Windows 2000 Professional<br/>                                                   |
| Fim do suporte do servidor<br/>    | Windows 2000 Server<br/>                                                         |
| parâmetro<br/>                   | <dl> <dt>Msident. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Msident. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IUserIdentity2**](iuseridentity2.md)
</dt> <dt>

[**IUserIdentityManager**](iuseridentitymanager.md)
</dt> <dt>

[**IEnumUserIdentity**](ienumuseridentity.md)
</dt> </dl>

 

 
