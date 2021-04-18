---
description: Associa um cabeçalho de vídeo ao adaptador de vídeo que o contém.
ms.assetid: d15f4350-1529-4246-9ea2-8453e52516c6
title: Classe CIM_VideoHeadOnController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoHeadOnController
- CIM_VideoHeadOnController.Antecedent
- CIM_VideoHeadOnController.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 18178e6d9d7f1e684af1d4fe74336e1f2a02eedc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787524"
---
# <a name="cim_videoheadoncontroller-class"></a>\_Classe CIM VideoHeadOnController

Associa um cabeçalho de vídeo ao adaptador de vídeo que o contém.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Experimental, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Controller"), AMENDMENT]
class CIM_VideoHeadOnController : CIM_HostedDependency
{
  CIM_DisplayController REF Antecedent;
  CIM_VideoHead         REF Dependent;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ VideoHeadOnController** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ VideoHeadOnController** tem essas propriedades.

<dl> <dt>

**Antecedent**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ DisplayController**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

O adaptador de vídeo que inclui o cabeçalho.

</dd> <dt>

**Depende**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ VideoHead**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente"), [**mín**](/windows/desktop/WmiSdk/standard-qualifiers) . (1)
</dt> </dl>

O cabeçalho no adaptador de vídeo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_HOSTEDDEPENDENCY CIM**](cim-hosteddependency.md)
</dt> </dl>

 

