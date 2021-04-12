---
description: Associa um objeto gerenciado a um domínio de aplicativo, que é um ambiente isolado em que os aplicativos são executados.
ms.assetid: 9357ea5d-6f86-4747-a923-16575ff13122
title: Classe AppDomainHelper (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AppDomainHelper
api_type:
- COM
ms.openlocfilehash: 6b4fbedbca631ec49dc2e416d939abdeb239e5b8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500898"
---
# <a name="appdomainhelper-class"></a>Classe AppDomainHelper

Associa um objeto gerenciado a um domínio de aplicativo, que é um ambiente isolado em que os aplicativos são executados.

## <a name="when-to-implement"></a>Quando implementar

Essa classe é implementada pelo COM+.



| Requisito | Valor |
|------------|-------------------------------------------------------|
| CLSID      | \_APPDOMAINHELPER GUID                                 |
| ProgID     | L "System. EnterpriseServices. Internal. AppDomainHelper" |
| Interfaces | [**IAppDomainHelper**](/windows/desktop/api/ComSvcs/nn-comsvcs-iappdomainhelper)          |



 

## <a name="when-to-use"></a>Quando usar

Use essa classe para acessar os métodos de [**IAppDomainHelper**](/windows/desktop/api/ComSvcs/nn-comsvcs-iappdomainhelper).

## <a name="remarks"></a>Comentários

Para criar esse objeto, chame [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).

Para usar essa classe do Microsoft Visual Basic, adicione uma referência à biblioteca de tipos de serviços COM+. Um objeto AppDomainHelper pode ser declarado usando "COMSVCSLib. AppDomainHelper" como o nome da classe.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP com SP1\]<br/>                                 |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                 |
| parâmetro<br/>                   | <dl> <dt>ComSvcs. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IAppDomainHelper**](/windows/desktop/api/ComSvcs/nn-comsvcs-iappdomainhelper)
</dt> </dl>

 

