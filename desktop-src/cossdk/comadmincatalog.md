---
description: Acessa os dados armazenados no catálogo COM+.
ms.assetid: d77123f6-9821-4c80-860c-5f1feaca7987
title: Classe COMAdminCatalog (COMAdmin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COMAdminCatalog
api_type:
- COM
api_location:
- ComAdmin.Idl
ms.openlocfilehash: fa6e71d13f5a3d157bd3ce1035d0616dc1e5a519
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457098"
---
# <a name="comadmincatalog-class"></a>Classe COMAdminCatalog

Acessa os dados armazenados no catálogo COM+.

## <a name="when-to-implement"></a>Quando implementar

Essa classe é implementada pelo COM+.



| Requisito | Valor |
|------------|-------------------------------------------------------------------------------------------------------------------|
| CLSID      | \_COMADMINCATALOG CLSID                                                                                            |
| ProgID     | L "COMAdmin. COMAdminCatalog"                                                                                       |
| Interfaces | [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)<br/> [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2)<br/> |



 

## <a name="when-to-use"></a>Quando usar

Você usa objetos criados a partir da classe **COMAdminCatalog** para iniciar o acesso programático aos dados de configuração com+ armazenados no catálogo com+. Essas informações baseiam-se nas pastas e nos itens na árvore de console da ferramenta de administração de serviços de componentes. A classe **COMAdminCatalog** permite que você acesse coleções no catálogo, instale aplicativos e componentes com+, inicie e interrompa os serviços, e conecte-se a servidores remotos e a administre.

As pastas na ferramenta de administração de serviços de componentes correspondem às coleções no catálogo, que você pode representar usando objetos criados na classe [**COMAdminCatalogCollection**](comadmincatalogcollection.md) . Os itens nas pastas correspondem aos itens nas coleções, que você pode representar usando objetos criados a partir da classe [**COMAdminCatalogObject**](comadmincatalogobject.md) .

Nem todas as coleções e os itens expostos por meio de [**COMAdminCatalogCollection**](comadmincatalogcollection.md) e [**COMAdminCatalogObject**](comadmincatalogobject.md) estão disponíveis na ferramenta de administração de serviços de componentes.

Para obter informações sobre coleções específicas e suas propriedades, consulte [coleções de administração do com+](com--administration-collections.md).

Para obter uma introdução à administração programática do COM+, consulte [automatizando a administração do com+](automating-com--administration.md).

## <a name="remarks"></a>Comentários

Para criar esse objeto, chame [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).

Para usar essa classe do Microsoft Visual Basic, adicione uma referência à biblioteca de tipos de administrador do COM+. Um objeto COMAdminCatalog pode ser declarado usando "COMAdmin. COMAdminCatalog" como o nome da classe.

No COM+ 1,5, lançado com o Windows XP, a classe **COMAdminCatalog** implementa a interface [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) . No entanto, no COM+ 1,0, lançado com o Windows 2000, a classe **COMAdminCatalog** implementa apenas a interface [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>COMAdmin. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>COMAdmin. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**COMAdminCatalogCollection**](comadmincatalogcollection.md)
</dt> <dt>

[**COMAdminCatalogObject**](comadmincatalogobject.md)
</dt> <dt>

[**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)
</dt> <dt>

[**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2)
</dt> </dl>

 

