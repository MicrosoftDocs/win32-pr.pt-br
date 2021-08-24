---
description: Acessa os dados armazenados no catálogo COM+.
ms.assetid: d77123f6-9821-4c80-860c-5f1feaca7987
title: Classe COMAdminCatalog (ComAdmin.h)
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
ms.openlocfilehash: 8be3f0f3f9aa59c2199c50b73b8a4d4488b0c9a65d3e0679b65350d6b8b07fd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128988"
---
# <a name="comadmincatalog-class"></a>Classe COMAdminCatalog

Acessa os dados armazenados no catálogo COM+.

## <a name="when-to-implement"></a>Quando implementar

Essa classe é implementada pelo COM+.



| Requisito | Valor |
|------------|-------------------------------------------------------------------------------------------------------------------|
| CLSID      | CLSID \_ COMAdminCatalog                                                                                            |
| ProgID     | L"COMAdmin.COMAdminCatalog"                                                                                       |
| Interfaces | [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)<br/> [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2)<br/> |



 

## <a name="when-to-use"></a>Quando usar

Você usa objetos criados da **classe COMAdminCatalog** para iniciar o acesso programático aos dados de configuração COM+ armazenados no catálogo COM+. Essas informações baseam-se nas pastas e itens na árvore de console da ferramenta de administração dos Serviços de Componentes. A **classe COMAdminCatalog** permite que você acesse coleções no catálogo, instale aplicativos e componentes COM+, inicie e pare serviços e conecte-se e administro servidores remotos.

As pastas na ferramenta de administração dos Serviços de Componentes correspondem a coleções no catálogo, que você pode representar usando objetos criados da [**classe COMAdminCatalogCollection.**](comadmincatalogcollection.md) Os itens nas pastas correspondem aos itens nas coleções, que você pode representar usando objetos criados da [**classe COMAdminCatalogObject.**](comadmincatalogobject.md)

Nem todas as coleções e itens expostos por [**meio de COMAdminCatalogCollection**](comadmincatalogcollection.md) e [**COMAdminCatalogObject**](comadmincatalogobject.md) estão disponíveis na ferramenta de administração dos Serviços de Componentes.

Para obter informações sobre coleções específicas e suas propriedades, consulte [Coleções de administração COM+.](com--administration-collections.md)

Para ver uma introdução à administração programática do COM+, consulte [Automatizando a administração COM+.](automating-com--administration.md)

## <a name="remarks"></a>Comentários

Para criar esse objeto, chame [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).

Para usar essa classe do Microsoft Visual Basic, adicione uma referência à Biblioteca de Tipos de Administrador COM+. Um objeto COMAdminCatalog pode ser declarado usando "COMAdmin.COMAdminCatalog" como o nome da classe.

No COM+ 1.5, lançado com Windows XP, a classe **COMAdminCatalog** implementa a interface [**ICOMAdminCatalog2.**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) No entanto, no COM+ 1.0, lançado com Windows 2000, a **classe COMAdminCatalog** implementa apenas a interface [**ICOMAdminCatalog.**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>ComAdmin.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>ComAdmin.Idl</dt> </dl> |



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

 

