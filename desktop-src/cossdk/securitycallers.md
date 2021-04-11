---
description: Fornece acesso a informações sobre chamadores individuais em uma coleção de chamadores. A coleção representa a cadeia de chamadas terminando com a chamada atual, e cada chamador na coleção representa a identidade de um chamador.
ms.assetid: 164fe12d-eeb3-402f-8aa3-e3545904d9c4
title: Classe SecurityCallers (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SecurityCallers
api_type:
- COM
ms.openlocfilehash: c757b11bba6a30e8951915e1eace0811b6b6f732
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296087"
---
# <a name="securitycallers-class"></a>Classe SecurityCallers

Fornece acesso a informações sobre chamadores individuais em uma coleção de chamadores. A coleção representa a cadeia de chamadas terminando com a chamada atual, e cada chamador na coleção representa a identidade de um chamador. Somente os chamadores que cruzam um limite onde a segurança está marcada são incluídos na cadeia de chamadores. (No ambiente COM+, a segurança é verificada em limites de aplicativo.) O acesso a informações sobre a identidade de um chamador específico é fornecido por meio da classe [**SecurityIdentity**](securityidentity.md) , uma coleção de identidades.

Somente aplicativos COM+ que usam segurança baseada em função podem acessar a classe **SecurityCallers** . Para obter mais informações sobre funções, consulte [Administração de segurança baseada em funções](role-based-security-administration.md).

## <a name="when-to-implement"></a>Quando implementar

Essa classe é implementada pelo COM+.



| Requisito | Valor |
|------------|------------------------------------------------------|
| Interfaces | [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll) |



 

## <a name="when-to-use"></a>Quando usar

Use essa classe para acessar os métodos de [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll).

## <a name="remarks"></a>Comentários

Você não pode criar diretamente um objeto **SecurityCallers** . Para usar os métodos de [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll), você deve obter uma referência à sua implementação chamando [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext), fornecendo \_ ISecurityCallContext de IID para o parâmetro *riid* . Em seguida, chame [**ISecurityCallContext:: get \_ Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-get_item) solicitando um item de contexto de chamada de segurança que é uma coleção de identidade de segurança (como "DirectCaller" ou "OriginalCaller").

Para usar essa classe do Microsoft Visual Basic, adicione uma referência à biblioteca de tipos de serviços COM+. Você não pode criar diretamente um objeto SecurityCallers. Para usar suas propriedades, você deve obter um refernece para sua implementação usando o [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext). Em seguida, obtenha a propriedade item do objeto, solicitando um item de contexto de chamada de segurança que seja uma coleção de identidades de segurança (como "DirectCaller" ou "OriginalCaller").

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

[**SecurityIdentity**](securityidentity.md)
</dt> </dl>

 

