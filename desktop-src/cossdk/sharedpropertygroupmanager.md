---
description: Cria grupos de propriedades compartilhadas e obtém acesso a grupos de propriedades compartilhadas existentes.
ms.assetid: 4ba05806-afda-4926-8ca4-abbf15ed8278
title: Classe SharedPropertyGroupManager (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SharedPropertyGroupManager
api_type:
- COM
ms.openlocfilehash: 680c5caef996d329e18192193f30841f61f02f27
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826318"
---
# <a name="sharedpropertygroupmanager-class"></a>Classe SharedPropertyGroupManager

Cria grupos de propriedades compartilhadas e obtém acesso a grupos de propriedades compartilhadas existentes.

Para obter mais informações sobre como usar o Gerenciador de Propriedades compartilhado no COM+, consulte [com+ Shared Gerenciador de propriedades](com--shared-property-manager.md).

## <a name="when-to-implement"></a>Quando implementar

Essa classe é implementada pelo COM+.



| Requisito | Valor |
|------------|--------------------------------------------------------------------|
| CLSID      | \_SHAREDPROPERTYGROUPMANAGER CLSID                                  |
| ProgID     | L "MTxSpm. SharedPropertyGroupManager"                               |
| Interfaces | [**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager) |



 

## <a name="when-to-use"></a>Quando usar

Use essa classe para acessar os métodos de [**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager).

## <a name="remarks"></a>Comentários

Para criar esse objeto, chame [**IObjectContext:: CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance).

Para usar essa classe do Microsoft Visual Basic, adicione uma referência à biblioteca de tipos de serviços COM+. Um objeto SharedPropertyGroupManager pode ser declarado usando "COMSVCSLib. SharedPropertyGroupManager" como o nome da classe.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>ComSvcs. h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager)
</dt> <dt>

[**SharedProperty**](sharedproperty.md)
</dt> <dt>

[**SharedPropertyGroup**](sharedpropertygroup.md)
</dt> </dl>

 

 




