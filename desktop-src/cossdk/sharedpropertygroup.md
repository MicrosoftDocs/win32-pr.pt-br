---
description: Cria e acessa as propriedades compartilhadas em um grupo de propriedades compartilhado.
ms.assetid: 20fd32f0-b2b2-4bed-8c59-1d1fdc8a399e
title: Classe SharedPropertyGroup (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SharedPropertyGroup
api_type:
- COM
ms.openlocfilehash: a6080dd59b26a989fff9a34bb5e5ce2623c6d620f9aa25cd8b84422ea4c725e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118812570"
---
# <a name="sharedpropertygroup-class"></a>Classe SharedPropertyGroup

Cria e acessa as propriedades compartilhadas em um grupo de propriedades compartilhado.

Para obter mais informações sobre como usar o Gerenciador de Propriedades compartilhado no COM+, consulte [com+ Shared Gerenciador de propriedades](com--shared-property-manager.md).

## <a name="when-to-implement"></a>Quando implementar

Essa classe é implementada pelo COM+.



| Requisito | Valor |
|------------|------------------------------------------------------|
| Interfaces | [**ISharedPropertyGroup**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup) |



 

## <a name="when-to-use"></a>Quando usar

Use essa classe para acessar os métodos de [**ISharedPropertyGroup**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup).

## <a name="remarks"></a>Comentários

Você pode criar um objeto **SharedPropertyGroup** usando o método [**CreateProperty**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroupmanager-createpropertygroup) do [**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager).

para usar essa classe do Microsoft Visual Basic, adicione uma referência à biblioteca de tipos de serviços COM+. Um objeto SharedPropertyGroup é criado chamando o método [**CreateProperty**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroupmanager-createpropertygroup) do objeto [**SharedPropertyGroupManager**](sharedpropertygroupmanager.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>ComSvcs. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ISharedPropertyGroup**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup)
</dt> <dt>

[**SharedProperty**](sharedproperty.md)
</dt> <dt>

[**SharedPropertyGroupManager**](sharedpropertygroupmanager.md)
</dt> </dl>

 

 




