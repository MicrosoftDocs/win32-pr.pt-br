---
description: Recupera informações sobre um assembly ao usar código gerenciado no Common Language Runtime de .NET Framework.
ms.assetid: 45dcdc6a-74df-4763-ba8b-82f604db78d4
title: Classe ClrAssemblyLocator (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ClrAssemblyLocator
api_type:
- COM
ms.openlocfilehash: ff5c1d21525a950208c1b919d4dee0e2122d2e50
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826269"
---
# <a name="clrassemblylocator-class"></a>Classe ClrAssemblyLocator

Recupera informações sobre um assembly ao usar código gerenciado no Common Language Runtime de .NET Framework.

## <a name="when-to-implement"></a>Quando implementar

Essa classe é implementada pelo COM+.



| Requisito | Valor |
|------------|-------------------------------------------------------|
| CLSID      | \_ASSEMBLYLOCATOR GUID                                 |
| ProgID     | L "System. EnterpriseServices. Internal. AssemblyLocator" |
| Interfaces | [**IAssemblyLocator**](/windows/desktop/api/ComSvcs/nn-comsvcs-iassemblylocator)          |



 

## <a name="when-to-use"></a>Quando usar

Use essa classe para acessar os métodos de [**IAssemblyLocator**](/windows/desktop/api/ComSvcs/nn-comsvcs-iassemblylocator).

## <a name="remarks"></a>Comentários

Para criar esse objeto, chame [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).

Para usar essa classe do Microsoft Visual Basic, adicione uma referência à biblioteca de tipos de serviços COM+. Um objeto ClrAssemblyLocator pode ser declarado usando "COMSVCSLib. ClrAssemblyLocator" como o nome da classe.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP com SP1\]<br/>                                 |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                 |
| parâmetro<br/>                   | <dl> <dt>ComSvcs. h</dt> </dl> |



 

