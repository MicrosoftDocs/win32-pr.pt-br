---
description: Recupera informações sobre um assembly ao usar código gerenciado no .NET Framework Common Language Runtime.
ms.assetid: 45dcdc6a-74df-4763-ba8b-82f604db78d4
title: Classe ClrAssemblyLocator (ComSvcs.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ClrAssemblyLocator
api_type:
- COM
ms.openlocfilehash: 78f041e8bdc614b1ac6007e21ffbf46ea4afe789a501bb1acefdd21263031859
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129268"
---
# <a name="clrassemblylocator-class"></a>Classe ClrAssemblyLocator

Recupera informações sobre um assembly ao usar código gerenciado no .NET Framework Common Language Runtime.

## <a name="when-to-implement"></a>Quando implementar

Essa classe é implementada pelo COM+.



| Requisito | Valor |
|------------|-------------------------------------------------------|
| CLSID      | GUID \_ AssemblyLocator                                 |
| ProgID     | L"System.EnterpriseServices.Internal.AssemblyLocator" |
| Interfaces | [**IAssemblyLocator**](/windows/desktop/api/ComSvcs/nn-comsvcs-iassemblylocator)          |



 

## <a name="when-to-use"></a>Quando usar

Use essa classe para acessar os métodos de [**IAssemblyLocator**](/windows/desktop/api/ComSvcs/nn-comsvcs-iassemblylocator).

## <a name="remarks"></a>Comentários

Para criar esse objeto, chame [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).

Para usar essa classe do Microsoft Visual Basic, adicione uma referência à Biblioteca de Tipos de Serviços COM+. Um objeto ClrAssemblyLocator pode ser declarado usando "COMSVCSLib.ClrAssemblyLocator" como o nome da classe.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP somente com \[ aplicativos da área de trabalho SP1\]<br/>                                 |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>ComSvcs.h</dt> </dl> |



 

