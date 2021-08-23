---
description: Não há suporte para IUserIdentity e pode ser alterado ou não disponível no futuro. Em vez disso, use Contas de Usuário com Troca rápida de usuário e Área de Trabalho Remota.
ms.assetid: c2f11f8b-f944-445b-b4fc-ac57b0fe3a74
title: Interface IUserIdentity (Msident.h)
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
ms.openlocfilehash: f7e721f60198791e530300d5181abaa84e96c1a04f285972314ab866dd86215f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713776"
---
# <a name="iuseridentity-interface"></a>Interface IUserIdentity

\[**Não há suporte para IUserIdentity** e pode ser alterado ou não disponível no futuro. Em vez disso, use [Contas de Usuário com a Opção de Usuário Rápida e Área de Trabalho Remota](fastuserswitching.md).\]

Expõe métodos que fornecem dados de identificação, registro e pasta para uma identidade de usuário específica.

## <a name="members"></a>Membros

A **interface IUserIdentity** herda da interface [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IUserIdentity** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A **interface IUserIdentity** tem esses métodos.



| Método                                                         | Descrição                                                                                      |
|:---------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**Getcookie**](iuseridentity-getcookie.md)                   | Preterido. Obtém o cookie usado para identificar exclusivamente essa identidade de usuário.<br/>             |
| [**GetIdentityFolder**](iuseridentity-getidentityfolder.md)   | Preterido. Obtém a pasta de arquivo associada a essa identidade.<br/>                       |
| [**GetName**](iuseridentity-getname.md)                       | Preterido. Obtém o nome associado a essa identidade de usuário.<br/>                         |
| [**OpenIdentityRegKey**](iuseridentity-openidentityregkey.md) | Preterido. Recupera a chave no Registro que corresponde a essa identidade de usuário.<br/> |



 

## <a name="remarks"></a>Comentários

Essa interface fornece informações que correspondem a uma identidade de usuário específica presente no sistema. Você pode acessar a pasta de identidade dessa identidade do usuário, sua chave do Registro e seu cookie de identificação, bem como recuperar o nome associado à identidade do usuário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Fim do suporte ao cliente<br/>    | Windows 2000 Professional<br/>                                                   |
| Fim do suporte ao servidor<br/>    | Windows 2000 Server<br/>                                                         |
| Cabeçalho<br/>                   | <dl> <dt>Msident.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Msident.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IUserIdentity2**](iuseridentity2.md)
</dt> <dt>

[**IUserIdentityManager**](iuseridentitymanager.md)
</dt> <dt>

[**IEnumUserIdentity**](ienumuseridentity.md)
</dt> </dl>

 

 
