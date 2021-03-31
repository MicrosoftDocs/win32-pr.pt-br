---
description: Fornece acesso a uma coleção de informações de segurança que representa a identidade de um chamador. Usando essa classe, você pode descobrir sobre um determinado chamador em uma cadeia de chamadores que faz parte do contexto de chamada de segurança.
ms.assetid: c6b28695-1b08-490a-8d56-eb55d82f3e7a
title: Classe SecurityIdentity (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SecurityIdentity
api_type:
- COM
ms.openlocfilehash: 6775c06bc25bfb32a1c2c247868fd2a9fbc9aade
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "103663841"
---
# <a name="securityidentity-class"></a>Classe SecurityIdentity

Fornece acesso a uma coleção de informações de segurança que representa a identidade de um chamador. Usando essa classe, você pode descobrir sobre um determinado chamador em uma cadeia de chamadores que faz parte do contexto de chamada de segurança. Para obter mais informações sobre como as informações de contexto de chamada de segurança são acessadas, consulte segurança de componente programático.

Somente aplicativos COM+ que usam segurança baseada em função podem acessar a classe **SecurityIdentity** . Para obter mais informações sobre funções, consulte [Administração de segurança baseada em funções](role-based-security-administration.md).

## <a name="when-to-implement"></a>Quando implementar

Essa classe é implementada pelo COM+.



| Requisito | Valor |
|------------|--------------------------------------------------------|
| Interfaces | [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll) |



 

## <a name="when-to-use"></a>Quando usar

Use essa classe para acessar os métodos de [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll).

## <a name="remarks"></a>Comentários

Você não pode criar diretamente um objeto **SecurityIdentity** . Para usar os métodos de [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll), você deve obter uma referência à sua implementação chamando [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext), fornecendo \_ ISecurityCallContext de IID para o parâmetro *riid* . Em seguida, chame [**ISecurityCallContext:: get \_ Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-get_item) solicitando um item de contexto de chamada de segurança que é uma coleção de identidade de segurança (como "DirectCaller" ou "OriginalCaller"). Em seguida, chame [**ISecurityIdentityColl:: get \_ Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecurityidentitycoll-get_item) para recuperar um item de identidade de segurança (como "Name" ou "AuthenticationService").

Para usar essa classe do Microsoft Visual Basic, adicione uma referência à biblioteca de tipos de serviços COM+. Você não pode criar diretamente um objeto SecurityIdentity. Para usar suas propriedades, você deve obter um refernece para sua implementação usando o [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext). Em seguida, obtenha a propriedade item do objeto, solicitando um item de contexto de chamada de segurança que seja uma coleção de identidades de segurança (como "DirectCaller" ou "OriginalCaller"). Em seguida, use a propriedade item do objeto SecurityIdentity para recuperar um item de identidade de segurança (como "nome" ou "AuthenticationService").

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>ComSvcs. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext)
</dt> <dt>

[**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll)
</dt> <dt>

[Segurança de componente programática](programmatic-component-security.md)
</dt> <dt>

[Administração de segurança baseada em funções](role-based-security-administration.md)
</dt> <dt>

[**SecurityCallContext**](securitycallcontext.md)
</dt> <dt>

[**SecurityCallers**](securitycallers.md)
</dt> </dl>

 

